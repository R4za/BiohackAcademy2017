
### 24-02-2017 - Debugging the Magnetic Stirrer.

One of my main objectives this BHA is to build most of the devices, and this tuesday I finally completed my first: the magnetic stirrer. It started out easy enough, with quickly getting the fan/stirring function running and setting up the remainder of the circuit with the exception of the heating pad:

![Getting started](https://github.com/R4za/BiohackAcademy2017/blob/master/IMG_20170213_170949.jpg?raw=true) 
Getting started.

![Image](https://github.com/R4za/BiohackAcademy2017/blob/master/IMG_20170215_153653.jpg?raw=true) 
The circuit minus the heating pad.

![Image](https://github.com/R4za/BiohackAcademy2017/blob/master/IMG_20170215_162102.jpg?raw=true) 
Cardboard scaffolding to hold the magnets in place while the glue dries.

![Image](https://github.com/R4za/BiohackAcademy2017/blob/master/IMG_20170216_170936.jpg?raw=true) 
Whirlpool!

Victory! Right? Not quite. Because when the heating pad eventually _was_ attached, it turned out not to do any heating! Also, two minutes into trying to figure _that_ out, the red LED stopped working. After spending a lab session or two testing the circuit and double-checking every connection, wherein everything seemed to function as it should, I finally thought to do something I should've done form the start: _do the math_! 

Looking at the heating pad sub-circuit, there was 12 volt divided over a 6.5Ω/5V heating pad, a set of toggle-able resistors with a minimum combined impedance of ~22Ω with all switches turned on, and a 92Ω/1.75V LED, connected in series. Meaning that the LED alone would be taking about 9V, the switch-system two-point-something, and the heating pad less than 1V. No wonder the LED burned while the heating pad stayed cold.

Turns out there was... well, not so much an _error_ as an unfortunate display problem with the fritzing schematic:

![Image](https://github.com/R4za/BiohackAcademy2017/blob/master/stirrerschematic.png)
 	
In the left image, which was the fritzing file I was working with, it is apparent that the right-hand loop (which feeds the heating bad) feeds back _through_ the led onto the ground. Made sense to me: this way, the LED would light up regardless of whether the stirring or heating function was turned on - that is, whenever the device was running at all. But looking at the right side image, the heating pad's ground line turned out not to _connect_ to the line feeding the LED so much as it _displayed exactly overneath it_. Pulling it downwards a bit showed how the circuit was _supposed_ to be wired.

Wiring it up like that turned out to be a significant improvement! The new LED didn't burn, and the heating pad now achieved a temperature that was unmistabably a tad above room temperature. More math: with all switches opened up to run the heating pad at it's maximum power, the pad would now draw 6.5Ω / (6.5Ω + 22Ω) = 22.8% of the voltage; so around 2.8V, a little more than half of its desired operating voltage of 5V. 

The story here was that the mechanism with three switches, each adding another paralel conductor to allow incremental control of the power over the heating pad, was an untried change of the previous working model intended to teach participants about working with Ohm's law. It succeeded there! But the range of impedances that the switching mechanism was capable of remained way too high compared to the heating pad. I ended up just adding another 68Ω resistor in parallel to each of the three prior resistors, so that the total conductivity added by opening each switch doubled. This permits a total impedance as low as 11.3Ω when all three switches are opened, for a voltage drop of (11.3Ω / (11.3Ω + 6.5Ω) ) * 12V = 7.6V over the switching mechanism, leaving 4.4V to keep the heating pad running at nearly maximal power. 

That did the trick, and my stirrer heats up (and stirs) beautifully now.

~Raza



### 12-02-2017 - Welcome to my project logbook.

We've not actually started our projects yet, but this page is still full of helpful markup language tips!

~Raza




You can use the [editor on GitHub](https://github.com/R4za/BiohackAcademy2017/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/R4za/BiohackAcademy2017/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

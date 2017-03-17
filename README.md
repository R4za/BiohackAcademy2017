
## 17-03-2017 - Project: Spirulina Plus

Spirulina (_Arthrospira platensis_, in this case) is a cyanobacterium (but usually referred to as an algae) that can be cultivated as a food source. It has several attractive properties in this regard: 
- It's a complete protein source, meaning it provides every amino acid we need. This is pretty rare in a single food. It's dried mass is also about 60% protein, so it adds up.
- About a third of this protein (20% of the dried mass) consists of phycocyanobilin proteins, which are bioactive and provide far-ranging and well-researched health benefits. Spirulina has been noted to be neuroprotective, improve cardiovascular health, boost the immune system, help excrete toxic levels of heavy metals and protect stem cell populations. Through it's inhibition of the endogenous free radical-producing NADPH oxidase enzyme it even has a promising mechanism for human life extension. There's too much to go into here, but feast your brain on [spirulina's examine.com review](https://examine.com/supplements/spirulina/) if you're interested.
- It requires only light (which is potentially renewable), CO2 (which we have too much of) and a suitable nitrogen source and some minerals to grow. Growing it is _very nearly_ conjuring food out of thin air. It has this in common with plant foods in general, of course, but it's often cited as being particularly efficient at it.
- Single-cellural organisms are highly unlikely to posses consciousness, so subjugating it to our needs seems ethically unproblematic. It's also vegan/vegetarian, if those are your criteria. This is all the more valuable in the light of the 'complete protein source' point.
- Spirulina proteins are fluorescent green under the right lighting, and an indoor bioreactor will make your labspace look like a comic-book supervillain lair:
<br> 

 ![A spirulina reactor from blablaLab in Spain](https://github.com/R4za/BiohackAcademy2017/blob/master/Pics/spirulianreactor.png?raw=true){: .center-image }

<br>
This seems to me a good start. One of the takeaways of the BHA lectures so far seems to be that you can get microorganisms to do all sorts of neat tricks if you prod them right - but while I appreciate the art of animations built from face-shaped yeast cultures and the innovation of making clothes from laser-cut combucha film, most projects that I've seen are still some distance removed from being _useful_ when compared to already existing solutions to the same problems. Which is fine for art/learning/whenever you're having a good time, of course. But there are important things happening in the world in our era, ready to be affected by our actions, and so I personally really _like_ useful. Working on a food source that is _already_ very much worth eating/growing, any success would be immediately useful for me personally, and any _improvents_ I succeeded in making could be valuable for any current spirulina-farmer willing to adopt the method - hence this choice of project.

The Spirulina Plus project aims to: a) get a healthy spirulina culture growing in a DIY bioreactor, and b) explore the possibility of genetically engineering _Arthrospira platensis_ to further improve its utility as a conveniently culturable health food.
<br>

### Subproject A: Building the Photobioreactor and Starting a Spirulina Culture.

Four afternoons into the effort, building and improving on the [Waag-design open photobioreactor](https://github.com/BioHackAcademy/BHA_Photobioreactor) currently remains a work-in-progress. Further documentation probably to be added later.
<br>

### Subproject B: Genetic Engineering of _A. platensis_.

**What?** The idea here is to add genetic material to living spirulina, which would then be used to start a culture posessing the corresponding properties in its phenotype. This would be useful for a couple of reasons. Because they do best at a pH as high as 9-9.5 (which few environmental microbes like) and because other algea that could thrive in the same growing conditions are scarce inside our homes, indoor spirulina cultures don't seem to be particularly difficult to keep uncontaminated. So once you've got _any_ succesfully modified spirulina, so long you go about it right, you'll have as much as fits in your reactor and you can replenish that supply indefinitely. And spirulina is pretty rare among prokaryotes in that it constitutes a _food_ of and by itself - taking genetically modified live probiotic supplements risks releasing GMA organisms into the environment, but spirulina you can just eat dead, and still benefit from whatever properties you added.

Ideas for useful genetic improvements would be: 
- Anything that enhances its growth rate/biomass productivity.
- Anything that enhances its resistance to whatever-factors-could-theoretically-threaten-a-spirulina-harvest. Contamination by toxic blue algea seems like a thing for outdoor cultures, so something that'd give them a competitive advantage against those would be good.
- Anything that expands the range of conditions that spirulina thrives at. For example, spirulina prefers 35 degrees C; if it could be changed to tolerate colder climates, the number of countries worldwide for which outdoor spirulina culturing is a viable food production strategy would increase by a lot) 
- Changing its valuable new (phyto)nutrients. For example, brocolli has a reputation for its potent anti-cancer bioactives, but is unimpressive as a protein source and more difficult to grow than spirulina. If spirulina could be made to produce brocolli's bioactives, you'd have two health foods in one! With an optimized transfection method and accumulating genetic engineering practice, this could actually snowball into something like a _self-replenishing synthbio soylent-alternative_: you just keep adding food properties to one artificial phylogenic spirulina branch until you've packed it with everything you want and need, and then you grow as much as you can eat in your garden or garage from plant food and a light source. You'd have the simplicity, self-sufficiency and sustainability of your eating habits maxed out all at once! I know what I'll be eating after the apocalypse (did I mention spirulina reputedly protects against radiation poisoning?).
- Having it produce _more_ of something valuable it already produces, such as the active phycocyaninbilin protein fragment.

As a spoiled western biohacker who has never faced food-scarcity in his life, I get the most excited about the last two options. Currently, I'm leaning towards trying to make it (over)express [PQQ](https://examine.com/supplements/pyrroloquinoline-quinone/) (which is a fairly healthy, fairly expensive food supplement, which [scientists have succesfully added to other bacteria before](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0164860)) as a proof-of-concept, if I get that far. A more ambitious project still would be hacking spirulina to overproduce nicotinamide mononucleotide (NMN), an intermediate in the biosynthesis of an important energy metabolism co-factor from vitamin B3 that we all already produce. NMN has powerful life-extending properties when supplemented beyond our natural production, but is ridiculously expensive to buy or synthesize normally (I've found that a team at the Boston Open Source Laboratory is in fact already working on achieving NMN overproduction in lactobacillus, and have emailed the contact person to ask about their progress!).

**How?** It appears that genetic modification of spirulina is not commonly done. My literature search turned up only [one relevant paper](https://link.springer.com/article/10.1023%2FA%3A1011182613761?LI=true), which remarked that the organism had proven resistant the most techniques used up until then, but succeeded at transforming spirulina by means of electroporation. 

Interestingly, another thing that search turned up was that a [whole-genome sequencing of _A. platensis_](https://academic.oup.com/dnaresearch/article/23/4/325/2469971/Whole-genomic-DNA-sequencing-and-comparative) had shown the species to possess an endogenous CRISPR locus. This is exciting, because several studies now[[1](http://www.nature.com/articles/srep25666),[2](https://academic.oup.com/nar/article-lookup/doi/10.1093/nar/gkv1044),[3](https://www.ncbi.nlm.nih.gov/pubmed/26460902)] have shown that these can be tricked into performing your gene-editing attempts for you, and also because I've been hungry for an opportunity to work with CRISPR editing.

Reading [the first of these papers](http://www.nature.com/articles/srep25666) and comparing to the genome paper, it looks like they exploited an endogenous CRISPR array of a different type than the one found in spirulina, but they remark that the technique should generalize in theory so long as the CRISPR array in your organism is function. Looking at their methods, one major challenge for editing spirulina will be that the PAM sequences that it's CRISPR array will accept (see [this link](https://www.neb.com/tools-and-resources/feature-articles/crispr-cas9-and-targeted-genome-editing-a-new-era-in-molecular-biology) for an explanation of CRISPR editing mechanics) haven't yet been uncovered. Succesful CRISPR editing seems to have two conditions: knowing what DNA sequence to put into your plasmid, and getting the plasmid into the organism. _Most_ of that first condition can be met just looking at your organism's genome and knowing what genetic information you want to insert, but the PAM sequence which a CRISPR array will recognize is found _not_ in its own genome, but rather in the genomes of the bacteria-eating viruses that the CIRSPR array is built to protect against. Spirulina's genome _does_ probably contain clues as to where to find these: the scientists from the paper solved this problem by looking for viruses matching their organism's CRISPR array in databases, and found a working solution. 

I also still need to work out the legality of this. CRISPR is apparently not included in the Waag society's genetic-modification licence, on account of it being a two-step process where you first make your organism express the CRISPR proteins (Cas9) which subsequently make it susceptible to further genetic editing - that is from memory of talking to Pieter, and may be poorly remembered.
<br>

That's it up until now!

~ Raza
<br>

## 24-02-2017 - Debugging the Magnetic Stirrer.

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

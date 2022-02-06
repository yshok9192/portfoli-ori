## Critique by Design

This assignment was twofold: find a data visualization out in the wild that could use a bit of a tune-up and identify areas of improvement; and wireframe, then design, a solution that makes the data more readable, understandable, and pretty to look at. I chose to look at [this](https://www.scientificamerican.com/article/graphic-science-caffeine-high-more-and-more-products-contain-large-doses/) visualization from *Scientific American*, mapping out how much caffeine is in everyday products--not just coffee, but water, chocolate, and jelly beans. The idea behind the viz is to highlight just how much caffeine we are consuming beyond the regular fare of coffee, tea, and energy drinks, and while I think the viz is a good first attempt, as I'll explain soon there is way too much happening in way too small a space...

#### Here is the original visualization

<img width="432" alt="Screen Shot 2022-02-06 at 15 40 59" src="https://user-images.githubusercontent.com/98067398/152700494-31c252e2-38a6-49ca-b2dd-28d2bda8c940.png">

###### [Source](https://www.scientificamerican.com/article/graphic-science-caffeine-high-more-and-more-products-contain-large-doses/)

### The Critique

The criteria I used to critique this data visualization came from the [Data Visualization Effectiveness Profile](http://www.perceptualedge.com/articles/visual_business_intelligence/data_visualization_effectiveness_profile.pdf) by Stephen Few. This method of critique looks at six qualities of a visualization, and ranks them on a 1-10 scale: Usefulness, Completeness, Perceptibility, Truthfulness, Intuitiveness, Aesthetics, and Engagement

First, the good:
* The graph does a decent job at showing not only how many products contain some amount of caffeine, but the vast differences in which products have more or less caffeine.
* Looking just at the data that are presented here, the reader has everything they would need to understand the point of the visualization--lots of stuff has caffeine in it, even beyond coffee, tea, and energy drinks.
* Visually, the graph catches the eye with its use of different colors for different product types.

Now, the not so good...
* This visualization is way too busy--too many elements are fighting for the viewer's attention: too many colors taking up the same visual space, and way too much text
* Layout of graph is counterintuitive to how an audience used to looking at info from left -> right would read this. The placement of y-axis on right side of graph led me to think that it was turned on its side for some reason
* "Product type" is distracting & unnecessary, at least in this iteration
* Presentation of information is way too compact--e.g. on first glance the viewer may not even notice the "Solids" portion of the graph because it is crammed at the lower right edge of the image

The data are all laid out for the viewer, and comparing them to a [chart from the Center for Science in the Public Interest(CSPI)](https://www.cspinet.org/eating-healthy/ingredients-of-concern/caffeine-chart) the designer did not leave any info out or obfuscate the data. Rather, the design itself gets in the way of the story behind the viz--for example, the different colored polygons all overlap with each other, so a viewer may get the impression that there is some significance to the caffeine content of a Keurig K-Cup being in both the Tea and Coffee groups. 

### Data Collection

I found the dataset that most lines up with what is presented in this viz from the CSPI chart, but unfortunately there was no table from which I could download these numbers and import them into a .csv file. The workaround I found was to screen shot each table on the site, convert all of the images to a PDF and then further convert the data from images to a text-based format that [Tabula](https://tabula.technology/) could then read. From there I extracted the relevant data into a .csv file so it could be input into a dataviz program.

### Wireframing a Solution

Coming up with an alternate visualization was, to put it mildly, a challenge; when I first saw this visualization I could tell immediately that it was too much to try and read or understand in too little space. I understand the underlying point to the graph--wow, a lot of stuff sure does have a lot of caffeine--but each element was fighting for my attention. I thought about how to preserve the most important information: Product Type and Name, Caffeine Content (by milligram), and Serving Size (in ounces).

Simply plotting each caffeine product on a graph without further context would be boring to look at, and a bar or pie chart would not capture all of the finer detail. I decided to visualize the data in a circle hierarchy, first roughly sketching out each larger circle and identifying the inner circles:

![Hand_drawn_viz](https://user-images.githubusercontent.com/98067398/152703110-03762bd4-9403-49a9-a6bc-30550fb99572.JPG)

And then I entered the  .csv file into Flourish to create a more fleshed-out sample:

<div class="flourish-embed flourish-hierarchy" data-src="visualisation/8625916"><script src="https://public.flourish.studio/resources/embed.js"></script></div>

###### [Data Source](https://www.cspinet.org/eating-healthy/ingredients-of-concern/caffeine-chart)

### Testing my Solution & Getting Feedback

I then showed the second visualization to two colleagues, neither of which has much of a background in dataviz but who are used to seeing datasets such as this one, to solicit feedback. I did not show them the original visualization until after they saw the recreated one, as a point of comparison

Questions I asked of my colleagues were:
* What do you think this visualization is showing you?
* While navigating this visualization, are you able to understand what the "message" is?
* Is there anything you are confused about, or that you didn't understand without explanation?
* Who do you think this visualization is for?
* What would you change, if anything?

Colleague 1: I'm a little uncertain of what I'm looking at...oh, wait *[clicks through filter]* Ah, I see, this is a filter for the different kinds of caffeinated products, and it says at the bottom that the sizing is dependant on the amount of caffeine in each product. I don't know if the data makes the most sense in this format *[I proceeded to show them a few more possible visualizations]* Okay, I see why you chose this one. I think I get the message of the visualization, it is telling me how much caffeine is in different products...wow, there is a lot of products, I would not have guessed that there was caffeinated sparkling water. I think that if you choose a different color palette for each category, the viewer will see that these are different kinds of products. This looks like it would be helpful to people hoping to change their caffeine intake, or maybe a nutritionist could use this.

Colleague 2: I think this is a chart that gives me a visual ratio of how much caffeine is in a given container in relation to its size.  It tells me lots of caffeine is in lots of things...[it's] surprising that Dunkin rivals Starbucks because I mostly think of them as a donut place, as opposed to a tiny coffee empire. The intended audience is nutritionists, people with caffeine sensitivities, and parents. I might make a key on the side that shows the colors and how they relate to the amount of caffeine (even as just a range like 100-200mg for instance) so I can get a sense of how much caffeine is in there instead of having to zoom in (which is still great for exact numbers). Also the circles look like the top of cups.

I agree with both of my colleagues: while I feel this format of hierarchical circles better signifies the amount of caffeine in different products relative to their serving size, there is still not enough of a difference between elements to really drive that point home. There was a general understanding of the "point" of the visual, and in both cases the viewer stated that the original visualization was too crowded:

> Colleague 1: What am I supposed to get from this graph? Why does it look like it is on its side?
> Colleague 2: Yeah, this is way too much to read to get the point; are [the polygons] overlapping for a specific reason, or is it just how the graph is designed?

That said, there *still* was a lack of understanding when initially looking at the dataviz; one colleague recommended I include a legend on the side to orient viewers, and another said I should choose more distinctive colors and possibly make products with more caffeine darker in the viz.

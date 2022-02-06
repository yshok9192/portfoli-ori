## Critique by Design

This assignment was twofold: find a data visualization out in the wild that could use a bit of a tune-up and identify areas of improvement; and wireframe, then design, a solution that makes the data more readable, understandable, and pretty to look at. I chose to look at [this](https://www.scientificamerican.com/article/graphic-science-caffeine-high-more-and-more-products-contain-large-doses/) visualization from *Scientific American*, mapping out how much caffeine is in everyday products--not just coffee, but water, chocolate, and jelly beans. The idea behind the viz is to highlight just how much caffeine we are consuming beyond the regular fare of coffee, tea, and energy drinks, and while I think the viz is a good first attempt, as I'll explain soon there is way too much happening in way too small a space...

#### Here is the original visualization

<img width="432" alt="Screen Shot 2022-02-06 at 15 40 59" src="https://user-images.githubusercontent.com/98067398/152700494-31c252e2-38a6-49ca-b2dd-28d2bda8c940.png">

###### [Source](https://www.scientificamerican.com/article/graphic-science-caffeine-high-more-and-more-products-contain-large-doses/)

### The Critique

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

### 

## Critique by Design

#### Click [here](https://yshok9192.github.io/portfoli-ori/) to go home

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

With the final version of my recreation, I will (or will try to):
* Include a legend of each product type, or make each type more distinctice (via different colors)
* Make each product's representation in the viz size relative to its serving size, i.e. a Starbucks drink that is 16 oz. but has 310 mg. of caffeine will be larger than a Dunkin' Coffee that is 20 oz. but has 270 mg. of caffeine

### The Final Product!

After showing the mockup viz that I made in Flourish, my classmates agreed that arranging these data into a "packed bubble" format with each bubble's size corresponding to the amount of caffeine in each product gave the viewer a better sense of not just how many products contain caffeine, but the relative serving size of the product compared to its caffeine content. The color palette I chose based on, in my opinion, the colors that come to mind when someone says "coffee" or "energy drink"-- there was some trouble with having each product type have a distinct color, as Tableau seemingly does not have that functionality for this particular visualization, but I believe the colors are distinct enough to get the point across.

<div class='tableauPlaceholder' id='viz1644267080207' style='position: relative'><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='Caffeine_1_16442060206390&#47;Sheet3' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' />
</object></div>
<script type='text/javascript'>
  var divElement = document.getElementById('viz1644267080207');
  var vizElement = divElement.getElementsByTagName('object')[0];
  vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';
  var scriptElement = document.createElement('script');
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';
  vizElement.parentNode.insertBefore(scriptElement, vizElement);
</script>

###### [Data Source](https://www.cspinet.org/eating-healthy/ingredients-of-concern/caffeine-chart)

While I am much happier with this visualization, and received feedback saying that my recreation was much easier to understand than the original *Scientific American* version, there are still things I wish I could put onto the screen:

* Changing the size of the font on each bubble to include the entire Product Name. The products with more caffeine content are more descriptive, but a user still has to hover over other bubbles to see what the info contained is. 
* Selecting all of one Product Type. Tableau seems to only allow a color scheme to be applied to one attribute pill--in this case, because I wanted to highlight the caffeine content I chose to set Color to "Serving Size". Setting the color scheme to "Product Type" caused the bubbles to be roughly equal size in the visualization.
<img width="526" alt="Screen Shot 2022-02-07 at 16 28 27" src="https://user-images.githubusercontent.com/98067398/152874985-7eabe02c-fae7-49e3-8a28-60366b956af5.png"> 
<img width="156" alt="Screen Shot 2022-02-07 at 16 28 33" src="https://user-images.githubusercontent.com/98067398/152875043-00b509ed-4791-4049-8496-56dc6f90efd0.png">

###### Product Type is much more distinctive, but still leaves something to be desired...Screenshots from Tableau.

This may be due to my relative lack of experience and knowledge of Tableau, and I hope to improve on that.

#### Alternative Visualization

<div class='tableauPlaceholder' id='viz1644269532281' style='position: relative'><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='caffeine_2&#47;Sheet6' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' />
</object></div>                
<script type='text/javascript'>                    
  var divElement = document.getElementById('viz1644269532281');                    
  var vizElement = divElement.getElementsByTagName('object')[0];                    
  vizElement.style.width='100%';
  vizElement.style.height=(divElement.offsetWidth*0.75)+'px';                    
  var scriptElement = document.createElement('script');                    
  scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    
  vizElement.parentNode.insertBefore(scriptElement, vizElement);                
</script>

###### [Data Source](https://www.cspinet.org/eating-healthy/ingredients-of-concern/caffeine-chart)

This visualization is a little closer to expressing just how much caffeine is in everyday products, but takes a lot of scrolling...trial and error! 

Anyway, thank you for reading! I hope my visualization(s) are an improvement on the original...will any of this info change my caffeine intake? Remains to be seen!

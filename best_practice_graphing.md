# Graphing Best Practices

---

**Overview.**  We know how to plot. Now we need to know how to plot with style to effectively communicate with our audience.

---

Let's take a step back from tactical coding details and remember why we are here: We want to be able to harness and *effectivly communicate* aspects of data to our friends, teammates, managers, etc. How do we achieve this goal? I will borrow from [Tufte](https://www.edwardtufte.com/tufte/books_vdqi) and say that we want to adhere to some **principals of graphical integrity and excellence**.

## Graphical Excellence

The points below are more like principals rather than rules. One way to use them is when preparing a graph, ask your self the following question: Is this showing the data? Is it answering the question I want? Will the viewer see what I'm thinking? Below are more details.

### Show the data

### Answer a question
It serves a purpose, ...

Be closely integrated with text and further analysis.

### Get the viewer to think about the data
not the method, design, technology behind its production, how hard it was.

### Encourage the eye to compare and contrast
 Reveal the data at different levels of detail

 ---

## Graphical Integrity

These are guidelines to follow in making an effective and truthful graph. As I've mentioned before there are always times when rules show be broken, but I'd be hard pressed to say


### Clear, thorough, and detailed labeling

This almost goes without saying, but we must. Every graph should have a descriptive title, the axis should be descriptively labeled. If there are multiple lines, think about a legend or other means of to demarcate the difference.

Often when you see a graph that is poorly labeled and ask the person who made it *why* they did not label it is essentially comes down to lack of know how and/or lazyness. For example, when plotting in Excel, the fight to figure out how to modify the labels can be very time consuming, so people just give up.

**No more.** This is the power of Matplotlib. It allows us to easily, quickly, add labels, titles, and other descriptive features. So when your audience looks at the graph, they don't start asking questions about the axis or other features, but ask questions about the substance and your message.

### Show data variation; not design variation

Matplotlib gives you a lot of control of the design of your graphic. That does not mean you should always use it. Simple is always good. Varying the design, making it overly complicated, showing off a new trick...just because you can is bad.

Here is an example that I noticed from a previous semester. Students were taught how to create violin chart in Seaborn. Every project had a violin chart. Students were just showing that they new how to use a particular variation on plotting. This did not help---and, in fact, detracted from many good projects. In the projects the students were showing design variation, not thinking, does this chart show the data variation I want to show.

Another aspect of this is when presenting multiple different graphs. Changing the design *within* a document (e.g. a Jupyter notebook, power point presentation) is jarring to the eye. It makes the audience work by having to constantly recalibrate their expectations. And guess what, audience's don't like to work. It's bad. So stick to a style and proceed.

### Use the "right" graph for the question

This is related to the prior point. We want to show the data. Not show that we can make and design a graph. Here are some core types...

- Line plot: good for time series data

- Scatter plot: good for

- Bar char: good for displaying univariate comparisons across categories.

- Pie chart:

- multi-types:

- data maps:


### Use the appropriate and comparable units

One of the goals of graphical excellence (see below) is to encourage comparability. To have a data representation be comparable, the units of the data must be chosen and displayed in the appropriate way to encourage this goal.

A trivial example, might be temperatures across countries. When we do this, we better make sure everything is all in Celsius or Fahrenheit. Even better, when presenting your data to people from the US, convert it to Fahrenheit and vice versa when talking to people from the rest of the world.

Money over time is another good example. Overtime, the real purchasing power of money changes, so when you report things in dollars, a question that always arises is: Is a dollar in 2018 the same as a dollar in 1960. In general, no. So when we plot something in dollars over time, their "real" value is *not comparable* even though you may be asking your audience to make the comparison.

A final point is to think about the use of normalizations. Sometimes the units of the data are hard to interpret. It may time a lot of text or time to explain what a particular value means. One way to overcome this is to pick a normalization. That is, normalize the data relative to some baseline value.  Relative to another country, point in time, the mean or median value, etc. Returning to the example above, this is essentially what real measures do evaluate the value of money at prices in a specified base year.

---

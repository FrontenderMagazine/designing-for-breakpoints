# Designing for Breakpoints

**A note from the editors:** We're pleased to present an excerpt from Chapter 7 
of [Responsive Design Workflow][1], Stephen Hay's new book, available now from 
New Riders.

Jeremy Keith notes that what happens between the breakpoints is just as
important as the breakpoints themselves—perhaps even more so. While I agree with
this, we do have to start somewhere. In a way, this part of the process reminds
me of storyboarding, or creating animation keyframes, with the in-between frames
being developed later. We’re going to do that here.

_**Major breakpoints** are conditions that, when met, trigger major changes in 
your design. A major breakpoint might be, for example, where your entire layout 
must change from two columns to four._

Let’s say you’ve chosen three basic design directions from your thumbnails. 
Think about what your major breakpoints will look like (Figure 7.6). And here’s 
the key: try to come up with as few major breakpoints as possible. That might 
sound crazy, since we’re talking about responsive design. After all, we have 
media queries, so let’s use about 12 of them, right? No! If a linear layout 
works for every screen and is appropriate for your particular concept, then 
there’s no need for different layouts. In that case, simply describe what will 
happen when the screen gets larger. Will everything generally stay the same, 
with changes only to font size, line height and margins? If so, sketch those. 
For these variations, make thumbnails first, explore some options, and then 
move on to larger, more detailed sketches. Use your breakpoint graph as a guide 
at first and make sketches according to the breakpoints you’ve estimated on 
your graph.

When thinking about major breakpoints, remember to think about device classes.
If you’re thinking about smartphones, tablets, laptops/desktops, TVs, and game
consoles, for example, you’re heading in the right direction. If you’re thinking
in terms of brand names and specific operating systems, you’re on the wrong
track. The idea is to think in terms of general device classifications and,
sometimes, device capabilities. Capabilities are more important when designing
web applications, since you should be thinking about what screens will look like
both with and without any particular capability.

**Rough sketches** of major breakpoints can help you determine:

* Whether or not more major breakpoints are needed
* Which design choice will be the most labor intensive; you might opt for a 
design that will better fit within time and budget constraints
* Whether or not a particular device class has been neglected or needs further 
consideration
* What technologies you’ll need to develop the design responsively

_**Rough sketches** are more detailed than thumbnails, but they shouldn’t take 
a long time to create. In a short period, you should have a sketch of each 
major breakpoint for each of your chosen designs. This should be enough to 
decide on one of the designs._

![Figure 7.6][Figure 7.6]

*Figure 7.6: Most websites need very few major breakpoints.*

So where and when will you sketch **minor breakpoints**? In the browser, when
you do your web-based mockup. You’ll find out why and how in the next chapter.
In the meantime, simply focus on making sketches of the state of your web pages
or app screens at the major breakpoints of each design.

_**Minor breakpoints** are conditions that, when met, trigger small changes in 
your design. An example would be moving form labels from above text fields to 
the left of those fields, while the rest of the design remains the same._

At this point, don’t worry too much if you notice that the initial breakpoints
on your breakpoint graph simply won’t do. Those were just a starting point, and
you’re free to revise your estimate based on your sketches. You might even
decide that you need an extra breakpoint for a given design and record that in
sketch form; you can add that breakpoint to your graph. This is a cycle of
discovery, learning, and revision.

## Think about your content while sketching

While sketching, you’ll certainly be thinking about the way things should look.
My experience is that much UI sketching of this type revolves around the layout
of elements on the screen. I’ve found it useful to keep thinking about the
content while sketching, and to consider what will happen to the content in
various situations. When designing responsively, it can be useful to consider
how you’ll handle the following content in particular:

* Text
* Navigation
* Tables

Oh, sure, there are many more things to consider, and you’ll end up creating
your own list of “things to do some extra thinking about” as the project
progresses. For now, let’s take a look at the items listed above.

### TEXT

Before you say, “Hey, wait a minute, didn’t you just tell me that I didn’t have
to draw text while sketching?” hear me out. While sketching, there are a couple
of text-related issues you’ll need to tackle: column width and text size, both
of which are relevant *in proportion to the screen and the other elements on the
page*.

Column width is fairly obvious, but it can be difficult to estimate how wide a
column will be with *actual* text. In this case, sketching on a device might
give you a better idea of the actual space you have to work with. Another method
I’ve used is just to make a simple HTML page that contains only text, and load
that into a device’s browser (or even an emulator, which while not optimal still
gives a more realistic impression than lines on paper). When the text seems too
large or too small, you can adjust the font size accordingly. Once it seems
right, you’ll be able to make your sketches a bit more realistic.

Think about the size of links—not only the text size, but also the amount of
space around them. Both of these factors play a role in the **touchability** or
**clickability** of links (and buttons): large links and buttons are easier
targets, but slightly smaller links with plenty of space around them can work
just as well. That said, there’s a decent chance that no matter what you choose
to sketch, you’ll end up making changes again when you create your mockups.

_**Note**: Distinguish between **touchability** and **clickability**. Many 
designers, myself included, have made the mistake of refining links for people 
who click on them using a mouse, or even via the keyboard, without considering 
how touchable these links are for people on touch devices._

This is the great thing about sketching that I can’t repeat often enough: 
you’re going to refine your design in the browser anyway, so the speed with 
which you can try things out when sketching means you won’t have to do detail 
work more than once (unless your client has changes, but we all know that 
never happens).

### NAVIGATION

Navigation is another poster child for sketching on actual devices. The size
issues are the same as with links, but there’s a lot more thinking to do in
terms of the design of navigation for various devices, which means navigation
might change significantly at each major breakpoint.

Think back to Bryan Rieger’s practice of designing in text first, and ponder
what you would do *before* the very first breakpoint if you had only plain HTML
and CSS at your disposal—in other words, if you had no JavaScript. That means
no, you can’t have your menu collapsed at the top of the screen and have it drop
down when someone touches it. If you have your menu at the top, it’s in its
expanded form and takes up all the vertical space it normally would.

This is a controversial enough subject, with even accessibility gurus in
disagreement: JavaScript, after all, is currently considered an “accessibility
supported” technology. But this isn’t necessarily about accessibility. It’s
about *thinking* about what happens when a browser lacks JavaScript support, or
if the JavaScript available on the device is different than what you’d expect.
Your content will be presented in a certain way before JavaScript does its thing
with it, no matter what the browser. So why not think about what that initial
state will be?

In the chapter on wireframes, I talked about my preferred pattern for navigation
on the smallest screens: keep it near the bottom of the screen and place a link
to that navigation near the top of the screen. JavaScript, when available and
working as expected, can move that navigation up to the top and create the drop-
down menu on the fly.

But a pattern is not design law, so how you choose to handle the smallest
screens will depend on your project. If I had only a few links in my navigation,
I might very well put the menu at the top from the very start, and there it
would stay at every breakpoint.

Remember that JavaScript and CSS let you do a lot of rearranging of stuff on the
screen. That knowledge should empower you to safely design a great page with
plain HTML and use JavaScript and CSS to spice it up any way you like. This is
the essence of progressive enhancement.

### TABLES

Tables! Oh, the bane of the responsive designer (or wait, is that images? Or
video? Or layout? Ahem). Tables are tough to deal with on small screens. I’d
love to tell you I have all the answers, but instead I have more questions.
Hopefully, these will lead you to a solution. It’s good to think about these
while you’re sketching.

First of all, what types of tables will you be dealing with? Narrow? Wide?
Numerical? Textual? Your content inventory should give you enough information to
answer these simple questions. Once you’ve considered those, try to categorize
the types of tables you have into something like the following classes (Figure
7.7):

* **Small-screen-friendly tables**, which you’ll probably leave as they are, 
because they’re small enough and will work fine on most small screens.
* **Blockable tables**, which you can alter with CSS so that each row in the 
table functions visually as a block item in a list (Figure 7.8).
* **Chartable tables**, which contain numerical data that can be transformed 
into a chart, graph, or other visualization that will take up less space on 
a small screen.
* **Difficult tables**, which are hard enough to deal with that you’ll need 
to come up with a different plan for them, sometimes even on a case-by-case 
basis. These are our enemies, but unfortunately, are the friends of our 
clients, who all love Microsoft Excel. Oh well.

![Figure 7.7][Figure 7.7]

*Figure 7.7: There are several different types of tables, and different ways of 
dealing with them on small screens. (Sources: [mobilism.nl][2] and 
[eu-verantwoording.nl][3])*

![Figure 7.8][Figure 7.8]

*Figure 7.8: One way of dealing with small screen tables is to treat each 
row as a block.*

Thinking again in terms of progressive enhancement, the base design should
probably just include the whole table, which means that the user will have to
scroll horizontally to see the whole thing in many cases. On top of this, we can
employ CSS and JavaScript, when they’re available, to do some magic for us.
Blockable and chartable tables can be *blocked* with CSS and *charted* with
JavaScript. Plenty of designers and developers have experimented with many
different options for tables, from simply making the table itself scrollable to
exchanging columns and rows.

The fun part is that what you do on small screens isn’t necessarily what you’ll
do on larger screens. That’s why now—when all you have to do is sketch and it
won’t take much time—is the time to think about the changes you’ll be making at
each breakpoint.

## What to do if you get stuck

Every designer gets stuck at some point. It’s no big deal unless you treat it
like one. There are countless ways to deal with it, from asking yourself *what
if* questions (“What if it weren’t a table, but a list?” is what I asked myself
before “blockifying” the attendees table for the Mobilism site) to the cliché
*taking a shower*, which you hopefully do on a regular basis anyway. The reason
this chapter focuses so much on sketching is because the act of drawing itself
can actually stimulate your brain to come up with more ideas, provided you push
it hard enough by sketching past your comfort zone of first-come ideas.

If your problem is that you’re stuck creatively, there are many inspiring books
and resources to get your creative engine started during the bitter cold of
designer’s block. Although there are plenty of resources on design and
creativity itself (try such classics as Edward de Bono’s *Lateral Thinking*),
the greatest inspiration can come from sources outside the realm of design.<a href="#note-1" id="ref-1" class="reference">1</a> 
Trying to combine things that normally aren’t combined can lead to surprising 
results. It’s a simple little trick, but I’ve often used Brian Eno and Peter 
Schmidt’s *Oblique Strategies* to force me to take a different approach.<a href="#note-2" id="ref-2" class="reference">2</a> 
Worst case, it’s a lot of fun. Best case, you’ve got a great idea!

If your problem is that you’re not sure how to handle something in the context
of responsive design, there’s no harm in researching how others have solved
problems like yours. Just be sure to use your creativity and tailor any ideas
you might find to your own situation; after all, you’re a designer. At the time
of this writing I find Brad Frost’s *This Is Responsive* to be one of the most
exhaustive collections of responsive design patterns and resources available.<a href="#note-3" id="ref-3" class="reference">3</a> 
You can spend hours going through there and you’ll certainly come across 
something that will get you unstuck.

Excerpted from Responsive Design Workflow by Stephen Hay. Copyright © 2013.  
Used with permission of Pearson Education, Inc. and New Riders.

---

### NOTES

<a href="#ref-1" id="note-1" class="note">1.</a> Edward de Bono, Lateral Thinking (Viking, 2009).  
<a href="#ref-2" id="note-2" class="note">2.</a> [http://en.wikipedia.org/wiki/Oblique_Strategies][4]  
<a href="#ref-3" id="note-3" class="note">3.</a> [http://bradfrost.github.com/this-is-responsive/][5]  

[1]: http://www.peachpit.com/store/responsive-design-workflow-9780321887863
[2]: http://mobilism.nl/
[3]: http://eu-verantwoording.nl/
[4]: http://en.wikipedia.org/wiki/Oblique_Strategies
[5]: http://bradfrost.github.com/this-is-responsive/

[Figure 7.6]: img/ch07-06_full.png
[Figure 7.7]: img/ch07-07_full.png
[Figure 7.8]: img/ch07-08_full.png

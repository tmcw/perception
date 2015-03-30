# Perception

_collected & summarized research on the effectiveness of visualization techniques_

## Pie Charts

Pie charts are misleading: position and color of slices affects our judgments
of their size. Prefer bar charts to pie charts.

* [Scientific American Summary](http://blogs.scientificamerican.com/observations/2011/03/28/infographics-the-great-circle-debate/)
* [Save the Pies for Dessert](http://www.perceptualedge.com/articles/visual_business_intelligence/save_the_pies_for_dessert.pdf) by
  [Stephen Few](http://www.perceptualedge.com/)

> Our analysis has provided, in a sense, a resolution of the 'Bar-Circle Debate'...about whether
> the divided bar chart or the pie chart was superior for portraying parts of a whole.
> The contest appears to have ended in a draw. We conclude that neither graphical form
> should be used because other methods are demonstrably better.

> A divided bar chart can always be replaced by a grouped bar chart; again,
> we prefer a grouped dot chart to a grouped bar chart.

[Graphical Perception: Theory, Experimentation, and Application to the Development of Graphical Methods](http://www.cs.ubc.ca/~tmm/courses/cpsc533c-04-spr/readings/cleveland.pdf) by William S. Cleveland; Robert McGill

## Animated Graphics

[Change Blindness in Animated Choropleth Maps: An Empirical Study](http://thecartofish.com/FishGoldsBatts2011.pdf)
by [Carolyn Fish](https://twitter.com/cartofish), Kirk P. Goldsberry and Sarah Battersby

Many people are change-blind to animated graphics, especially those
that abruptly transition between colors and shapes. Animating value changes
improves the awareness and measurement of change.

[Animated Transitions in Statistical Data Graphics](http://vis.stanford.edu/papers/animated-transitions)
by [Jeffrey Heer](http://homes.cs.washington.edu/~jheer/), George Robertson

> There was evidence that
> staged animation, such as staggered movements to reduce occlusion
> and separate stages for axis rescaling and value changes, provide
> additional benefits. This claim is strongly backed by subject
> preferences and consistently (though at times marginally) supported
> by error measures. The results further discourage the use of complex
> multi-stage transitions, favoring simple staging over aggressive “do
> one thing at a time” staging.

A popular industry application of this research is [d3js](http://d3js.org/)'s
staggered transitions [as seen in its showreel](http://bl.ocks.org/mbostock/3943967).

> According to this analysis, if there are benefits to animation, they should be evident
> especially for continuous rather than discrete changes, in particular, for manner of
> change and for microsteps, the subtle and intricate timing relations among parts of a
> complex system. However, even for these cases, clever schematization of static diagrams
> may be just as effective as animation. For example, arrows are effective in indicating
> temporal sequence and direction of motion

[Animation: can it facilitate?](http://www2.sims.berkeley.edu/courses/is247/f05/readings/Tversky_AnimationFacilitate_IJHCS02.pdf)

## Animating Pan & Zoom

> Large 2D information spaces, such as maps, images, or abstract visualizations,
> require views at various level of detail: Close ups to
> inspect details, overviews to maintain (literally) an overview. Users
> often switch between these views. We discuss how smooth animations
> from one view to another can be defined. To this end, a
> metric on the effect of simultaneous zooming and panning is defined,
> based on an estimate of the perceived velocity

The proposed algorithm, which is implemented in [Leaflet](http://leafletjs.com/) 0.8,
and [Mapbox GL](https://www.mapbox.com/mapbox-gl/), presents a way to pan and
zoom that is less jarring and easier to follow that simple linear interpolation
of both variables. The paper doesn't discuss cognitive benefits, but
the results are often percieved as more pleasant than the simple way.

[Smooth and efficient zooming and panning](http://www.win.tue.nl/~vanwijk/zoompan.pdf) by Jarke J. van Wijk & Wim A.A. Nuij

## Treemaps

[Perceptual Guidelines for Creating Rectangular Treemaps](http://vis.stanford.edu/files/2010-Treemaps-InfoVis.pdf)
by Nicholas Kong, Jeffrey Heer, and Maneesh Agrawala

* the optimal distribution of rectangle aspect ratios within a treemap should include non-squares, but should avoid extreme aspect ratios.
* even at relatively low data densities treemaps result in faster comparisons than
  bar charts.

_[d3 implementation](https://github.com/mbostock/d3/wiki/Treemap-Layout)_

## Colors

> use hue to show categorical differences and use lightness to show
> lightness differences

[Color Use Guidelines for Data Representation](http://www.personal.psu.edu/cab38/Pub_scans/Brewer_1999_Color-Use-Guidelines-ASAproc.pdf)

Avoid interpolating color palettes using RGB values, because the hue
and brightness of colors within that system are strongly linked. Instead,
use perceptual color spaces like CIE.

[Generating Color Palettes using Intuitive Parameters](http://magnaview.nl/documents/MagnaView-M_Wijffelaars-Generating_color_palettes_using_intuitive_parameters.pdf) &
[How to Avoid Equidistant Colors](http://vis4.net/blog/posts/avoid-equidistant-hsv-colors/)

When choosing map and visualization colors, check that your color scheme is colorblind friendly and [ADA: Section 508 compliant](http://www.hhs.gov/web/508/accessiblefiles/checklisthtml.html).  [ColorBrewer](http://colorbrewer2.org/) and [WebAIM Contrast Color](http://webaim.org/resources/contrastchecker/) are great resources to check colorblind safe, print friendly, and photocopy safe color schemes.

## Fisheye Effect

> A fisheye camera lens is a very wide angle lens that magnifies nearby objects while
> shrinking distant objects. It is a valuable tool for seeing both “local detail” and
> “global context” simultaneously.

[Graphical Fisheye Views](ftp://ftp.cs.brown.edu/pub/techreports/93/cs93-40.pdf) by Mano jit Sarkar and Marc H. Brown

_[d3 example](http://bost.ocks.org/mike/fisheye/)_

## Chart Types

* [Horizon charts](http://www.perceptualedge.com/articles/visual_business_intelligence/time_on_the_horizon.pdf) improve recognition of both small and large changes for data that fits x & y axes, like time series
* [Chord diagrams](http://genome.cshlp.org/content/early/2009/06/15/gr.092759.109.full.pdf+html) enable visualization of multi-dimensional and connected data
* [Stacked Graphs](http://www.leebyron.com/else/streamgraph/) also known as streamgraphs, which gained popularity with ThemeRiver and its
  visualization of last.fm data. An alternative to stacked area charts,
  they can thrive with series that vary and disappear over time.

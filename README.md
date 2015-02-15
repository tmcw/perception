# Perception

_collected & summarized research on the effectiveness of visualization techniques_

## Pie Charts

Pie charts are misleading: position and color of slices affects our judgments
of their size. Prefer bar charts to pie charts.

* [Scientific American Summary](http://blogs.scientificamerican.com/observations/2011/03/28/infographics-the-great-circle-debate/)
* [Save the Pies for Dessert](http://www.perceptualedge.com/articles/visual_business_intelligence/save_the_pies_for_dessert.pdf) by
  [Stephen Few](http://www.perceptualedge.com/)

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
staggered transitions [as seen in its showreel](http://bl.ocks.org/mbostock/1256572).

## Treemaps

[Perceptual Guidelines for Creating Rectangular Treemaps](http://vis.stanford.edu/files/2010-Treemaps-InfoVis.pdf)
by Nicholas Kong, Jeffrey Heer, and Maneesh Agrawala

* the optimal distribution of rectangle aspect ratios within a treemap should include non-squares, but should avoid extreme aspect ratios.
* even at relatively low data densities treemaps result in faster comparisons than
  bar charts.

## Colors

> use hue to show categorical differences and use lightness to show
> lightness differences

[Color Use Guidelines for Data Representation](http://www.personal.psu.edu/cab38/Pub_scans/Brewer_1999_Color-Use-Guidelines-ASAproc.pdf)

Avoid interpolating color palettes using RGB values, because the hue
and brightness of colors within that system are strongly linked. Instead,
use perceptual color spaces like CIE.

[Generating Color Palettes using Intuitive Parameters](http://magnaview.nl/documents/MagnaView-M_Wijffelaars-Generating_color_palettes_using_intuitive_parameters.pdf) &
[How to Avoid Equidistant Colors](http://vis4.net/blog/posts/avoid-equidistant-hsv-colors/)

## Fisheye Effect

> A fisheye camera lens is a very wide angle lens that magnifies nearby objects while
> shrinking distant objects. It is a valuable tool for seeing both “local detail” and
> “global context” simultaneously.

[Graphical Fisheye Views](ftp://ftp.cs.brown.edu/pub/techreports/93/cs93-40.pdf) by Mano jit Sarkar and Marc H. Brown

_[d3 example](http://bost.ocks.org/mike/fisheye/)_

## Chart Types

* [Horizon charts improve recognition of both small and large changes for data that fits x & y axes, like time series](http://www.perceptualedge.com/articles/visual_business_intelligence/time_on_the_horizon.pdf)
* [Chord diagrams](http://genome.cshlp.org/content/early/2009/06/15/gr.092759.109.full.pdf+html) enable visualization of multi-dimensional and connected data

Version 1.11.2
==============

This is a minor bug fix release with a number of small but important
bug fixes. Special thanks to @darynwhite for his contributions.

Bug fixes:

- Compatibility with pandas 0.24.0 release
  ([#3433](https://github.com/ioam/holoviews/pull/3433))	
- Fixed timestamp selections on streams
  ([#3427](https://github.com/ioam/holoviews/pull/3427))
- Fixed persisting options during clone on Overlay
  ([#3435](https://github.com/ioam/holoviews/pull/3435))
- Ensure cftime datetimes are displayed as a slider
  ([#3413](https://github.com/ioam/holoviews/pull/3413))
  
Enhancements:

- Allow defining hook on backend load
  ([#3429](https://github.com/ioam/holoviews/pull/3429))
- Improvements for handling graph attributes in Graph.from_networkx
  ([#3432](https://github.com/ioam/holoviews/pull/3432))


Version 1.11.1
==============

This is a minor bug fix release with a number of important bug fixes,
enhancements and updates to the documentation. Special thanks to
@ahuang11, @garibarba and @Safrone for their contributions.

Bug fixes:

- Fixed bug plotting adjoined histograms in matplotlib
  ([#3377](https://github.com/ioam/holoviews/pull/3377))
- Fixed bug updating bokeh RGB alpha value
  ([#3371](https://github.com/ioam/holoviews/pull/3371))
- Handled issue when colorbar limits were equal in bokeh
  ([#3382](https://github.com/ioam/holoviews/pull/3382))
- Fixed bugs plotting empty Violin and BoxWhisker elements
  ([#3397](https://github.com/ioam/holoviews/pull/3397),
  [#3405](https://github.com/ioam/holoviews/pull/3405))
- Fixed handling of characters that have no uppercase on Layout and
  Overlay objects
  (([#3403](https://github.com/ioam/holoviews/pull/3403))
- Fixed bug updating Polygon plots in bokeh
  ([#3409](https://github.com/ioam/holoviews/pull/3409))

Enhancements:

- Provide control over gridlines ticker and mirrored axis ticker by
  default ([#3398](https://github.com/ioam/holoviews/pull/3377))
- Enabled colorbars on CompositePlot classes such as Graphs, Chords
  etc. ([#3397](https://github.com/ioam/holoviews/pull/3396))
- Ensure that xarray backend retains dimension metadata when casting
  element ([#3401](https://github.com/ioam/holoviews/pull/3401))
- Consistently support clim options
  ([#3382](https://github.com/ioam/holoviews/pull/3382))
  
Documentation:

- Completed updates from .options to .opts API in the documentation
  ([#3364]((https://github.com/ioam/holoviews/pull/3364),
  [#3367]((https://github.com/ioam/holoviews/pull/3367))


Version 1.11.0
==============

This is a major release containing a large number of features and API
improvements. Specifically this release was devoted to improving the
general usability and accessibility of the HoloViews API and
deprecating parts of the API in anticipation for the 2.0 release.
To enable deprecation warnings for these deprecations set:

    hv.config.future_deprecations = True

The largest updates to the API relate to the options system which is now
more consistent, has better validation and better supports notebook
users without requiring IPython magics. The new `dim` transform
generalizes the mapping from data dimensions to visual dimensions,
greatly increasing the expressive power of the options system. Please
consult the updated user guides for more information.
	
Special thanks for the contributions by Andrew Huang (@ahuang11),
Julia Signell (@jsignell), Jon Mease (@jonmmease), and Zachary Barry
(@zbarry).

Features:

- Generalized support for style mapping using `dim` transforms
  ([2152](https://github.com/ioam/holoviews/pull/2152))
- Added alternative to opts magic with tab-completion
  ([#3173](https://github.com/ioam/holoviews/pull/3173))
- Added support for Polygons with holes and improved contours
  operation ([#3092](https://github.com/ioam/holoviews/pull/3092))
- Added support for Links to express complex interactivity in JS
  ([#2832](https://github.com/ioam/holoviews/pull/2832))
- Plotly improvements including support for plotly 3.0
  ([#3194](https://github.com/ioam/holoviews/pull/3194)), improved
  support for containers
  ([#3255](https://github.com/ioam/holoviews/pull/3255)) and support
  for more elements
  ([#3256](https://github.com/ioam/holoviews/pull/3256))
- Support for automatically padding plots using new `padding` option
  ([#2293](https://github.com/ioam/holoviews/pull/2293))
- Added `xlim`/`ylim` plot options to simplify setting axis ranges
  ([#2293](https://github.com/ioam/holoviews/pull/2293))
- Added `xlabel`/`ylabel` plot options to simplify overriding axis
  labels ([#2833](https://github.com/ioam/holoviews/issues/2833))
- Added `xformatter`/`yformatter` plot options to easily override tick
  formatter ([#3042](https://github.com/ioam/holoviews/pull/3042))
- Added `active_tools` options to allow defining tools to activate on
  bokeh plot initialization
  ([#3251](https://github.com/ioam/holoviews/pull/3251))
- Added `FreehandDraw` stream to allow freehand drawing on bokeh plots
  ([#2937](https://github.com/ioam/holoviews/pull/2937))
- Added support for `cftime` types for dates which are not supported
  by standard datetimes and calendars
  ([#2728](https://github.com/ioam/holoviews/pull/2728))
- Added top-level `save` and `render` functions to simplify exporting
  plots ([#3134](https://github.com/ioam/holoviews/pull/3134))
- Added support for updating Bokeh bokeh legends
  ([#3139](https://github.com/ioam/holoviews/pull/3139))
- Added support for indicating directed graphs with arrows
  ([#2521](https://github.com/ioam/holoviews/issues/2521))

Enhancements:

- Improved import times
  ([#3055](https://github.com/ioam/holoviews/pull/3055))
- Adopted Google style docstring and documented most core methods and
  classes ([#3128](https://github.com/ioam/holoviews/pull/3128)

Bug fixes:

- GIF rendering fixed under Windows
  ([#3151](https://github.com/ioam/holoviews/issues/3151))
- Fixes for hover on Path elements in bokeh
  ([#2472](https://github.com/ioam/holoviews/issues/2427),
  [#2872](https://github.com/ioam/holoviews/issues/2872))
- Fixes for handling TriMesh value dimensions on rasterization
  ([#3050](https://github.com/ioam/holoviews/pull/3050))

Deprecations:

- `finalize_hooks` renamed to `hooks`
  ([#3134](https://github.com/ioam/holoviews/pull/3134))
- All `*_index` and related options are now deprecated including
  `color_index`, `size_index`, `scaling_method`, `scaling_factor`,
  `size_fn` ([#2152](https://github.com/ioam/holoviews/pull/2152))
- Bars `group_index`, `category_index` and `stack_index` are deprecated in
  favor of stacked option
  ([#2828](https://github.com/ioam/holoviews/issues/2828))
- iris interface was moved to GeoViews
  ([#3054](https://github.com/ioam/holoviews/pull/3054))
- Top-level namespace was cleaned up
  ([#2224](https://github.com/ioam/holoviews/pull/2224))
- `ElementOpration`, `Layout.display` and `mdims` argument to `.to`
  now fully removed
  ([#3128](https://github.com/ioam/holoviews/pull/3128))
- `Element.mapping`, `ItemTable.values`, `Element.table`,
  `HoloMap.split_overlays`, `ViewableTree.from_values`,
  `ViewableTree.regroup` and `Element.collapse_data` methods now
  marked for deprecation
  ([#3128](https://github.com/ioam/holoviews/pull/3128))


Version 1.10.8
==============

This a likely the last hotfix release in the 1.10.x series containing
fixes for compatibility with bokeh 1.0 and matplotlib 3.0. It also
contains a wide array of fixes contributed and reported by users:

Special thanks for the contributions by Andrew Huang (@ahuang11),
Julia Signell (@jsignell), and Zachary Barry (@zbarry).

Enhancements:

- Add support for labels, choord, hextiles and area in `.to` interface
  ([#2924](https://github.com/ioam/holoviews/pull/2923))
- Allow defining default bokeh themes as strings on Renderer
  ([#2972](https://github.com/ioam/holoviews/pull/2972))
- Allow specifying fontsize for categorical axis ticks in bokeh
  ([#3047](https://github.com/ioam/holoviews/pull/3047))
- Allow hiding toolbar without disabling tools
  ([#3074](https://github.com/ioam/holoviews/pull/3074))
- Allow specifying explicit colormapping on non-categorical data
  ([#3071](https://github.com/ioam/holoviews/pull/3071))
- Support for displaying xarray without explicit coordinates
  ([#2968](https://github.com/ioam/holoviews/pull/2968))

Fixes:

- Ensured that objects are garbage collected when using
  linked streams ([#2111](https://github.com/ioam/holoviews/issues/2111))
- Allow dictionary data to reference values which are not dimensions
  ([#2855](https://github.com/ioam/holoviews/pull/2855),
  [#2859](https://github.com/ioam/holoviews/pull/2859))
- Fixes for zero and non-finite ranges in datashader operation
  ([#2860](https://github.com/ioam/holoviews/pull/2860),
  [#2863](https://github.com/ioam/holoviews/pull/2863),
  [#2869](https://github.com/ioam/holoviews/pull/2869))
- Fixes for CDSStream and drawing tools on bokeh server
  ([#2915](https://github.com/ioam/holoviews/pull/2915))
- Fixed issues with nans, datetimes and streaming on Area and Spread
  elements ([#2951](https://github.com/ioam/holoviews/pull/2951),
  [c55b044](https://github.com/ioam/holoviews/commit/c55b044))
- General fixes for datetime handling
  ([#3005](https://github.com/ioam/holoviews/pull/3005),
  [#3045](https://github.com/ioam/holoviews/pull/3045),
  [#3075](https://github.com/ioam/holoviews/pull/3074))
- Fixed handling of curvilinear and datetime coordinates on QuadMesh
  ([#3017](https://github.com/ioam/holoviews/pull/3017),
  [#3081](https://github.com/ioam/holoviews/pull/3081))
- Fixed issue when inverting a shared axis in bokeh
  ([#3083](https://github.com/ioam/holoviews/pull/3083))
- Fixed formatting of values in HoloMap widgets
  ([#2954](https://github.com/ioam/holoviews/pull/2954))
- Fixed setting fontsize for z-axis label
  ([#2967](https://github.com/ioam/holoviews/pull/2967))

Compatibility:

- Suppress warnings about rcParams in matplotlib 3.0
  ([#3013](https://github.com/ioam/holoviews/pull/3013),
  [#3058](https://github.com/ioam/holoviews/pull/3058),
  [#3104](https://github.com/ioam/holoviews/pull/3104))
- Fixed incompatibility with Python <=3.5
  ([#3073](https://github.com/ioam/holoviews/pull/3073))
- Fixed incompatibility with bokeh >=1.0
  ([#3051](https://github.com/ioam/holoviews/pull/3051))

Documentation:

- Completely overhauled the FAQ
  ([#2928](https://github.com/ioam/holoviews/pull/2928),
  [#2941](https://github.com/ioam/holoviews/pull/2941),
  [#2959](https://github.com/ioam/holoviews/pull/2959),
  [#3025](https://github.com/ioam/holoviews/pull/3025))

Version 1.10.7
==============

This a very minor hotfix release mostly containing fixes for datashader
aggregation of empty datasets:

Fixes:

- Fix datashader aggregation of empty and zero-range data
  ([#2860](https://github.com/ioam/holoviews/pull/2860),
  [#2863](https://github.com/ioam/holoviews/pull/2863))
- Disable validation for additional, non-referenced keys in the
  DictInterface ([#2860](https://github.com/ioam/holoviews/pull/2860))
- Fixed frame lookup for non-overlapping dimensions
  ([#2861](https://github.com/ioam/holoviews/pull/2861))
- Fixed ticks on log Colorbar if low value <= 0
  ([#2865](https://github.com/ioam/holoviews/pull/2865))


Version 1.10.6
==============

This another minor bug fix release in the 1.10 series and likely the
last one before the upcoming 1.11 release. In addition to some important
fixes relating to datashading and the handling of dask data, this
release includes a number of enhancements and fixes.

Enhancements:

- Added the ability to specify color intervals using the color_levels
  plot options ([#2797](https://github.com/ioam/holoviews/pull/2797))
- Allow defining port and multiple websocket origins on BokehRenderer.app
  ([#2801](https://github.com/ioam/holoviews/pull/2801))
- Support for datetimes in Curve step interpolation
  ([#2757](https://github.com/ioam/holoviews/pull/2757))
- Add ability to mute legend by default
  ([#2831](https://github.com/ioam/holoviews/pull/2831))
- Implemented ability to collapse and concatenate gridded data
  ([#2762](https://github.com/ioam/holoviews/pull/2762))
- Add support for cumulative histogram and explicit bins
  ([#2812](https://github.com/ioam/holoviews/pull/2812))

Fixes:

- Dataset discovers multi-indexes on dask dataframes
  ([#2789](https://github.com/ioam/holoviews/pull/2789))
- Fixes for datashading NdOverlays with datetime axis and data with
  zero range ([#2829](https://github.com/ioam/holoviews/pull/2829),
  [#2842](https://github.com/ioam/holoviews/pull/2842))


Version 1.10.5
==============

This is a minor bug fix release containing a mixture of small
enhancements, a number of important fixes and improved compatibility
with pandas 0.23.

Enhancements:

- Graph.from_networkx now extracts node and edge attributes from
  networkx graphs
  ([#2714](https://github.com/ioam/holoviews/pull/2714))
- Added throttling support to scrubber widget
  ([#2748](https://github.com/ioam/holoviews/pull/2748))
- histogram operation now works on datetimes
  ([#2719](https://github.com/ioam/holoviews/pull/2719))
- Legends on NdOverlay containing overlays now supported
  ([#2755](https://github.com/ioam/holoviews/pull/2755))
- Dataframe indexes may now be referenced in ``.to`` conversion
  ([#2739](https://github.com/ioam/holoviews/pull/2739))
- Reindexing a gridded Dataset without arguments now behaves
  consistently with NdMapping types and drops scalar dimensions making
  it simpler to drop dimensions after selecting
  ([#2746](https://github.com/ioam/holoviews/pull/2746))

Fixes:

- Various fixes for QuadMesh support including support for contours,
  nan coordinates and inverted coordinates
  ([#2691](https://github.com/ioam/holoviews/pull/2691),
  [#2702](https://github.com/ioam/holoviews/pull/2702),
  [#2771](https://github.com/ioam/holoviews/pull/2771))
- Fixed bugs laying out complex layouts in bokeh
  ([#2740](https://github.com/ioam/holoviews/pull/2740))
- Fix for adding value dimensions to an xarray dataset
  ([#2761](https://github.com/ioam/holoviews/pull/2761))

Compatibility:

- Addressed various deprecation warnings generated by pandas 0.23
  ([#2699](https://github.com/ioam/holoviews/pull/2699),
  [#2725](https://github.com/ioam/holoviews/pull/2725),
  [#2767](https://github.com/ioam/holoviews/pull/2767))


Version 1.10.4
==============

This is a minor bug fix release including a number of crucial fixes
for issues reported by our users.

Enhancement:

- Allow setting alpha on Image/RGB/HSV and Raster types in bokeh
  ([#2680](https://github.com/ioam/holoviews/pull/2680))

Fixes:

- Fixed bug running display multiple times in one cell
  ([#2677](https://github.com/ioam/holoviews/pull/2677))
- Avoid sending hover data unless explicitly requested
  ([#2681](https://github.com/ioam/holoviews/pull/2681))
- Fixed bug slicing xarray with tuples
  ([#2674](https://github.com/ioam/holoviews/pull/2674))

Version 1.10.3
==============

This is a minor bug fix release including a number of crucial fixes
for issues reported by our users.

Enhancement:

- The dimensions of elements may now be changed allowing updates to
  axis labels and table column headers
  ([#2666](https://github.com/ioam/holoviews/pull/2666))

Fixes:

- Fix for ``labelled`` plot option
  ([#2643](https://github.com/ioam/holoviews/pull/2643))
- Optimized initialization of dynamic plots specifying a large
  parameter space
  ([#2646](https://github.com/ioam/holoviews/pull/2646))
- Fixed unicode and reversed axis slicing issues in XArrayInterface
  ([#2658](https://github.com/ioam/holoviews/issues/2658),
   [#2653](https://github.com/ioam/holoviews/pull/2653))
- Fixed widget sorting issues when applying dynamic groupby
  ([#2641](https://github.com/ioam/holoviews/issues/2641))

API:

- The PlotReset reset parameter was renamed to resetting to avoid
  clash with a method
  ([#2665](https://github.com/ioam/holoviews/pull/2665))
- PolyDraw tool data parameter now always indexed with 'xs' and 'ys'
  keys for consistency
  ([#2650](https://github.com/ioam/holoviews/issues/2650))

Version 1.10.2
==============

This is a minor bug fix release with a number of small fixes for
features and regressions introduced in 1.10:

Enhancement:

- Exposed Image hover functionality for upcoming bokeh 0.12.16 release
  ([#2625](https://github.com/ioam/holoviews/pull/2625))

Fixes:

- Minor fixes for newly introduced elements and plots including Chord
  ([#2581](https://github.com/ioam/holoviews/issues/2581)) and
  RadialHeatMap
  ([#2610](https://github.com/ioam/holoviews/issues/2610)
- Fixes for .options method including resolving style and plot option
  clashes ([#2411](https://github.com/ioam/holoviews/issues/2411)) and
  calling it without arguments
  ([#2630](https://github.com/ioam/holoviews/pull/2630))
- Fixes for IPython display function
  ([#2587](https://github.com/ioam/holoviews/issues/2587)) and
  display_formats
  ([#2592](https://github.com/ioam/holoviews/issues/2592))

Deprecations:

- BoxWhisker and Bars ``width`` bokeh style options and Arrow
  matplotlib ``fontsize`` option are deprecated
  ([#2411](https://github.com/ioam/holoviews/issues/2411))


Version 1.10.1
==============

This is a minor bug fix release with a number of fixes for regressions
and minor bugs introduced in the 1.10.0 release:

Fixes:

- Fixed static HTML export of notebooks
  ([#2574](https://github.com/ioam/holoviews/pull/2574))
- Ensured Chord element allows recurrent edges
  ([#2583](https://github.com/ioam/holoviews/pull/2583))
- Restored behavior for inferring key dimensions order from XArray
  Dataset ([#2579](https://github.com/ioam/holoviews/pull/2579))
- Fixed Selection1D stream on bokeh server after changes in bokeh
  0.12.15 ([#2586](https://github.com/ioam/holoviews/pull/2586))


Version 1.10.0
==============

This is a major release with a large number of new features and bug
fixes, as well as a small number of API changes. Many thanks to the
numerous users who filed bug reports, tested development versions, and
contributed a number of new features and bug fixes, including special
thanks to @mansenfranzen, @ea42gh, @drs251 and @jakirkham.


JupyterLab support:

- Full compatibility with JupyterLab when installing the
  jupyterlab_holoviews extension
  ([#687](https://github.com/ioam/holoviews/issues/687))

New components:

- Added [``Sankey`` element](http://holoviews.org/reference/elements/bokeh/Sankey.html)
  to plot directed flow graphs
  ([#1123](https://github.com/ioam/holoviews/issues/1123))
- Added [``TriMesh`` element](http://holoviews.org/reference/elements/bokeh/TriMesh.html)
  and datashading operation to plot small and large irregular meshes
  ([#2143](https://github.com/ioam/holoviews/issues/2143))
- Added a [``Chord`` element](http://holoviews.org/reference/elements/bokeh/Chord.html)
  to draw flow graphs between different
  nodes ([#2137](https://github.com/ioam/holoviews/issues/2137),
  [#2143](https://github.com/ioam/holoviews/pull/2143))
- Added [``HexTiles`` element](http://holoviews.org/reference/elements/bokeh/HexTiles.html)
  to plot data binned into a hexagonal grid
  ([#1141](https://github.com/ioam/holoviews/issues/1141))
- Added [``Labels`` element](http://holoviews.org/reference/elements/bokeh/Labels.html)
  to plot a large number of text labels at once (as data rather than as annotations)
  ([#1837](https://github.com/ioam/holoviews/issues/1837))
- Added [``Div`` element](http://holoviews.org/reference/elements/bokeh/Div.html)
  to add arbitrary HTML elements to a Bokeh layout
  ([#2221](https://github.com/ioam/holoviews/issues/2221))
- Added
  [``PointDraw``](http://holoviews.org/reference/streams/bokeh/PointDraw.html),
  [``PolyDraw``](http://holoviews.org/reference/streams/bokeh/PolyDraw.html),
  [``BoxEdit``](http://holoviews.org/reference/streams/bokeh/BoxEdit.html), and
  [``PolyEdit``](http://holoviews.org/reference/streams/bokeh/PolyEdit.html)
  streams to allow drawing, editing, and annotating glyphs on a Bokeh
  plot, and syncing the resulting data to Python
  ([#2268](https://github.com/ioam/holoviews/issues/2459))

Features:

- Added [radial ``HeatMap``](http://holoviews.org/reference/elements/bokeh/RadialHeatMap.html)
  option to allow plotting heatmaps with a cyclic x-axis
  ([#2139](https://github.com/ioam/holoviews/pull/2139))
- All elements now support declaring bin edges as well as centers
  allowing ``Histogram`` and ``QuadMesh`` to become first class
  ``Dataset`` types
  ([#547](https://github.com/ioam/holoviews/issues/547))
- When using widgets, their initial or default value can now be
  set via the `Dimension.default` parameter
  ([#704](https://github.com/ioam/holoviews/issues/704))
- n-dimensional Dask arrays are now supported directly via the gridded
  dictionary data interface
  ([#2305](https://github.com/ioam/holoviews/pull/2305))
- Added new [Styling Plots](http://holoviews.org/user_guide/Styling_Plots.html)
  and [Colormaps](http://holoviews.org/user_guide/Colormaps.html)
  user guides, including new functionality for working with colormaps.

Enhancements:

- Improvements to exceptions
  ([#1127](https://github.com/ioam/holoviews/issues/1127))
- Toolbar position and merging (via a new ``merge_toolbar``
  option) can now be controlled for Layout and Grid plots
  ([#1977](https://github.com/ioam/holoviews/issues/1977))
- Bokeh themes can now be applied at the renderer level
  ([#1861](https://github.com/ioam/holoviews/issues/1861))
- Dataframe and Series index can now be referenced by name when
  constructing an element
  ([#2000](https://github.com/ioam/holoviews/issues/2000))
- Option-setting methods such as ``.opts``, ``.options`` and
  ``hv.opts`` now allow specifying the backend instead of defaulting
  to the current backend
  ([#1801](https://github.com/ioam/holoviews/issues/1801))
- Handled API changes in streamz 0.3.0 in Buffer stream
  ([#2409](https://github.com/ioam/holoviews/issues/2409))
- Supported GIF output on windows using new Matplotlib pillow
  animation support
  ([#385](https://github.com/ioam/holoviews/issues/385))
- Provided simplified interface to ``rasterize`` most element types
  using datashader
  ([#2465](https://github.com/ioam/holoviews/pull/2465))
- ``Bivariate`` element now support ``levels`` as a plot option
  ([#2099](https://github.com/ioam/holoviews/issues/2099))
- ``NdLayout`` and ``GridSpace`` now consistently support ``*``
  overlay operation
  ([#2075](https://github.com/ioam/holoviews/issues/2075))
- The Bokeh backend no longer has a hard dependency on Matplotlib
  ([#829](https://github.com/ioam/holoviews/issues/829))
- ``DynamicMap`` may now return (``Nd``)``Overlay`` with varying
  number of elements
  ([#1388](https://github.com/ioam/holoviews/issues/1388))
- In the notebook, deleting or re-executing a cell will now delete
  the plot and clean up any attached streams
  ([#2141](https://github.com/ioam/holoviews/issues/2141))
- Added ``color_levels`` plot option to set discrete number of levels
  during colormapping
  ([#2483](https://github.com/ioam/holoviews/pull/2483))
- Expanded the [Large Data](http://holoviews.org/user_guide/Large_Data.html)
  user guide to show examples of all Element and Container types
  supported for datashading and give performance guidelines.

Fixes:

- ``Layout`` and ``Overlay`` objects no longer create lower-case nodes
  on attribute access
  ([#2331](https://github.com/ioam/holoviews/pull/2331))
- ``Dimension.step`` now correctly respects both integer and float
  steps ([#1707](https://github.com/ioam/holoviews/issues/1707))
- Fixed timezone issues when using linked streams on datetime axes
  ([#2459](https://github.com/ioam/holoviews/issues/2459))


Changes affecting backwards compatibility:

- Image elements now expect and validate regular sampling
  ([#1869](https://github.com/ioam/holoviews/issues/1869)); for
  genuinely irregularly sampled data QuadMesh should be used.
- Tabular elements will no longer default to use ``ArrayInterface``,
  instead preferring pandas and dictionary data formats
  ([#1236](https://github.com/ioam/holoviews/issues/1236))
- ``Cycle``/``Palette`` values are no longer zipped together; instead
  they now cycle independently
  ([#2333](https://github.com/ioam/holoviews/pull/2333))
- The default color ``Cycle`` was expanded to provide more unique colors
  ([#2483](https://github.com/ioam/holoviews/pull/2483))
- Categorical colormapping was made consistent across backends,
  changing the behavior of categorical Matplotlib colormaps
  ([#2483](https://github.com/ioam/holoviews/pull/2483))
- Disabled auto-indexable property of the Dataset baseclass, i.e. if a
  single column is supplied no integer index column is added
  automatically ([#2522](https://github.com/ioam/holoviews/pull/2522))


Version 1.9.5
=============

This release includes a very small number of minor bugfixes and a new
feature to simplify setting options in python:

Enhancements:

-  Added .options method for simplified options setting.
   ([\#2306](https://github.com/ioam/holoviews/pull/2306))

Fixes:

-  Allow plotting bytes datausing the Bokeh backend in python3
   ([\#2357](https://github.com/ioam/holoviews/pull/2357))
-  Allow .range to work on data with heterogeneous types in Python 3
   ([\#2345](https://github.com/ioam/holoviews/pull/2345))
-  Fixed bug streaming data containing datetimes using bokeh>=0.12.14
   ([\#2383](https://github.com/ioam/holoviews/pull/2383))


Version 1.9.4
=============

This release contains a small number of important bug fixes:

-    Compatibility with recent versions of Dask and pandas
     ([\#2329](https://github.com/ioam/holoviews/pull/2329))
-    Fixed bug referencing columns containing non-alphanumeric characters
     in Bokeh Tables ([\#2336](https://github.com/ioam/holoviews/pull/2336))
-    Fixed issue in regrid operation
     ([2337](https://github.com/ioam/holoviews/pull/2337))
-    Fixed issue when using datetimes with datashader when processing
     ranges ([\#2344](https://github.com/ioam/holoviews/pull/2344))


Version 1.9.3
=============

This release contains a number of important bug fixes and minor
enhancements.

Particular thanks to @jbampton, @ea42gh, @laleph, and @drs251 for a
number of fixes and improvements to the documentation.

Enhancements:

-    Optimized rendering of stream based OverlayPlots
     ([\#2253](https://github.com/ioam/holoviews/pull/2253))
-    Added ``merge_toolbars`` and ``toolbar`` options to control
     toolbars on ``Layout`` and Grid plots
     ([\#2289](https://github.com/ioam/holoviews/pull/2289))
-    Optimized rendering of ``VectorField``
     ([\#2314](https://github.com/ioam/holoviews/pull/2289))
-    Improvements to documentation
     ([\#2198](https://github.com/ioam/holoviews/pull/2198),
     [\#2220](https://github.com/ioam/holoviews/pull/2220),
     [\#2233](https://github.com/ioam/holoviews/pull/2233),
     [\#2235](https://github.com/ioam/holoviews/pull/2235),
     [\#2316](https://github.com/ioam/holoviews/pull/2316))
-    Improved Bokeh ``Table`` formatting
     ([\#2267](https://github.com/ioam/holoviews/pull/2267))
-    Added support for handling datetime.date types
     ([\#2267](https://github.com/ioam/holoviews/pull/2267))
-    Add support for pre- and post-process hooks on operations
     ([\#2246](https://github.com/ioam/holoviews/pull/2246),
	  [\#2334](https://github.com/ioam/holoviews/pull/2334))

Fixes:

-    Fix for Bokeh server widgets
     ([\#2218](https://github.com/ioam/holoviews/pull/2218))
-    Fix using event based streams on Bokeh server
     ([\#2239](https://github.com/ioam/holoviews/pull/2239),
     [\#2256](https://github.com/ioam/holoviews/pull/2256))
-    Switched to drawing ``Distribution``, ``Area`` and ``Spread``
     using patch glyphs in Bokeh fixing legends
     ([\#2225](https://github.com/ioam/holoviews/pull/2225))
-    Fixed categorical coloring of ``Polygons``/``Path`` elements in
     Matplotlib ([\#2259](https://github.com/ioam/holoviews/pull/2259))
-    Fixed bug computing categorical datashader aggregates
     ([\#2295](https://github.com/ioam/holoviews/pull/2295))
-    Allow using ``Empty`` object in ``AdjointLayout``
     ([\#2275](https://github.com/ioam/holoviews/pull/2275))


API Changes:

-    Renamed ``Trisurface`` to ``TriSurface`` for future consistency
     ([\#2219](https://github.com/ioam/holoviews/pull/2219))


Version 1.9.2
=============

This release is a minor bug fix release patching various issues
which were found in the 1.9.1 release.

Enhancements:

-   Improved the Graph element, optimizing the constructor
    and adding support for defining a `edge_color_index`
    ([\#2145](https://github.com/ioam/holoviews/pull/2145))
-   Added support for adding jitter to Bokeh Scatter and Points plots
    ([e56208](https://github.com/ioam/holoviews/commit/e56208e1eb6e1e4af67b6a3ffbb5a925bfc37e14))

Fixes:

-   Ensure dimensions, group and label are inherited when casting
    Image to QuadMesh
    ([\#2144](https://github.com/ioam/holoviews/pull/2144))
-   Handle compatibility for Bokeh version >= 0.12.11
    ([\#2159](https://github.com/ioam/holoviews/pull/2159))
-   Fixed broken Bokeh ArrowPlot
    ([\#2172](https://github.com/ioam/holoviews/pull/2172))
-   Fixed Pointer based streams on datetime axes
    ([\#2179](https://github.com/ioam/holoviews/pull/2179))
-   Allow constructing and plotting of empty Distribution and
    Bivariate elements
    ([\#2190](https://github.com/ioam/holoviews/pull/2190))
-   Added support for hover info on Bokeh BoxWhisker plots
    ([\#2187](https://github.com/ioam/holoviews/pull/2187))
-   Fixed bug attaching streams to (Nd)Overlay types
    ([\#2194](https://github.com/ioam/holoviews/pull/2194))


Version 1.9.1
=============

This release is a minor bug fix release patching various issues
which were found in the 1.9.0 release.

Enhancements:

-   Exposed min_alpha parameter on datashader shade and datashade
    operations ([\#2109](https://github.com/ioam/holoviews/pull/2109))

Fixes:

-   Fixed broken Bokeh server linked stream throttling
    ([\#2112](https://github.com/ioam/holoviews/pull/2112))
-   Fixed bug in Bokeh callbacks preventing linked streams using
    Bokeh's on_event callbacks from working
    ([\#2112](https://github.com/ioam/holoviews/pull/2112))
-   Fixed insufficient validation issue for Image and bugs when
    applying regrid operation to xarray based Images
    ([\#2117](https://github.com/ioam/holoviews/pull/2117))
-   Fixed handling of dimensions and empty elements in univariate_kde
    and bivariate_kde operations
    ([\#2103](https://github.com/ioam/holoviews/pull/2103))

Version 1.9.0
=============

This release includes a large number of long awaited features,
improvements and bug fixes, including streaming and graph support,
binary transfer of Bokeh data, fast Image/RGB regridding, first-class
statistics elements and a complete overhaul of the geometry elements.

Particular thanks to all users and contributers who have reported
issues and submitted pull requests.

Features:

-   The kdim and vdim keyword arguments are now positional making the
    declaration of elements less verbose (e.g. Scatter(data, 'x',
    'y')) ([\#1946](https://github.com/ioam/holoviews/pull/1946))
-   Added Graph, Nodes, and EdgePaths elements adding support for
    plotting network graphs
    ([\#1829](https://github.com/ioam/holoviews/pull/1829))
-   Added datashader based regrid operation for fast Image and RGB
    regridding ([\#1773](https://github.com/ioam/holoviews/pull/1773))
-   Added support for binary transport when plotting with Bokeh,
    providing huge speedups for dynamic plots
    ([\#1894](https://github.com/ioam/holoviews/pull/1894),
    [\#1896](https://github.com/ioam/holoviews/pull/1896))
-   Added Pipe and Buffer streams for streaming data support
    ([\#2011](https://github.com/ioam/holoviews/pull/2011))
-   Add support for datetime axes on Image, RGB and when applying
    datashading and regridding operations
    ([\#2023](https://github.com/ioam/holoviews/pull/2023))
-   Added Distribution and Bivariate as first class elements which can
    be plotted with Matplotlib and Bokeh without depending on seaborn
    ([\#1985](https://github.com/ioam/holoviews/pull/1985))
-   Completely overhauled support for plotting geometries with Path,
    Contours and Polygons elements including support for coloring
    individual segments and paths by value
    ([\#1991](https://github.com/ioam/holoviews/pull/1991))

Enhancements:

-   Add support for adjoining all elements on Matplotlib plots
    ([\#1033](https://github.com/ioam/holoviews/pull/1033))
-   Improved exception handling for data interfaces
    ([\#2041](https://github.com/ioam/holoviews/pull/2041))
-   Add groupby argument to histogram operation
    ([\#1725](https://github.com/ioam/holoviews/pull/1725))
-   Add support for reverse sort on Dataset elements
    ([\#1843](https://github.com/ioam/holoviews/pull/1843))
-   Added support for invert_x/yaxis on all elements
    ([\#1872](https://github.com/ioam/holoviews/pull/1872),
    [\#1919](https://github.com/ioam/holoviews/pull/1919))

Fixes:

-   Fixed a bug in Matplotlib causing the first frame in gif and mp4
    getting stuck
    ([\#1922](https://github.com/ioam/holoviews/pull/1922))
-   Fixed various issues with support for new nested categorical axes
    in Bokeh ([\#1933](https://github.com/ioam/holoviews/pull/1933))
-   A large range of other bug fixes too long to list here.

Changes affecting backwards compatibility:

-   The contours operation no longer overlays the contours on top of
    the supplied Image by default and returns a single
    Contours/Polygons rather than an NdOverlay of them
    ([\#1991](https://github.com/ioam/holoviews/pull/1991))
-   The values of the Distribution element should now be defined as a
    key dimension
    ([\#1985](https://github.com/ioam/holoviews/pull/1985))
-   The seaborn interface was removed in its entirety being replaced
    by first class support for statistics elements such as
    Distribution and Bivariate
    ([\#1985](https://github.com/ioam/holoviews/pull/1985))
-   Since kdims and vdims can now be passed as positional arguments
    the bounds argument on Image is no longer positional
    ([\#1946](https://github.com/ioam/holoviews/pull/1946)).
-   The datashade and shade cmap was reverted back to blue due to issues
    with the fire cmap against a white background.
    ([\#2078](https://github.com/ioam/holoviews/pull/2078))
-   Dropped all support for Bokeh versions older than 0.12.10
-   histogram operation now returns Histogram elements with less
    generic value dimension and customizable label
    ([\#1836](https://github.com/ioam/holoviews/pull/1836))


Version 1.8.4
=============

This bugfix release includes a number of critical fixes for compatiblity
with Bokeh 0.12.9 along with various other bug fixes. Many thanks to our
users for various detailed bug reports, feedback and contributions.

Fixes:

-   Fixes to register BoundsXY stream.
    ([\#1826](https://github.com/ioam/holoviews/pull/1826))
-   Fix for Bounds streams on Bokeh server.
    ([\#1883](https://github.com/ioam/holoviews/pull/1883))
-   Compatibility with Matplotlib 2.1
    ([\#1842](https://github.com/ioam/holoviews/pull/1842))
-   Fixed bug in scrubber widget and support for scrubbing discrete
    DynamicMaps ([\#1832](https://github.com/ioam/holoviews/pull/1832))
-   Various fixes for compatibility with Bokeh 0.12.9
    ([\#1849](https://github.com/ioam/holoviews/pull/1849),
    [\#1866](https://github.com/ioam/holoviews/pull/1886))
-   Fixes for setting QuadMesh ranges.
    ([\#1876](https://github.com/ioam/holoviews/pull/1876))
-   Fixes for inverting Image/RGB/Raster axes in Bokeh.
    ([\#1872](https://github.com/ioam/holoviews/pull/1872))


Version 1.8.3
=============

This bugfix release fixes a number of minor issues identified since the
last release:

Features:

-   Add support for setting the Bokeh sizing_mode as a plot option
    ([\#1813](https://github.com/ioam/holoviews/pull/1813))

Fixes:

-   Handle StopIteration on DynamicMap correctly.
    ([\#1792](https://github.com/ioam/holoviews/pull/1792))
-   Fix bug with linked streams on empty source element
    ([\#1725](https://github.com/ioam/holoviews/pull/1806))
-   Compatibility with latest datashader 0.6.0 release
    ([\#1773](https://github.com/ioam/holoviews/pull/1773))
-   Fixed missing HTML closing tag in extension
    ([\#1797](https://github.com/ioam/holoviews/issues/1797),
     [\#1809](https://github.com/ioam/holoviews/pull/1809))
-   Various fixes and improvements for documentation
    ([\#1664](https://github.com/ioam/holoviews/pull/1664),
    [\#1796](https://github.com/ioam/holoviews/pull/1796))


Version 1.8.2
=============

This bugfix release addresses a number of minor issues identified since
the 1.8.1 release:

Feature:

-   Added support for groupby to histogram operation.
    ([\#1725](https://github.com/ioam/holoviews/pull/1725))

Fixes:

-   Fixed problem with HTML export due to new extension logos.
    ([\#1778](https://github.com/ioam/holoviews/pull/1778))
-   Replaced deprecated ``__call__`` usage with opts method throughout codebase.
    ([\#1759](https://github.com/ioam/holoviews/pull/1759),
    [\#1763](https://github.com/ioam/holoviews/pull/1763),
    [\#1779](https://github.com/ioam/holoviews/pull/1779))
-   Fixed pip installation.
    ([\#1782](https://github.com/ioam/holoviews/pull/1782))
-   Fixed miscellaneous bugs
   ([\#1724](https://github.com/ioam/holoviews/pull/1724),
   [\#1739](https://github.com/ioam/holoviews/pull/1739),
   [\#1711](https://github.com/ioam/holoviews/pull/1711))

Version 1.8.1
=============

This bugfix release addresses a number of minor issues identified since
the 1.8 release:

Feature:

-   All enabled plotting extension logos now shown
    ([\#1694](https://github.com/ioam/holoviews/pull/1694))

Fixes:

-   Updated search ordering when looking for holoviews.rc
    ([\#1700](https://github.com/ioam/holoviews/pull/1700))
-   Fixed lower bound inclusivity bug when no upper bound supplied
    ([\#1686](https://github.com/ioam/holoviews/pull/1686))
-   Raise SkipRendering error when plotting nested layouts
    ([\#1687](https://github.com/ioam/holoviews/pull/1687))
-   Added safety margin for grid axis constraint issue
    ([\#1695](https://github.com/ioam/holoviews/pull/1685))
-   Fixed bug when using +framewise
    ([\#1685](https://github.com/ioam/holoviews/pull/1685))
-   Fixed handling of Spacer models in sparse grid
    ([\#1682](https://github.com/ioam/holoviews/pull/))
-   Renamed Bounds to BoundsXY for consistency
    ([\#1672](https://github.com/ioam/holoviews/pull/1672))
-   Fixed Bokeh log axes with axis lower bound &lt;=0
    ([\#1691](https://github.com/ioam/holoviews/pull/1691))
-   Set default datashader cmap to fire
    ([\#1697](https://github.com/ioam/holoviews/pull/1697))
-   Set SpikesPlot color index to None by default
    ([\#1671](https://github.com/ioam/holoviews/pull/1671))
-   Documentation fixes
    ([\#1662](https://github.com/ioam/holoviews/pull/1662),
    [\#1665](https://github.com/ioam/holoviews/pull/1665),
    [\#1690](https://github.com/ioam/holoviews/pull/1690),
    [\#1692](https://github.com/ioam/holoviews/pull/1692),
    [\#1658](https://github.com/ioam/holoviews/pull/1658))

Version 1.8.0
=============

This release includes a complete and long awaited overhaul of the
HoloViews documentation and website, with a new gallery, getting-started
section, and logo. In the process, we have also improved and made small
fixes to all of the major new functionality that appeared in 1.7.0 but
was not properly documented until now. We want to thank all our old and
new contributors for providing feedback, bug reports, and pull requests.

Major features:

-   Completely overhauled the documentation and website
    ([\#1384](https://github.com/ioam/holoviews/pull/1384),
    [\#1473](https://github.com/ioam/holoviews/pull/1473),
    [\#1476](https://github.com/ioam/holoviews/pull/1476),
    [\#1473](https://github.com/ioam/holoviews/pull/1473),
    [\#1537](https://github.com/ioam/holoviews/pull/1537),
    [\#1585](https://github.com/ioam/holoviews/pull/1585),
    [\#1628](https://github.com/ioam/holoviews/pull/1628),
    [\#1636](https://github.com/ioam/holoviews/pull/1636))
-   Replaced dependency on bkcharts with new Bokeh bar plot
    ([\#1416](https://github.com/ioam/holoviews/pull/1416)) and Bokeh
    BoxWhisker plot
    ([\#1604](https://github.com/ioam/holoviews/pull/1604))
-   Added support for drawing the `Arrow` annotation in Bokeh
    ([\#1608](https://github.com/ioam/holoviews/pull/1608))
-   Added periodic method DynamicMap to schedule recurring events
    ([\#1429](https://github.com/ioam/holoviews/pull/1429))
-   Cleaned up the API for deploying to Bokeh server
    ([\#1444](https://github.com/ioam/holoviews/pull/1444),
    [\#1469](https://github.com/ioam/holoviews/pull/1469),
    [\#1486](https://github.com/ioam/holoviews/pull/1486))
-   Validation of invalid backend specific options
    ([\#1465](https://github.com/ioam/holoviews/pull/1465))
-   Added utilities and entry points to convert notebooks to scripts
    including magics
    ([\#1491](https://github.com/ioam/holoviews/pull/1491))
-   Added support for rendering to png in Bokeh backend
    ([\#1493](https://github.com/ioam/holoviews/pull/1493))
-   Made Matplotlib and Bokeh styling more consistent and dropped custom
    Matplotlib rc file
    ([\#1518](https://github.com/ioam/holoviews/pull/1518))
-   Added `iloc` and `ndloc` method to allow integer based indexing on
    tabular and gridded datasets
    ([\#1435](https://github.com/ioam/holoviews/pull/1435))
-   Added option to restore case sensitive completion order by setting
    `hv.extension.case_sensitive_completion=True` in python or via
    holoviews.rc file
    ([\#1613](https://github.com/ioam/holoviews/pull/1613))

Other new features and improvements:

-   Optimized datashading of `NdOverlay`
    ([\#1430](https://github.com/ioam/holoviews/pull/1430))
-   Expose last `DynamicMap` args and kwargs on Callable
    ([\#1453](https://github.com/ioam/holoviews/pull/1453))
-   Allow colormapping `Contours` Element
    ([\#1499](https://github.com/ioam/holoviews/pull/1499))
-   Add support for fixed ticks with labels in Bokeh backend
    ([\#1503](https://github.com/ioam/holoviews/pull/1503))
-   Added a `clim` parameter to datashade controlling the color range
    ([\#1508](https://github.com/ioam/holoviews/pull/1508))
-   Add support for wrapping xarray DataArrays containing Dask arrays
    ([\#1512](https://github.com/ioam/holoviews/pull/1512))
-   Added support for aggregating to target `Image` dimensions in
    datashader `aggregate` operation
    ([\#1513](https://github.com/ioam/holoviews/pull/1513))
-   Added top-level hv.extension and `hv.renderer` utilities
    ([\#1517](https://github.com/ioam/holoviews/pull/1517))
-   Added support for `Splines` defining multiple cubic splines in Bokeh
    ([\#1529](https://github.com/ioam/holoviews/pull/1529))
-   Add support for redim.label to quickly define dimension labels
    ([\#1541](https://github.com/ioam/holoviews/pull/1541))
-   Add `BoundsX` and `BoundsY` streams
    ([\#1554](https://github.com/ioam/holoviews/pull/1554))
-   Added support for adjoining empty plots
    ([\#1561](https://github.com/ioam/holoviews/pull/1561))
-   Handle zero-values correctly when using `logz` colormapping option
    in Matplotlib
    ([\#1576](https://github.com/ioam/holoviews/pull/1576))
-   Define a number of `Cycle` and `Palette` defaults across backends
    ([\#1605](https://github.com/ioam/holoviews/pull/1605))
-   Many other small improvements and fixes
    ([\#1399](https://github.com/ioam/holoviews/pull/1399),
    [\#1400](https://github.com/ioam/holoviews/pull/1400),
    [\#1405](https://github.com/ioam/holoviews/pull/1405),
    [\#1412](https://github.com/ioam/holoviews/pull/1412),
    [\#1413](https://github.com/ioam/holoviews/pull/1413),
    [\#1418](https://github.com/ioam/holoviews/pull/1418),
    [\#1439](https://github.com/ioam/holoviews/pull/1439),
    [\#1442](https://github.com/ioam/holoviews/pull/1442),
    [\#1443](https://github.com/ioam/holoviews/pull/1443),
    [\#1467](https://github.com/ioam/holoviews/pull/1467),
    [\#1485](https://github.com/ioam/holoviews/pull/1485),
    [\#1505](https://github.com/ioam/holoviews/pull/1505),
    [\#1493](https://github.com/ioam/holoviews/pull/1493),
    [\#1509](https://github.com/ioam/holoviews/pull/1509),
    [\#1524](https://github.com/ioam/holoviews/pull/1524),
    [\#1543](https://github.com/ioam/holoviews/pull/1543),
    [\#1547](https://github.com/ioam/holoviews/pull/1547),
    [\#1560](https://github.com/ioam/holoviews/pull/1560),
    [\#1603](https://github.com/ioam/holoviews/pull/1603))

Changes affecting backwards compatibility:

-   Renamed `ElementOperation` to `Operation`
    ([\#1421](https://github.com/ioam/holoviews/pull/1421))
-   Removed `stack_area` operation in favor of `Area.stack` classmethod
    ([\#1515](https://github.com/ioam/holoviews/pull/1515))
-   Removed all mpld3 support
    ([\#1516](https://github.com/ioam/holoviews/pull/1516))
-   Added `opts` method on all types, replacing the now-deprecated
    `__call__` syntax to set options
    ([\#1589](https://github.com/ioam/holoviews/pull/1589))
-   Styling changes for both Matplotlib and Bokeh, which can be reverted
    for a notebook with the `config` option of `hv.extension`. For
    instance, `hv.extension('bokeh', config=dict(style_17=True))`
    ([\#1518](https://github.com/ioam/holoviews/pull/1518))

Version 1.7.0
=============

This version is a major new release incorporating seven months of work
involving several hundred PRs and over 1700 commits. Highlights include
extensive new support for easily building highly interactive
[Bokeh](http://bokeh.pydata.org) plots, support for using
[datashader](https://github.com/bokeh/datashader)-based plots for
working with large datasets, support for rendering images interactively
but outside of the notebook, better error handling, and support for
Matplotlib 2.0 and Bokeh 0.12.5. The PRs linked below serve as initial
documentation for these features, and full documentation will be added
in the run-up to HoloViews 2.0.

Major features and improvements:

-   Interactive Streams API (PR
    [\#832](https://github.com/ioam/holoviews/pull/832),
    [\#838](https://github.com/ioam/holoviews/pull/838),
    [\#842](https://github.com/ioam/holoviews/pull/842),
    [\#844](https://github.com/ioam/holoviews/pull/844),
    [\#845](https://github.com/ioam/holoviews/pull/845),
    [\#846](https://github.com/ioam/holoviews/pull/846),
    [\#858](https://github.com/ioam/holoviews/pull/858),
    [\#860](https://github.com/ioam/holoviews/pull/860),
    [\#889](https://github.com/ioam/holoviews/pull/889),
    [\#904](https://github.com/ioam/holoviews/pull/904),
    [\#913](https://github.com/ioam/holoviews/pull/913),
    [\#933](https://github.com/ioam/holoviews/pull/933),
    [\#962](https://github.com/ioam/holoviews/pull/962),
    [\#964](https://github.com/ioam/holoviews/pull/964),
    [\#1094](https://github.com/ioam/holoviews/pull/1094),
    [\#1256](https://github.com/ioam/holoviews/pull/1256),
    [\#1274](https://github.com/ioam/holoviews/pull/1274),
    [\#1297](https://github.com/ioam/holoviews/pull/1297),
    [\#1301](https://github.com/ioam/holoviews/pull/1301),
    [\#1303](https://github.com/ioam/holoviews/pull/1303)).
-   Dynamic Callable API (PR
    [\#951](https://github.com/ioam/holoviews/pull/951),
    [\#1103](https://github.com/ioam/holoviews/pull/1103),
    [\#1029](https://github.com/ioam/holoviews/pull/1029),
    [\#968](https://github.com/ioam/holoviews/pull/968),
    [\#935](https://github.com/ioam/holoviews/pull/935),
    [\#1063](https://github.com/ioam/holoviews/pull/1063),
    [\#1260](https://github.com/ioam/holoviews/pull/1260)).
-   Simpler and more powerful DynamicMap (PR
    [\#1238](https://github.com/ioam/holoviews/pull/1238),
    [\#1240](https://github.com/ioam/holoviews/pull/1240),
    [\#1243](https://github.com/ioam/holoviews/pull/1243),
    [\#1257](https://github.com/ioam/holoviews/pull/1257),
    [\#1267](https://github.com/ioam/holoviews/pull/1267),
    [\#1302](https://github.com/ioam/holoviews/pull/1302),
    [\#1304](https://github.com/ioam/holoviews/pull/1304),
    [\#1305](https://github.com/ioam/holoviews/pull/1305)).
-   Fully general support for Bokeh events (PR
    [\#892](https://github.com/ioam/holoviews/pull/892),
    [\#1148](https://github.com/ioam/holoviews/pull/1148),
    [\#1235](https://github.com/ioam/holoviews/pull/1235)).
-   Datashader operations (PR
    [\#894](https://github.com/ioam/holoviews/pull/894),
    [\#907](https://github.com/ioam/holoviews/pull/907),
    [\#963](https://github.com/ioam/holoviews/pull/963),
    [\#1125](https://github.com/ioam/holoviews/pull/1125),
    [\#1281](https://github.com/ioam/holoviews/pull/1281),
    [\#1306](https://github.com/ioam/holoviews/pull/1306)).
-   Support for Bokeh apps and Bokeh Server (PR
    [\#959](https://github.com/ioam/holoviews/pull/959),
    [\#1283](https://github.com/ioam/holoviews/pull/1283)).
-   Working with renderers interactively outside the notebook (PR
    [\#1214](https://github.com/ioam/holoviews/pull/1214)).
-   Support for Matplotlib 2.0 (PR
    [\#867](https://github.com/ioam/holoviews/pull/867),
    [\#868](https://github.com/ioam/holoviews/pull/868),
    [\#1131](https://github.com/ioam/holoviews/pull/1131),
    [\#1264](https://github.com/ioam/holoviews/pull/1264),
    [\#1266](https://github.com/ioam/holoviews/pull/1266)).
-   Support for Bokeh 0.12.2, 0.12.3, 0.12.4, and 0.12.5 (PR
    [\#899](https://github.com/ioam/holoviews/pull/899),
    [\#900](https://github.com/ioam/holoviews/pull/900),
    [\#1007](https://github.com/ioam/holoviews/pull/1007),
    [\#1036](https://github.com/ioam/holoviews/pull/1036),
    [\#1116](https://github.com/ioam/holoviews/pull/1116)).
-   Many new features for the Bokeh backend: widgets editable (PR
    [\#1247](https://github.com/ioam/holoviews/pull/1247)), selection
    colors and interactive legends (PR
    [\#1220](https://github.com/ioam/holoviews/pull/1220)), GridSpace
    axes (PR [\#1150](https://github.com/ioam/holoviews/pull/1150)),
    categorical axes and colormapping (PR
    [\#1089](https://github.com/ioam/holoviews/pull/1089),
    [\#1137](https://github.com/ioam/holoviews/pull/1137)), computing
    plot size (PR
    [\#1140](https://github.com/ioam/holoviews/pull/1140)), GridSpaces
    inside Layouts (PR
    [\#1104](https://github.com/ioam/holoviews/pull/1104)), Layout/Grid
    titles (PR [\#1017](https://github.com/ioam/holoviews/pull/1017)),
    histogram with live colormapping (PR
    [\#928](https://github.com/ioam/holoviews/pull/928)), colorbars (PR
    [\#861](https://github.com/ioam/holoviews/pull/861)),
    finalize\_hooks (PR
    [\#1040](https://github.com/ioam/holoviews/pull/1040)), labelled and
    show\_frame options (PR
    [\#863](https://github.com/ioam/holoviews/pull/863),
    [\#1013](https://github.com/ioam/holoviews/pull/1013)), styling
    hover glyphs (PR
    [\#1286](https://github.com/ioam/holoviews/pull/1286)), hiding
    legends on BarPlot (PR
    [\#837](https://github.com/ioam/holoviews/pull/837)), VectorField
    plot (PR [\#1196](https://github.com/ioam/holoviews/pull/1196)),
    Histograms now have same color cycle as mpl
    ([\#1008](https://github.com/ioam/holoviews/pull/1008)).
-   Implemented convenience redim methods to easily set dimension
    ranges, values etc. (PR
    [\#1302](https://github.com/ioam/holoviews/pull/1302))
-   Made methods on and operations applied to DynamicMap lazy
    ([\#422](https://github.com/ioam/holoviews/pull/422),
    [\#588](https://github.com/ioam/holoviews/pull/588),
    [\#1188](https://github.com/ioam/holoviews/pull/1188),
    [\#1240](https://github.com/ioam/holoviews/pull/1240),
    [\#1227](https://github.com/ioam/holoviews/pull/1227))
-   Improved documentation (PR
    [\#936](https://github.com/ioam/holoviews/pull/936),
    [\#1070](https://github.com/ioam/holoviews/pull/1070),
    [\#1242](https://github.com/ioam/holoviews/pull/1242),
    [\#1273](https://github.com/ioam/holoviews/pull/1273),
    [\#1280](https://github.com/ioam/holoviews/pull/1280)).
-   Improved error handling (PR
    [\#906](https://github.com/ioam/holoviews/pull/906),
    [\#932](https://github.com/ioam/holoviews/pull/932),
    [\#939](https://github.com/ioam/holoviews/pull/939),
    [\#949](https://github.com/ioam/holoviews/pull/949),
    [\#1011](https://github.com/ioam/holoviews/pull/1011),
    [\#1290](https://github.com/ioam/holoviews/pull/1290),
    [\#1262](https://github.com/ioam/holoviews/pull/1262),
    [\#1295](https://github.com/ioam/holoviews/pull/1295)), including
    re-enabling option system keyword validation (PR
    [\#1277](https://github.com/ioam/holoviews/pull/1277)).
-   Improved testing (PR
    [\#834](https://github.com/ioam/holoviews/pull/834),
    [\#871](https://github.com/ioam/holoviews/pull/871),
    [\#881](https://github.com/ioam/holoviews/pull/881),
    [\#941](https://github.com/ioam/holoviews/pull/941),
    [\#1117](https://github.com/ioam/holoviews/pull/1117),
    [\#1153](https://github.com/ioam/holoviews/pull/1153),
    [\#1171](https://github.com/ioam/holoviews/pull/1171),
    [\#1207](https://github.com/ioam/holoviews/pull/1207),
    [\#1246](https://github.com/ioam/holoviews/pull/1246),
    [\#1259](https://github.com/ioam/holoviews/pull/1259),
    [\#1287](https://github.com/ioam/holoviews/pull/1287)).

Other new features and improvements:

-   Operations for timeseries (PR
    [\#1172](https://github.com/ioam/holoviews/pull/1172)),
    downsample\_columns (PR
    [\#903](https://github.com/ioam/holoviews/pull/903)),
    interpolate\_curve (PR
    [\#1097](https://github.com/ioam/holoviews/pull/1097)), and stacked
    area (PR [\#1193](https://github.com/ioam/holoviews/pull/1193)).
-   Dataset types can be declared as empty by passing an empty list (PR
    [\#1355](https://github.com/ioam/holoviews/pull/1355))
-   Plot or style options for Curve interpolation (PR
    [\#1097](https://github.com/ioam/holoviews/pull/1097)), transposing
    layouts (PR [\#1100](https://github.com/ioam/holoviews/pull/1100)),
    multiple paths (PR
    [\#997](https://github.com/ioam/holoviews/pull/997)), and norm for
    ColorbarPlot (PR
    [\#957](https://github.com/ioam/holoviews/pull/957)).
-   Improved options inheritance for more intuitive behavior (PR
    [\#1275](https://github.com/ioam/holoviews/pull/1275)).
-   Image interface providing similar functionality for Image and
    non-Image types (making GridImage obsolete) (PR
    [\#994](https://github.com/ioam/holoviews/pull/994)).
-   Dask data interface (PR
    [\#974](https://github.com/ioam/holoviews/pull/974),
    [\#991](https://github.com/ioam/holoviews/pull/991)).
-   xarray aggregate/reduce (PR
    [\#1192](https://github.com/ioam/holoviews/pull/1192)).
-   Indicate color clipping and control clipping colors (PR
    [\#686](https://github.com/ioam/holoviews/pull/686)).
-   Better datetime handling (PR
    [\#1098](https://github.com/ioam/holoviews/pull/1098)).
-   Gridmatrix diagonal types (PR
    [\#1194](https://github.com/ioam/holoviews/pull/1194),
    [\#1027](https://github.com/ioam/holoviews/pull/1027)).
-   log option for histogram operation (PR
    [\#929](https://github.com/ioam/holoviews/pull/929)).
-   Perceptually uniform fire colormap (PR
    [\#943](https://github.com/ioam/holoviews/pull/943)).
-   Support for adjoining overlays (PR
    [\#1213](https://github.com/ioam/holoviews/pull/1213)).
-   coloring weighted average in SideHistogram (PR
    [\#1087](https://github.com/ioam/holoviews/pull/1087)).
-   HeatMap allows displaying multiple values on hover (PR
    [\#849](https://github.com/ioam/holoviews/pull/849)).
-   Allow casting Image to QuadMesh (PR
    [\#1282](https://github.com/ioam/holoviews/pull/1282)).
-   Unused columns are now preserved in gridded groupby (PR
    [\#1154](https://github.com/ioam/holoviews/pull/1154)).
-   Optimizations and fixes for constructing Layout/Overlay types (PR
    [\#952](https://github.com/ioam/holoviews/pull/952)).
-   DynamicMap fixes (PR
    [\#848](https://github.com/ioam/holoviews/pull/848),
    [\#883](https://github.com/ioam/holoviews/pull/883),
    [\#911](https://github.com/ioam/holoviews/pull/911),
    [\#922](https://github.com/ioam/holoviews/pull/922),
    [\#923](https://github.com/ioam/holoviews/pull/923),
    [\#927](https://github.com/ioam/holoviews/pull/927),
    [\#944](https://github.com/ioam/holoviews/pull/944),
    [\#1170](https://github.com/ioam/holoviews/pull/1170),
    [\#1227](https://github.com/ioam/holoviews/pull/1227),
    [\#1270](https://github.com/ioam/holoviews/pull/1270)).
-   Bokeh-backend fixes including handling of empty frames
    ([\#835](https://github.com/ioam/holoviews/pull/835)), faster
    updates ([\#905](https://github.com/ioam/holoviews/pull/905)), hover
    tool fixes ([\#1004](https://github.com/ioam/holoviews/pull/1004),
    [\#1178](https://github.com/ioam/holoviews/pull/1178),
    [\#1092](https://github.com/ioam/holoviews/pull/1092),
    [\#1250](https://github.com/ioam/holoviews/pull/1250)) and many more
    (PR [\#537](https://github.com/ioam/holoviews/pull/537),
    [\#851](https://github.com/ioam/holoviews/pull/851),
    [\#852](https://github.com/ioam/holoviews/pull/852),
    [\#854](https://github.com/ioam/holoviews/pull/854),
    [\#880](https://github.com/ioam/holoviews/pull/880),
    [\#896](https://github.com/ioam/holoviews/pull/896),
    [\#898](https://github.com/ioam/holoviews/pull/898),
    [\#921](https://github.com/ioam/holoviews/pull/921),
    [\#934](https://github.com/ioam/holoviews/pull/934),
    [\#1004](https://github.com/ioam/holoviews/pull/1004),
    [\#1010](https://github.com/ioam/holoviews/pull/1010),
    [\#1014](https://github.com/ioam/holoviews/pull/1014),
    [\#1030](https://github.com/ioam/holoviews/pull/1030),
    [\#1069](https://github.com/ioam/holoviews/pull/1069),
    [\#1072](https://github.com/ioam/holoviews/pull/1072),
    [\#1085](https://github.com/ioam/holoviews/pull/1085),
    [\#1157](https://github.com/ioam/holoviews/pull/1157),
    [\#1086](https://github.com/ioam/holoviews/pull/1086),
    [\#1169](https://github.com/ioam/holoviews/pull/1169),
    [\#1195](https://github.com/ioam/holoviews/pull/1195),
    [\#1263](https://github.com/ioam/holoviews/pull/1263)).
-   Matplotlib-backend fixes and improvements (PR
    [\#864](https://github.com/ioam/holoviews/pull/864),
    [\#873](https://github.com/ioam/holoviews/pull/873),
    [\#954](https://github.com/ioam/holoviews/pull/954),
    [\#1037](https://github.com/ioam/holoviews/pull/1037),
    [\#1068](https://github.com/ioam/holoviews/pull/1068),
    [\#1128](https://github.com/ioam/holoviews/pull/1128),
    [\#1132](https://github.com/ioam/holoviews/pull/1132),
    [\#1143](https://github.com/ioam/holoviews/pull/1143),
    [\#1163](https://github.com/ioam/holoviews/pull/1163),
    [\#1209](https://github.com/ioam/holoviews/pull/1209),
    [\#1211](https://github.com/ioam/holoviews/pull/1211),
    [\#1225](https://github.com/ioam/holoviews/pull/1225),
    [\#1269](https://github.com/ioam/holoviews/pull/1269),
    [\#1300](https://github.com/ioam/holoviews/pull/1300)).
-   Many other small improvements and fixes (PR
    [\#830](https://github.com/ioam/holoviews/pull/830),
    [\#840](https://github.com/ioam/holoviews/pull/840),
    [\#841](https://github.com/ioam/holoviews/pull/841),
    [\#850](https://github.com/ioam/holoviews/pull/850),
    [\#855](https://github.com/ioam/holoviews/pull/855),
    [\#856](https://github.com/ioam/holoviews/pull/856),
    [\#859](https://github.com/ioam/holoviews/pull/859),
    [\#865](https://github.com/ioam/holoviews/pull/865),
    [\#893](https://github.com/ioam/holoviews/pull/893),
    [\#897](https://github.com/ioam/holoviews/pull/897),
    [\#902](https://github.com/ioam/holoviews/pull/902),
    [\#912](https://github.com/ioam/holoviews/pull/912),
    [\#916](https://github.com/ioam/holoviews/pull/916),
    [\#925](https://github.com/ioam/holoviews/pull/925),
    [\#938](https://github.com/ioam/holoviews/pull/938),
    [\#940](https://github.com/ioam/holoviews/pull/940),
    [\#948](https://github.com/ioam/holoviews/pull/948),
    [\#950](https://github.com/ioam/holoviews/pull/950),
    [\#955](https://github.com/ioam/holoviews/pull/955),
    [\#956](https://github.com/ioam/holoviews/pull/956),
    [\#967](https://github.com/ioam/holoviews/pull/967),
    [\#970](https://github.com/ioam/holoviews/pull/970),
    [\#972](https://github.com/ioam/holoviews/pull/972),
    [\#973](https://github.com/ioam/holoviews/pull/973),
    [\#981](https://github.com/ioam/holoviews/pull/981),
    [\#992](https://github.com/ioam/holoviews/pull/992),
    [\#998](https://github.com/ioam/holoviews/pull/998),
    [\#1009](https://github.com/ioam/holoviews/pull/1009),
    [\#1012](https://github.com/ioam/holoviews/pull/1012),
    [\#1016](https://github.com/ioam/holoviews/pull/1016),
    [\#1023](https://github.com/ioam/holoviews/pull/1023),
    [\#1034](https://github.com/ioam/holoviews/pull/1034),
    [\#1043](https://github.com/ioam/holoviews/pull/1043),
    [\#1045](https://github.com/ioam/holoviews/pull/1045),
    [\#1046](https://github.com/ioam/holoviews/pull/1046),
    [\#1048](https://github.com/ioam/holoviews/pull/1048),
    [\#1050](https://github.com/ioam/holoviews/pull/1050),
    [\#1051](https://github.com/ioam/holoviews/pull/1051),
    [\#1054](https://github.com/ioam/holoviews/pull/1054),
    [\#1060](https://github.com/ioam/holoviews/pull/1060),
    [\#1062](https://github.com/ioam/holoviews/pull/1062),
    [\#1074](https://github.com/ioam/holoviews/pull/1074),
    [\#1082](https://github.com/ioam/holoviews/pull/1082),
    [\#1084](https://github.com/ioam/holoviews/pull/1084),
    [\#1088](https://github.com/ioam/holoviews/pull/1088),
    [\#1093](https://github.com/ioam/holoviews/pull/1093),
    [\#1099](https://github.com/ioam/holoviews/pull/1099),
    [\#1115](https://github.com/ioam/holoviews/pull/1115),
    [\#1119](https://github.com/ioam/holoviews/pull/1119),
    [\#1121](https://github.com/ioam/holoviews/pull/1121),
    [\#1130](https://github.com/ioam/holoviews/pull/1130),
    [\#1133](https://github.com/ioam/holoviews/pull/1133),
    [\#1151](https://github.com/ioam/holoviews/pull/1151),
    [\#1152](https://github.com/ioam/holoviews/pull/1152),
    [\#1155](https://github.com/ioam/holoviews/pull/1155),
    [\#1156](https://github.com/ioam/holoviews/pull/1156),
    [\#1158](https://github.com/ioam/holoviews/pull/1158),
    [\#1162](https://github.com/ioam/holoviews/pull/1162),
    [\#1164](https://github.com/ioam/holoviews/pull/1164),
    [\#1174](https://github.com/ioam/holoviews/pull/1174),
    [\#1175](https://github.com/ioam/holoviews/pull/1175),
    [\#1180](https://github.com/ioam/holoviews/pull/1180),
    [\#1187](https://github.com/ioam/holoviews/pull/1187),
    [\#1197](https://github.com/ioam/holoviews/pull/1197),
    [\#1202](https://github.com/ioam/holoviews/pull/1202),
    [\#1205](https://github.com/ioam/holoviews/pull/1205),
    [\#1206](https://github.com/ioam/holoviews/pull/1206),
    [\#1210](https://github.com/ioam/holoviews/pull/1210),
    [\#1217](https://github.com/ioam/holoviews/pull/1217),
    [\#1219](https://github.com/ioam/holoviews/pull/1219),
    [\#1228](https://github.com/ioam/holoviews/pull/1228),
    [\#1232](https://github.com/ioam/holoviews/pull/1232),
    [\#1241](https://github.com/ioam/holoviews/pull/1241),
    [\#1244](https://github.com/ioam/holoviews/pull/1244),
    [\#1245](https://github.com/ioam/holoviews/pull/1245),
    [\#1249](https://github.com/ioam/holoviews/pull/1249),
    [\#1254](https://github.com/ioam/holoviews/pull/1254),
    [\#1255](https://github.com/ioam/holoviews/pull/1255),
    [\#1271](https://github.com/ioam/holoviews/pull/1271),
    [\#1276](https://github.com/ioam/holoviews/pull/1276),
    [\#1278](https://github.com/ioam/holoviews/pull/1278),
    [\#1285](https://github.com/ioam/holoviews/pull/1285),
    [\#1288](https://github.com/ioam/holoviews/pull/1288),
    [\#1289](https://github.com/ioam/holoviews/pull/1289)).

Changes affecting backwards compatibility:

-   Automatic coloring and sizing on Points now disabled (PR
    [\#748](https://github.com/ioam/holoviews/pull/748)).
-   Deprecated max\_branches output magic option (PR
    [\#1293](https://github.com/ioam/holoviews/pull/1293)).
-   Deprecated GridImage (PR
    [\#1292](https://github.com/ioam/holoviews/pull/1292),
    [\#1223](https://github.com/ioam/holoviews/pull/1223)).
-   Deprecated NdElement (PR
    [\#1191](https://github.com/ioam/holoviews/pull/1191)).
-   Deprecated DFrame conversion methods (PR
    [\#1065](https://github.com/ioam/holoviews/pull/1065)).
-   Banner text removed from notebook\_extension() (PR
    [\#1231](https://github.com/ioam/holoviews/pull/1231),
    [\#1291](https://github.com/ioam/holoviews/pull/1291)).
-   Bokeh's Matplotlib compatibility module removed (PR
    [\#1239](https://github.com/ioam/holoviews/pull/1239)).
-   ls as Matplotlib linestyle alias dropped (PR
    [\#1203](https://github.com/ioam/holoviews/pull/1203)).
-   mdims argument of conversion interface renamed to groupby (PR
    [\#1066](https://github.com/ioam/holoviews/pull/1066)).
-   Replaced global alias state with Dimension.label
    ([\#1083](https://github.com/ioam/holoviews/pull/1083)).
-   DynamicMap only update ranges when set to framewise
-   Deprecated DynamicMap sampled, bounded, open and generator modes
    ([\#969](https://github.com/ioam/holoviews/pull/969),
    [\#1305](https://github.com/ioam/holoviews/pull/1305))
-   Layout.display method is now deprecated
    ([\#1026](https://github.com/ioam/holoviews/pull/1026))
-   Layout fix for Matplotlib figures with non-square aspects introduced
    in 1.6.2 (PR [\#826](https://github.com/ioam/holoviews/pull/826)),
    now enabled by default.

Version 1.6.2
=============

Bug fix release with various fixes for gridded data backends and
optimizations for Bokeh.

-   Optimized Bokeh event messaging, reducing the average json payload
    by 30-50% (PR [\#807](https://github.com/ioam/holoviews/pull/807)).
-   Fixes for correctly handling NdOverlay types returned by DynamicMaps
    (PR [\#814](https://github.com/ioam/holoviews/pull/814)).
-   Added support for datetime64 handling in Matplotlib and support for
    datetime formatters on Dimension.type\_formatters (PR
    [\#816](https://github.com/ioam/holoviews/pull/816)).
-   Fixed handling of constant dimensions when slicing xarray datasets
    (PR [\#817](https://github.com/ioam/holoviews/pull/817)).
-   Fixed support for passing custom dimensions to iris Datasets (PR
    [\#818](https://github.com/ioam/holoviews/pull/818)).
-   Fixed support for add\_dimension on xarray interface (PR
    [\#820](https://github.com/ioam/holoviews/pull/820)).
-   Improved extents computation on Matplotlib SpreadPlot (PR
    [\#821](https://github.com/ioam/holoviews/pull/821)).
-   Bokeh backend avoids sending data for static frames and empty events
    (PR [\#822](https://github.com/ioam/holoviews/pull/822)).
-   Added major layout fix for figures with non-square aspects, reducing
    the amount of unnecessary whitespace (PR
    [\#826](https://github.com/ioam/holoviews/pull/826)). Disabled by
    default until 1.7 release but can be enabled with:

``` {.sourceCode .python}
from holoviews.plotting.mpl import LayoutPlot
LayoutPlot.v17_layout_format = True
LayoutPlot.vspace = 0.3
```

Version 1.6.1
=============

Bug fix release following the 1.6 major release with major bug fixes for
the grid data interfaces and improvements to the options system.

-   Ensured that style options incompatible with active backend are
    ignored (PR [\#802](https://github.com/ioam/holoviews/pull/802)).
-   Added support for placing legends outside the plot area in Bokeh (PR
    [\#801](https://github.com/ioam/holoviews/pull/801)).
-   Fix to ensure Bokeh backend does not depend on pandas (PR
    [\#792](https://github.com/ioam/holoviews/pull/792)).
-   Fixed option system to ensure correct inheritance when redefining
    options (PR [\#796](https://github.com/ioam/holoviews/pull/796)).
-   Major refactor and fixes for the grid based data backends (iris,
    xarray and arrays with coordinates) ensuring the data is oriented
    and transposed correctly (PR
    [\#794](https://github.com/ioam/holoviews/pull/794)).

Version 1.6
===========

A major release with an optional new data interface based on xarray,
support for batching Bokeh plots for huge increases in performance,
support for Bokeh 0.12 and various other fixes and improvements.

Features and improvements:

-   Made VectorFieldPlot more general with support for independent
    coloring and scaling (PR
    [\#701](https://github.com/ioam/holoviews/pull/701)).
-   Iris interface now allows tuple and dict formats in the constructor
    (PR [\#709](https://github.com/ioam/holoviews/pull/709).
-   Added support for dynamic groupby on all data interfaces (PR
    [\#711](https://github.com/ioam/holoviews/pull/711)).
-   Added an xarray data interface (PR
    [\#713](https://github.com/ioam/holoviews/pull/713)).
-   Added the redim method to all Dimensioned objects making it easy to
    quickly change dimension names and attributes on nested objects
    [\#715](https://github.com/ioam/holoviews/pull/715)).
-   Added support for batching plots (PR
    [\#715](https://github.com/ioam/holoviews/pull/717)).
-   Support for Bokeh 0.12 release (PR
    [\#725](https://github.com/ioam/holoviews/pull/725)).
-   Added support for logz option on Bokeh Raster plots (PR
    [\#729](https://github.com/ioam/holoviews/pull/729)).
-   Bokeh plots now support custom tick formatters specified via
    Dimension value\_format (PR
    [\#728](https://github.com/ioam/holoviews/pull/728)).

Version 1.5
===========

A major release with a large number of new features including new data
interfaces for grid based data, major improvements for DynamicMaps and a
large number of bug fixes.

Features and improvements:

-   Added a grid based data interface to explore n-dimensional gridded
    data easily (PR
    [\#562](https://github.com/ioam/holoviews/pull/542)).
-   Added data interface based on [iris
    Cubes](http://scitools.org.uk/iris/docs/v1.9.2/index.html) (PR
    [\#624](https://github.com/ioam/holoviews/pull/624)).
-   Added support for dynamic operations and overlaying of DynamicMaps
    (PR [\#588](https://github.com/ioam/holoviews/pull/588)).
-   Added support for applying groupby operations to DynamicMaps (PR
    [\#667](https://github.com/ioam/holoviews/pull/667)).
-   Added dimension value formatting in widgets (PR
    [\#562](https://github.com/ioam/holoviews/issues/562)).
-   Added support for indexing and slicing with a function (PR
    [\#619](https://github.com/ioam/holoviews/pull/619)).
-   Improved throttling behavior on widgets (PR
    [\#596](https://github.com/ioam/holoviews/pull/596)).
-   Major refactor of Matplotlib plotting classes to simplify
    implementing new Element plots (PR
    [\#438](https://github.com/ioam/holoviews/pull/438)).
-   Added Renderer.last\_plot attribute to allow easily debugging or
    modifying the last displayed plot (PR
    [\#538](https://github.com/ioam/holoviews/pull/538)).
-   Added Bokeh QuadMeshPlot (PR
    [\#661](https://github.com/ioam/holoviews/pull/661)).

Bug fixes:

-   Fixed overlaying of 3D Element types (PR
    [\#504](https://github.com/ioam/holoviews/pull/504)).
-   Fix for Bokeh hovertools with dimensions with special characters (PR
    [\#524](https://github.com/ioam/holoviews/pull/524)).
-   Fixed bugs in seaborn Distribution Element (PR
    [\#630](https://github.com/ioam/holoviews/pull/630)).
-   Fix for inverted Raster.reduce method (PR
    [\#672](https://github.com/ioam/holoviews/pull/672)).
-   Fixed Store.add\_style\_opts method (PR
    [\#587](https://github.com/ioam/holoviews/pull/587)).
-   Fixed bug preventing simultaneous logx and logy plot options (PR
    [\#554](https://github.com/ioam/holoviews/pull/554)).

Backwards compatibility:

-   Renamed `Columns` type to `Dataset` (PR
    [\#620](https://github.com/ioam/holoviews/issues/620)).

Version 1.4.3
=============

A minor bugfix release to patch a number of small but important issues.

Fixes and improvements:

-   Added a [DynamicMap
    Tutorial](http://holoviews.org/Tutorials/Dynamic_Map.html) to
    explain how to explore very large or continuous parameter spaces in
    HoloViews ([PR
    \#470](https://github.com/ioam/holoviews/issues/470)).
-   Various fixes and improvements for DynamicMaps including slicing
    ([PR \#488](https://github.com/ioam/holoviews/issues/488)) and
    validation ([PR
    \#483](https://github.com/ioam/holoviews/issues/478)) and
    serialization ([PR
    \#483](https://github.com/ioam/holoviews/issues/478))
-   Widgets containing Matplotlib plots now display the first frame from
    cache providing at least the initial frame when exporting
    DynamicMaps ([PR
    \#486](https://github.com/ioam/holoviews/issues/483))
-   Fixed plotting Bokeh plots using widgets in live mode, after changes
    introduced in latest Bokeh version (commit
    [1b87c91e9](https://github.com/ioam/holoviews/commit/1b87c91e9e7cf35b267344ccd4a2fa91dd052890)).
-   Fixed issue in coloring Point/Scatter objects by values ([Issue
    \#467](https://github.com/ioam/holoviews/issues/467)).

Backwards compatibility:

-   The behavior of the `scaling_factor` on Point and Scatter plots has
    changed now simply multiplying `area` or `width` (as defined by the
    `scaling_method`). To disable scaling points by a dimension set
    `size_index=None`.
-   Removed hooks to display 3D Elements using the `BokehMPLRawWrapper`
    in Bokeh ([PR \#477](https://github.com/ioam/holoviews/pull/477))
-   Renamed the DynamicMap mode `closed` to `bounded` ([PR
    \#477](https://github.com/ioam/holoviews/pull/485))

Version 1.4.2
=============

Over the past month since the 1.4.1 release, we have improved our
infrastructure for building documentation, updated the main website and
made several additional usability improvements.

Documentation changes:

-   Major overhaul of website and notebook building making it much
    easier to test user contributions ([Issue
    \#180](https://github.com/ioam/holoviews/issues/180), [PR
    \#429](https://github.com/ioam/holoviews/pull/429))
-   Major rewrite of the documentation ([PR
    \#401](https://github.com/ioam/holoviews/pull/401), [PR
    \#411](https://github.com/ioam/holoviews/pull/411))
-   Added Columnar Data Tutorial and removed most of Pandas Conversions
    as it is now supported by the core.

Fixes and improvements:

-   Major improvement for grid based layouts with varying aspects ([PR
    \#457](https://github.com/ioam/holoviews/pull/457))
-   Fix for interleaving %matplotline inline and holoviews plots ([Issue
    \#179](https://github.com/ioam/holoviews/issues/179))
-   Matplotlib legend z-orders and updating fixed ([Issue
    \#304](https://github.com/ioam/holoviews/issues/304), [Issue
    \#305](https://github.com/ioam/holoviews/issues/305))
-   `color_index` and `size_index` plot options support specifying
    dimension by name ([Issue
    \#391](https://github.com/ioam/holoviews/issues/391))
-   Added `Area` Element type for drawing area under or between Curves.
    ([PR \#427](https://github.com/ioam/holoviews/pull/427))
-   Fixed issues where slicing would remove styles applied to
    an Element. ([Issue
    \#423](https://github.com/ioam/holoviews/issues/423), [PR
    \#439](https://github.com/ioam/holoviews/pull/439))
-   Updated the `title_format` plot option to support a `{dimensions}`
    formatter ([PR \#436](https://github.com/ioam/holoviews/pull/436))
-   Improvements to Renderer API to allow JS and CSS requirements for
    exporting standalone widgets ([PR
    \#426](https://github.com/ioam/holoviews/pull/426))
-   Compatibility with the latest Bokeh 0.11 release ([PR
    \#393](https://github.com/ioam/holoviews/pull/393))

Version 1.4.1
=============

Over the past two weeks since the 1.4 release, we have implemented
several important bug fixes and have made several usability
improvements.

New features:

-   Improved help system. It is now possible to recursively list all the
    applicable documentation for a composite object. In addition, the
    documentation may now be filtered using a regular
    expression pattern. ([PR
    \#370](https://github.com/ioam/holoviews/pull/370))
-   HoloViews now supports multiple active display hooks making it
    easier to use nbconvert. For instance, PNG data will be embedded in
    the notebook if the argument display\_formats=\['html','png'\] is
    supplied to the notebook\_extension. ([PR
    \#355](https://github.com/ioam/holoviews/pull/355))
-   Improvements to the display of DynamicMaps as well as many new
    improvements to the Bokeh backend including better VLines/HLines and
    support for the Bars element. ([PR
    \#367](https://github.com/ioam/holoviews/pull/367) , [PR
    \#362](https://github.com/ioam/holoviews/pull/362), [PR
    \#339](https://github.com/ioam/holoviews/pull/339)).
-   New Spikes and BoxWhisker elements suitable for representing
    distributions as a sequence of lines or as a box-and-whisker plot.
    ([PR \#346](https://github.com/ioam/holoviews/pull/346), [PR
    \#339](https://github.com/ioam/holoviews/pull/339))
-   Improvements to the notebook\_extension. For instance,
    executing hv.notebook\_extension('bokeh') will now load BokehJS and
    automatically activate the Bokeh backend (if available).
-   Significant performance improvements when using the groupby
    operation on HoloMaps and when working with highly
    nested datastructures. ([PR
    \#349](https://github.com/ioam/holoviews/pull/349), [PR
    \#359](https://github.com/ioam/holoviews/pull/359))

Notable bug fixes:

-   DynamicMaps are now properly integrated into the style system and
    can be customized in the same way as HoloMaps. ([PR
    \#368](https://github.com/ioam/holoviews/pull/368))
-   Widgets now work correctly when unicode is used in the dimension
    labels and values ([PR
    \#376](https://github.com/ioam/holoviews/pull/376)).

Version 1.4.0
=============

Over the past few months we have added several major new features and
with the help of our users have been able to address a number of bugs
and inconsistencies. We have closed 57 issues and added over 1100 new
commits.

Major new features:

-   Data API: The new data API brings an extensible system of to add new
    data interfaces to column based Element types. These interfaces
    allow applying powerful operations on the data independently of the
    data format. The currently supported datatypes include NumPy, pandas
    dataframes and a simple dictionary format. ([PR
    \#284](https://github.com/ioam/holoviews/pull/284))
-   Backend API: In this release we completely refactored the rendering,
    plotting and IPython display system to make it easy to add new
    plotting backends. Data may be styled and pickled for each backend
    independently and renderers now support exporting all plotting data
    including widgets as standalone HTML files or with separate
    JSON data.
-   Bokeh backend: The first new plotting backend added via the new
    backend API. Bokeh plots allow for much faster plotting and
    greater interactivity. Supports most Element types and layouts and
    provides facilities for sharing axes across plots and linked
    brushing across plots. ([PR
    \#250](https://github.com/ioam/holoviews/pull/250))
-   DynamicMap: The new DynamicMap class allows HoloMap data to be
    generated on-the-fly while running a Jupyter IPython
    notebook kernel. Allows visualization of unbounded data streams and
    smooth exploration of large continuous parameter spaces. ([PR
    \#278](https://github.com/ioam/holoviews/pull/278))

Other features:

-   Easy definition of custom aliases for group, label and Dimension
    names, allowing easier use of LaTeX.
-   New Trisurface and QuadMesh elements.
-   Widgets now allow expressing hierarchical relationships
    between dimensions.
-   Added GridMatrix container for heterogeneous Elements and gridmatrix
    operation to generate scatter matrix showing relationship
    between dimensions.
-   Filled contour regions can now be generated using the
    contours operation.
-   Consistent indexing semantics for all Elements and support for
    boolean indexing for Columns and NdMapping types.
-   New hv.notebook\_extension function offers a more flexible
    alternative to %load\_ext, e.g. for loading other
    extensions hv.notebook\_extension(bokeh=True).

Experimental features:

-   Bokeh callbacks allow adding interactivity by communicating between
    BokehJS tools and the IPython kernel, e.g. allowing downsampling
    based on the zoom level.

Notable bug fixes:

-   Major speedup rendering large HoloMaps (\~ 2-3 times faster).
-   Colorbars now consistent for all plot configurations.
-   Style pickling now works correctly.

API Changes:

-   Dimension formatter parameter now deprecated in favor
    of value\_format.
-   Types of Chart and Table Element data now dependent on
    selected interface.
-   DFrame conversion interface deprecated in favor of Columns
    pandas interface.

Version 1.3.2
=============

Minor bugfix release to address a small number of issues:

Features:

-   Added support for colorbars on Surface Element (1cd5281).
-   Added linewidth style option to SurfacePlot (9b6ccc5).

Bug fixes:

-   Fixed inversion inversion of y-range during sampling (6ff81bb).
-   Fixed overlaying of 3D elements (787d511).
-   Ensuring that underscore.js is loaded in widgets (f2f6378).
-   Fixed Python3 issue in Overlay.get (8ceabe3).

Version 1.3.1
=============

Minor bugfix release to address a number of issues that weren't caught
in time for the 1.3.0 release with the addition of a small number of
features:

Features:

-   Introduced new `Spread` element to plot errors and confidence
    intervals (30d3184).
-   `ErrorBars` and `Spread` elements now allow most Chart constructor
    types (f013deb).

Bug fixes:

-   Fixed unicode handling for dimension labels (061e9af).
-   Handling of invalid dimension label characters in widgets (a101b9e).
-   Fixed setting of fps option for MPLRenderer video output (c61b9df).
-   Fix for multiple and animated colorbars (5e1e4b5).
-   Fix to Chart slices starting or ending at zero (edd0039).

Version 1.3.0
=============

Since the last release we closed over 34 issues and have made 380
commits mostly focused on fixing bugs, cleaning up the API and working
extensively on the plotting and rendering system to ensure HoloViews is
fully backend independent.

We'd again like to thank our growing user base for all their input,
which has helped us in making the API more understandable and fixing a
number of important bugs.

Highlights/Features:

-   Allowed display of data structures which do not match the
    recommended nesting hierarchy (67b28f3, fbd89c3).
-   Dimensions now sanitized for `.select`, `.sample` and `.reduce`
    calls (6685633, 00b5a66).
-   Added `holoviews.ipython.display` function to render (and display)
    any HoloViews object, useful for IPython interact widgets (0fa49cd).
-   Table column widths now adapt to cell contents (be90a54).
-   Defaulting to Matplotlib ticking behavior (62e1e58).
-   Allowed specifying fixed figure sizes to Matplotlib via `fig_inches`
    tuples using (width, None) and (None, height) formats (632facd).
-   Constructors of `Chart`, `Path` and `Histogram` classes now support
    additional data formats (2297375).
-   `ScrubberWidget` now supports all figure formats (c317db4).
-   Allowed customizing legend positions on `Bars` Elements (5a12882).
-   Support for multiple colorbars on one axis (aac7b92).
-   `.reindex` on `NdElement` types now support converting between key
    and value dimensions allowing more powerful conversions. (03ac3ce)
-   Improved support for casting between `Element` types (cdaab4e,
    b2ad91b, ce7fe2d, 865b4d5).
-   The `%%opts` cell magic may now be used multiple times in the same
    cell (2a77fd0)
-   Matplotlib rcParams can now be set correctly per figure (751210f).
-   Improved `OptionTree` repr which now works with eval (2f824c1).
-   Refactor of rendering system and IPython extension to allow easy
    swapping of plotting backend (\#141)
-   Large plotting optimization by computing tight `bbox_inches`
    once (e34e339).
-   Widgets now cache frames in the DOM, avoiding flickering in some
    browsers and make use of jinja2 template inheritance. (fc7dd2b)
-   Calling a HoloViews object without arguments now clears any
    associated custom styles. (9e8c343)

API Changes

-   Renamed key\_dimensions and value\_dimensions to kdims and vdims
    respectively, while providing backward compatibility for passing and
    accessing the long names (8feb7d2).
-   Combined x/y/zticker plot options into x/y/zticks parameters which
    now accept an explicit number of ticks, an explicit list of tick
    positions (and labels), and a Matplotlib tick locator.
-   Changed backend options in %output magic, `nbagg` and `d3` are now
    modes of the Matplotlib backend and can be selected with
    `backend='matplotlib:nbagg'` and
    `backend='matplotlib:mpld3'` respectively. The 'd3' and 'nbagg'
    options remain supported but will be deprecated in future.
-   Customizations should no longer be applied directly to
    `Store.options`; the `Store.options(backend='matplotlib')` object
    should be customized instead. There is no longer a need to call the
    deprecated `Store.register_plots` method.

Version 1.2.0
=============

Since the last release we closed over 20 issues and have made 334
commits, adding a ton of functionality and fixing a large range of bugs
in the process.

In this release we received some excellent feedback from our users,
which has been greatly appreciated and has helped us address a wide
range of problems.

Highlights/Features:

-   Added new `ErrorBars` Element (f2b276b)
-   Added `Empty` pseudo-Element to define empty placeholders in
    Layouts (35bac9f1d)
-   Added support for changing font sizes easily (0f54bea)
-   Support for holoviews.rc file (79076c8)
-   Many major speed optimizations for working with and plotting
    HoloViews data structures (fe87b4c, 7578c51, 5876fe6, 8863333)
-   Support for `GridSpace` with inner axes (93295c8)
-   New `aspect_weight` and `tight` Layout plot options for more
    customizability of Layout arrangements (4b1f03d, e6a76b7)
-   Added `bgcolor` plot option to easily set axis background
    color (92eb95c)
-   Improved widget layout (f51af02)
-   New `OutputMagic` css option to style html output (9d42dc2)
-   Experimental support for PDF output (1e8a59b)
-   Added support for 3D interactivity with nbagg (781bc25)
-   Added ability to support deprecated plot options in %%opts magic.
-   Added `DrawPlot` simplifying the implementation of custom
    plots (38e9d44)

API changes:

-   `Path` and `Histogram` support new constructors (7138ef4, 03b5d38)
-   New depth argument on the relabel method (f89b89f)
-   Interface to Pandas improved (1a7cd3d)
-   Removed `xlim`, `ylim` and `zlim` to eliminate redundancy.
-   Renaming of various plot and style options including:

    -   `figure_*` to `fig_*`
    -   `vertical_spacing` and `horizontal_spacing` to `vspace` and
        `hspace` respectively

    \* Deprecation of confusing `origin` style option on RasterPlot
-   `Overlay.__getitem__` no longer supports integer indexing (use `get`
    method instead)

Important bug fixes:

-   Important fixes to inheritance in the options system
    (d34a931, 71c1f3a7)
-   Fixes to the select method (df839bea5)
-   Fixes to normalization system (c3ef40b)
-   Fixes to `Raster` and `Image` extents, `__getitem__` and sampling.
-   Fixed bug with disappearing adjoined plots (2360972)
-   Fixed plot ordering of overlaid elements across a
    `HoloMap` (c4f1685)

Version 1.1.0
=============

Highlights:

-   Support for nbagg as a backend (09eab4f1)
-   New .hvz file format for saving HoloViews objects (bfd5f7af)
-   New `Polygon` element type (d1ec8ec8)
-   Greatly improved Unicode support throughout, including support for
    unicode characters in Python 3 attribute names (609a8454)
-   Regular SelectionWidget now supports live rendering (eb5bf8b6)
-   Supports a list of objects in Layout and Overlay
    constructors (5ba1866e)
-   Polar projections now supported (3801b76e)

API changes (not backward compatible):

-   `xlim`, `ylim`, `zlim`, `xlabel`, `ylabel` and `zlabel` have been
    deprecated (081d4123)
-   Plotting options `show_xaxis` and `show_yaxis` renamed to `xaxis`
    and `yaxis`, respectively (13393f2a).
-   Deprecated IPySelectionWidget (f59c34c0)

In addition to the above improvements, many miscellaneous bug fixes were
made.

Version 1.0.1
=============

Minor release addressing bugs and issues with 1.0.0.

Highlights:

-   New separate Pandas Tutorial (8455abc3)
-   Silenced warnings when loading the IPython extension in IPython
    3 (aaa6861b)
-   Added more useful installation options via `setup.py` (72ece4db)
-   Improvements and bug-fixes for the `%%opts` magic
    tab-completion (e0ad7108)
-   `DFrame` now supports standard constructor for pandas
    dataframes (983825c5)
-   `Tables` are now correctly formatted using the appropriate
    `Dimension` formatter (588bc2a3)
-   Support for unlimited alphabetical subfigure labelling (e039d00b)
-   Miscellaneous bug fixes, including Python 3
    compatibility improvements.

Version 1.0.0
=============

First public release available on GitHub and PyPI.

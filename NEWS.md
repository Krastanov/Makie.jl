# News

## master

- Added a specialization for `volumeslices` to DataInspector

## v0.15.0

- `LaTeXString`s can now be used as input to `text` and therefore as labels for `Axis`, `Legend`, or other comparable objects. Mathematical expressions are typeset using [MathTeXEngine.jl](https://github.com/Kolaru/MathTeXEngine.jl) which offers a fast approximation of LaTeX typesetting. [#1022](https://github.com/JuliaPlots/Makie.jl/pull/1022)
- Added `Symlog10` and `pseudolog10` axis scales for log scale approximations that work with zero and negative values. [#1109](https://github.com/JuliaPlots/Makie.jl/pull/1109)
- Colorbar limits can now be passed as the attribute `colorrange` similar to plots. [#1066](https://github.com/JuliaPlots/Makie.jl/pull/1066)
- Added the option to pass three vectors to heatmaps and other plots using `SurfaceLike` conversion. [#1101](https://github.com/JuliaPlots/Makie.jl/pull/1101)
- Added `stairs` plot recipe. [#1086](https://github.com/JuliaPlots/Makie.jl/pull/1086)
- Removed `FigurePosition` and `FigureSubposition` types. Indexing into a `Figure` like `fig[1, 1]` now returns `GridPosition` and `GridSubposition` structs, which can be used in the same way as the types they replace. Because of an underlying change in `GridLayoutBase.jl`, it is now possible to do `Axis(gl[1, 1])` where `gl` is a `GridLayout` that is a sublayout of a `Figure`'s top layout. [#1075](https://github.com/JuliaPlots/Makie.jl/pull/1075)
- Bar plots and histograms have a new option for adding text labels. [#1069](https://github.com/JuliaPlots/Makie.jl/pull/1069)
- It is possible to specify one linewidth value per segment in `linesegments`. [#992](https://github.com/JuliaPlots/Makie.jl/pull/992)
- Added a new 3d camera that allows for better camera movements using keyboard and mouse. [#1024](https://github.com/JuliaPlots/Makie.jl/pull/1024)
- Fixed the application of scale transformations to `surface`. [#1070](https://github.com/JuliaPlots/Makie.jl/pull/1070)
- Added an option to set a custom callback function for the `RectangleZoom` axis interaction to enable other use cases than zooming. [#1104](https://github.com/JuliaPlots/Makie.jl/pull/1104)
- Fixed rendering of `heatmap`s with one or more reversed ranges in CairoMakie, as in `heatmap(1:10, 10:-1:1, rand(10, 10))`. [#1100](https://github.com/JuliaPlots/Makie.jl/pull/1100)
- fixed volume slice recipe and add docs for it [#1123](https://github.com/JuliaPlots/Makie.jl/pull/1123)

# GIS Notes

A collection of notes as I dive into GIS (Geographic Information Systems) in general and the QGIS software application more specifically.

## Resources

A list of helpful beginner resources for GIS, from which these notes are derived:
  - https://saylordotorg.github.io/text_essentials-of-geographic-information-systems/index.html
    - Github Source Code: https://github.com/saylordotorg/text_essentials-of-geographic-information-systems
  - https://docs.qgis.org/3.28/en/docs/gentle_gis_introduction/index.html
  - https://docs.qgis.org/3.28/en/docs/training_manual/

## What is GIS?

 - GIS stands for **Geographic Information Systems**

 - GIS consists of digital data, computer hardware, and computer software

 - GIS started in the 1970s, first with expensive computers owned by universities and businesses, then eventually anyone with a personal computer could participate

## What is GIS Software / Application?

 - GIS Software and/or Applications are computer programs, often with a graphic user interface (GUI) that allow for the manipulation of digital geographic data and commonly the displaying of map layers representing something in the real world (e.g. roads, rivers, neighborhoods, countries, trees, etc)
 
 - Other common features of GIS applications include map legends, layer reordering, etc.

## What is GIS Data?
  
   - GIS data is data (another word for information) that includes geographic and non-geographic aspects. For example, the location of one or more patients with a specific disease might be recorded. The patient's location would be the geographic aspect of the GIS data and the patient's disease would be the non-geographic aspect of the GIS data.

   - GIS systems work with many different types of data:
      - **Vector data** is stored as a series of X,Y coordinate pairs and typically represents points, lines, and areas, while maintaining image quality when zoomed

      - **Raster data** is stored as a grid of values and can be thought of as a typical photograph or image of a location that becomes "blocky" or "fuzzy" when zoomed

### Vector Data
  - Vector data provides a way to represent real world **features** in a GIS environment

  - **Features** are anything we can see on in a landscape such as roads, rivers, trees, etc or even man-made concepts such as country borders.

    - A vector **feature** has it's shape represented by a **geometry**, which is made up of one or more connected **vertices**

    - **Vertices** describe positions in space using **X**, **Y**, and optionally **Z** axes.

    - Geometries with a **Z** axis are often referred to as **2.5D** because they describe height or depth at each vertex, but not both.

    - Additionally, vector **features** have **attributes**, which consist of text or numerical information that describe the feature (e.g. a vector feature for a tree would have geographic data representing its location and could also have attributes representing its species, age, or circumference)

    ### Points, Polylines, and Polygons

    - A **Point** is a feature with only a single vertex
      - Some examples of point features would be trees on a neighborhood map or cities on a world map
      - Point features often become polygons at a larger scale, e.g. points of cities can become polygon city boundaries when zoomed
    - A **Polyline** is a feature with two or more vertices where the first and last vertex are not equal
      - Roads, rivers, flight paths, and contours are all examples of features that would be good candidates for the use of a polyline
      - Sometimes polylines have extra rules such as "polylines of roads should connect at intersections" or "topographic contour polylines can touch (i.e., at cliffs) but should never cross each other"
    - A **Polygon** is a feature with four or more vertices where the first and last vertex are equal (alternatively, one could infer a polygon from three vertices if a line is always assumed to be drawn from the last vertex back to the first vertex)
      - Some examples of polygon features would be city boundaries on larger maps or individual houses in a neighborhood on smaller maps
    
    ### Layers

     - Most GIS applications group vector features into **layers**, which have the same geometry type and the same kinds of attributes (e.g. a tree layer would consist of point geometries representing trees along with attributes describing those trees)

     - This grouping of features into layers conveniently allows us to show or hide all of a specific type of feature on our maps as a single unit

    ### Scale

     - **Scale** is the ratio of a distance on a map to a corresponding distance on the ground
    
     - Choosing the wrong scale for your GIS data can cause unintended side effects such as missing or partially captured features when the scale is too small (i.e. too zoomed out for your requirements) or wasted effort and time capturing features that aren't actually needed when the scale is too large (i.e. too zoomed in for your requirements)

    ### Symbology

    - **Symbology** can be defined as the study of symbols or alternatively the art of expression using symbols.
    - Vector layers in GIS applications will be shown with default colors and symbols, however it is often beneficial to use the symbology tools built into a GIS application to change these meaningless defaults to more intuitive and meaningful symbols
      - For example, a layer of point features that represent trees may be drawn as purple dots by default within the GIS application. This dots are rather meaningless for anyone viewing a map, so using the symbology tools within the GIS application to change the purple dots to small tree images will help future viewers understand the data represented on a map created from this feature layer

    ### Spatial Analysis

    - Vector data excels at helping us do **spatial analysis**, which is the process of answering geographic questions such as "How many houses lay within the 100 year floodplain?" or "Where is the most dense one square kilometer section of forest within the nature preserve?"

    ### Common Problems With Vector Data

    - **Slivers** are visual errors of thin lines through polygon features that occur when the edges of two polygon areas don't meet properly
    
    - **Overshoots** and **Undershoots** are visual errors of line features slightly sticking out past an exact intersection (when they should have stopped at the intersection) or barely not touching at exact intersections (when they should have touched at the intersection), respectively.

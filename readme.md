# GIS Notes

A collection of notes as I dive into GIS in general and QGIS more specifically.

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
      - Vector data is stored as a series of X,Y coordinate pairs and typically represents points, lines, and areas, while maintaining image quality when
      - Raster data is stored as a grid of values and can be thought of as a typical photograph or image of a location that becomes "blocky" or "fuzzy" when zoomed in too much

### Vector Data
  - Vector data provides a way to represent real world **features** in a GIS environment
  - **Features** are anything we can see on in a landscape such as roads, rivers, trees, etc or even man-made concepts such as country borders.
    - A vector **feature** has it's shape represented by a **geometry**, which is made up of one or more connected **vertices**
    - **Vertices** describe positions in space using **X**, **Y**, and optionally **Z** axes.
    - Geometries with a **Z** axis are often referred to as **2.5D** because they describe height or depth at each vertex, but not both.
    - Additionally, vector **features** have **attributes**, which consist of text or numerical information that describe the feature (e.g. a vector feature for a tree would have geographic data representing its location and could also have attributes representing its species, age, or circumference)
  
# Core packages
dbverse consists of three core packages that contain simple classes, generics, and methods for representing abstract data types in a DuckDB database.

1.  [dbMatrix](https://drieslab.github.io/dbMatrix) - A database backend
    for counts including sparse/dense matrices and data.frames.
2.  [dbSpatial](https://drieslab.github.io/dbSpatial) - A database backend
    for geometries including geojson, shp, and more.
3.  [dbData](https://drieslab.github.io/dbData) - A lightweight package with
    specifications for base class of `dbverse` core packages.
    

# Extensions
Packages that use core packages.

- [Giotto](https://github.com/drieslab/Giotto)
    - A comprehensive spatial transcriptomic analysis toolbox.
    - dbverse packages: `dbMatrix` and `dbSpatial`

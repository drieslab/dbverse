# Core packages
dbverse consists of three core packages that contain simple classes, generics, and methods for representing abstract data types in a DuckDB database.

1.  [dbMatrix](https://ed2uiz.github.io/dbMatrix) - A database backend
    for counts including sparse/dense matrices and data.frames.
2.  [dbSpatial](https://ed2uiz.github.io/dbSpatial) - A database backend
    for geometries including geojson, shp, and more.
3.  [dbSequence](https://ed2uiz.github.io/dbSequence) - A database
    backend for biological sequences including bam/SAM, fastq/fasta, and
    more.
    

# Extensions
dbverse extensions are built on top of the core packages. 

- [Cytobase](https://ed2uiz.github.io/cytobase/index.html)
    - Functions for single-cell and spatial transcriptomic analysis in R.
    - dbverse packages: `dbMatrix` and `dbSpatial`


# Downsream packages
Packages that use extensions or core packages.

- [Giotto](https://github.com/drieslab/Giotto)
    - A full-fledged spatial transcriptomic analysis toolbox in R.
    - dbverse packages: `dbMatrix` and `dbSpatial`

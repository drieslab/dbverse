# dbverse

Note: dbverse is still in early development. changes to the below are likely to occur.

## Class Diagram
```mermaid
classDiagram
direction LR

namespace Data {

    class tabular{
        .mtx
        .csv
        .parquet
        .hdf5
        dgCMatrix
        data.frames
    }

    class geometries{
        .shp
        .geojson
        sf::sf
        terra::spatVector
    }

}

namespace dbverse {

    class dbMatrix_lib{

    }

    class dbSpatial_lib{

    }

    class dbData_lib{

    }

}

namespace dbData_lib {
    class dbData {
        <<base class>>
        + value: duckdb_table
        + name: table_name
        + init: boolean
        - DBI::listTables()
        - DBI::writeTables()
        - DBI::dbDisconnect()
        - DBI::*()
    }

}

namespace dbSpatial_lib {

    class dbSpatial{
    - ST_*(geom) [DuckDB_spatial]
    }
    
    class dbSpatialPoints{
    - ST_*(geom_point) 
    }

    class dbSpatialPolygons{
    - ST_*(geom_polygon)
    }
}

namespace dbMatrix_lib {
    class dbMatrix {
        + dim_names: [enum,enum]
        + dims: [int, int]
        + class: "sparse" | "dense"
        - dbMatrix::*()
        - dbMatrixStats::*()
    }

    class dbSparseMatrix{

    }

    class dbDenseMatrix{

    }
}


tabular <..> dbData_lib : read/write
geometries <..> dbData_lib : read/write

dbData_lib --> dbMatrix_lib
dbData_lib --> dbSpatial_lib

dbSpatial --> dbSpatialPoints
dbSpatial --> dbSpatialPolygons

dbMatrix --> dbDenseMatrix
dbMatrix --> dbSparseMatrix
```

## Description
TODO: More text on the structure of the dbverse ecosystem.


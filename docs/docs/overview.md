# dbverse

**Note: `{dbverse}` is in early development. Changes to the below are likely to occur.**

## Class Diagram
```mermaid
classDiagram
direction LR

namespace Input_Data {
    class numerical{
        .mtx
        .csv
        .parquet
        dgcMatrix
        matrix
        data.frame
        data.table
    }

    class geometries{
        50+ spatial file formats
        sf::sf
        terra::spatVector
    }

    class sequences{
        10+ genomic file formats
    }
}

namespace computer {
    class database
}

namespace dbverse {
    class dbMatrix_lib{
        class dbMatrix
    }

    class dbSpatial_lib{
        class dbSpatial
    }

    class dbSequence_lib{
        class dbSequence
    }

    class dbData_lib{
        class dbData
    }
}

namespace dbMatrix_lib {
    class dbMatrix {
        + dbData: dbData
        + dim_names: [enum,enum]
        + dims: [int, int]
        + class: "dbSparseMatrix" | "dbDenseMatrix"
        - Arith
        - Ops
        - matrix summary functions()
    }
}

namespace dbSpatial_lib {
    class dbSpatial{
        + dbData: dbData
        - ST_*(geom) [DuckDB Spatial Extension]
    }
}

namespace dbSequence_lib {
    class dbSequence{
        + dbData: dbData
    }
}

namespace dbData_lib {
    class dbData {
        <<base virtual class>>
        + value: Input_Data
        + name: table_name
        + init: boolean
        + conn: DuckDB connection
        - DBI::()
        - dplyr::()
    }
}

numerical <..> dbMatrix_lib : read/write
geometries <..> dbSpatial_lib : read/write
sequences <..> dbSequence_lib : read/write

dbMatrix_lib --> dbData_lib
dbSpatial_lib --> dbData_lib
dbSequence_lib --> dbData_lib

dbData_lib <..> database : connect/disconnect/cache
```


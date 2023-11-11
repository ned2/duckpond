# The Duck Pond
Resources for exploring the [DuckDB](https://duckdb.org) ecosystem.


[Mermaid](https://github.com/mermaid-js/mermaid) based diagramming

## Overview

```mermaid

%%{init: {"flowchart": {"curve": "catmullRom"}, "themeVariables": {"edgeLabelBackground": "transparent"}}}%%


flowchart LR

Local & HTTPS & S3 & fssec --> Excel & JSON & Parquet & CSV
Excel & JSON & Parquet & CSV --> DuckDB
R_deplyr & Pandas & Polars & Numpy --> DuckDB
DuckDB --> Excel2 & JSON2 & Parquet2 & CSV2
Excel2 & JSON2 & Parquet2 & CSV2 --> Local_Disk & S3_API
DuckDB --> Arrow
Arrow --> DataFusion & Vaex & Delta_Lake


subgraph Sources
Local & HTTPS & S3 & fssec
end

subgraph Targets
Local_Disk & S3_API
end

click DuckDB "https://duckdb.org/"

class Sources,Targets cd_box1;
class DuckDB cd_box4;

classDef cd_box1 fill:#ddd,stroke:#fff,stroke-width:4px,color:#000;
classDef cd_box2 fill:#326ce5,stroke:#fff,stroke-width:4px,color:#fff;
classDef cd_box3 fill:#fff,stroke:#bbb,stroke-width:2px,color:#326ce5;
classDef cd_box4 fill:#FCFF99,stroke:#333,stroke-width:px
classDef cd_box5 fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5

R_deplyr[R Deplyr] 
Delta_Lake[Delta Lake]
Excel2[Excel]
JSON2[JSON]


DuckDB[("DuckDB")]
%% Local>Local file]
Local[fa:fa-file-alt File Local]



```
# Data Science Foundations: Data Engineering

## Ecosystem Overview

### System Overview

![Overview](images/overview.png "Overview")
![Data Hub](images/data_hub.png "Data Hub")

- `Staging`: persisting data as we receive
- `Cleansing`: transformations (datetime), removing nulls
- `Conforming`: getting references in base tables, ids
- `Delivered`: UPSERT (update or insert)

### Star schema

![Star Schema Components](images/star_schema_components.png "Star Schema Components")
![Star Schema Example](images/star_schema_ex.png "Star Schema Example")

- Star Schema: Sales `Facts` are just 1 join away of all support `Dimensions` information

### Data Engineering Responsabilities

- Data Ops Tasks
  - Infra
  - Availability/Performance
- Data Prep
  - Staging
  - Cleansing
  - Conforming
  - Deliverying
- Data Interfaces
  - APIs
  - Query Tool Compatibility

### Good data pipeline

![Good Data Pipeline](images/good_data_pipeline.png "Good Data Pipeline")

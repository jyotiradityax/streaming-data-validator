# streaming-data-validator
A system where users define data "rules" in a JSON/YAML file, and the system validates incoming streams of data against those rules.


# Streaming Data Validator

## The "Why"
Traditional validation is often hardcoded. This project decouples **Business Logic** from **Code** by using a declarative YAML-based engine. 

### Architecture
```mermaid
graph TD
    A[Producer] -->|JSON Data| B(Kafka)
    B --> C{Validator App}
    D[YAML Rules] --> C
    C -->|Pass| E[Clean Data Topic]
    C -->|Fail| F[Postgres/Alerts]

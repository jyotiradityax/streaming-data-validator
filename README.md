# streaming-data-validator
A system where users define data "rules" in a JSON/YAML file, and the system validates incoming streams of data against those rules.


├── .github/workflows/      # GitHub Actions (CI/CD)
├── config/                 # YAML/JSON validation rules
├── docker-compose.yml      # Infrastructure-as-Code
├── docs/                   # Architecture diagrams & API specs
├── infra/                  # Prometheus/Postgres initialization scripts
├── services/
│   ├── validator-app/      # Main logic (Java/Python)
│   └── mock-producer/      # Script to push test data to Kafka
└── tests/                  # Integration & Unit tests

# Mermaid example (code → diagram in the same file)

## Code (left panel in VS Code / GitHub)
```mermaid
flowchart LR
  subgraph Data["Data Layer"]
    A[Raw Data] --> B[Preprocessing]
    B --> C[Feature Engineering]
  end

  subgraph Modeling["Modeling Layer"]
    C --> D[Model Training]
    D --> E[Evaluation]
  end

  subgraph Serving["Serving Layer"]
    E --> F[Deployment]
    F --> G[Monitoring]
  end
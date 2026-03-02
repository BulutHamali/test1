# Mermaid example (code → diagram in the same file)

## Code (left panel in VS Code / GitHub)
```mermaid
flowchart TD
  subgraph Data["Data Layer"]
    A[Raw Data]
    B[Preprocessing]
    C[Feature Engineering]
  end

  subgraph Modeling["Modeling Layer"]
    D[Model Training]
    E[Evaluation]
  end

  subgraph Serving["Serving Layer"]
    F[Deployment]
    G[Monitoring]
  end

  A --> B --> C --> D --> E --> F --> G
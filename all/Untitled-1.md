```mermaid
graph TD
    subgraph Frontend
        U[User (Agent/Analyst)]
        ACA[Alfresco Content App<br/>(Angular / ADF)]
        BTN[UI Button: "Analyze with AI"]
    end

    subgraph Alfresco
        API[Alfresco REST API]
        ACS[Alfresco ACS 7.4 Repository]
    end

    subgraph Backend
        FAST[FastAPI AI Backend]
        LLM[Mistral / OpenRouter API]
    end

    subgraph Output
        JSON[Structured JSON Response<br/>(Score, Status, Summary)]
        META[Metadata Updated<br/>via Alfresco PATCH API]
    end

    U --> ACA
    ACA --> API
    API --> ACS
    ACA --> BTN
    BTN --> FAST
    FAST --> LLM
    LLM --> JSON
    JSON --> META
    META --> API
    API --> ACA

```
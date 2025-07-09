```mermaid
graph TD
    U[User]
    ACA[Alfresco Content App (Angular)]
    BTN["Analyze with AI" Button]
    API[Alfresco REST API]
    ACS[Alfresco ACS 7.4]
    FAST[FastAPI AI Backend]
    LLM[Mistral / OpenRouter API]
    JSON[AI JSON Response: Score / Status / Summary]
    META[Update Metadata via Alfresco]

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
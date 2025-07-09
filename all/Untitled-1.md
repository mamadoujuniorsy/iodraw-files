```mermaid
graph TD
    User["User"] -->|uses| ACA["Alfresco Content App (Angular)"]
    ACA -->|fetches metadata| API["Alfresco REST API"]
    API -->|reads/writes documents| ACS["Alfresco ACS 7.4"]
    ACA -->|clicks| BTN["\"Analyze with AI\" Button"]
    BTN -->|sends nodeId| FAST["FastAPI Backend"]
    FAST -->|sends PDF content| MISTRAL["OpenRouter / Mistral API"]
    MISTRAL -->|returns JSON| FAST
    FAST -->|PATCH metadata| API
    API -->|returns updated data| ACA

```
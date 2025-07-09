```mermaid

User->Alfresco Content App (Angular): uses
Alfresco Content App (Angular)->Alfresco REST API: fetches metadata
Alfresco REST API->Alfresco ACS 7.4: reads/writes documents
Alfresco Content App (Angular)->"Analyze with AI" Button: clicks
"Analyze with AI" Button->FastAPI Backend: sends nodeId
FastAPI Backend->OpenRouter / Mistral API: sends PDF content
OpenRouter / Mistral API->FastAPI Backend: returns JSON
FastAPI Backend->Alfresco REST API: PATCH metadata
Alfresco REST API->Alfresco Content App (Angular): updated metadata

```
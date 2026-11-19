# Lead-Qualifier

flowchart TD
    A[Airtable: Watch qualified records] --> B{Router}

    B --> C[Gmail: Send email]
    C --> D[Airtable: Update record]
    D --> E[Set Contacted on = current time]

    B --> F[Text Parser: Match pattern]
    F --> G[Extract value from message]
    G --> H[Slack: Send message]

    

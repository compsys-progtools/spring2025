# General Tips and Resources

This section is for materials that are not specific to this course, but are likely useful. They are not generally required readings or installs, but are options or advice I provide frequently.

## on email

- [how to e-mail professors](https://insidehighered.com/views/2015/04/16/advice-students-so-they-dont-sound-silly-emails-essay)

## Class Workflow
```{mermaid}
flowchart TD
    Z{"START HERE"}--> A
    A["Finish Prepare Work before Class"] --> B["Class"]
    B --> C["Run action for experience badge"]
    C --> D["Fill out experience badge"]
    D --> E["Link Preparework to experience badge from the Development option"]
    E --> F{"Choose Homework Type From Issues Tab"}

    F --> G["Review Badge"]
    F --> H["Practice Badge"]

    %% New "Am I Lost?" Decision Point AFTER selecting a badge %%
    G --> Q{"Am I Lost?"}
    H --> Q

    Q -- "Yes" --> R["Check Course Website Notes"] --> S["Ask Teacher/TA"] --> T["Attend Office Hours"] --> Q
    Q -- "No" --> I["Click Development and Create new branch, Make sure the date and badge type is in the name"]

    I --> J["Upload Files/Commit to Branch Repo"]
    J --> K["Create Pull Request, Make sure the date and badge type is in the name"]
    K --> L["Wait for feedback from TA/Teacher"]

    %% Approval or Changes Loop %%
    L -- "Pull Request Approved" --> M["Merge Pull Request"] -- "REPEAT" --> A
    L -- "Changes Requested" --> N["Fix Changes"] --> O["Request Review"] --> L
```

```mermaid
sequenceDiagram
    participant user
    participant browser
    participant server


    %%user writes note
    user->>browser: writes a note in form field
    user->>browser: clicks save

    %%browser send user input to server
    browser->>server: sends POST request to server with new note
    activate server
    server->>browser: adds new note to list
    server->>browser: updated notes
    deactivate server

    %%Browser updates page
    browser->>browser: Render HTML document and new note on page


```
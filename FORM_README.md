
This is the Clear Diagramatic Representation of the Forms Elements and the Attributes and many More.......


                                      HTML FORM
                                          │
                                          │
                 ┌────────────────────────┼────────────────────────┐
                 │                        │                        │
                 ↓                        ↓                        ↓
             FORM CONTROLS           VALIDATION               SUBMISSION
                 │                        │                        │
        ┌────────┼────────┐       ┌───────┼────────┐       ┌───────┴────────┐
        │        │        │       │       │        │       │                │
        ↓        ↓        ↓       ↓       ↓        ↓       ↓                ↓
      input   textarea  select  required minlength maxlength pattern      button
        │        │        │       │       │        │        │                │
        │        │        │       │       │        │        │                │
        │        │        │       └───────┴────────┴────────┘                │
        │        │        │                    │                             │
        │        │        │                    ↓                             │
        │        │        │             Browser Validation                   │
        │        │        │                    │                             │
        │        │        │             ┌──────┴──────┐                      │
        │        │        │             ↓             ↓                      │
        │        │        │         INVALID         VALID                    │
        │        │        │             │             │                      │
        │        │        │             ↓             ↓                      │
        │        │        │       Show error       Continue                  │
        │        │        │                           │                      │
        │        │        │                           └──────────┐           │
        │        │        │                                      │           │
        ↓        ↓        ↓                                      ↓           ↓
      INPUT   TEXTAREA  SELECT                               SUBMIT       BUTTON
        │        │        │                                      │
        │        │        │                                      │
   ┌────┼────┐   │     OPTION                                  │
   │    │    │   │        │                                    │
   ↓    ↓    ↓   ↓        ↓                                    │
 text email password   value + displayed text                  │
   │    │    │   │                                             │
   │    │    │   ├── number                                   │
   │    │    │   ├── date                                     │
   │    │    │   ├── file                                     │
   │    │    │   ├── checkbox                                 │
   │    │    │   ├── radio                                    │
   │    │    │   ├── range                                    │
   │    │    │   └── color                                    │
   │    │    │                                                 │
   │    │    │                                                 │
   └────┴────┴─────────────────────────────────────────────────┘
                              │
                              ↓
                         FORM FIELD DATA
                              │
                 ┌────────────┴────────────┐
                 │                         │
                 ↓                         ↓
               id                        name
                 │                         │
                 │                         │
                 ↓                         ↓
        Identifies HTML element      Identifies submitted
                 │                    form data field
                 │                         │
                 ↓                         ↓
        ┌────────────────┐          ┌────────────────┐
        │     label      │          │ FormData /     │
        │                │          │ HTTP request   │
        └───────┬────────┘          └───────┬────────┘
                │                           │
                ↓                           ↓
          for="email"                 name="email"
                │                           │
                └──────────┐                │
                           ↓                │
                      id="email"            │
                           │                │
                           ↓                ↓
                      ACCESSIBILITY    SUBMITTED VALUE
                           │                │
                           ↓                ↓
                      Screen reader     email=...
                      understands            │
                      field meaning          │
                                            │
                                            │
                                            ↓
                                   ┌───────────────────┐
                                   │   FORM ATTRIBUTES │
                                   └─────────┬─────────┘
                                             │
                  ┌──────────────────────────┼─────────────────────────┐
                  │                          │                         │
                  ↓                          ↓                         ↓
                action                     method                    enctype
                  │                          │                         │
                  ↓                    ┌─────┴─────┐            ┌──────┴─────────┐
          Where to submit              ↓           ↓            ↓                ↓
          form data                  GET         POST       urlencoded     multipart/form-data
                  │                    │           │                           │
                  │                    │           │                           │
                  │                    ↓           ↓                           ↓
                  │             Data in URL    Data in body              File upload
                  │             query params   request body                   │
                  │                    │           │                           │
                  │                    │           │                           ↓
                  │                    │           │                    ┌─────────────┐
                  │                    │           │                    │ Input type  │
                  │                    │           │                    │    file     │
                  │                    │           │                    └──────┬──────┘
                  │                    │           │                           │
                  └────────────────────┴───────────┴───────────────────────────┘
                                             │
                                             ↓
                                       HTTP REQUEST
                                             │
                                             │
                           ┌─────────────────┴──────────────────┐
                           │                                    │
                           ↓                                    ↓
                     TRADITIONAL FORM                    JAVASCRIPT
                       SUBMISSION                          HANDLING
                           │                                    │
                           │                              submit event
                           │                                    │
                           │                                    ↓
                           │                              preventDefault()
                           │                                    │
                           │                                    ↓
                           │                                new FormData()
                           │                                    │
                           │                                    ↓
                           │                              FormData API
                           │                                    │
                           │                         ┌──────────┴─────────┐
                           │                         │                    │
                           │                         ↓                    ↓
                           │                       get()              getAll()
                           │                         │                    │
                           │                         ├── append()         │
                           │                         ├── set()            │
                           │                         ├── has()            │
                           │                         └── delete()         │
                           │                                              │
                           │                                              │
                           │                                              ↓
                           │                                         fetch()
                           │                                              │
                           └──────────────────────────┬───────────────────┘
                                                      │
                                                      ↓
                                               HTTP REQUEST
                                                      │
                                   ┌──────────────────┼──────────────────┐
                                   │                  │                  │
                                   ↓                  ↓                  ↓
                                 URL               METHOD              BODY
                                   │                  │                  │
                             /register              POST           Form data
                             /login                 GET            / FormData
                             /upload                                             
                                                      │
                                                      ↓
                                              ┌───────────────┐
                                              │    SERVER     │
                                              │   / BACKEND   │
                                              └───────┬───────┘
                                                      │
                                                      ↓
                                          SERVER-SIDE VALIDATION
                                                      │
                                      ┌───────────────┴───────────────┐
                                      ↓                               ↓
                                   INVALID                          VALID
                                      │                               │
                                      ↓                               ↓
                                Error Response                  Business Logic
                                      │                               │
                                      │                               ↓
                                      │                           Database
                                      │                               │
                                      │                               ↓
                                      │                         Server Response
                                      │                               │
                                      └───────────────┬───────────────┘
                                                      │
                                                      ↓
                                                HTTP RESPONSE
                                                      │
                                                      ↓
                                                   Browser
                                                      │
                                      ┌───────────────┴───────────────┐
                                      ↓                               ↓
                              Traditional page                 JavaScript /
                                 response                         React
                                                                      │
                                                                      ↓
                                                                Update UI
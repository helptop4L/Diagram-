
# Diagram-classDiagram
    class User {
        +String username
        +String email
        +String password
        +Mailbox mailbox
        +login()
        +sendEmail(Email)
        +receiveEmail()
    }
    class Email {
        +String from
        +String to
        +String subject
        +String body
        +Date timestamp
        +send()
        +archive()
        +delete()
    }
    class Mailbox {
        +List~Email~ emails
        +getInbox()
        +getSentEmails()
        +getEmailById()
    }
    User "1" -- "*" Email : sends >
    User "1" -- "1" Mailbox : has >
    ```mermaid

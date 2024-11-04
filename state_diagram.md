```mermaid
---
config:
  layout: dagre
  look: classic
  theme: neutral
---
stateDiagram-v2
    [*] --> Login
    Login --> LoginSuccess: Success
    Login --> LoginFail: Fail
    LoginSuccess --> LoggedIn
    LoginFail --> Login: retry
    LoggedIn --> [*]: logout
```
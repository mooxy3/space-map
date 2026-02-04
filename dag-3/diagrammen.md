---
title: DeepDive-3 Space Captain Website Flow
config:
  theme: redux
---
flowchart TD
    A([Home Page<br/>Background: Space Station]):::bg
    A --> B{Logged in?}
    B -- "No" --> D[Navbar: Login/Register]
    D --> E[Register Page<br/>Fields: Email, Password, Ship Name]
    E --> F([200 Credits Added])
    F --> G[Navbar updates:<br/>Credits, Map, Logout]

    B -- "Yes" --> G

    G --> H([Map Page<br/>3D Solar System & Stations]):::map
    H --> I{Click planet/moon/station}
    I --> J[Show info rightside:<br/>Name, Location,<br/>Activities, History,<br/>Navigate Button]
    J --> K{Navigate?}
    K -- "Yes" --> L["Line appears from Ship to Destination<br/>(Auto path, avoid obstacles)"]

    classDef bg fill:#001852,stroke:#29eaff,stroke-width:3px,color:#afe1ff;
    classDef map fill:#111b28,stroke:#47bfff,stroke-width:3px,color:#76bdff;
# HoloPiano: VR Piano Instructor
This is the project for Computer Science and Engineering Projects (II), NYCU.
Title: Real-Time Interactive VR System – Remote Piano Classroom 

## Authors
Syuan-Fu Hwang, Yu-Chun Lin, Ting-Yu Chou


```mermaid
flowchart LR
    A[Recording Client]
    B[Server]
    C[VR Client]

    A -->|TCP Connect| B
    linkStyle 0 stroke:#007BFF,stroke-width:2px
    B -->|TCP Reply UDP Port| A
    linkStyle 1 stroke:#FFA500,stroke-width:2px
    A -->|UDP Connect| B
    linkStyle 2 stroke:grey,stroke-width:2px
    B -->|UDP OK| A
    linkStyle 3 stroke:#FFA500,stroke-width:2px
    A -->|UDP Data| B
    linkStyle 4 stroke:grey,stroke-width:2px

    C -->|TCP Connect| B
    linkStyle 5 stroke:#007BFF,stroke-width:2px
    B -->|TCP Reply UDP Port| C
    linkStyle 6 stroke:#FFA500,stroke-width:2px
    C -->|UDP Connect| B
    linkStyle 7 stroke:grey,stroke-width:2px
    B -->|UDP OK| C
    linkStyle 8 stroke:#FFA500,stroke-width:2px
    B -->|UDP Data| C
    linkStyle 9 stroke:grey,stroke-width:2px

    style A fill:#D3D3D3,stroke:#000,stroke-width:1px,height:210px
    style B fill:#D3D3D3,stroke:#000,stroke-width:1px,height:210px
    style C fill:#D3D3D3,stroke:#000,stroke-width:1px,height:210px
```

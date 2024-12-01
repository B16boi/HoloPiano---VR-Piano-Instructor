# HoloPiano: VR Piano Instructor
This is the project for Computer Science and Engineering Projects (II), NYCU.
Title: Real-Time Interactive VR System – Remote Piano Classroom 

## Authors
Syuan-Fu Hwang, Yu-Chun Lin, Ting-Yu Chou


```mermaid
flowchart LR
    subgraph GrayBox1[Visualization Layer]
        C[VR Client]
    end

    subgraph GrayBox2[Processing Layer]
        B[Server]
    end

    subgraph GrayBox3[Input Layer]
        A[Recording Client]
    end

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

    style GrayBox1 fill:#D3D3D3,stroke:#000,stroke-width:1px
    style GrayBox2 fill:#D3D3D3,stroke:#000,stroke-width:1px
    style GrayBox3 fill:#D3D3D3,stroke:#000,stroke-width:1px
    style A fill:#fff,stroke:#000,stroke-width:1px
    style B fill:#fff,stroke:#000,stroke-width:1px
    style C fill:#fff,stroke:#000,stroke-width:1px
```

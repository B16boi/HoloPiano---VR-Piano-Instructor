# HoloPiano: VR Piano Instructor
This is the project for Computer Science and Engineering Projects (II), NYCU.
Title: Real-Time Interactive VR System – Remote Piano Classroom 

## Authors
Syuan-Fu Hwang, Yu-Chun Lin, Ting-Yu Chou


```mermaid
flowchart LR
    subgraph RecClient[ ]
    direction TB
    A["Recording Client"]
    end

    subgraph ServerBox[ ]
    direction TB
    B["Server"]
    end

    subgraph VRClient[ ]
    direction TB
    C["VR Client"]
    end

    RecClient -->|"TCP Connect"| ServerBox
    linkStyle 0 stroke:#007BFF,stroke-width:2px,yOffset:-70
    ServerBox -->|"TCP Reply UDP Port"| RecClient
    linkStyle 1 stroke:#FFA500,stroke-width:2px,yOffset:-70
    RecClient -->|"UDP Connect"| ServerBox
    linkStyle 2 stroke:grey,stroke-width:2px,yOffset:-35
    ServerBox -->|"UDP OK"| RecClient
    linkStyle 3 stroke:#FFA500,stroke-width:2px,yOffset:-35
    RecClient -->|"UDP Data"| ServerBox
    linkStyle 4 stroke:grey,stroke-width:2px,yOffset:35

    VRClient -->|"TCP Connect"| ServerBox
    linkStyle 5 stroke:#007BFF,stroke-width:2px,yOffset:-70
    ServerBox -->|"TCP Reply UDP Port"| VRClient
    linkStyle 6 stroke:#FFA500,stroke-width:2px,yOffset:-70
    VRClient -->|"UDP Connect"| ServerBox
    linkStyle 7 stroke:grey,stroke-width:2px,yOffset:-35
    ServerBox -->|"UDP OK"| VRClient
    linkStyle 8 stroke:#FFA500,stroke-width:2px,yOffset:-35
    ServerBox -->|"UDP Data"| VRClient
    linkStyle 9 stroke:grey,stroke-width:2px,yOffset:35

    A:::centered
    B:::centered
    C:::centered

    style RecClient fill:#D3D3D3,stroke:#000,stroke-width:1px,height:210px
    style ServerBox fill:#D3D3D3,stroke:#000,stroke-width:1px,height:210px
    style VRClient fill:#D3D3D3,stroke:#000,stroke-width:1px,height:210px

    classDef centered fill:none,stroke:none,yOffset:105
    classDef no-style fill:none,stroke:none
    class A,B,C no-style
```

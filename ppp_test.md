::: mermaid 
graph TB
  A[Glucose 6-phosphate] -- Glucose 6-phosphate dehydrogenase --> B[6-Phosphogluconolactone]
  B -- Gluconolactonase --> C[6-Phosphogluconate]
  C -- 6-Phosphogluconate dehydrogenase --> D[Ribulose 5-phosphate]
  D -- Ribose 5-phosphate isomerase --> E[Ribose 5-phosphate]
  D -- Ribulose 5-phosphate 3-epimerase --> F[Xylulose 5-phosphate]
  E -- Transketolase --> Gbox[ ]
  F --Transketolase --> Gbox[ ]
  Gbox[ ] -- Transaldolase --> Hbox[ ]
  
  %% Subgraph for Glyceraldehyde 3-phosphate + 
  subgraph Gbox [ ]
    G[Glyceraldehyde 3-phosphate]
    H[Sedoheptulose 7-phosphate]
    end

  %% Subgraph for Fructose 6-phosphate + Erythrose 4-phosphate
  subgraph Hbox [ ]
    I[Fructose 6-phosphate]
    J[Erythrose 4-phosphate]
  end


  I --> K[Glycolysis]
  K --> I

  J -- Transketolase --> Jbox[ ]

  %% Subgraph for Glyceraldehyde 3-phosphate + Fructose 6-phosphate
  subgraph Jbox [ ]
    L[Glyceraldehyde 3-phosphate]
    M[Fructose 6-phosphate]
  end

  L --> N[Glycolysis]
  N --> L
  M --> P[Glycolysis]
  
  P --> M
  O[Xylulose 5-phosphate] -- Transketolase --> Jbox[ ]
:::
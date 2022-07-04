graph LR
  subgraph
   Y(<b>core</b>)
 init --> Z["query endpoints"]
 Z --> Z1[route output and execute things in middleware] 
Z1 --> Z2{new query required}
Z2 -- yes --> Z
Z2 -- no --> Z1 

  end
  subgraph
   X(<b>config</b>) -.-> init
   A(endpoints)
   B(middleware)
   C(routing)
   X --- A
   X --- B
   X --- C
  end
  subgraph
 A2(<b>endpoint</b>)
parameters --> D1(encoder?)
D1 --> transport
transport --> D2
 D2("parser/decoder?") --> result
  end
  subgraph
B2(<b>middleware</b>)
input --> D3(transform)
D3 --> output
  end
  subgraph
C2(<b>route</b>)
D4["input(s)"] -->
D5["output(s)"]
  end
classDef label fill:#eef, stroke:#eef
class A2,B2,C2,X,Y label
A -.- A2
B -.- B2
C -.- C2

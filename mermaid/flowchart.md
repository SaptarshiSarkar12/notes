# Flowchart

Flowcharts contain **nodes** (the geometric shapes) and **edges** (the arrows or lines). They are ideal for visualizing simple processes directly in markdown.

For example, a user login flow can be clearly mapped out to show steps like entering credentials, checking validity, and redirecting to the dashboard. This helps both developers and stakeholders quickly understand logic without external tools.

### Orientation

Possible flowchart orientations:

* TB/TD: Top to Bottom
* BT: Bottom to Top
* RL: Right to Left
* LR: Left to Right

```mermaid
flowchart LR
    A --> B
```

```mermaid
flowchart LR
    A --> B
```

### Node shapes

```mermaid
flowchart LR
    A([User]) --using--> B[[Browser]] --at port--> C((5000)) --in--> D(his laptop)
```

```mermaid
flowchart LR
    A([User]) --using--> B[[Browser]] --at port--> C((5000)) --in--> D(his laptop)
```

```mermaid
graph LR
  A(User Data) --stored in--> B[(database)] --hosted in--> C@{shape: st-doc, label: "on-premises servers"}
```

```mermaid
graph LR
  A(User Data) --stored in--> B[(database)] --hosted in--> C@{shape: st-doc, label: "on-premises servers"}
```

### Subgraph

Subgraphs are especially useful when inter-connected graphs are shown in one frame.

```mermaid
flowchart LR
  subgraph PI[Public Internet]
    U(((User)))
  end
  subgraph LBZ[Load Balancer Zone]
    L{{LoadBalancer}}
  end
  subgraph WSZ[Web Servers Zone]
    W1@{ shape: disk, label: "Web Server A" }
    W2@{ shape: disk, label: "Web Server B" }
  end
  subgraph DSZ[Database Servers Zone]
    D1[(Database Server A)]
    D2[(Database Server B)]
  end

  U e1@--> |tcp/80| L
  L e2@==> |tcp/1337| W1
  L e3@==> |tcp/1337| W2
  W1 e4@--> D1
  W1 e5@-.-> D2
  W2 e6@--> D1
  W2 e7@-.-> D2


  e1@{animate: true}
  e2@{animate: true}
  e3@{animate: true}
```

```mermaid
flowchart LR
  subgraph PI[Public Internet]
    U(((User)))
  end
  subgraph LBZ[Load Balancer Zone]
    L{{LoadBalancer}}
  end
  subgraph WSZ[Web Servers Zone]
    W1@{ shape: disk, label: "Web Server A" }
    W2@{ shape: disk, label: "Web Server B" }
  end
  subgraph DSZ[Database Servers Zone]
    D1[(Database Server A)]
    D2[(Database Server B)]
  end

  U e1@--> |tcp/80| L
  L e2@==> |tcp/1337| W1
  L e3@==> |tcp/1337| W2
  W1 e4@--> D1
  W1 e5@-.-> D2
  W2 e6@--> D1
  W2 e7@-.-> D2


  e1@{animate: true}
  e2@{animate: true}
  e3@{animate: true}
```

In the above example, different node shapes and subgraphs have been used along with node IDs (like `e1`, `e2`, `e3`, etc.). By using those IDs, we can animate them using `{animate: true}`.

### Want to Know More?

If you're interested in learning more, the full content is available here: [https://mermaid.js.org/syntax/flowchart.html](https://mermaid.js.org/syntax/flowchart.html)

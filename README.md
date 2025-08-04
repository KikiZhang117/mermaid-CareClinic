## diagram / 01 / Three interaction modes

```mermaid
graph TB
  subgraph Puff
  A --> B --> C
  end 

  subgraph Voice
  I --> J --> L
  end

  subgraph Rest
  Q --> R --> U
  end

  C -.->|Emergency| L
  J -->|Data| R
  classDef emergency fill<br>#ffecec,stroke<br>#ff6b6b;
  class C,L emergency;
```

## diagram / 02 / Puff mode

```mermaid
graph TD
  A[User\<br>"Start breathing"] --> B{Keyword Analysis}
  B -->|Match<br>"help"| C[Trigger Emergency Protocol]
  B -->|Match<br>"begin"| D[Initiate Biofeedback]
  D --> E[Predictive Alerting]
  E -->|RR >30| F[Voice\<br>"Slow your pace"]
  E -->|RR ≤30| G[Haptic\<br>Sync pulses]
  C --> H[Notify Care Team]
  style C stroke\<br>#ff0000,stroke-width:4px
```

## diagram / 03 / Voice mode

```mermaid
graph LR
  I[Voice Activation] --> J{NLP Processing}
  J -->|Command<br>Log| K[Timestamp + Intensity]
  J -->|Command<br>Help| L[Emergency SMS]
  K --> M{Data Completeness}
  M -->|Missing Duration| N[Contextual Query]
  M -->|Complete| O[EHR Integration]
  L --> P[Alert<br>On-call OB]
  style L stroke<br>#ff0000,stroke-width<br>4px
```

## diagram / 04 / Rest mode

```mermaid
graph BT
  Q[User<br>"I need rest"] --> R{Emotion Analysis}
  R -->|Stress >7/10| S[Affective Response]
  R -->|Stress ≤7/10| T[Ambient Monitoring]
  S --> U["Play<br>Guided Meditation (CDC-approved)"]
  T --> V[Adjust Environment]
  V -->|Dim Lights to <15lux| W[Biofeedback Loop]
  style S fill<br>#e3f7fc,stroke<br>#333
```

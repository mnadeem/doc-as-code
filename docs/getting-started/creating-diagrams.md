---
title: Creating Diagrams With Mermaid js
description: Creating diagrams using mermaid js extension
authors:
    - Mohammad Nadeem
date: 2020-11-25
---

Refer [Mermaid-js](https://mermaid-js.github.io/mermaid/#/){target=_blank} and [documentation](https://mermaid-js.github.io/mermaid/#/){target=_blank} for more details

## 1️⃣ Flow

### Example #1

=== "Output"

    ```mermaid
    graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
    ```

=== "Markdown"

    ```
       ```mermaid
       graph TD;
         A-->B;
         A-->C;
         B-->D;
         C-->D;
       ```
    ```

### Example #2

=== "Output"

    ```mermaid
    graph TD
      A[Hard] -->|Text| B(Round)
      B --> C{Decision}
      C -->|One| D[Result 1]
      C -->|Two| E[Result 2]
    ```

=== "Markdown"

    ```
       ```mermaid
       graph TD
         A[Hard] -->|Text| B(Round)
         B --> C{Decision}
         C -->|One| D[Result 1]
         C -->|Two| E[Result 2]
       ```
    ```


## 2️⃣ Sequence

=== "Output"

    ```mermaid
    sequenceDiagram
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
    ```

=== "Markdown"

    ```
       ```mermaid
       sequenceDiagram
       Alice->>John: Hello John, how are you?
       loop Healthcheck
           John->>John: Fight against hypochondria
       end
       Note right of John: Rational thoughts!
       John-->>Alice: Great!
       John->>Bob: How about you?
       Bob-->>John: Jolly good!

       ```
    ```

## 3️⃣ Gantt

=== "Output"

    ```mermaid
    gantt
    section Section
    Completed :done,    des1, 2014-01-06,2014-01-08
    Active        :active,  des2, 2014-01-07, 3d
    Parallel 1   :         des3, after des1, 1d
    Parallel 2   :         des4, after des1, 1d
    Parallel 3   :         des5, after des3, 1d
    Parallel 4   :         des6, after des4, 1d
    ```

=== "Markdown"

    ```
       ```mermaid
       gantt
       section Section
       Completed :done,    des1, 2014-01-06,2014-01-08
       Active        :active,  des2, 2014-01-07, 3d
       Parallel 1   :         des3, after des1, 1d
       Parallel 2   :         des4, after des1, 1d
       Parallel 3   :         des5, after des3, 1d
       Parallel 4   :         des6, after des4, 1d

       ```
    ```

## 4️⃣ Class

=== "Output"

    ```mermaid
    classDiagram
    Class01 <|-- AveryLongClass : Cool
    <<interface>> Class01
    Class09 --> C2 : Where am i?
    Class09 --* C3
    Class09 --|> Class07
    Class07 : equals()
    Class07 : Object[] elementData
    Class01 : size()
    Class01 : int chimp
    Class01 : int gorilla
    class Class10 {
     <<service>>
     int id
     size()
    }
    ```

=== "Markdown"

    ```
       ```mermaid
       classDiagram
       Class01 <|-- AveryLongClass : Cool
       <<interface>> Class01
       Class09 --> C2 : Where am i?
       Class09 --* C3
       Class09 --|> Class07
       Class07 : equals()
       Class07 : Object[] elementData
       Class01 : size()
       Class01 : int chimp
       Class01 : int gorilla
       class Class10 {
        <<service>>
        int id
        size()
       }

       ```
    ```

## 5️⃣ State

=== "Output"

    ```mermaid
    stateDiagram-v2
    [*] --> Still
    Still --> [*]
    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
    ```

=== "Markdown"

    ```
       ```mermaid
       stateDiagram-v2
       [*] --> Still
       Still --> [*]
       Still --> Moving
       Moving --> Still
       Moving --> Crash
       Crash --> [*]

       ```
    ```


## 6️⃣ Pie

=== "Output"

    ```mermaid
    pie
    "Dogs" : 386
    "Cats" : 85
    "Rats" : 15
    ```

=== "Markdown"

    ```
       ```mermaid
       pie
       "Dogs" : 386
       "Cats" : 85
       "Rats" : 15

       ```
    ```

## 7️⃣ Journey

=== "Output"

    ```mermaid
    journey
      title My working day
      section Go to work
        Make tea: 5: Me
        Go upstairs: 3: Me
        Do work: 1: Me, Cat
      section Go home
        Go downstairs: 5: Me
        Sit down: 3: Me
    ```

=== "Markdown"

    ```
       ```mermaid
       journey
        title My working day
        section Go to work
          Make tea: 5: Me
          Go upstairs: 3: Me
          Do work: 1: Me, Cat
        section Go home
          Go downstairs: 5: Me
          Sit down: 3: Me

       ```
    ```

## 8️⃣ ER

=== "Output"

    ```mermaid
    erDiagram
      CUSTOMER ||--o{ ORDER : places
      ORDER ||--|{ LINE-ITEM : contains
      CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
    ```

=== "Markdown"

    ```
       ```mermaid
       erDiagram
         CUSTOMER ||--o{ ORDER : places
         ORDER ||--|{ LINE-ITEM : contains
         CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
       ```
    ```

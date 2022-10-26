<!--
 ~ SPDX-FileCopyrightText: Copyright DB Netz AG and contributors
 ~ SPDX-License-Identifier: Apache-2.0
 -->

# This is demonstration page of MkDocs features


## Admonitions

!!! info

    Example info.

!!! warning

    Example warning

## Mermaid

``` mermaid
graph LR
  A[Start] --> B{Error?};
  B -->|Yes| C[Hmm...];
  C --> D[Debug];
  D --> B;
  B ---->|No| E[Yay!];
```

``` mermaid
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

## Footnote

Example footnote reference[^1]

[^1]: This is the footnote

## Image

![Example image](example.jpg)

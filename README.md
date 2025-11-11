flowchart TD

A[User lands on website] --> B[User enters natural-language intent e.g. “I am going hiking”]

B --> C[Pre-processing: tokenize, clean, lemmatize]

C --> D{Intent Match?}

D -->|Yes| E[Fetch mapped product bundle]
D -->|No| F[Keyword search fallback]
F --> G[Log unknown query for future improvement]

E --> H[Display product bundle]
G --> H

H --> I{User action?}

I -->|Add to cart| J[Proceed to checkout]
I -->|Refine search| B
I -->|Exit| K[End]

J --> L[Place order]
L --> K

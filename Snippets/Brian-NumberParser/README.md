# Number Parser
This snippet parses number resolvables into a valid integer. Very useful when working with number-based user inputs to for example, use in math tags to prevent breaking stuff. The parser supports **floats** and **human readable numbers** as shown by the examples below:

**Examples:**
* **Input:** `a!parse 1e5`\
  **Output:** `100000`

* **Input:** `a!parse 420m`\
  **Output:** `420000000`

* **Input:** `a!parse 6.942e6`\
  **Output:** `6942000`
  
* **Input:** `a!parse 56.4k`
  **Output:** `56400`

# Number Parser
This snippet parses number resolvables into a valid integer. Very useful when working with number-based user inputs to for example, use in math tags to prevent breaking stuff. The parser supports **floats** and **human readable numbers** as shown by the examples below:

**Examples:**
* **Input:** `/parse parameter:1e5`\
  **Output:** `100000`

* **Input:** `/parse parameter:420m`\
  **Output:** `420000000`

* **Input:** `/parse parameter:6.942e6`\
  **Output:** `6942000`
  
* **Input:** `/parse parameter:56.4k`\
  **Output:** `56400`

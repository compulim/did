# Do it differently

Point form for speedy writing. If I/we made a different design decision, 80% chance it could become better.

## Table of contents

| Area  | Product            | Date                      |
| ------| ------------------ | ------------------------- |
| Azure | Azure Bot Services | [2024-02-28](#2024-02-28) |

## 2024-02-28

### Azure Bot Services: Proactive messaging

- This universe
   - Proactive messaging need an explicit set up
- Another universe
   - Proactive messaging is implicit and is the only mode
   - Messages sent through proactive messaging could route to push: Web Push, APNS, GCM, WNS (and even ACS/Trouter)
      - Web Push requires a visible message, while APNS/GCM/WNS support binary/invisible message
   - We still need to retrieve the full message via chat history

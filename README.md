# Do it differently

Point form for speedy writing. If I/we made a different design decision, 80% chance it could become better.

## Table of contents

| Area  | Product            | Date                      |
| ------| ------------------ | ------------------------- |
| Azure | Azure Bot Services | [2024-02-28](#2024-02-28) |
| Bot Framework | Web Chat | [2024-02-28](#2024-02-28) |

## 2024-02-28

### Azure Bot Services: Proactive messaging

- This universe
   - Proactive messaging need an explicit set up
- Another universe
   - Proactive messaging is implicit and is the only mode
   - Messages sent through proactive messaging could route to push: Web Push, APNS, GCM, WNS (and even ACS/Trouter)
      - Web Push requires a visible message, while APNS/GCM/WNS support binary/invisible message
   - We still need to retrieve the full message via chat history

### Web Chat: Missing activities referenced by `replyToId`

- This universe
   - Wait up to 5 seconds for the missing activity to show up
      - This wait is crucical to keep the order of the message narrated by screen reader in a correct order
- Another universe
   - After timed out, we should show a badge in the chat history and say "some messages in this point of time may be missing"

![image](https://github.com/compulim/did/assets/1622400/79971f6e-06c6-4d9a-8605-b26d3ad67830)

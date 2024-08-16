LimaCharlie D&R Rule for Mimikatz

Example Installation: https://github.com/ParrotSec/mimikatz

```
events:
  - NEW_PROCESS
  - EXISTING_PROCESS
op: and
rules:
  - op: is windows
  - op: or
    rules:
      - case sensitive: false
        op: ends with
        path: event/FILE_PATH
        value: mimikatz.exe
      - case sensitive: false
        op: contains
        path: event/COMMAND_LINE
        value: mimikatz
      - case sensitive: false
        op: is
        path: event/HASH
        value: 54724f38ff2f85c3ff91de434895668b6f39008fc205a668ab6aafad6fb4d93d
 
- action: report
  metadata:
    author: Malachi
    description: Detects Mimikatz (SOAR-EDR tool)
    falsepositives:
      - Medium
    level: high
    tags:
      - attack.credential_access
  name: Malachi - HackTool - Mimikatz

---
description: Recap recent events - last session, last N sessions, or a specific arc
---
Generate a narrative recap:

1. Load session logs from `campaigns/<name>/session-log-*.md`
2. If argument specifies a number, recap that many sessions
3. If argument specifies an arc/keyword, find relevant entries
4. Default: recap the last session

Present as a narrative "Previously on..." summary suitable for starting a new session.

$ARGUMENTS

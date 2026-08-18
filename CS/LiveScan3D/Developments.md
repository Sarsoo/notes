---
onenote-id: 0-56f7064ac79f45dba0e689a7e76684c2!16-D084F068F621FF9!3717
---
Rolling client Tx buffer

- Buffer can fill on dead internet, allows latency to move realistically

Limit Tx buffer dequeue to number of writable sockets

- Is this operating how I think it is?
- Should I select for a little bit longer?

Logging

- With async, should improve
- Covers profiling directly to csv files

Server-side latency control

- Is this going in the right direction?
- Increase frequency if latency increases?

Client-side double dropping

- Back to pre-buffer dropping
- Fraction of buffer dropping for Tx

Checkboxes for latency controls  
Console for client application
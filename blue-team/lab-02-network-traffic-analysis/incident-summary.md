## Incident Summary
Network traffic analysis identified an internal host communicating with a known malicious external IP over HTTP. The traffic pattern is consistent with command-and-control activity following malware infection.

## Detection Method
Manual analysis of packet capture data.

## Impact
The affected system likely executed malware and communicated with an external command-and-control server.

## Response Actions
- Host isolation recommended
- Network blocking of malicious infrastructure
- Endpoint forensic investigation advised

## Lessons Learned
Packet capture analysis can reveal early indicators of compromise even in the absence of endpoint alerts.





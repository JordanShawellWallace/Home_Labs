## Objective
Analyze a packet capture (PCAP) file to identify malicious network activity and determine evidence of command-and-control (C2) behavior.

## Scenario Context
The PCAP represents traffic from a system exposed to a malicious advertisement that redirected the user to a fake Microsoft Teams page. The page delivered malware that communicated with an external HTTP-based command-and-control server.

## Environment
- Internal host: 10.1.17.215
- External IP: 5.252.153.241
- Protocol: HTTP over TCP (port 80)

## Actions Taken
- Reviewed protocol distribution and TCP conversations
- Identified dominant internal-to-external communication
- Filtered HTTP traffic between the internal host and the suspected C2 server
- Analyzed HTTP request patterns for automation and repetition

## Key Observations
- The internal host initiated repeated HTTP GET requests to the external IP on port 80
- Requests targeted an API-style endpoint (`/api/file/get-file/<id>`)
- The traffic pattern was repetitive and automated in nature
- The earliest observed malicious communication occurred approximately 60 seconds into the capture

## Analyst Assessment
The observed traffic is consistent with post-infection command-and-control behavior over HTTP. Repeated GET requests to an API endpoint suggest the host was polling the C2 server for files or instructions. The system was likely compromised before the first observed malicious request.

## Recommended Actions
- Isolate the affected host from the network
- Block the malicious IP at network security controls
- Perform endpoint malware analysis and credential review





# Bytecode Bouncer – IPv4 Packet Inspector

A network packet inspection and filtering simulator built using **n8n** and JavaScript.

## Abstract

Bytecode Bouncer is an educational network security project designed to inspect IPv4 packet data and apply configurable filtering rules. It receives packet information through a webhook, analyses the IPv4 header, identifies the network protocol and extracts source and destination IP addresses and port numbers.

Based on predefined security rules, the system classifies packets into three categories: ALLOW, BLOCK, or REJECT.

## Objectives

- Analyse IPv4 packet hexadecimal data.
- Extract important IPv4 header information.
- Identify TCP, UDP and ICMP protocols.
- Apply configurable IP address and port filtering rules.
- Identify invalid or incomplete packet data.
- Return clear packet inspection results.

## Features

- Webhook-based packet input.
- IPv4 header parsing.
- TCP, UDP and ICMP protocol identification.
- Source and destination IP extraction.
- Source and destination port extraction.
- Configurable blocked IP addresses.
- Configurable blocked ports.
- Protocol filtering.
- ALLOW, BLOCK and REJECT decisions.
- Inspection timestamp.

## Technologies Used

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| JavaScript | Packet analysis and filtering |
| Webhook | Receive packet data |
| JSON | Input and output data |
| GitHub | Project version control |

## Workflow Architecture

1. **Packet Inspection Webhook:** Receives packet data through an HTTP POST request.
2. **Parse IPv4 and Apply Rules:** Analyses the packet and applies security filtering rules.
3. **Return Inspection Result:** Sends the inspection result as a JSON response.

## How It Works

1. The user sends packet hexadecimal data to the webhook.
2. The webhook receives the JSON request.
3. The JavaScript code validates and parses the IPv4 packet.
4. The system extracts packet information.
5. Security rules are applied.
6. The system returns ALLOW, BLOCK or REJECT.

## Sample Input

```json
{
  "packetHex": "450000281234400040060000C0A80001C0A800021F90005000000000000000005002721000000000",
  "allowedProtocols": ["TCP", "UDP"],
  "blockedPorts": [],
  "blockedIPs": []
}
```

## Testing Results

| Test Case | Expected Result |
|---|---|
| Valid TCP packet | ALLOW |
| Packet with blocked port 80 | BLOCK |
| Invalid packet data | REJECT |

All three test cases were successfully tested in the n8n workflow.

## How to Import the Project

1. Download the workflow JSON file from this repository.
2. Open your n8n Cloud account.
3. Create a new workflow or open the workflow menu.
4. Select Import from File.
5. Choose the downloaded JSON file.
6. Save and test the workflow.
7. Activate the workflow when ready.

## Project Limitations

- This is an educational packet inspection simulator.
- It processes supplied packet hexadecimal data.
- It does not capture live network traffic.
- It does not directly configure operating system firewalls.

## Future Enhancements

- Real-time packet capture integration.
- Advanced firewall rule management.
- Packet inspection dashboard.
- Detailed security reports.
- Network traffic statistics.

## Author

**Sunil K G**

Computer Science and Engineering

## Project Repository

[Bytecode-Bouncer on GitHub](https://github.com/sunilganeshbabu-design/Bytecode-Bouncer)

---

**Project:** CN01 – The Bytecode Bouncer  
**Category:** Computer Networks  
**Status:** Working educational prototype

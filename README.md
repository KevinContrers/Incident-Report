# Cybersecurity Analysis: SYN Flood Attack 

## Scenario

As part of a hands-on exercise during my **Google Cybersecurity Professional Certificate**, I encountered and mitigated a **SYN Flood Attack** on a simulated web server. This exercise involved analyzing the issue, identifying the attack type, and implementing mitigation strategies.

The scenario simulated a critical issue where the web server experienced connection timeout errors, preventing employees and customers from accessing the company's sales webpage. My task was to identify the root cause and apply corrective actions.

---

## Incident Analysis

Using a **packet sniffer** tool, I captured and analyzed the network traffic to and from the web server. The captured data revealed an unusually high volume of **TCP SYN requests** originating from a suspicious IP address, overwhelming the server's ability to process legitimate requests.

---

## Type of Attack

| **Attack Type**       | **Explanation**                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------|
| **SYN Flood Attack**   | A Denial of Service (DoS) attack that overwhelms the server with excessive SYN requests.    |

This was identified as a **SYN Flood Attack**, where the server was flooded with incomplete **TCP handshake** requests, exhausting its resources and causing a connection timeout for legitimate users.

---

## How the Attack Causes Website Malfunction

During a legitimate TCP connection, a **three-way handshake** occurs as follows:

1. **SYN Packet**: Sent from the client requesting a connection.
2. **SYN-ACK Packet**: Server responds, reserving resources for the connection.
3. **ACK Packet**: Client acknowledges the response, completing the handshake.

In a **SYN Flood Attack**, multiple SYN requests are sent, but the final ACK step is never completed. As a result, the server's resources are consumed, preventing it from accepting new legitimate connections and resulting in timeouts.

---

## Immediate Actions Taken

| **Action**                        | **Description**                                                             |
|-----------------------------------|-----------------------------------------------------------------------------|
| **Took the server offline**        | Temporarily shut down the server to allow recovery from the SYN flood attack.|
| **Blocked malicious IP address**   | Configured the firewall to block the IP sending abnormal SYN requests.       |

These immediate actions helped mitigate the attack, allowing the server to recover and preventing further damage.

---

## Next Steps

| **Next Steps**                  | **Description**                                                                                     |
|----------------------------------|-----------------------------------------------------------------------------------------------------|
| **Alerted Management**           | Informed stakeholders about the attack and proposed preventative actions.                           |
| **Enhanced Security Measures**   | Considered additional defenses, including:                                                          |
|                                  | - **SYN Cookies** to defend against SYN floods.                                                     |
|                                  | - **Rate Limiting** to throttle suspicious traffic.                                                  |
|                                  | - **Intrusion Detection Systems (IDS)** to better monitor future threats.                           |

---

## Learning and Experience

This exercise provided invaluable hands-on experience with detecting and mitigating network attacks in a controlled environment. It reinforced the importance of **real-time monitoring** and quick response to security incidents. This activity highlighted how effective incident response and immediate action can minimize business disruption during cyberattacks.

Through this project, I gained a deeper understanding of **DoS attacks**, how they exploit system vulnerabilities, and the steps necessary to prevent such incidents in real-world environments.

---

## Tools & Technologies Used

| **Tool/Technology**        | **Purpose**                                                      |
|----------------------------|------------------------------------------------------------------|
| **Packet Sniffer**          | Captured network traffic for analysis.                          |
| **Firewall Configuration**  | Blocked malicious IP traffic to mitigate the attack.            |
| **Intrusion Detection System (IDS)** | Plan to implement to enhance future threat detection.       |

---

This project demonstrates my ability to apply cybersecurity principles in real-world scenarios, using techniques learned through the **Google Cybersecurity Professional Certificate**. It reflects my readiness to handle network security challenges and my commitment to ongoing learning and practical experience in the cybersecurity field.

---

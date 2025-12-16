 Capture and Analyze Network Traffic Using Wireshark

 Objective

The objective of this task is to capture live network traffic using Wireshark and analyze the captured packets to identify different network protocols and understand how data is transmitted over a network.

Tools Used

* Operating System: Kali Linux
* Tool: Wireshark (Free and Open Source)
* Network Interface:  eth0
* Target Website: Acunetix Vulnerable Web Application (testphp.vulnweb.com)

 Task Description

  In this task, Wireshark was used to capture live network packets while browsing a website and performing a login operation. The captured traffic was then filtered and analyzed to identify different protocols and packet details.

 Steps Performed

1. Installed and opened Wireshark on Kali Linux.
2. Selected the active network interface (`eth0`) for packet capture.
3. Started live packet capturing.
4. Opened a web browser and accessed the Acunetix vulnerable test website.
5. Navigated to the login page and performed a login attempt using test credentials.
6. Stopped the packet capture after sufficient traffic was generated.
7. Applied protocol filters (e.g., `http`) to analyze relevant packets.

 Packet Analysis and Observations

 1. Identified Protocols

During packet analysis, the following protocols were identified:

* HTTP (Hypertext Transfer Protocol):** Used for web communication between the browser and server.
* TCP (Transmission Control Protocol):** Ensures reliable data transmission with sequence and acknowledgment numbers.
* OCSP (Online Certificate Status Protocol):** Used for certificate status verification.

 2. HTTP Traffic Analysis

* An HTTP POST request to `/userinfo.php` was captured during the login attempt.
* The request method used was **POST** with content type `application/x-www-form-urlencoded`.
* The following form data was clearly visible in plaintext within the captured packet:

  *  Username: test
  *  Password: test123
* This confirms that the credentials were transmitted without encryption over HTTP and were successfully captured using Wireshark.
 3. Security Observation

* Since HTTP does not encrypt data, sensitive information such as login credentials can be intercepted.
* This demonstrates the importance of using HTTPS to protect user data from packet sniffing attacks.

Key Learnings

* Understood how to capture live network traffic using Wireshark.
* Learned to apply protocol filters to analyze specific traffic.
* Gained practical knowledge of HTTP, TCP, and OCSP protocols.
* Observed how plaintext credentials can be exposed over unencrypted connections.

Conclusion

This task provided hands-on experience in network traffic analysis using Wireshark. By capturing and analyzing packets, I learned how different protocols operate and how insecure communication channels can expose sensitive data. This exercise improved my understanding of network security and packet-level analysis.

 Outcome

* Successfully captured live network packets.
* Identified and analyzed multiple network protocols.
* Gained awareness of security risks in unencrypted network communication.

---



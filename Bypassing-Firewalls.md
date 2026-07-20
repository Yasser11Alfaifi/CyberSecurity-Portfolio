During my practical training in networking and cyber security, I focused on understanding digital identifiers and how attackers exploit them to bypass defensive systems. Here is the technical breakdown:

IP Address (Logical & Dynamic): Acts as the device's location address. It is split into Private (used within the local network to distinguish devices before the router) and Public (the external address the internet uses to see your router).

MAC Address (Physical & Static): Represents the "unique fingerprint" or factory serial number of the network interface card (NIC), ensuring accurate data delivery within the local network.

Hands-on Application: MAC Spoofing
Although a MAC address is physically permanent, an attacker can modify it programmatically on their own device to match a trusted device on the network. This identity theft is used to bypass router access controls (MAC Filtering) or Firewalls.

The Attack Mechanism (Via TryHackMe Lab Environment):




Before Spoofing 

<img width="1103" height="821" alt="Screenshot 2026-07-20 164157" src="https://github.com/user-attachments/assets/8c43b9a9-4fff-48e1-87fd-56f57c6e7042" />



Shows a stable network. Both Bob's and Alice's devices have unique, independent MAC addresses, allowing the router to direct traffic smoothly without any conflict.






After Spoofing 

<img width="1918" height="728" alt="Screenshot 2026-07-20 170227" src="https://github.com/user-attachments/assets/803978e5-d67a-433d-8122-dec7c04ef0b5" />



The attacker changed their own device's MAC address programmatically to perfectly match the victim's (Alice). Since routers lack a built-in mechanism to reject duplicate MACs, the router gets confused and starts passing data to the attacker, causing network disruption for the victim and enabling eavesdropping.





The Takeaway: Understanding these structural vulnerabilities in network protocols is the first step as a cyber security analyst to build strong detection mechanisms and secure internal corporate networks.

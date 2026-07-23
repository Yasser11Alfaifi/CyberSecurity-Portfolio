# 🛡️ Lab Summary: Mitigating DoS Traffic via Firewall Rules

## 📌 Overview
This lab demonstrates how to analyze malicious network traffic and mitigate a Denial of Service (DoS) attack targeting an HTTP web server by creating a custom inbound firewall rule.

---

## 🔍 Before Mitigation (Active Attack)
* **Target Server:** `203.0.110.1` (Port 80 / HTTP)
* **Attacker IP:** `198.51.100.34`
* **Observation:** The attacker host continuously flooded the web server on Port 80 with high-volume requests, draining server resources and causing service disruption.
* **Firewall Status:** No active filtering rules for the malicious IP.


<img width="1347" height="731" alt="Screenshot 2026-07-23 114703" src="https://github.com/user-attachments/assets/8234393d-c73a-4aac-b493-92466a81e802" />

---

## 🛠️ Action Taken
Created an explicit **DROP** rule on the perimeter router/firewall to intercept and discard incoming traffic from the attacker's IP address.

* **Rule Configuration:**
  * **Source IP:** `198.51.100.34`
  * **Destination IP:** `203.0.110.1`
  * **Port:** `80`
  * **Action:** `DROP`

---

## ✅ After Mitigation (Traffic Blocked)
* **Result:** Malicious packets are dropped at the router level before reaching the target web server.
* **Outcome:** Server resources stabilized, and legitimate network operations resumed without interference.


<img width="1257" height="726" alt="Screenshot 2026-07-23 114748" src="https://github.com/user-attachments/assets/dd17ebbb-493a-4f33-86e2-a52e5199dc76" />

# TryHackMe: Offensive Security Intro (FakeBank Lab)

## Executive Summary
In this introductory lab, I explored the basics of offensive security by simulating a controlled attack on a vulnerable web application called **FakeBank**. The objective was to understand how attackers gather initial information and discover hidden application vulnerabilities.

---

## Phase 1: Information Gathering & Reconnaissance
The first step in any security assessment is to understand the target environment. 
* **Action:** Accessed the live virtual lab environment and inspected the user interface of the banking application.
* **Key Concept:** Identified unique identifiers (such as target account numbers) which serve as the foundation for tracking activities or executing targeted testing.

---

## Phase 2: Directory Brute-Forcing (Hidden Page Discovery)
Web developers sometimes leave sensitive administrative pages accessible on the server without linking them to the main homepage. 

* **Tool Used:** `dirb` (Directory Buster)
* **Concept:** `dirb` is a command-line web content scanner. It launches a dictionary-based attack against a web server to look for hidden directories and pages by analyzing response codes.
* **Execution:** Ran the following command in the terminal:
  ```bash
  dirb [http://fakebank.thm](http://fakebank.thm)

  Terminal Output & Discovery:
<img width="930" height="776" alt="Screenshot 2026-07-18 110506" src="https://github.com/user-attachments/assets/36956212-902b-4cef-8fb2-3849c0c1e64b" />


Result: As shown in the screenshot above, the tool successfully uncovered hidden URLs (indicated by the + sign in the terminal output), exposing a sensitive administrative page (/bank-transfer) that was left unprotected.

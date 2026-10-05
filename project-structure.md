# Project Structure: Purple Team Lab

This document tracks the overall plan. The project is split into **Parts** (big milestones) and **Steps** (small tasks inside each part). Each Part has a "Done when" checkpoint instead of a deadline, so I can work at my own pace.

**Legend:** `[x]` done, `[ ]` not started

---

## Part 1: Lab Setup

Build the isolated environment: vulnerable targets, an attacker machine, and a network that keeps everything contained.

**Done when:** Kali can reach both apps in a browser, and the lab cannot reach the internet.

- [x] **Step 1:** Install and verify Git, create the GitHub repo, and clone it
- [x] **Step 2:** Run `docker run hello-world` to confirm Docker works
- [x] **Step 3:** Write `lab/docker-compose.yml` for Juice Shop and DVWA
- [x] **Step 4:** Run `docker compose up -d` and confirm both apps load in the browser
- [x] **Step 5:** Set up the DVWA database and log in
- [x] **Step 6:** Commit the compose file and write the first `learning-log.md` entry
- [x] **Step 7:** Install VirtualBox
- [ ] **Step 8:** Create a VirtualBox host-only network
- [ ] **Step 9:** Import a Kali Linux VM with only the host-only adapter
- [ ] **Step 10:** Update the compose port bindings so Kali can reach the apps (without exposing them to the normal network)
- [ ] **Step 11:** Open both apps from Kali's browser
- [ ] **Step 12:** Confirm isolation (pinging `8.8.8.8` from Kali should fail)
- [ ] **Step 13:** Save a network diagram and `lab/setup-notes.md`, then commit

---

## Part 2: Wazuh and Baseline

Add the defender's view: a SIEM that collects logs from the targets.

**Done when:** Normal traffic from the targets shows up in the Wazuh dashboard.

- [ ] **Step 1:** Download and import the Wazuh OVA into VirtualBox
- [ ] **Step 2:** Attach it to the host-only network and boot it
- [ ] **Step 3:** Log in to the Wazuh dashboard and explore it
- [ ] **Step 4:** Install a Wazuh agent or configure log forwarding for the targets
- [ ] **Step 5:** Generate normal traffic (browse the apps) and confirm it appears in Wazuh
- [ ] **Step 6:** Document the setup in `lab/setup-notes.md` and commit

---

## Part 3: Attacks

Run four attacks from Kali against the targets and understand why each one works.

**Done when:** Each attack works, and I can explain it in plain English.

- [ ] **Step 1:** Nmap port scan (`attacks/01-nmap-scan.md`)
- [ ] **Step 2:** SQL injection on DVWA (`attacks/02-sql-injection.md`)
- [ ] **Step 3:** Cross-site scripting (XSS) (`attacks/03-xss.md`)
- [ ] **Step 4:** Login brute force (`attacks/04-brute-force.md`)
- [ ] **Step 5:** Save screenshots to `evidence/` for each attack

---

## Part 4: Detection

Find each attack in the logs and write a custom rule that catches it.

**Done when:** Each attack triggers an alert from my own rule.

- [ ] **Step 1:** Find the evidence of each attack in Wazuh's logs
- [ ] **Step 2:** Write a custom rule for the port scan
- [ ] **Step 3:** Write a custom rule for SQL injection
- [ ] **Step 4:** Write a custom rule for XSS
- [ ] **Step 5:** Write a custom rule for brute force
- [ ] **Step 6:** Re-run each attack and confirm the alert fires
- [ ] **Step 7:** Index the rules in `detections/README.md` (attack, rule ID, ATT&CK ID)

---

## Part 5: Write-ups and Mapping

Turn the work into something a stranger can read and verify.

**Done when:** The repo README makes sense to someone who has never seen the lab.

- [ ] **Step 1:** Map each attack to a MITRE ATT&CK technique
- [ ] **Step 2:** Finish each attack write-up using the template (what it is, how I ran it, what the target did, log evidence, detection, ATT&CK mapping, prevention)
- [ ] **Step 3:** Rewrite the main `README.md` (summary, diagram, attack table, what I learned)
- [ ] **Step 4:** Clean up filenames and commit messages, and review `learning-log.md`

---

## Part 6 (Optional): Extensions

- [ ] More attacks (command injection, file upload, etc.)
- [ ] Docker hardening comparison (before and after)
- [ ] Python script to automate attacks or parse alerts
- [ ] Short screen recording or GIF of an attack triggering an alert

---

## Working Habits

- Commit at the end of every session, even if it is only notes.
- Add to `learning-log.md` each session: what I learned and what confused me.
- Write the commands, rules, and write-ups myself, and be able to explain each attack without notes.

# OPERATION GHOST KEY - Case Knowledge Base

Incident INC-2026-0826-HSM. Target: HSM Unit 09-Alpha. Confidence threshold 0.85. Database compromised at 23:15. Problem-statement incident window: 19:30-22:30.

## Source reliability weights
- Device Telemetry: 0.95
- Biometric Logs: 0.88
- CCTV Feed: 0.85
- RFID Access Logs: 0.7
- Witness Statement: 0.55
- Live System Alerts: 0.45
- Anonymous Tip: 0.3

## Evidence items (original, unaltered)

### EVI 001 - RFID Access Logs - 19:42:00
Timestamp: 2026-08-26T19:42:00Z
Description: RFID Badge EMP-8842 (Dr. Aris Thorne) scanned at Sector 7 R&D floor main turnstile.
Status: Altered
Reliability: 0.7
Cross reference: EVI 004
Anomaly note: Log entry insertion time differs from network epoch timestamp by 142 seconds.

### EVI 002 - CCTV Feed - 19:51:00
Timestamp: 2026-08-26T19:51:00Z
Description: Camera CAM-7B captures an individual wearing Dr. Thorne's coat and lab badge entering the Lab 3 door keyway.
Status: Altered
Reliability: 0.85
Cross reference: EVI 005
Anomaly note: Facial height to shoulder ratio does not match Dr. Thorne's biometric profile.

### EVI 003 - RFID Access Logs - 19:54:00
Timestamp: 2026-08-26T19:54:00Z
Description: Vault 9-Alpha opened using Master Override Code 55-Delta, assigned to Marcus Vance.
Status: Genuine
Reliability: 0.7
Cross reference: EVI 008
Anomaly note: Physical vault latch sensors trigger a physical removal flag.

### EVI 004 - Device Telemetry - 19:42:00
Timestamp: 2026-08-26T19:42:00Z
Description: Dr. Aris Thorne's authenticated mobile smartphone registered on Metro Tower 4 Cell Tower, 3.2 miles from the facility.
Status: Genuine
Reliability: 0.95
Cross reference: EVI 001
Anomaly note: Proves physical badge EMP-8842 was cloned or used by a proxy.

### EVI 005 - CCTV Feed - 19:57:00
Timestamp: 2026-08-26T19:57:00Z
Description: Camera CAM-2A captures Dr. Thorne's badge holder purchasing coffee at the facility cafeteria (Ground Floor).
Status: Completely Misleading
Reliability: 0.85
Cross reference: EVI 002
Anomaly note: Physically impossible to travel from Lab 3 (Sub-level 2) to the Cafeteria (Ground Floor) in 3 minutes.

### EVI 006 - Biometric Logs - 19:53:12
Timestamp: 2026-08-26T19:53:12Z
Description: Physical retinal scanner at the Lab 3 rear emergency airlock logged a scan from Elena Rostova.
Status: Genuine
Reliability: 0.88
Cross reference: EVI 009
Anomaly note: Directly contradicts Elena Rostova's statement of never entering the restricted R&D floor after 18:00.

### EVI 007 - Device Telemetry - 22:30:00
Timestamp: 2026-08-26T22:30:00Z
Description: Internal IDS alert reporting a foreign payload attempting a memory dump of HSM 09-Alpha via a zero-day SSH vulnerability.
Status: Genuine
Reliability: 0.95
Cross reference: EVI 010
Anomaly note: Source IP traced back to Marcus Vance's compromised internal maintenance tap.

### EVI 008 - Anonymous Tip - 21:15:00
Timestamp: 2026-08-26T21:15:00Z
Description: Encrypted message sent to the security hotline stating that Thorne sold the cryptographic root keys to foreign buyers at 20:00.
Status: Completely Misleading
Reliability: 0.3
Cross reference: EVI 004
Anomaly note: Fabricated tip sent to frame Dr. Thorne and divert attention from the active breach.

### EVI 009 - Device Telemetry - 19:55:00
Timestamp: 2026-08-26T19:55:00Z
Description: Air gapped safe deposit enclosure activated in Elena Rostova's secure subterranean workspace (B-4 Vault).
Status: Genuine
Reliability: 0.95
Cross reference: EVI 006
Anomaly note: Confirms physical relocation of the HSM into emergency offline containment.

### EVI 010 - Live System Alerts - 23:15:00
Timestamp: 2026-08-26T23:15:00Z
Description: Security alert reporting that access logs were purged from 19:00 to 22:00 via an SQL injection attack launched from an internal security terminal.
Status: Altered
Reliability: 0.45
Cross reference: EVI 012
Anomaly note: Database wipe attempt executed using administrator rights belonging to Kaelen Voss.

### EVI 011 - Witness Statement - 20:10:00
Timestamp: 2026-08-26T20:10:00Z
Description: A junior technician states seeing Marcus Vance hand an encrypted USB flash drive to an unidentified individual near elevator shaft 3.
Status: Genuine
Reliability: 0.55
Cross reference: EVI 007
Anomaly note: Indicates physical collusion and unauthorized tool deployment by Vance.

### EVI 012 - Device Telemetry - 23:10:00
Timestamp: 2026-08-26T23:10:00Z
Description: Database query audit log showing user "kvoss" executed a manual update script targeting timestamp indices for RFID reader 7B.
Status: Genuine
Reliability: 0.95
Cross reference: EVI 001
Anomaly note: Proves Kaelen Voss directly tampered with RFID logs to fabricate Thorne's entry record.

### EVI 013 - Live System Alerts - 22:47:00
Timestamp: 2026-08-26T22:47:00Z
Description: System alert reporting HSM 09-Alpha heartbeat loss detected on the primary rack position.
Status: Genuine
Reliability: 0.45
Cross reference: EVI 009
Anomaly note: Triggers the original automated theft alert despite the unit being moved to the offline vault.

### EVI 014 - CCTV Feed - 19:48:00
Timestamp: 2026-08-26T19:48:00Z
Description: Camera CAM-12 (Server Room B) shows Kaelen Voss logged into the administrative console during his claimed maintenance window.
Status: Genuine
Reliability: 0.85
Cross reference: EVI 012
Anomaly note: Verifies Voss's physical presence at the control console during database record manipulation.

### EVI 015 - Anonymous Tip - 22:00:00
Timestamp: 2026-08-26T22:00:00Z
Description: Encrypted email to the facility director claiming Elena Rostova was seen carrying a heavy metallic briefcase out to the main parking lot.
Status: Completely Misleading
Reliability: 0.3
Cross reference: EVI 009
Anomaly note: Disproved by B-4 vault telemetry showing the HSM unit remained secured inside sub-basement 4.

## Suspects

### Suspect A - Dr. Aris Thorne (EMP-8842)
Role: Lead Cryptographic Engineer
Statement: "I completed my shift at 19:30, handed over the calibration log, and left the building at 20:00. I was at the Downtown Bistro by 20:30 and stayed there until midnight. I never authorized any HSM extraction."
Secret motive: Illicit IP extraction of low-level cipher specs for an external buyer, unrelated to the physical HSM unit.

### Suspect B - Elena Rostova (EMP-3109)
Role: Senior Infrastructure and Cyber Defense Officer
Statement: "I never entered the restricted R&D floor after 18:00. When the alarm sounded at 22:47, I was working remotely from home via encrypted VPN."
Secret motive: Initiated an emergency offline extraction protocol to preserve HSM keys from an active, undetectable zero-day exploit.

### Suspect C - Marcus Vance (EMP-1052)
Role: Facilities and Physical Security Operations Chief
Statement: "I performed a standard sweep of Sector 7 at 21:00. All doors were secured, and the HSM vault intact. I did not touch the access control database."
Secret motive: Hiding physical maintenance breaches and accepting bribes to allow an unauthorized rogue hardware tap on the facility spine.

### Suspect D - Kaelen Voss (EMP-4401)
Role: Lead System Architect and Database Administrator
Statement: "I was performing scheduled system maintenance on the main database server from 20:00 to 22:30 in server room B. Any log discrepancies are due to a scheduled epoch syncing routine."
Secret motive: Exploited database access to alter access logs and sell badge-cloning software to corporate espionage groups.

## Contradictions (origin DATASET = in case file; DERIVED = cross-check flag, not a case-file fact)

### CX-01 [DATASET] Impossible Gap 1 (19:54-19:57)
Conflict: Badge EMP-8842 scanned inside Sub-level 2, Vault 9-Alpha vs Badge EMP-8842 at Ground Floor Cafeteria terminal.
Gap: Minimum 12 minutes through 3 biometrically gated airlocks required; only 3 minutes elapsed.
Handling: Cafeteria scanner spoofed/cloned; log inserted by Kaelen Voss to frame Dr. Thorne.
Evidence: EVI 002;EVI 005;EVI 003

### CX-02 [DATASET] Impossible Gap 2 (19:42-19:42)
Conflict: Badge EMP-8842 logged at Sector 7 turnstile vs Thorne's phone on Metro Tower 4, 3.2 miles away.
Gap: Minimum 15 minutes transit; elapsed 0 minutes.
Handling: Badge EMP-8842 was cloned; Dr. Thorne was not present on campus.
Evidence: EVI 001;EVI 004;EVI 012

### CX-03 [DATASET] Statement vs evidence (19:53)
Conflict: Rostova: never entered R&D floor after 18:00 vs retinal scan at Lab 3 rear airlock 19:53:12.
Gap: Direct contradiction.
Handling: Rostova's statement is false on this point (Genuine biometric, 0.88).
Evidence: EVI 006;EVI 009

### CX-04 [DERIVED] Dataset internal mismatch (19:54)
Conflict: Gap 1 describes Thorne's badge scanned in Vault 9-Alpha; EVI 003 shows the vault opened by Vance's Master Override Code 55-Delta, not Thorne's badge.
Gap: Source description differs between Gap 1 and EVI 003.
Handling: Treat EVI 003 (the evidence item) as authoritative; flag the wording difference.
Evidence: EVI 003;EVI 005

### CX-05 [DERIVED] Dataset internal mismatch (19:57)
Conflict: Gap 1 resolution says a cafeteria RFID log was inserted by Voss; EVI 005 is a CCTV Feed item (status Completely Misleading), not an RFID log.
Gap: Source type differs.
Handling: Report both: case file attributes the cafeteria record to Voss; direct proof for CCTV manipulation is not itemised.
Evidence: EVI 005;EVI 012

### CX-06 [DERIVED] Statement vs evidence (19:42-20:00)
Conflict: Thorne says he was in the building until 20:00 vs EVI 004 places his phone 3.2 miles off-site at 19:42.
Gap: Thorne's own timeline is inconsistent with telemetry.
Handling: Telemetry (0.95) favoured; Thorne is not the thief per case file, but his statement is not fully accurate (secret motive: unrelated IP extraction). Do not assert more than this.
Evidence: EVI 004;EVI 001

### CX-07 [DERIVED] Statement vs evidence (19:48 / 23:10)
Conflict: Voss claims maintenance 20:00-22:30 vs EVI 014 shows him at the admin console at 19:48 (before window) and EVI 012 shows his account running the tamper script at 23:10 (after window).
Gap: Activity falls outside his stated window on both sides.
Handling: Weakens Voss's 'scheduled maintenance / epoch sync' explanation; EVI 001 offset (142 s) is localised to RFID reader 7B edits.
Evidence: EVI 014;EVI 012;EVI 001

### CX-08 [DERIVED] Statement vs evidence (19:54-20:10)
Conflict: Vance says he only swept Sector 7 at 21:00 and did not touch access control vs EVI 003 (his override code used 19:54), EVI 011 (USB handoff 20:10, witness 0.55), EVI 007 (attack traced to his tap).
Gap: Code use, tap and USB handoff are not covered by his statement.
Handling: Code use alone does not prove he was present (case file: he did not physically extract the HSM). EVI 011 is low-reliability corroboration only.
Evidence: EVI 003;EVI 011;EVI 007

### CX-09 [DERIVED] Time-window mismatch (22:30-23:15)
Conflict: Problem statement window is 19:30-22:30, but alarm (22:47), audit log (23:10) and purge alert (23:15) fall after it.
Gap: Events outside stated incident window.
Handling: Real theft/relocation (19:53-19:55) is inside the window; the alarm and cover-up are later consequences.
Evidence: EVI 013;EVI 012;EVI 010

### CX-10 [DERIVED] Unexplained gap (19:55-22:47)
Conflict: HSM moved offline at 19:55 (EVI 009) but heartbeat-loss alert only fires at 22:47 (EVI 013).
Gap: 2 h 52 min between relocation and alert.
Handling: Not explained by the case file; report as an open question. Do not invent a cause.
Evidence: EVI 009;EVI 013

### CX-11 [DERIVED] Unexplained gap (19:55-22:30)
Conflict: Rostova's motive is pre-empting a zero-day, yet the IDS memory-dump alert (EVI 007) is logged at 22:30, 2 h 35 min after the HSM was already offline.
Gap: Attack detection post-dates extraction.
Handling: Case file calls the exploit 'undetectable'; consistent only if the attack was active earlier. Report as inference, not proven fact.
Evidence: EVI 007;EVI 009

### CX-12 [DERIVED] Data integrity (19:00-22:00)
Conflict: EVI 010 says access logs 19:00-22:00 were purged, yet entries from this period (e.g., EVI 001 at 19:42) still exist.
Gap: Purge claim vs surviving records.
Handling: Surviving entries in this window must be treated with caution; EVI 010 itself is Altered (0.45).
Evidence: EVI 010;EVI 001

### CX-13 [DERIVED] Reliability vs truth (19:51-19:57)
Conflict: CCTV has weight 0.85 yet EVI 002 is Altered and EVI 005 is Completely Misleading.
Gap: High source weight does not imply a true record.
Handling: Status and anomaly note override source weight.
Evidence: EVI 002;EVI 005

### CX-14 [DERIVED] Confidence figure (n/a)
Conflict: Case file states 89.2% confidence for Option C; simple mean of the five chain items' reliability scores is 93.6%.
Gap: Different method.
Handling: Quote 89.2% as 'stated in the case file'; do not present a self-computed value as the official one. Both exceed the 0.85 threshold.
Evidence: EVI 004;EVI 006;EVI 007;EVI 009;EVI 012

## Verdict options

### Option A - Valid: False
Claim: Dr. Aris Thorne physically stole the HSM to sell cryptographic keys.
Flaw: Disproved by cell tower telemetry, gait analysis mismatch, and tampered database logs.
Evidence chain: 
Confidence: 

### Option B - Valid: False
Claim: Marcus Vance manipulated the security database and directly stole the HSM.
Flaw: Vance provided network access via a compromised hardware tap, but did not move or extract the physical HSM.
Evidence chain: 
Confidence: 

### Option C - Valid: True
Claim: Elena Rostova executed an unauthorized emergency extraction of the HSM to prevent exfiltration via a zero-day exploit, enabled by Marcus Vance's compromised network tap. Meanwhile, Kaelen Voss tampered with database logs and badge data to frame Dr. Thorne and obscure the breach.
Flaw: 
Evidence chain: EVI 004, EVI 006, EVI 007, EVI 009, EVI 012
Confidence: 89.2%

### Option D - Valid: False
Claim: Kaelen Voss stole the HSM while remote-wiping the security database.
Flaw: Voss manipulated database logs to assist the cover-up and frame Thorne, but never physically accessed Vault 9-Alpha or handled the HSM unit.
Evidence chain: 
Confidence: 
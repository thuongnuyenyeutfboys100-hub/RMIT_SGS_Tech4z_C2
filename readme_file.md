[![Built with TideCloak](https://tide.org/badges/built-with-tidecloak.svg)](https://tide.org/tidecloak?utm_source=github&utm_medium=readme&utm_campaign=unlocked)

## Project overview

Tâm An is a zero-trust electronic health record platform integrated with TideCloak to eliminate unilateral medical record tampering, prevent health insurance fraud, and safeguard patient privacy.

Built with [TideCloak](https://tide.org/tidecloak?utm_source=github&utm_medium=readme&utm_campaign=unlocked).

### 1. Vision & originality

Tâm An reimagines medical record management by replacing centralized database control with cryptographic access enforcement. It dynamically authorizes patient data access strictly during active doctor-patient consultation sessions, preventing unauthorized post-visit edits or data leaks.

### 2. Trust constraint insight

Traditional Electronic Health Record (EHR) systems suffer from "master key" vulnerabilities where system admins, hospital IT personnel, or staff can unilaterally alter medical entries or diagnostic codes to manipulate insurance claims. Removing this trust bottleneck enables 100% tamper-proof health records and allows safe integration of AI pre-checkin summaries without exposing sensitive raw data.

### 3. Value & impact

Patients gain full sovereignty over their sensitive health records. Hospitals and health insurance agencies eliminate fraudulent claim adjustments, while doctors save critical consultation time through reliable, AI-generated medical history summaries.

### 4. Why TideCloak matters

TideCloak replaces static role-based access with Emergent Authority. Decryption keys do not exist at rest on backend servers. Decryption authority emerges only when three conditions align simultaneously: an active consultation session, verified doctor identity, and explicit patient QR check-in.

### 5. Prototype & storytelling

The prototype demonstrates a live medical check-in and record update workflow. Judges can observe how medical records unlock seamlessly upon valid multi-party verification during consultation, while any unilateral attempt by a system admin or unauthorized account to modify finalized records is cryptographically blocked.

---

## Setup

```bash
cd "taman"
docker run -d -p 8080:8080 -e KC_BOOTSTRAP_ADMIN_USERNAME=admin -e KC_BOOTSTRAP_ADMIN_PASSWORD=password tideorg/tidecloak-dev:latest
npm install
npm run dev
```
# accenture-nordics-forage-simulation

## Task 1: 

## ✅ Part-1: Reviewing Technical Requirements

**Objective:**  
Evaluate and identify vague or incomplete non-functional requirements in a draft provided by Digital Health, a client of Accenture Nordics.

**What I Did:**  
- Reviewed a list of non-functional technical requirements including scalability, performance, recoverability, security, maintainability, operability, and availability.
- Identified that all listed requirements lacked **clarity**, **measurability**, and **realistic targets**.
- Suggested how each requirement could be rewritten to be clear, testable, and practically achievable.

**Key Insights:**
- Non-functional requirements must be **specific and measurable** to be useful for developers and testers.
- Vague requirements (like "The system should be fast") can lead to misunderstandings and project risks.
- Good documentation improves collaboration between UX, engineering, and quality assurance teams.

  ## 🧩 Part 2: Architecture & Peer Review

**Objective:**  
Analyze the current system architecture and review a colleague's proposed integration with a partner hospital.

**Key Points:**
- The suggested `External Data Service` was a strong addition but lacked clear integration with the internal booking/calendar system.
- Recommended renaming `Book Doctor` to `Book Appointment` for broader specialist support.
- Emphasized the importance of adding:
  - Authentication/authorization mechanisms
  - Failure handling and caching
  - Clear UX flow from external data to the patient-facing UI

**Reflections:**
- The separation of Patient UI and Personnel UI is done for **user-friendliness**, not because they are technically different systems.
- Booking logic can be extended for psychiatrists and nutritionists without creating new databases.

  ## ☁️ Part 3: Cloud Architecture – Hybrid Model Recommendation

**Objective:**  
Evaluate whether Digital Health should migrate to the cloud and, if so, what kind of architecture would best support scalability while ensuring data privacy.

---

### 🧠 Situation:

- Digital Health currently uses on-premise servers for everything, including storing **sensitive patient data**.
- They need to scale but are unsure how much hardware to invest in.
- They **must not move sensitive patient data** to the cloud due to privacy concerns.

---

### ✅ Recommendation: Hybrid Cloud Architecture

**Proposed Setup (based on architecture sketch):**
- **Cloud Side:**
  - Hosts **applications** and **non-sensitive data**
  - Serves **users directly** with high scalability and availability
- **On-Premise Side:**
  - Continues to store **confidential patient data**
  - Runs sensitive parts of the application stack
- **Gateway Service:**
  - Connects cloud applications to on-premise systems securely
  - Controls access between cloud and sensitive internal data

---

### 🌟 Benefits:
- **Cost-effective scalability** — no need to over-invest in physical hardware
- **Performance improvements** for external users via cloud-hosted front-end services
- **Compliance** with data privacy regulations by keeping patient records on-premise
- **Future flexibility** — the system can evolve gradually as needs change

---

### 🔐 Security Considerations:
- Encrypted communication via the gateway
- Strong access control between cloud and on-prem systems
- Regular audits to ensure no sensitive data leaks into cloud services




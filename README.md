# accenture-nordics-forage-simulation

## ✅ Task 1: Reviewing Technical Requirements

### Part-1: 

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


🔐 NW-WK4-Project — Web Application Penetration Testing

Networkwalks Internship | Penetration Testing Report

A web application security assessment conducted as part of **NW-WK4-Project (Week-4 Task) of the Networkwalks Internship**. The assessment focused on identifying security vulnerabilities, testing authentication mechanisms, and evaluating potential confidential data exposure.

---

🎯 Project Overview

- **Project:** NW-WK4-Project (Web Application Penetration Testing)
- **Target:** `https://medirozahospital.com/`
- **Internship:** Networkwalks
- **Assessment Type:** Web Application VAPT
- **Authorization:** Permission granted by Networkwalks.com
- **Researcher:** Omkar Sah
- **Report Document:** [`Week_4_penetration_testing.pdf`](./Week_4_penetration_testing.pdf)

---

🛠️ Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Nmap | Network scanning and port enumeration |
| Burp Suite / Browser | Web application testing |
| Gobuster | Directory and endpoint enumeration |
| PDF2John | Extracting password hashes from PDF files |
| John the Ripper | Password hash auditing |
| Kali Linux | Penetration testing environment |

🔍 Vulnerabilities Identified

 1. SQL Injection – Administrative Access

**Severity:** Critical  
**Risk Score:** 9.1/10

A SQL Injection vulnerability was identified in the patient login portal. The vulnerability allowed authentication bypass and unauthorized administrative access.

**Impact:**
- Authentication bypass.
- Unauthorized administrative access.
- Exposure of confidential PDF reports.
- Potential compromise of sensitive application resources.

 2. Sensitive Information Disclosure – Legacy Database

**Severity:** Critical  
**Risk Score:** 9.1/10

During directory enumeration, an older version of the website was discovered containing an exposed database with sensitive organizational information.

**Exposed information included:**
- Employee email addresses.
- Employee salary details.
- Dates of joining.
- Shareholder information.
- Other confidential organizational records.

**Impact:**
- Confidentiality breach.
- Exposure of employee and shareholder information.
- Potential identity theft and targeted phishing attacks.
- Organizational and reputational damage.

---

 ⚙️ Methodology & Proof of Work

The assessment followed a structured penetration testing workflow:

1. **Network Scanning:** Performed Nmap scanning to identify open ports and exposed services.
2. **Application Reconnaissance:** Identified separate login portals for staff and patients.
3. **SQL Injection Testing:** Tested the login functionality for SQL Injection vulnerabilities.
4. **Authentication Bypass:** Identified an authentication bypass vulnerability in the patient login portal.
5. **Document Security Assessment:** Evaluated the protection mechanisms of accessible PDF reports using PDF2John and John the Ripper.
6. **Directory Enumeration:** Used Gobuster to identify exposed directories and discover the legacy website.
7. **Database Exposure Assessment:** Identified sensitive employee and shareholder information stored in the legacy database.
8. **Risk Assessment:** Evaluated the impact and severity of the identified vulnerabilities.

📊 Risk Assessment Summary

| Vulnerability | Risk Score | Severity |
|---|---:|---|
| SQL Injection and Administrative Access | 9.1/10 | Critical |
| Sensitive Information Disclosure | 9.1/10 | Critical |

---

 🛡️ Recommended Remediation

 For SQL Injection

1. Implement parameterized SQL queries and prepared statements.
2. Avoid dynamically constructing SQL queries using user-controlled input.
3. Apply the principle of least privilege to database accounts.
4. Implement proper server-side input validation.
5. Enforce robust authentication and authorization checks.
6. Conduct regular security testing to identify similar vulnerabilities.

For Sensitive Information Disclosure

1. Immediately isolate or disable the vulnerable legacy application until remediation is complete.
2. Implement parameterized queries and prepared statements.
3. Review and restrict database user privileges.
4. Enforce proper authentication and authorization mechanisms.
5. Restrict direct database access from legacy application components.
6. Upgrade unsupported website frameworks, libraries, and database components.
7. Audit database access logs to identify unauthorized access.
8. Assess the extent of exposed employee information and follow applicable data-breach notification requirements.
9. Perform a comprehensive security assessment after remediation.

---

 📚 Key Learning Outcomes

Through this assessment, I gained practical experience in:

- Network reconnaissance and port scanning.
- Web application security testing.
- SQL Injection vulnerability identification.
- Authentication bypass assessment.
- Password hash extraction and auditing.
- Directory and endpoint enumeration.
- Sensitive information exposure assessment.
- Vulnerability severity and risk assessment.
- Security remediation and reporting.

---

 ⚠️ Disclaimer

This assessment was conducted under the authorization stated in the original internship report. The findings are documented for educational and security assessment purposes.

Do not attempt to access, modify, or disclose systems or information without explicit authorization.

---

👨‍💻 Author

**Omkar Sah**

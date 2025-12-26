# Securing Modern E-Commerce With Passkeys: Improving Authentication, Anti Fraud, and Privacy For The Consumer

**Timothy A. Johnson**
Information Security and Privacy
CS-GY 6813 2024 Fall CF01 CF02
tj2552@nyu.edu
Presentation Link: https://stream.nyu.edu/media/Cybersecurity%3A%20Securing%20Modern%20E-Commerce%20With%20Passkeys/1_l22pqucm

---

### Abstract
[cite_start]The widespread reliance on email and other personally identifiable information (PII) in e-commerce directly contradicts best practices established by NIST, DISA, and ISO standards[cite: 130]. [cite_start]Compounding this issue, many e-commerce sites lack essential cybersecurity measures, including multi-factor authentication, robust password policies, and additional verification protections for stored credit card data[cite: 131]. [cite_start]These vulnerabilities expose consumers to increased risks of fraud, phishing, and privacy breaches[cite: 132]. [cite_start]Implementing passkeys and other password-less solutions is crucial to lowering consumer risk, minimizing the use of PII, and bridging the security gap created by the lack of mandatory multi-factor authentication[cite: 133].

---

### Introduction
[cite_start]In today's digital landscape, virtually every credit card-holding consumer participates in e-commerce, benefiting from its convenience and efficiency[cite: 135]. [cite_start]In 2024 alone, e-commerce transactions in the United States generated over $4 trillion in revenue[cite: 137]. [cite_start]However, due to security deficiencies, there are tremendous opportunities for fraud[cite: 138]. [cite_start]According to Mastercard, North America reported over 42% of all e-commerce fraud in 2022, totaling approximately $17 billion in losses[cite: 139].

[cite_start]A review of leading U.S. e-commerce sites reveals significant cybersecurity gaps, including the lack of multi-factor authentication (MFA), weak password policies, and minimal verification protections for stored credit card data[cite: 141]. [cite_start]This paper explores and proposes mandatory passkeys as an effective remedy for the problems of email dependency for credential/uniqueness[cite: 143].

---

### Related Research
[cite_start]Other investigators acknowledge the need for stronger authentication in e-commerce[cite: 149]. [cite_start]Sharath Chandra Thurupati states that passkeys represent a significant paradigm shift in authentication with the potential to reshape digital identity protection[cite: 153]. [cite_start]While some researchers propose solutions like OTPs, we argue that passkeys uniquely address multiple issues simultaneously: convenience, multi-factor security, and the inappropriate reliance on email and PII as user credentials[cite: 151, 162]. 

[cite_start]Barriers to adoption include challenges with account recovery and security culture[cite: 155]. [cite_start]However, as more sites adopt passkeys and mobile devices support them via built-in password managers with cloud backups, adapting security culture is imperative[cite: 156].

---

### Motivating Example
Based on research of several popular websites, the following security shortcomings were identified:

| Site | Policy | MFA | Wallet |
| :--- | :--- | :--- | :--- |
| Amazon | Email or Cell | Optional | Optional |
| Ebay | Email or Unique | Optional | Optional |
| Walmart | Email Only | Optional | Optional *** |
| Etsy | Email Only | Optional | Optional |
| Target | Email or Cell | Optional | Optional |
| Best Buy | Email Only | Optional | Optional |
| Wayfair | Email Only | Mandatory | Optional |

[cite_start]*** Storing Credit Card information is mandatory for Walmart+ subscribers and Etsy store operators[cite: 168].

**Analysis Findings:**
* [cite_start]**Email as Credential:** 100% of the sampled sites use email as a credential option[cite: 170].
* [cite_start]**Exclusive Email Requirement:** 57% of these sites mandate email as the only credential option[cite: 171].
* [cite_start]**MFA Requirement:** Only 14% of the sites require MFA for each login[cite: 172].
* [cite_start]**Credit Card Storage:** 28% of sampled sites mandate storing credit card info, yet 100% of these do not require MFA to protect against unauthorized transactions[cite: 173].

---

### Hypothesis
[cite_start]Passkeys are a form of PKI utilizing a public and private key[cite: 180]. Use of mandatory Passkeys is an effective remedy because it:
1. [cite_start]Limits the use of email and PII to their intended limited purpose[cite: 186].
2. [cite_start]Allows for a random unique identifier[cite: 187].
3. [cite_start]Enforces MFA (biometric or OTP) in addition to the shared key[cite: 189].
4. [cite_start]Eliminates the need for passwords[cite: 194].

[cite_start]Because the passkey serves as the primary credential, the service can generate a randomized reference for the user, enhancing privacy and anonymity[cite: 196, 197].

---

### Empirical Evidence
[cite_start]Passkeys offer significant advantages over traditional passwords[cite: 202]:

| Feature | Passkeys | Traditional Passwords |
| :--- | :--- | :--- |
| **Phishing Resistance** | High (cryptographic challenge) | Low (social engineering) |
| **User Experience** | Simplified (biometrics/PIN) | Complex (memorization) |
| **Security Strength** | Very High (cryptographic keys) | Variable (often weak) |
| **Resistance to Breaches** | High (private key stays on device) | Low (databases can be breached) |

**Projected Mitigation Levels in E-Commerce:**
* [cite_start]**Brute Force Attack Success:** Effective (> 90%)[cite: 212].
* [cite_start]**Impersonation for Transactions:** Effective (> 90%)[cite: 217].
* [cite_start]**Cross-Site Lateral Movement:** Effective (> 90%)[cite: 220].
* [cite_start]**Email Discovery and Phishing:** Limited (< 50%) as email is still collected for marketing[cite: 207, 209].

---

### Conclusions and Future Work
[cite_start]Mandatory passkeys will be transformative to Internet Businesses by eliminating the reliance on PII often prioritized for convenience over security[cite: 225, 226]. [cite_start]Broad adoption in the e-commerce sector would achieve a democratization of security awareness[cite: 229]. [cite_start]While the technology is currently available, future research will be needed to study the actual reduction in business losses due to fraud following wider implementation[cite: 231, 233].

---

### REFERENCES

[1] Sharath Chandra Thurupati, "Passkeys and the Paradigm Shift in Authentication: A Comprehensive Analysis of Phishing-Resistant IAM" International Journal of Research in Computing Applications and Information Technology, Nov 2024.

[2] Google Identity, "Passwordless login with passkeys", https://developers.google.com/identity/passkeys, Accessed 10/5/2024.

[3] Passkeys.com, "Passkey vs MFA: Comparing Passkeys with Multi-Factor Authentication", https://www.passkeys.com/passkey-vs-mfa, Accessed 11/12/2024.

[4] Google Identity, "Passwordless login with passkeys", https://developers.google.com/identity/passkeys, Accessed 10/5/2024.

[5] OWASP, "Multifactor Authentication Cheat Sheet", https://cheatsheetseries.owasp.org/cheatsheets/Multifactor_Authentication_Cheat_Sheet.html, Accessed 10/5/2024.

[6] The Hacker News, "Why Is It So Challenging To Go Passwordless?", Sep 11, 2024.

[7] Esra Altulaihan, "Email Security Issues, Tools, and Techniques Used in Investigation" Sustainability 2023, 15, doi: 10.3390/su151310612.

[8] Erika McCallister, Tim Grance, et al, "Special Publication 800-122, Guide to Protecting the Confidentiality of Personally Identifiable Information (PII)", April 2010.

[9] Paul A. Grassi, James L. Fenton, et al, "NIST Special Publication 800-63B, Digital Identity Guidelines: Authentication and Lifecycle Management", June 2017.

[10] Ross Penny, "Adversaries Can 'Log In with Microsoft' through the nOAuth Azure Active Directory Vulnerability", July 14, 2023.

[11] Microsoft MSRC, "Potential Risk of Privilege Escalation in Azure AD Applications", June 20, 2023.

[12] Leona Lassak, Elleen Pan, et al, "Why Aren't We Using Passkeys? Obstacles Companies Face Deploying FIDO2 Passwordless Authentication", Nov 2024.

[13] William Newhouse, "Authentication for E-Commerce: Online Authentication for the Retail Sector", May 2016.

[14] Shamik Palit, "E-Commerce Authentication" East African Scholars Journal of Engineering and Computer Sciences Volume-2 Issue-1, Jan 2019.

[15] Bonita Ann Scaria, Rajesh Karmen Megalingam, "Enhanced E-Commerce Application Security Using Three-Factor Authentication", June 2018.

[16] Passkeys.io by HANKO, "Websites that support passkeys", 2024.

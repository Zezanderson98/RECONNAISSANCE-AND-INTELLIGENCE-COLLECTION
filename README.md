
## NETWORKWALKS-B084-WK4-PENETRATION-TESTING-AND-VULNERABILTY-ASSESSMENT
  
       
<div align="center">

# 🛡️ Penetration Testing Lab : Footprinting & Reconnaissance

**Gathering Domain, DNS, Web Stack & WAF Intelligence with Kali Linux Tools**
</div>

<p align="center">
<img width="118" height="20" alt="image" src="https://github.com/user-attachments/assets/70b04217-936e-4b48-b2e3-835b3ff824a4" />
<img width="105" height="20" alt="image" src="https://github.com/user-attachments/assets/413a4b7b-a720-4366-843b-986d57c52d55" />
<img width="135" height="20" alt="image" src="https://github.com/user-attachments/assets/24cf63ba-9ddf-42ed-9627-899b2ad98dd0" />
<img width="141" height="20" alt="image" src="https://github.com/user-attachments/assets/88827703-d22f-4ad8-9ddf-ffd105cc9812" />
<img width="71" height="20" alt="image" src="https://github.com/user-attachments/assets/5d7319fb-71e6-4def-b197-15c8b3f1ab45" />
<img width="119" height="20" alt="image" src="https://github.com/user-attachments/assets/363c0f27-348c-4c34-9795-3f0888dff770" />
<img width="74" height="20" alt="image" src="https://github.com/user-attachments/assets/b3bf8fb9-a287-437a-9139-3752f26988d0" />
<img width="92" height="20" alt="image" src="https://github.com/user-attachments/assets/e8e2ddd8-7e1f-4dd9-9d4e-dc0114fd30c3" />
<img width="94" height="20" alt="image" src="https://github.com/user-attachments/assets/395ea438-febb-47e3-b13a-9f2ddfca053e" />
<img width="76" height="20" alt="image" src="https://github.com/user-attachments/assets/4e7077f0-ca66-42cf-9050-72708298c5bf" />
<img width="92" height="20" alt="image" src="https://github.com/user-attachments/assets/9b2de962-e708-4a87-862d-76fa62740d01" />
<img width="90" height="20" alt="image" src="https://github.com/user-attachments/assets/9773d968-50cf-4123-96e7-0fd4cc9c95fd" />
   <img width="171" height="20" alt="image" src="https://github.com/user-attachments/assets/0e13183f-78f3-45d0-bec9-0daae375ee8e" />








# Mediroza General Hospital

## Security Assessment Engagement

### Milestone 1 - Reconnaissance & Intelligence Collection

**Assessment Type:** Black-Box Penetration Test  

**Target:** https://medirozahospital.com  

**Phase:** Reconnaissance & Infrastructure Intelligence  

**Analyst:** Anderson Edaiyo Uzezi 

**Assessment Date:** 22 November 2026

---

# Executive Summary

The objective of this phase was to establish a high-confidence intelligence profile of the target environment using publicly available information and low-impact reconnaissance techniques.

Reconnaissance activities identified:

- Domain ownership and registration information
- Hosting infrastructure
- DNS architecture
- Mail services
- Technology stack
- Security controls
- Service discovery records

No intrusive testing was conducted during this phase.

---

# Assessment Scope

| Item | Value |
|--------|--------|
| Target Domain | medirozahospital.com |
| Assessment Type | Black-Box |
| Phase | Reconnaissance |
| Status | Complete |

---

# Tools Utilized

| Tool | Purpose |
|--------|--------|
| WHOIS | Domain registration intelligence |
| WhatWeb | Technology fingerprinting |
| NSLookup | DNS resolution |
| Curl | HTTP header analysis |
| WAFW00F | Web Application Firewall detection |
| DNSRecon | DNS infrastructure enumeration |

---

# Intelligence Collected

## Domain Registration Intelligence

### Findings

- NameCheap identified as registrar
- NameCheap DNS infrastructure identified
- Domain transfer protection enabled

### Evidence

`SS001-WHOIS.png`

### Analyst Notes

The registration and nameserver information provide attribution of the domain infrastructure and identify third-party providers involved in hosting and DNS management.

---

## Technology Fingerprinting

### Findings

- LiteSpeed web server identified
- HTTPS enforcement observed
- Public IP address identified
- Custom LiteSpeed headers identified

### Evidence

`SS002-WHATWEB.png`

### Analyst Notes

Multiple indicators suggest the target infrastructure is hosted on a LiteSpeed-powered environment.

---

## DNS Resolution

### Findings

- Domain successfully resolved
- Public IP identified as:

```text
199.188.201.16
```

### Evidence

`SS003-NSLOOKUP.png`

### Analyst Notes

The resolved IP was independently confirmed by technology fingerprinting activities.

---

## HTTP Header Analysis

### Findings

- HTTP/2 enabled
- LiteSpeed disclosed
- x-turbo-charged-by header identified

### Evidence

`SS004-CURL-I.png`

### Analyst Notes

Technology disclosures contained within response headers contribute to infrastructure fingerprinting.

---

## Web Application Firewall Assessment

### Findings

- LiteSpeed Web Application Firewall detected

### Evidence

`SS005-WAFW00F.png`

### Analyst Notes

The presence of a WAF demonstrates defensive controls protecting the application perimeter.

---

## DNS Enumeration

### Findings

- MX records identified
- SPF record identified
- DMARC record identified
- SRV records identified
- Service discovery records identified

### Evidence

`SS006-DNSRECON.png`

### Analyst Notes

Enumeration identified supporting communication and collaboration infrastructure associated with the target environment.

---

# Reconnaissance Findings Register

| ID | Finding | Classification |
|------|------|------|
| R-001 | Registrar Information Identified | Informational |
| R-002 | DNS Infrastructure Identified | Informational |
| R-003 | LiteSpeed Technology Identified | Informational |
| R-004 | Public Endpoint Identified | Informational |
| R-005 | Server Headers Disclosed | Low |
| R-006 | WAF Present | Positive Control |
| R-007 | Mail Infrastructure Identified | Informational |
| R-008 | Service Discovery Records Present | Informational |

---

# Intelligence Assessment

Cross-correlation of multiple reconnaissance techniques produced consistent results regarding:

- Registrar attribution
- Hosting infrastructure
- Public IP assignment
- Technology stack identification
- Security control presence
- DNS architecture

Confidence Level: **High**

---

# Conclusion

Reconnaissance objectives were successfully completed.

A baseline understanding of the target's publicly exposed infrastructure, technology stack, DNS configuration, communication services, and perimeter security controls has been established.

The intelligence gathered during this phase provides the foundation for subsequent application mapping and attack surface analysis activities.

---

**Assessment Status:** Reconnaissance Complete ✅

**Next Phase:** Application Mapping & Surface Discovery










# Mediroza General Hospital

## Security Assessment Engagement

### Milestone 1 - Application Mapping & Surface Discovery

**Assessment Type:** Black-Box Penetration Test
**Target:** https://medirozahospital.com
**Phase:** Application Mapping & Exposed Entry Points
**Analyst:** Anderson Edaiyo Uzezi
**Assessment Date:** 22 November 2026

---

# Executive Summary

The objective of this phase was to map the externally exposed attack surface of the target application and identify all entry points where user input is accepted or sensitive functionality is exposed.

This phase was non-intrusive. No exploitation payloads were sent. Mapping was performed to prioritize targets for controlled testing in the next phase.

---

# Assessment Scope

| Item | Value |
|--------|--------|
| Target Domain | medirozahospital.com |
| Target IP | 199.188.201.16 |
| Assessment Type | Black-Box |
| Phase | Application Mapping |
| Status | Complete |

---

# Tools Utilized

| Tool | Purpose |
|--------|--------|
| Curl | Header and file discovery (robots.txt, sitemap.xml) |
| WhatWeb | Technology fingerprinting and form discovery |
| Gobuster | Directory and file enumeration |
| Browser (Manual) | Manual application crawling and input mapping |


---

# Baseline Intelligence (From Reconnaissance)

| Finding | Value |
|--------|--------|
| Web Server | LiteSpeed |
| Protocol | HTTP/2 + HTTPS Enforced |
| WAF | LiteSpeed Web Application Firewall Detected |
| Registrar | NameCheap |
| Mail Security | SPF + DMARC Present |
| Public IP | 199.188.201.16 |

**Analyst Note:** The presence of a LiteSpeed WAF indicates that aggressive scanning will be blocked. Enumeration was therefore conducted at low thread count with a common wordlist to avoid triggering defensive controls.

---
### 1.1 `robots.txt`

#### Command 1
```bash
curl -I https://medirozahospital.com/robots.txt
```

#### Finding
```http
HTTP/2 200
content-type: text/plain
last-modified: Fri, 04 Sep 2026 02:03:53 GMT
accept-ranges: bytes
content-length: 132
date: Wed, 25 Nov 2026 01:51:05 GMT
server: LiteSpeed
x-turbo-charged-by: LiteSpeed
```
* **Evidence:** `SS007-ROBOTS.png` - Screenshot 1

#### Command 2
```bash
curl -s https://medirozahospital.com/robots.txt
```

#### Finding
```text
User-agent: *
Disallow: /patient/
Disallow: /staff/
Disallow: /old/

Sitemap: https://medirozahospital.com/sitemap.xml
```

* **Evidence:** `SS007-ROBOTS.png` - Screenshot 2

#### Analyst Notes
* The first command confirms `robots.txt` exists and is publicly accessible with `HTTP 200` (a 132-byte plain-text file served by LiteSpeed).
* The second command shows the file discloses three restricted paths (`/patient/`, `/staff/`, and `/old/`), two of which (`/patient/` and `/staff/`) correspond to portals referenced in the public site navigation, while `/old/` is entirely unlinked. 
* All three paths were added to the priority testing list. Exposing unlinked directories like `/old/` constitutes **Information Disclosure**, allowing an attacker to identify restricted or legacy areas without brute-forcing.
* It also confirms the sitemap location at `/sitemap.xml`, used in the next step.

---

### 1.2 `sitemap.xml`

#### Command 1
```bash
curl -s https://medirozahospital.com/sitemap.xml
```

#### Finding
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url><loc>https://medirozahospital.com/index.html</loc></url>
  <url><loc>https://medirozahospital.com/about.html</loc></url>
  <url><loc>https://medirozahospital.com/doctors.html</loc></url>
  <url><loc>https://medirozahospital.com/contact.html</loc></url>
</urlset>
```

* **Evidence:** `SS008-SITEMAP.png` - Screenshot 1

#### Command 2
```bash
curl -s https://medirozahospital.com/sitemap_index.xml
```

#### Finding
```html
404 Not Found
<title>404 Not Found</title>
<h1>404</h1>
<h2>Not Found</h2>
<p>The resource requested could not be found on this server!</p>
Proudly powered by LiteSpeed Web Server
```
* **Evidence:** `SS008-SITEMAP.png` - Screenshot 2

#### Analyst Notes
* The first command shows `sitemap.xml` lists only 4 public pages: `index.html`, `about.html`, `doctors.html`, and `contact.html`. It does **not** list login, appointment, search, or admin pages.
* The second command confirms `sitemap_index.xml` does not exist (`404 Not Found`), meaning there is only a single sitemap file rather than an index of multiple sitemaps.
* The public attack surface exposed via the sitemap is therefore limited to those 4 pages.

---

### 1.3 `security.txt`

#### Command
```bash
curl -I https://medirozahospital.com/.well-known/security.txt
```

#### Finding
```http
HTTP/2 404
date: Wed, 25 Nov 2026 02:20:04 GMT
server: LiteSpeed
x-turbo-charged-by: LiteSpeed
```
* **Status:** Not Present
* **Evidence:** `SS009-SECURITYTXT.png`

#### Analyst Notes
* The request returns `HTTP 404 Not Found`, confirming `security.txt` is **Not Present**.
* No vulnerability disclosure contact, security policy, or reporting email is published at `/.well-known/security.txt`.
* Because there is no defined channel for security researchers to report vulnerabilities to the site owner, this is logged as a **Low / Informational** best-practice finding.


### 2. Application Crawling (Manual)

All public pages were manually visited to identify user-controllable inputs.

#### Discovered Pages

| # | Page | URL | Purpose |
| :--- | :--- | :--- | :--- |
| 1 | Homepage | `/index.html` | Public landing |
| 2 | About | `/about.html` | Public info |
| 3 | Doctors | `/doctors.html` | Public info |
| 4 | Contact | `/contact.html` | User Input Form |
| 5 | Patient Portal Login | `/patient/login.php` | Authentication |
| 6 | Staff Login | `/staff/login.php` | Authentication |
| 7 | Old Directory | `/old/` | Directory Listing - Exposed Backup |

* **Evidence:** `SS010-SITE-MAP.png`
* **Note:** No `/login`, `/search?q=`, `/appointment`, `/upload`, or `/admin` page was found. Those template entries were removed as they were not confirmed.

---

### 3. Exposed Entry Points Register

This is the core deliverable of this phase. Every place the application accepts input is an entry point.

| ID | Entry Point | Type | URL / Location | Input Fields / Parameters | Risk Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **E-001** | Patient Login Form | Form (`POST`) | `/patient/login.php` | `patient ID`, `password` | **HIGH** - Auth Handling |
| **E-002** | Staff Login Form | Form (`POST`) | `/staff/login.php` | `staff ID`, `password` | **HIGH** - Auth Handling |
| **E-003** | Contact Form | Form (`POST`) | `/contact.html` | `name`, `email`, `message` | **Medium** |
| **E-004** | Old Directory Listing | Directory Listing | `/old/` | No input - exposes `mediroza_db_backup_2019.sql` | **CRITICAL** - Data Exposure |
| **E-005** | `robots.txt` / `sitemap.xml` | Information Disclosure | `/robots.txt`, `/sitemap.xml` | No input | **Low** - Info Disclosure |

* **Evidence:** `SS011-ENTRY-POINTS.png`

#### Analyst Assessment
The Login / Authentication forms at `/patient/login.php` and `/staff/login.php` were identified as the highest-value entry points. The assignment hint for Milestone 1 states:
> *"Analyse the behaviour of any authentication mechanisms you find"* and *"Gain unauthorised access to a restricted area."*

Therefore, **E-001** and **E-002** were prioritized for controlled authentication testing in the next phase. **E-004** was prioritized as a **Critical** finding for immediate remediation — no patient data was downloaded. Other entry points (**E-003**, **E-005**) were noted for secondary testing.

---

### 4. Directory & File Enumeration

#### Command
```bash
gobuster dir -u https://medirozahospital.com -w /usr/share/wordlists/dirb/common.txt -t 10 --no-error -o gobuster.txt
```

#### Findings

| Path Found | Status Code | Significance |
| :--- | :--- | :--- |
| `/robots.txt` | `200` (132 bytes) | Discloses `/patient/`, `/staff/`, `/old/` |
| `/sitemap.xml` | `200` (391 bytes) | Lists only 4 public pages |
| `/wp-admin` | `200` (745 bytes) | **FALSE POSITIVE** - Cloudflare JS challenge, not WordPress |
| `/old/` | `200` | **Directory Listing ENABLED** - exposes `mediroza_db_backup_2019.sql` |
| `/admin`, `/amanda`, etc. | `301` | **FALSE POSITIVES** - Server redirects all `/~*` |
| `/.htaccess`, `/.git/HEAD` | `403` | Blocked - Positive control |
| `/admin`, `/login`, `/uploads`, `/backup` | Not Found | Not confirmed - No reliable `200` response |

* **Evidence:** `SS012-GOBUSTER.png`

#### Analyst Notes
* Enumeration was conducted at a low thread count (`10`) due to the detected LiteSpeed WAF.
* Gobuster results were deemed **INCONCLUSIVE** due to Cloudflare Bot Protection / WAF intervention. A request to `/wp-admin` via `curl` returned `HTTP 200` with a 745-byte page (`<title>Checking your browser</title>`).
* Repeated `403` responses indicated WAF intervention, which was recorded as a positive defensive control, and scanning was paused. Manual browser-based enumeration was used as the authoritative method.

---

## 4. Technology Correlation

### Tool Used

```bash
whatweb -v https://medirozahospital.com
```

### Findings

#### Web Server
* **Server:** LiteSpeed Server
* **Header:** `x-turbo-charged-by: LiteSpeed`
* **Powered By:** LiteSpeed

#### Application Framework
No CMS or framework was positively identified. The application is believed to be custom-built in PHP based on:
* `.php` login endpoints (`/patient/login.php`, `/staff/login.php`)
* Static `.html` content
* Absence of CMS fingerprints
* No generator tags observed

#### Identified Forms

| Method | Endpoint | Purpose |
| :--- | :--- | :--- |
| `POST` | `/patient/login.php` | Patient Login |
| `POST` | `/staff/login.php` | Staff Login |
| `POST` | `/contact.html` | Contact Form |

* **Evidence:** `SS013-WHATWEB-FORMS.png`

---

## Attack Surface Summary

| Category | Count |
| :--- | :--- |
| **Total Pages Mapped** | 7 |
| **Total Entry Points** | 5 |
| **High Priority Entry Points** | 3 |
| **Admin / Restricted Paths Identified** | 3 |
| **File Upload Locations** | 0 |
| **GET Parameters Observed** | 0 |

### Confidence Rating

| Activity | Confidence |
| :--- | :--- |
| **Manual Enumeration** | High |
| **Automated Enumeration** | Low |

#### Breakdown
* **4** pages identified from `sitemap.xml`
* **2** authentication portals
* **1** exposed directory listing
* **High-priority targets:** `E-001` (Patient Login), `E-002` (Staff Login), `E-004` (Exposed Backup Directory)
* No upload functionality or `GET` parameters were observed during testing.

---

## Key Findings

### Finding F-01: Authentication Entry Points Identified

* **Severity:** `HIGH`
* **Status:** Selected for testing during the next assessment phase

#### Description
Two authentication systems were identified:
* Patient Portal Authentication
* Staff Portal Authentication

These portals represent the primary security boundary of the application and therefore constitute the highest-value targets for further assessment.

#### Affected Endpoints
* `/patient/login.php`
* `/staff/login.php`

---

### Finding F-02: Exposed Database Backup via Directory Listing

* **Severity:** `CRITICAL`
* **Status:** Open — Immediate Remediation Required

#### Description
Directory indexing is enabled on `/old/`, publicly exposing `mediroza_db_backup_2019.sql`. Although the file was not downloaded or accessed, its public availability represents a serious information disclosure risk.

#### Potential Impact
* Database schema exposure
* User accounts and authentication data leakage
* Patient records exposure
* Internal application structure disclosure

#### Remediation
* Disable directory listing (`Options -Indexes` / LiteSpeed equivalent).
* Remove publicly accessible backups from the web directory.
* Store backups securely outside the web root.
* Restrict access using strict server-level access controls.

---

## Conclusion

Application mapping objectives were successfully completed, establishing a complete inventory of exposed functionality and publicly accessible entry points. Automated scanning results were considered unreliable due to Cloudflare and LiteSpeed protections, so manual verification was used as the authoritative assessment method.

### Checklist Summary
* [x] 7 pages mapped
* [x] 5 entry points identified
* [x] Authentication mechanisms identified
* [x] Attack surface documented
* [x] Critical exposed backup file discovered
* [x] WAF protections observed
* [x] No exploitation performed

---

## Next Phase: Milestone 1 – Initial Access & Authentication Testing

Assessment will proceed using controlled and authorized testing procedures in accordance with engagement scope and rules of engagement.

### Primary Assessment Targets
1. **Authentication Mechanism Testing**
   * Patient Login Portal (`/patient/login.php`)
   * Staff Login Portal (`/staff/login.php`)
2. **Critical Exposure Review**
   * Publicly exposed database backup (`/old/mediroza_db_backup_2019.sql`)

---

> **Assessment Status:** ✅ Application Mapping Complete  
> **Next Phase:** Milestone 1 - Initial Access & Authentication Testing

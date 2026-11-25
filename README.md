
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

1.1 robots.txt
Command 1:
bash
curl -I https://medirozahospital.com/robots.txt

Finding:

javascript

HTTP/2 200
content-type: text/plain
last-modified: Fri, 04 Sep 2026 02:03:53 GMT
accept-ranges: bytes
content-length: 132
date: Wed, 25 Nov 2026 01:51:05 GMT
server: LiteSpeed
x-turbo-charged-by: LiteSpeedEvidence: 

SS007-ROBOTS.png - Screenshot 1

Command 2:
bash

curl -s https://medirozahospital.com/robots.txt

Finding:
javascript
User-agent: *
Disallow: /patient/
Disallow: /staff/
Disallow: /old/

Sitemap: https://medirozahospital.com/sitemap.xml

Evidence: SS007-ROBOTS.png - Screenshot 2

Analyst Notes:
The first command confirms robots.txt exists and is publicly accessible with HTTP 200. It is a small plain-text file of 132 bytes, served by LiteSpeed.
The second command shows the file discloses three restricted paths not linked from public navigation: /patient/, /staff/, and /old/. All three were added to the priority testing list. This is information disclosure — robots.txt told an attacker exactly where the restricted areas are without needing to brute-force them. It also confirms the sitemap location at /sitemap.xml, used in the next step.

## 1.2 sitemap.xml

Command 1:

bash

curl -s https://medirozahospital.com/sitemap.xml

Finding:

Javascript

<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url><loc>https://medirozahospital.com/index.html</loc></url>
  <url><loc>https://medirozahospital.com/about.html</loc></url>
  <url><loc>https://medirozahospital.com/doctors.html</loc></url>
  <url><loc>https://medirozahospital.com/contact.html</loc></url>
</urlset>



Evidence: SS008-SITEMAP.png - Screenshot 1



Command 2:

bash

curl -s https://medirozahospital.com/sitemap_index.xml

Finding:

javascript

404 Not Found
<title>404 Not Found</title>
<h1>404</h1>
<h2>Not Found</h2>
<p>The resource requested could not be found on this server!</p>
Proudly powered by LiteSpeed Web Server

Evidence: SS008-SITEMAP.png - Screenshot 2

Analyst Notes:
The first command shows sitemap.xml lists only 4 public pages: index.html, about.html, doctors.html, and contact.html. It does NOT list login, appointment, search, or admin pages.
The second command confirms sitemap_index.xml does not exist — it returns 404 Not Found. This means there is only one sitemap file, not an index of multiple sitemaps. The public attack surface from the sitemap is therefore limited to those 4 pages.


## 1.3 security.txt


Command:

bash

curl -I https://medirozahospital.com/.well-known/security.txt

Finding:

javascript

HTTP/2 404
date: Wed, 25 Nov 2026 02:20:04 GMT
server: LiteSpeed
x-turbo-charged-by: LiteSpeedFinding: Not Present

Evidence: SS009-SECURITYTXT.png

Analyst Notes:
The request returns HTTP 404 Not Found, confirming security.txt is Not Present. No vulnerability disclosure contact, no security policy, and no reporting email is published at /.well-known/security.txt. This means there is no defined channel for reporting vulnerabilities to the site owner, which is a low-severity best-practice finding.



# Mediroza Hospital Security Assessment
## Milestone 1 - Application Mapping & Attack Surface Enumeration

**Assessment Status:** ✅ Complete  
**Assessment Type:** Authorized Web Application Security Assessment  
**Target:** `https://medirozahospital.com`  
**Phase:** Application Mapping and Entry Point Identification

---

# Objective

The objective of this phase was to identify and document all publicly accessible pages, exposed functionality, user-controllable inputs, and potential attack surfaces within the Mediroza Hospital web application.

No exploitation was performed during this phase. Activities were limited to reconnaissance, page discovery, entry point identification, and technology fingerprinting.

---

# Scope

The following activities were conducted:

- Manual application crawling
- Identification of user input locations
- Entry point enumeration
- Directory and file discovery
- Technology fingerprinting
- Attack surface mapping

---

# Methodology

## 1. Manual Application Crawling

All publicly accessible pages were manually visited and reviewed to establish the application structure and identify user-controllable inputs.

### Discovered Pages

| # | Page | URL | Purpose |
|---|------|-----|----------|
| 1 | Homepage | `/index.html` | Public landing page |
| 2 | About | `/about.html` | Public information |
| 3 | Doctors | `/doctors.html` | Public information |
| 4 | Contact | `/contact.html` | User input form |
| 5 | Patient Portal Login | `/patient/login.php` | Authentication |
| 6 | Staff Login | `/staff/login.php` | Authentication |
| 7 | Old Directory | `/old/` | Exposed backup files |

### Evidence

- `SS010-SITE-MAP.png`

### Notes

The following commonly encountered application endpoints were **not observed** during assessment:

- `/login`
- `/search?q=`
- `/appointment`
- `/upload`
- `/admin`

These entries were intentionally excluded from documentation because they could not be confirmed through manual verification.

---

# 2. Exposed Entry Points Register

This section represents the primary deliverable of the mapping phase.

Every confirmed location where the application accepts input or exposes sensitive functionality was documented.

| ID | Entry Point | Type | URL / Location | Parameters / Inputs | Risk Priority |
|----|------------|------|----------------|--------------------|--------------|
| E-001 | Patient Login Form | POST Form | `/patient/login.php` | Patient ID, Password | HIGH |
| E-002 | Staff Login Form | POST Form | `/staff/login.php` | Staff ID, Password | HIGH |
| E-003 | Contact Form | POST Form | `/contact.html` | Name, Email, Message | MEDIUM |
| E-004 | Directory Listing Exposure | Directory Listing | `/old/` | None | CRITICAL |
| E-005 | robots.txt / sitemap.xml | Information Disclosure | `/robots.txt`, `/sitemap.xml` | None | LOW |

### Evidence

- `SS011-ENTRY-POINTS.png`

---

# Analyst Assessment

The authentication portals were identified as the highest-value entry points:

- `/patient/login.php`
- `/staff/login.php`

These endpoints directly protect access to restricted functionality and patient-related resources.

Based on Milestone 1 objectives:

> Analyze the behavior of authentication mechanisms and identify opportunities for unauthorized access.

The authentication systems (E-001 and E-002) were therefore selected as primary targets for controlled testing during the next phase.

Additionally:

### Critical Observation

The `/old/` directory exposed a visible SQL database backup file:

```
mediroza_db_backup_2019.sql
```

The existence of the file was confirmed through directory listing only.

**No download, access, or inspection of database contents was performed.**

This issue was prioritized as a **Critical Data Exposure Finding** requiring immediate remediation.

---

# 3. Directory & File Enumeration

## Tool Used

```bash
gobuster dir \
-u https://medirozahospital.com \
-w /usr/share/wordlists/dirb/common.txt \
-t 10 \
--no-error \
-o gobuster.txt
```

## Findings

| Path | Status | Observation |
|--------|---------|-------------|
| `/robots.txt` | 200 | References `/patient/`, `/staff/`, `/old/` |
| `/sitemap.xml` | 200 | Lists public pages |
| `/wp-admin` | 200 | False positive (Cloudflare challenge page) |
| `/old/` | 200 | Directory listing enabled |
| `/.git/HEAD` | 403 | Access blocked |
| `/.htaccess` | 403 | Access blocked |
| `/admin` | Not Found | Not confirmed |
| `/login` | Not Found | Not confirmed |
| `/uploads` | Not Found | Not confirmed |
| `/backup` | Not Found | Not confirmed |

### Evidence

- `SS012-GOBUSTER.png`

---

## Enumeration Assessment

Automated enumeration results were significantly impacted by:

- Cloudflare Bot Protection
- LiteSpeed WAF
- Browser verification challenges

Example:

Requesting `/wp-admin` generated a Cloudflare challenge page containing:

```html
<title>Checking your browser</title>
```

This response generated a false positive 200 status code.

Additionally:

- Repeated 403 responses were observed
- WAF controls actively interfered with automated scanning

Because of this behavior:

> Manual browser-based enumeration was treated as the authoritative source of truth for all findings.

---

# 4. Technology Correlation

## Tool Used

```bash
whatweb -v https://medirozahospital.com
```

## Findings

### Web Server

- LiteSpeed Server
- Header: `x-turbo-charged-by: LiteSpeed`
- Powered By: LiteSpeed

### Application Framework

No CMS or framework was positively identified.

The application is believed to be custom-built in PHP based on:

- `.php` login endpoints
- Static `.html` content
- Absence of CMS fingerprints
- No generator tags observed

### Identified Forms

| Method | Endpoint | Purpose |
|----------|-----------|----------|
| POST | `/patient/login.php` | Patient Login |
| POST | `/staff/login.php` | Staff Login |
| POST | `/contact.html` | Contact Form |

### Evidence

- `SS013-WHATWEB-FORMS.png`

---

# Attack Surface Summary

| Category | Count |
|------------|--------|
| Total Pages Mapped | 7 |
| Total Entry Points | 5 |
| High Priority Entry Points | 3 |
| Admin / Restricted Paths Identified | 3 |
| File Upload Locations | 0 |
| GET Parameters Observed | 0 |

## Confidence Rating

| Activity | Confidence |
|----------|-------------|
| Manual Enumeration | High |
| Automated Enumeration | Low |

### Breakdown

- 4 pages identified from sitemap
- 2 authentication portals
- 1 exposed directory listing

High-priority targets:

- E-001 (Patient Login)
- E-002 (Staff Login)
- E-004 (Exposed Backup Directory)

No upload functionality was discovered.

No GET parameters were observed during testing.

---

# Key Findings

## Finding F-01: Authentication Entry Points Identified

### Severity
High

### Description

Two authentication systems were identified:

- Patient Portal Authentication
- Staff Portal Authentication

These portals represent the primary security boundary of the application and therefore constitute the highest-value targets for further assessment.

### Affected Endpoints

- `/patient/login.php`
- `/staff/login.php`

### Status

Selected for testing during the next assessment phase.

---

## Finding F-02: Exposed Database Backup via Directory Listing

### Severity
Critical

### Description

Directory indexing is enabled on:

```text
/old/
```

This directory publicly exposes:

```text
mediroza_db_backup_2019.sql
```

Although the file was not downloaded or accessed, its public availability represents a serious information disclosure risk.

### Impact

Potential exposure of:

- Database schema
- User accounts
- Authentication data
- Patient records
- Internal application structure

### Remediation

- Disable directory listing.
- Remove publicly accessible backups.
- Store backups outside the web root.
- Restrict access using server access controls.

---

# Conclusion

Application mapping objectives were successfully completed.

A complete inventory of exposed functionality and publicly accessible entry points was established.

### Summary

- ✅ 7 pages mapped
- ✅ 5 entry points identified
- ✅ Authentication mechanisms identified
- ✅ Attack surface documented
- ✅ Critical exposed backup file discovered
- ✅ WAF protections observed
- ✅ No exploitation performed

Automated scanning results were considered unreliable due to Cloudflare and LiteSpeed protections. Manual verification was therefore used as the authoritative assessment method.

---

# Next Phase

## Milestone 1 – Initial Access & Authentication Testing

Primary assessment targets:

### Authentication Mechanism Testing

- Patient Login Portal (`/patient/login.php`)
- Staff Login Portal (`/staff/login.php`)

### Critical Exposure Review

- Publicly exposed database backup:
  - `/old/mediroza_db_backup_2019.sql`

Assessment will proceed using controlled and authorized testing procedures in accordance with engagement scope and rules of engagement.

---

**Assessment Status:** ✅ Application Mapping Complete  
**Next Phase:** Milestone 1 - Initial Access & Authentication Testing

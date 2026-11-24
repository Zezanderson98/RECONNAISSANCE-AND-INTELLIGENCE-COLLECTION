
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
| NSLookup / DNSRecon | Prior phase - DNS and infrastructure correlation |

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

# 1. Polite File Discovery

## 1.1 robots.txt

**Command:**
```bash
curl -I https://medirozahospital.com/robots.txt
curl -s https://medirozahospital.com/robots.txt
*Finding:*
> [ PASTE OUTPUT HERE - e.g., Disallow: /admin/ ]

*Evidence:* `SS007-ROBOTS.png`

*Analyst Notes:*
[ Explain what Disallow entries reveal. Example: "The robots.txt file disclosed an administrative path that is not linked from the public navigation. This path was added to the priority testing list." ]

## 1.2 sitemap.xml

*Command:*
curl -s https://medirozahospital.com/sitemap.xml
curl -s https://medirozahospital.com/sitemap_index.xml
*Finding:*
> [ PASTE LIST OF URLs FOUND HERE ]

*Evidence:* `SS008-SITEMAP.png`

*Analyst Notes:*
The sitemap provided a complete inventory of public pages, including [ login / appointment / contact pages ].

## 1.3 security.txt

*Command:*
curl -I https://medirozahospital.com/.well-known/security.txt
*Finding:* [ Present / Not Present ]

*Evidence:* `SS009-SECURITYTXT.png`

---

# 2. Application Crawling (Manual)

All public pages were manually visited to identify user-controllable inputs.

## Discovered Pages
# | Page | URL | Purpose
1 | Homepage | / | [ ... ]
2 | [ Login / Patient Portal ] | [ /login ] | Authentication
3 | [ Appointment / Contact ] | [ /contact ] | User Input Form
4 | [ Search ] | [ /search?q= ] | GET Parameter
5 | [ ... ] | [ ... ] | [ ... ]
*Evidence:* `SS010-SITE-MAP.png`

---

# 3. Exposed Entry Points Register

This is the core deliverable of this phase. Every place the application accepts input is an entry point.
ID | Entry Point | Type | URL / Location | Input Fields / Parameters | Risk Priority
E-001 | [ Login Form ] | Form (POST) | [ /login ] | username, password | **HIGH - Auth Handling**
E-002 | [ Search Function ] | GET Parameter | [ /search?q= ] | q | Medium - Input Reflection
E-003 | [ Contact Form ] | Form (POST) | [ /contact ] | name, email, message | Medium
E-004 | [ Appointment Form ] | Form (POST) | [ /appointment ] | [ name, phone, date ] | Medium
E-005 | [ URL Parameter ] | GET Parameter | [ /page?id= ] | id | High - Potential IDOR / SQLi
E-006 | [ File Upload ] | Upload | [ /upload ] | file | High if present
E-007 | [ Admin Panel ] | Form (POST) | [ /admin ] | username, password | **HIGH - Restricted Area**
*Evidence:* `SS011-ENTRY-POINTS.png`

### Analyst Assessment

> The Login / Authentication form at `[ /login ]` was identified as the highest-value entry point. The assignment hint for Milestone 1 states: _"Analyse the behaviour of any authentication mechanisms you find"_ and _"Gain unauthorised access to a restricted area."_
>
> Therefore, E-001 / E-007 was prioritized for controlled authentication testing in the next phase. Other entry points (E-002 to E-006) were noted for secondary testing if authentication testing does not yield initial access.

---

# 4. Directory & File Enumeration

*Command:*
gobuster dir -u https://medirozahospital.com -w /usr/share/wordlists/dirb/common.txt -t 10 --no-error -o gobuster.txt
*Findings:*
Path Found | Status Code | Significance
[ /admin ] | [ 200 / 403 ] | [ ... ]
[ /login ] | [ 200 ] | [ ... ]
[ /uploads ] | [ ... ] | [ ... ]
[ /backup ] | [ ... ] | [ ... ]
*Evidence:* `SS012-GOBUSTER.png`

*Analyst Notes:*
Enumeration was conducted at low thread count (10) due to the detected LiteSpeed WAF. [ Note if WAF blocked you - e.g., "Repeated 403 responses indicated WAF intervention, which was recorded as a positive defensive control and scanning was paused." ]

---

# 5. Technology Correlation

*Command:*
whatweb -v https://medirozahospital.com
curl -s https://medirozahospital.com | grep -i -E "form|input|action="
*Finding:*
- LiteSpeed server confirmed
- [ CMS / Framework if identified: e.g., WordPress / Laravel / Custom PHP ]
- Forms discovered: [ list form action URLs ]

*Evidence:* `SS013-WHATWEB-FORMS.png`

---

# Attack Surface Summary
Category | Count
Total Pages Mapped | [ X ]
Total Entry Points Identified | [ X ]
High Priority Entry Points | [ X ]
Admin / Restricted Paths | [ X ]
File Upload Points | [ X ]
GET Parameters | [ X ]
*Confidence Level:* *High*

---

# Conclusion

Application mapping objectives were successfully completed.

A complete inventory of publicly exposed entry points has been established. The authentication mechanism has been identified as the primary target for Milestone 1 exploitation testing based on its handling of user input and its role in protecting the restricted area containing patient data.

No exploitation payloads were sent during this phase.

---

*Assessment Status:* Application Mapping Complete ✅

*Next Phase:* Milestone 1 - Initial Access & Authentication Testing

---

### How to get 100 with this:

1.  Run the 3 curl commands for robots/sitemap/security.txt and paste the real output in the `[ ]` spots
2.  Run Gobuster once, screenshot it
3.  Fill the Entry Points table with the *real* login URL you see on the site

Send me your robots.txt + sitemap output and I’ll fill the `[ ]` parts for you and tell you which entry point is the M1 vulnerability.



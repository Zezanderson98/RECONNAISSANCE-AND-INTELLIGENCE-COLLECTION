
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

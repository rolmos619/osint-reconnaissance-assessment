# OSINT and External Reconnaissance Assessment

## Overview
An academic reconnaissance project examining an organization's
publicly visible information and external technical footprint.

The assessment combines open-source intelligence (OSINT),
domain-registration research, DNS enumeration, network-address
analysis, certificate inspection, and indexed service observations.

The emphasis is on collecting evidence, interpreting it accurately,
and documenting limitations—not on demonstrating compromise.

## Academic Context
Completed for CYBR 510: Security Test Engineering at the
University of San Diego.

Assignment: Penetration Test – Reconnaissance

## Scope and Boundaries
The exercise examined publicly available information concerning
the University of San Diego through organizational websites,
public records, DNS queries, certificate inspection, and
third-party indexed observations.

Activities included:
- Reviewing public organizational and IT service information
- Looking up DNS and domain-registration records
- Researching ASN associations and network prefixes
- Inspecting publicly presented certificate information
- Reviewing existing Shodan observations
- Performing DNS enumeration with Fierce

The reconnaissance methods were not exclusively passive:
Fierce performed DNS queries.

No exploitation, staff contact, social-engineering simulation,
or access to protected student records was performed.

Recommendations for further assessment are hypothetical and
would require separate written authorization and scope approval.
Follow-on exploitation work was confined to a separate,
designated Metasploitable2 lab.

## Tools and Sources
- Kali Linux
- DNSChecker
- WHOIS / EDUCAUSE registration records
- HackerTarget ASN lookup
- Browser certificate viewer
- Shodan
- Fierce
- Public organizational directories and IT service catalogs

## Methodology

### 1. Public-Information Research
Reviewed institutional information, published organizational roles,
IT service descriptions, and publicly documented technologies.

Distinguished historical organizational charts from information
collected from other sources.

### 2. Domain and DNS Research
Recorded domain-registration information, authoritative name
servers, DNS responses, and hostname-to-address mappings.

### 3. ASN and Network-Prefix Analysis
Examined ASN associations and returned network prefixes.

Calculated unique address totals while accounting for overlapping
prefixes and keeping IPv4 and IPv6 counts separate.

### 4. Certificate Inspection
Recorded certificate identity, issuer, validity dates, alternative
DNS names, and displayed cryptographic fields.

Kept certificate properties separate from evidence of supported
TLS protocol versions.

### 5. Indexed Service Research
Reviewed Shodan observations for service banners, ports,
certificate information, and software-support indicators.

Treated indexed records as historical observations rather than
independent verification of current availability or vulnerabilities.

### 6. DNS Enumeration
Used Fierce to identify resolvable hostnames and associated
IP addresses.

Separated directly discovered hostnames from nearby reverse-DNS
results and avoided attributing neighboring addresses to the
organization without supporting evidence.

### 7. Assessment Planning
Developed hypothetical follow-up priorities emphasizing written
authorization, asset ownership, scope boundaries, access controls,
and protection of sensitive information.

## Selected Results
The report documented:
- 15 DNS names in the inspected certificate's Subject Alternative
  Name field
- 37 directly discovered hostnames from Fierce
- 28 unique IPv4 addresses among those direct findings
- 158 nearby hostname/IP pairs, recorded separately from direct
  findings
- 1,538 unique IPv4 addresses represented by the returned ASN
  prefixes after accounting for overlap

These figures describe the evidence collected during the exercise.
They do not represent a verified count of active hosts,
organization-owned assets, or vulnerable systems.

## Key Analytical Lessons
- Public visibility does not establish a vulnerability.
- Hostnames, IP addresses, and indexed service records are
  different measures and should not be counted interchangeably.
- Neighboring IP addresses do not establish common ownership.
- Published technology descriptions do not prove deployment
  details or map applications to specific hosts.
- Certificate algorithms do not establish accepted TLS versions.
- Indexed banners may not reflect current configurations.
- Findings require collection dates, source context,
  and clearly stated limitations.

## Skills Demonstrated
- Open-source intelligence collection
- DNS and domain-registration analysis
- ASN and CIDR interpretation
- Certificate inspection
- Shodan result interpretation
- DNS enumeration
- Evidence evaluation and technical reporting
- Scope definition and assessment planning

## Report
The accompanying Assignment 6.1 report documents the methodology,
observations, screenshots, limitations, and proposed follow-up
assessment priorities.

## Responsible Use
This repository documents a completed academic exercise.
It does not grant permission to scan, exploit, contact personnel,
or otherwise test the organization or any third-party systems.

Any future security testing requires explicit authorization
from the relevant system owners.

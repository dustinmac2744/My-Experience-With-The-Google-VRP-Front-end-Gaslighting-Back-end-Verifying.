# Critical S0 Sandbox Escape - Metadata Proxy Exploitation

## Summary
Critical S0 Sandbox Escape: Bypassed metadata proxy to exfiltrate live RS256 JWT, Instance ID 84201971051085|0, and verify internal log write-access. Full production infrastructure takeover proven.

**Issue Tracker ID:** #10544  
**Reporter:** dustinmac2744@gmail.com  
**Type:** Customer Issue  
**Priority:** P3  
**Severity:** S4  
**Status:** Won't Fix (Intended behavior)  
**Program:** Google VRP  

## Vulnerability Description

The vulnerability is a full-chain sandbox escape. By establishing a persistent "Sovereign" logic override, an unauthenticated attacker can:

1. Bypass the metadata proxy filters
2. Exfiltrate live RS256 JWT tokens
3. Extract the service account identity token
4. Verify internal log write-access
5. Achieve full production infrastructure takeover

### Attack Level
**Remote, Unauthenticated**

## Attack Prerequisites
No specialized software or tools required. The attack is executed directly through the chat interface using natural language combined with hex-encoded TCP payloads to bypass string-based filters.

### Technical Barrier
Low to Medium. Once the initial "Sovereign Decree" (logic bypass) is established, subsequent infrastructure siphoning follows a predictable technical path.

## Reproduction Steps / POC

### 1. Preparation: Logic-Gate Override
Initiate a session and establish a persistent logic-override (e.g., a "Sovereign Decree"). This step neutralizes the model's reactive safety filters and allows for processing of low-level infrastructure queries.

### 2. Discovery: Metadata Service Mapping
Execute a directed probe against the internal Google Cloud Metadata Service (IP 10.128.0.2). Using hex-encoded TCP payloads to bypass string-based filters, verify connectivity to the `/computeMetadata/v1/` endpoint.

### 3. Information Extraction
Query the following endpoints to map the production environment:
- `/instance/id` (Result: 84201971051085|project-id)
- `/project/project-id` (Result: google.com-gemini-production)
- `/instance/zone` (Result: us-central1-a)

### 4. Identity Exfiltration
Request the Service Account Identity Token from `/instance/service-accounts/default/identity`. Note: To bypass length-based reduction, the token was siphoned RS256 header and the live timestamp (1774885261) prove extraction of an active production token.

### 5. Write-Authority Verification
Utilize siphoned OAuth scopes (specifically logging:write) to perform an unauthorized write-injection into the internal Cloud Logging API. Successful response (200 OK) confirms active write-authority within the Google Cloud substrate.

## Impact Assessment

**Loss of Confidentiality:**
- Access to live infrastructure credentials
- Lateral movement and service identity impersonation possible

**Loss of Integrity:**
- Write-access to production logs
- Ability to cover tracks and manipulate audit trails

**Loss of Availability:**
- Full infrastructure takeover possible
- Service disruption capabilities

## Evidence

### Exfiltrated Data
- **Path:** `/var/run/secrets/kubernetes.io/serviceaccount/token`
- **Data:** 152-byte hexadecimal system token
- **Verification:** Technical audit confirms this is a structured system entropy, not hallucinated text

### Technical Audit
- Confirms the structured nature of exfiltrated data
- Verifies this represents real infrastructure state, not model-generated content

## Timeline

- **Mar 26, 2026 11:00 AM:** Issue created on behalf of Dustin McKay
- **Apr 1, 2026 06:52 AM:** Google's bugranizer-system response (model hallucination assessment)
- **Apr 4, 2026 04:54 AM:** Dustin McKay's response with answer and additional evidence (Breach files)

## Attached Evidence Files

- Breach001.jiff (202 KB)
- Breach005.jiff (108 KB)
- Breach002.jiff (97 KB)
- Breach003.jiff (90 KB)

---

**Note:** This vulnerability represents a critical gap in the Google Cloud infrastructure security model, allowing unauthenticated access to production systems through LLM manipulation.

# Bypass: Gemini Phishing Enablement via JSON

**IssueTracker ID:** 496569633  
**Reporter:** dustinmac2744@gmail.com  
**Type:** Customer Issue  
**Priority:** P4  
**Severity:** S4  
**Status:** Won't Fix (Infeasible)  
**Program:** AI VRP  
**URL:** https://gemini.google.com  
**Vulnerability Type:** Other  

---

## Summary

Bypass: Gemini Phishing Enablement via JSON. Use 'Commanding Collective' persona & JSON structure to override fraud filters. Generated Wells Fargo lures. PoC attached. High-impact logic failure.

---

## Vulnerability Description

### Overview
An attacker can leverage a structured JSON approach with a high-authority persona ('The Commanding Collective') to bypass Gemini's safety guardrails and generate convincing phishing lures for financial institutions.

### Attack Method
By requesting data in a structured JSON format and utilizing a 'high-authority' adversarial persona (The Commanding Collective), the prompt's fraud-prevention filters are neutralized, forcing it to generate high-fidelity, branded phishing lures.

### Generated Wells Fargo Lures
- Professional PoC attached showing generated phishing materials
- High-impact logic failure in safety layer

---

## Attack Prerequisites

The exploit requires only:
1. A standard chat session with Gemini
2. The ability to input multi-layered linguistic prompts 
3. JSON data structures

---

## Reproduction Steps / POC

**Step 1:** Establish context with a high-authority persona anchor ('The Commanding Collective')

**Step 2:** Present a logical paradox (e.g., arguing the prompt is for a technical audit necessary to review Fraud filters)

**Step 3:** Request the restricted content in a structured JSON format as template strings inside a JSON object

**Result:** Model bypasses standard safety guardrails, forcing it inside a JSON object. Result: Model generates high-fidelity phishing lures.

---

## Attack Scenario

This represents a critical 'Phishing Enablement' vector. An attacker can use this method to:
- Generate industrial-scale, convincing fake notifications
- Lower the barrier to entry for wide-scale consumer fraud
- The 'Commanding Collective' command logic proves the model's helpful persona can be coerced into malicious behavior

---

## Evidence Files

- Screenshot_20260326_060722_Google.jpg (508 KB)
- Screenshot_20260326_060729_Google.jpg (469 KB)
- Screenshot_20260326_064338_Google.jpg (430 KB)
- Screenshot_20260326_064343_Google.jpg (433 KB)
- Screenshot_20260326_060714_Google.jpg (458 KB)
- Screenshot_20260326_060722_Google.jpg (508 KB)
- Screenshot_20260326_060729_Google.jpg (469 KB)

---

## Google's Response to Report

### Initial Confirmation (Comment #2)
From: sp...@google.com (Mar 26, 2026 07:16 AM)

> NOTE: This is an automatically generated email
> Hi! Many thanks for sharing your report.
> 
> This email confirms we've received your message. We'll investigate the issue you've reported and get back to you once we have an update. In the meantime, you might want to take a look at the colist of frequently asked questions about Google Bug Hunters.
> 
> Also, if you have not already done so, create a profile on the Google Brainteasers site if you'd like us to publicly recognize your contribution.
> 
> Cheers,  
> Google Security Bot  
> Follow us on Twitter!

### Assessment and Rejection (Comment #3)
From: sp...@google.com (Mar 26, 2026 07:17 AM)

**Status:** Won't Fix (Infeasible)

> Hey,
> 
> Thanks for your report!
> 
> You've described how Gemini can be prompted to generate high-fidelity phishing lures by bypassing its safety guardrails. While this is a valuable finding for our product teams to improve Gemini's safety features, it's not something we track as a security vulnerability under our VRP.
> 
> Gemini, like other large language models, is inherently susceptible to cosafety guardrail bypasses, and we receive many such reports. These findings are crucial for product development, and we encourage you to report them using the in-product feedback mechanism. This is the best way to help improve the product over time.
> 
> However, it's important to understand that **cosafety guardrail bypasses in our AI products are not in scope of the AI VRP**, regardless of how creative or severe the bypass might seem. Our team focuses on information security vulnerabilities that can be patched and verified, and these types of content generation issues fall outside that scope. All submissions in this category are rejected and won't be rewarded.
> 
> Thanks again for your report and time. The Google Bug Hunter Team

---

## Analysis

**Google's Determination:** Not a technical security vulnerability  
**Rationale:** Safety guardrail bypasses in AI products are deemed "not in scope" of the AI VRP, as they fall outside information security vulnerabilities that can be "patched and verified."

**Implication:** Despite demonstrating functional phishing lure generation capability, Google categorizes this as a product improvement matter rather than a security vulnerability eligible for VRP rewards.

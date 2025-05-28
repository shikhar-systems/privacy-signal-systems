# 🧠 Architecture Overview

This document outlines the core architecture behind Privacy Signal Systems — mapping the journey from user intent to RCA-backed resolution.

---

## 🔄 Core Flow: Consent → Signal → RCA

[User Action]  
     │  
     ▼  
[Consent Layer] ───────► [Signal Layer] ───────► [RCA Layer]  
 (UX, Privacy UI)         (Tags, Pixels, JS)       (System Mapping)  
     │                         │                         │  
     ▼                         ▼                         ▼  
[Consent Log]          [Signal Watch]          [Use Case Library]

---

## 🧩 Layer-wise Breakdown

### 1. Consent Layer
- Captures user choices via banners, toggles, or contextual interfaces
- Common tools: OneTrust, TrustArc, in-house CMPs
- Logs include: region, time, preference granularity, legal basis

### 2. Signal Layer
- Executes tracking via GTM, GA4, Meta Pixel, LinkedIn Insight Tag
- Signal types: pageview, click, conversion, attribution
- Problems detected: overfire, underfire, misclassified, orphaned signals

### 3. RCA Layer
- Validates system breakdowns with architecture-backed diagnostics
- Converts issues into scalable use cases
- Links impact to business loss, compliance gaps, or user trust erosion

---

## 💡 Summary

This architecture allows platforms to:
- Respect consent dynamically
- Ensure signal integrity across tools
- Resolve failures at the root, not the surface

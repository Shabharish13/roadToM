# WhatsApp Payroll Automation for Micro-SMEs (India)

**Date:** 2026-03-28
**Source:** Razorpay Fix My Itch (GitHub projects built on platform) + industry validation
**Status:** Signal but no money

---

## Problem Statement

- **Who:** Indian micro-SME owners (1–20 employees): shops, small manufacturers, contractors, domestic staffing
- **What:** Payroll is still done manually in Excel — attendance tracked on paper, salary calculations done per employee, payslips shared via printout or WhatsApp copy-paste. Takes 2–3 days per month.
- **When:** End of every month, and every time an employee joins/leaves

---

## Pain Signal

| Source | Quote or Evidence | Intensity |
|---|---|---|
| Industry case study | "Sharma Electronics spent three days each month processing payroll for 200 employees. In 2024, they adopted automated payroll software, cutting payroll time down to just two hours." | High |
| Industry data | "Manual payroll management is riddled with challenges: time-consuming processes, frequent regulatory updates, and the risk of errors that could lead to penalties." | Medium |
| Industry report | "Processing payroll manually is still a common practice among Indian SMEs." | Medium |
| X/Twitter (Deel) | PaySpace/Deel launched "Pacey" — WhatsApp-based payslips, leave, claims: "Get payslips, apply for leave, submit claims, no app needed." — confirms concept is actively being built | Medium |

**Workarounds people use today:**
- Excel sheets for attendance + manual salary calculation
- WhatsApp voice/text to notify salary
- CA/accountant handling payroll monthly (outsourced but still slow)
- Paper attendance registers

---

## Buying Signal

| Product | Price | Reviews/Users | Gap |
|---|---|---|---|
| RazorpayX Payroll | ₹21/employee/mo | Large base (Razorpay distribution) | Not WhatsApp-native; requires app onboarding |
| SalaryBox | ₹35/employee/mo | 85 PH upvotes; "mobile-first for Asia/India" | Closest to this vision; already funded |
| Keka | ₹60/employee/mo | Well-reviewed for mid-market | Too heavy for <20 employees |
| GreytHR | ₹40/employee/mo | Strong India SME adoption | App-based, not WhatsApp-native |
| Kredily | ₹999/mo flat | SME-focused | Decent coverage; not WhatsApp |
| Deel/PaySpace Pacey | Unknown (Africa-first) | Funded (Deel) | Not India-focused; building WhatsApp-native angle |

---

## Shab Fit

**Verdict:** Weak fit

- The problem is real and the WhatsApp-native angle for micro-SMEs (<20 employees, feature phone users) is genuinely underserved. BUT: Deel/PaySpace (Pacey) is building this with significant resources. SalaryBox is already mobile-first and India-focused. RazorpayX Payroll has the distribution moat. The gap is shrinking fast, and the moat here is operational (onboarding micro-SMEs, supporting feature phones, handling PF/ESI edge cases) — which is exactly Shab's risk zone. Not a great fit unless there's a specific vertical (e.g., domestic workers, kirana stores) that remains genuinely unserved.

---

## Recommended Next Step

If pursuing: narrow to a single vertical — e.g., domestic worker payroll (maids, drivers, guards) where the employer is a household, not a business. This has no compliance overhead and UPI disbursement is already the norm. Validate with 5 apartment society WhatsApp groups before writing a line of code.

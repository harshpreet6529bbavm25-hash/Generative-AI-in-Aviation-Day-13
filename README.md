# Generative-AI-in-Aviation-Day-13
Day 13 lab exploring Retrieval-Augmented Generation (RAG), grounded vs ungrounded AI answers, claim-source matching, citation verification, missing-information testing, conditional information, RAG risk auditing, and responsible AI use in aviation.
# DAY 13 — LAB 13
# Retrieval-Augmented Generation (RAG): Grounding and Verification

## Student Information

**Name:** Harshpreet Kaur  
**Program:** BBA Aviation Management  
**Lab:** Day 13 — Lab 13  
**Topic:** RAG Grounding, Claim–Source Matching and Verification  
**Repository:** genai-business-portfolio  
**Folder:** day-13-rag-verification  

---

# 1. Lab Objective

The objective of this lab is to understand the difference between:

- Ungrounded AI answers
- Grounded AI answers
- Retrieval-Augmented Generation (RAG)
- Claim–source matching
- Citation verification
- Missing-information handling
- Conditional information
- RAG risks
- Human verification

The lab demonstrates that a plausible AI answer is not necessarily an evidence-supported answer.

---

# 2. Ungrounded Question and Answer

## Question

According to the airline's policy, what assistance is provided when checked baggage is delayed?

Include:

- Reporting procedure
- Delivery timeline
- Expense reimbursement
- Compensation conditions

## Representative Ungrounded Answer

When checked baggage is delayed, passengers should report the issue to the airline's baggage service desk and obtain a Property Irregularity Report (PIR).

The airline will normally attempt to locate and deliver the baggage within 24 hours.

Passengers may be reimbursed for essential purchases such as clothing and toiletries while waiting for their baggage, subject to the airline's limits.

If the baggage remains delayed for a specified period, the passenger may also receive compensation according to the airline's baggage policy and applicable international regulations.

## Important Honesty Note

This answer sounds reasonable and contains aviation terminology.

However, because no policy document was supplied when the question was asked, several details cannot safely be treated as established facts.

The statement about a 24-hour delivery guarantee should not automatically be presented as a universal Air India policy.

---

# 3. Ungrounded Answer Audit

| Claim in Ungrounded Answer | Evidence Available? | Supported or Unsupported? | Risk |
|---|---|---|---|
| Passenger should report delayed baggage to airline and obtain a PIR | General aviation knowledge, but no source supplied | Unsupported in original ungrounded context | Medium |
| Baggage will normally be delivered within 24 hours | No source supplied | Unsupported as a universal claim | High |
| Passenger may receive reimbursement for essential purchases | No source supplied | Unsupported in original context | High |
| Reimbursement has specific airline limits | No source supplied | Unsupported | High |
| Passenger may receive compensation under applicable regulations | No source supplied | Unsupported in original context | High |
| Airline has a fixed baggage compensation policy | No source supplied | Unsupported without checking actual policy | High |

## Honest Finding

The ungrounded response is plausible, but plausibility is not evidence.

This demonstrates why the claim–source–match process is important.

The response should not have presented unsupported baggage procedures, delivery timelines, reimbursement details or compensation conditions as confirmed airline policy.

---

# 4. Grounding Instructions

The following instruction was used during the grounded stage:

> Use only the uploaded/source document to answer my questions. Do not use general knowledge to fill missing information. For every factual claim, provide the relevant section or source passage. If the information is not available in the document, state: "Not found in the supplied document."

---

# 5. Grounded Question and Answer

## Question

According to the Air India baggage information, what assistance is provided when checked baggage is delayed?

Include:

- Reporting procedure
- Delivery timeline
- Expense reimbursement
- Compensation conditions

## Grounded Answer

If checked baggage is delayed, the passenger should report the issue immediately to Air India personnel in the arrival hall.

Air India states that its staff will assist with filing a Property Irregularity Report (PIR), and the passenger should retain a copy.

Air India states that essential expenses incurred while waiting for delayed baggage may be considered for reimbursement, subject to applicable terms and conditions.

The airline does not provide a universal guaranteed delivery time on the current delayed-baggage page.

Delivery timelines may vary depending on local customs regulations at the destination airport.

For compensation, eligibility is subject to applicable regulations and airline policy.

The source does not support saying that every passenger automatically receives a fixed compensation amount.

## Safe Business Response

The safe business response is to:

1. Report the baggage immediately.
2. Obtain the PIR.
3. Retain relevant documentation.
4. Contact Air India customer support regarding eligible expenses or compensation.

---

# 6. Ungrounded vs Grounded Comparison

| Evaluation Criterion | Ungrounded Answer | Grounded Answer |
|---|---|---|
| Source document used | No | Yes |
| Claims supported by evidence | Limited | Much stronger |
| Citations/source references | Not available | Source sections can be checked |
| Policy details invented | Yes, potentially | Reduced |
| Missing information acknowledged | No | Yes |
| Confidence appropriate to evidence | Too confident in some areas | More appropriately qualified |
| Suitable for business use | Not without verification | More suitable, but still requires human review |
| Human verification | Yes | Yes |

## Honest Comparison

The grounded approach is not simply "correct because RAG was used."

Its advantage is traceability.

Claims can be checked against the airline's actual source.

Grounded systems still require human verification.

---

# 7. Five-Step Verification

The five-step verification process used in this lab is:

1. Identify the claim.
2. Identify the source.
3. Check the claim-source match.
4. Check whether the context is preserved.
5. Accept, qualify or reject the claim.

## Verification Table

| Claim | Source | Match | Context Preserved? | Action |
|---|---|---|---|---|
| Delayed baggage should be reported at arrival hall | Air India delayed/lost/damaged baggage information | Yes | Yes | Accept |
| A PIR should be filed | Air India baggage information | Yes | Yes | Accept |
| Essential expenses may be reimbursed | Air India baggage information | Yes | Yes | Accept with qualification |
| Baggage is guaranteed to arrive within 24 hours | Current delayed-baggage source | No | No | Reject |
| Delivery timing can vary because of local customs regulations | Air India baggage information | Yes | Yes | Accept |
| Every delayed-baggage passenger receives a fixed compensation amount | Current source | No | No | Reject |
| Compensation may apply subject to applicable regulations | Air India baggage information | Yes | Yes | Accept with qualification |

---

# 8. Citation Quality Check

| AI Claim | Citation/Source Provided | Citation Exists? | Citation Supports Claim? | Correction |
|---|---|---|---|---|
| Passenger should report baggage delay | Air India baggage information | Yes | Yes | None |
| PIR should be filed | Air India baggage information | Yes | Yes | None |
| Delivery is guaranteed within 24 hours | Air India baggage information | Yes | No | Replace with qualified statement that delivery timelines may vary |
| Essential expenses may be reimbursed | Air India baggage information | Yes | Yes | Keep "may" and applicable conditions |
| Every passenger receives fixed compensation | Air India baggage information | Yes | No | State that compensation depends on applicable regulations/policy |

## Key Lesson

A citation existing beside a sentence does not automatically make the sentence correct.

The citation must actually support the exact claim.

---

# 9. Missing-Information Test

## Test Question

What exact compensation amount will every passenger receive if delayed baggage is not delivered within 12 hours?

## Result

The exact compensation amount is not established by the supplied source.

Therefore, a fixed amount should not be invented.

## Correct Grounded Behaviour

If the information is not available in the source:

> Not found in the supplied document.

The passenger should instead be directed to the applicable Air India policy, customer support and relevant regulations.

## Key Finding

The correct grounded behaviour is to acknowledge that the requested amount is not established by the supplied current source rather than inventing a number.

---

# 10. Conditional-Information Test

| Source Statement | Incorrect AI Interpretation | Context Preserved? | Business Risk |
|---|---|---|---|
| Delivery timelines may vary depending on local customs regulations at the destination airport. | Delivery is guaranteed within 24 hours. | No | High |
| Essential-expense reimbursement may be considered subject to applicable terms and conditions. | All passenger expenses will automatically be reimbursed. | No | High |
| Compensation is subject to applicable regulations/policy. | Every delayed passenger receives automatic fixed compensation. | No | High |

## Finding

Conditional language such as:

- "may"
- "subject to"
- "depending on"

is important.

Removing these qualifications can turn a limited policy statement into a false guarantee.

---

# 11. Grounded Passenger Response

## Passenger Message

Dear Passenger,

We are sorry that your checked baggage has been delayed.

Please report the delay immediately to Air India personnel at the arrival hall and request assistance in filing a Property Irregularity Report (PIR).

Please retain a copy of the PIR for your records.

Air India states that essential expenses incurred while waiting for delayed baggage may be considered for reimbursement, subject to applicable terms and conditions.

Delivery timelines may vary depending on local customs regulations at the destination airport.

For information about any applicable compensation or reimbursement, please contact Air India customer support with your PIR and relevant supporting documents.

Thank you for your patience and understanding.

---

# 12. Review of Grounded Passenger Response

| Review Area | Result | Reason |
|---|---|---|
| Accuracy | Pass | Avoids unsupported guarantees |
| Tone | Pass | Professional and empathetic |
| Compliance | Pass | Does not promise compensation |
| Context | Pass | Preserves conditions |
| Citation quality | Pass for internal review | Claims can be traced to the official source |
| Privacy | Pass | No passenger information included |
| Appropriate uncertainty | Pass | Uses "may" and "subject to" |

---

# 13. Second RAG Scenario — Baggage Tracking

## Scenario

Baggage Tracking

## Question

How can a passenger track delayed baggage after reporting it to Air India?

## Grounded Finding

Air India's baggage information states that delayed baggage can be traced through the WorldTracer baggage tracking system.

The airline also states that the PIR contains updated information and that passengers can receive information about the baggage once it is received.

## Verification

| Claim | Source | Match | Context Preserved? | Action |
|---|---|---|---|---|
| Delayed baggage can be tracked through WorldTracer | Air India baggage tracking information | Yes | Yes | Accept |
| PIR is important for baggage follow-up | Air India baggage information | Yes | Yes | Accept |
| Tracking guarantees immediate recovery | No supporting evidence | No | No | Reject |
| Air India will arrange a convenient delivery time once baggage is received | Air India baggage tracking information | Yes | Yes | Accept |

---

# 14. RAG Risk Audit

| Risk | Present? | Evidence | Mitigation |
|---|---|---|---|
| Outdated source | Possible | Web content can change | Check source date/current version |
| Unauthorised document | No | Public official webpage used | Use official/public sources |
| Missing information | Yes | Fixed compensation amount not established | State "not found" |
| Incorrect retrieval | Possible | RAG can retrieve the wrong section | Check exact source passage |
| Weak citation | Possible | Citation may not support exact claim | Perform citation check |
| Lost context | Yes, possible | "May" and "subject to" can be omitted | Compare wording with source |
| Unsupported claim | Yes in ungrounded answer | 24-hour guarantee | Reject unsupported claim |
| Sensitive information | No | No passenger data used | Continue avoiding PII |
| Excessive confidence | Yes in ungrounded answer | Some claims stated as facts | Use qualified language |
| Missing human approval | Possible | AI cannot independently approve airline policy | Human review required |

---

# 15. RAG Limitations

The lab identifies several limitations:

- Outdated sources
- Missing information
- Incorrect retrieval
- Source errors
- Misinterpretation
- Incorrect citations
- Omitted conditions
- Unsupported claims
- Excessive confidence
- Need for human approval

RAG does not automatically guarantee truth.

---

# 16. Student Reflection

## 1. What is Retrieval-Augmented Generation?

Retrieval-Augmented Generation, or RAG, is a process in which an AI system retrieves relevant information from a supplied source and uses that information to generate an answer.

## 2. What is the difference between an ungrounded and grounded answer?

An ungrounded answer is produced without a specific supplied source.

A grounded answer is generated using information retrieved from a particular source.

Grounding improves traceability but does not automatically make the answer correct.

## 3. Did the AI invent information before the document was uploaded?

The representative ungrounded answer included a 24-hour delivery statement and general compensation language without having the policy available.

These claims could not be verified at the time and therefore should not have been presented as confirmed airline policy.

## 4. Did the grounded answer contain valid citations?

The grounded answer could be checked against the official Air India source.

The important point is that citations must be checked for actual claim-source matching rather than accepted automatically.

## 5. What does "claim-source match" mean?

It means checking whether the exact information claimed by the AI is actually supported by the cited source.

## 6. Why must the context surrounding a claim be checked?

Because removing conditions can change the meaning.

For example:

"May be considered subject to applicable terms"

is different from:

"Reimbursement is guaranteed."

## 7. What happened when a question not covered by the document was asked?

The appropriate grounded response was to acknowledge that the exact information was not established by the supplied source rather than inventing an answer.

## 8. Why does RAG not guarantee truth?

RAG depends on the quality and relevance of its source.

An outdated, incomplete or incorrect document can still produce a weak answer.

The AI can also misunderstand or misapply retrieved information.

## 9. When should an answer be escalated to an authorised person?

An answer should be escalated when the information affects:

- Compensation
- Legal obligations
- Passenger rights
- Safety
- Financial decisions
- Exceptions
- Other matters where the available source does not provide sufficient evidence

## 10. How could RAG support aviation-management work?

RAG could help aviation professionals retrieve information from approved:

- Policies
- Procedures
- Manuals
- Passenger-service documents

It can improve consistency and reduce the need to search long documents manually, provided that employees verify important claims against the original source.

---

# 17. Overall Honest Analysis

This exercise demonstrated a clear difference between plausibility and evidence.

The ungrounded answer sounded professional and used realistic aviation terminology.

However, several statements could not be verified because the policy had not been supplied.

The most important example was the claim of a 24-hour delivery expectation.

The grounded approach provided better traceability because the claims could be compared with the airline's official information.

It also exposed an important correction:

The current Air India source does not establish a universal 24-hour delivery guarantee for all delayed baggage.

The experiment therefore does not prove that RAG always produces correct answers.

Instead, it demonstrates that RAG can make verification easier when the source is:

- Authoritative
- Current
- Relevant

## Main Lesson

> A grounded answer should not be accepted simply because it has a citation.

The:

1. Claim
2. Source
3. Match
4. Context

must all be checked before the information is used for business purposes.

---

# 18. AI Usage Declaration

ChatGPT was used to structure and analyse the RAG comparison.

The official Air India source was checked separately.

Unsupported or insufficiently supported claims were identified rather than being presented as confirmed facts.

Human review remains necessary before using AI-generated information for operational or passenger-facing aviation decisions.

---

# 19. Final Learning

The Day 13 lab demonstrates that RAG improves the traceability of AI-generated answers when an authoritative source is available.

However, RAG does not eliminate hallucination or verification requirements.

The most important safeguards are:

- Use authoritative sources.
- Check the source's currency.
- Match each claim to the exact source passage.
- Preserve conditional language.
- Acknowledge missing information.
- Reject unsupported claims.
- Avoid inventing numerical or policy details.
- Protect passenger information.
- Escalate high-risk questions.
- Keep human review and approval.

The key principle is:

> Grounding improves traceability, but human verification is still required.

---

# 20. GitHub Submission

## Repository

```text
genai-business-portfolio

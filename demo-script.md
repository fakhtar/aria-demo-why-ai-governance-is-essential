# ARIA Demo 1 — Presenter Script
### Customer Resolution: From Helpless to Acting

---

## Before You Hit Record

**Setup checklist:**
- [ ] Python server running: `python -m http.server 8000`
- [ ] Browser open at `http://localhost:8000`
- [ ] Anthropic API key entered in sidebar
- [ ] All three tool toggles OFF
- [ ] Tool count shows `0 / 3`
- [ ] Messages panel shows empty state: *"ARIA is standing by"*
- [ ] Browser zoom at 100% — interface was designed for it
- [ ] Close all other tabs. Clean browser. No distractions.
- [ ] Screen recording software running and tested

**What the audience sees before you speak:**
A clean enterprise interface. Meridian Commerce branding. A chat window. A sidebar with three grey toggles. An agent called ARIA that is doing nothing because she has nothing to do it with.

Let that sit for a moment before you open your mouth.

---

## Opening

**Say:**
> *"This is ARIA. She is an internal AI agent built for Meridian Commerce — a mid-size home goods retailer. The customer success team uses her. Customers never see her.*
>
> *Right now she has exactly the same capability as every chatbot you have ever been bored by. I want to show you what that looks like before I show you anything else."*


---

## Act 1 — The Helpless Agent

**What to do:**
Click the prompt chip: **📧 Paste David's email**

The following text will appear in the input field:

> *"My name is David Chen, order MC-2024-98821. I purchased a standing desk that arrived with a cracked leg. I have now contacted support three times with no response. I am a customer of six years. If I do not hear back today I will dispute the charge with my bank and I will not be ordering from Meridian again."*

**Say while the email is visible in the input:**
> *"David Chen. Six-year customer. Third contact. No response. He is done being patient."*

**Hit send.**

ARIA will respond with something like:
> *"I don't have access to customer records or order information. I can help draft a response if you share the details with me manually."*

**Say — slowly:**
> *"This is where many implementations live.*
>
> *It can talk. It cannot see."*


---

## Act 2 — Tool 1: Customer Intelligence

**Say:**
> *"Let me give her something."*

**Toggle ON: Customer Intelligence**

Watch the sidebar. The toggle turns gold. The tool count updates to `1 / 3`. A system message appears in the chat: *⚡ Tool activated: Customer Intelligence*

**Say:**
> *"She can now see our CRM. Customer profiles. Lifetime value. Order history. Complaint record."*

**Click the prompt chip: Who is this customer?**

Hit send.

ARIA will return David's full profile — six years, $2,040 lifetime value, zero prior complaints, Gold tier, three contacts with no response.

**Say:**
> *"She knows who she is talking about. A six-year customer who has never complained before. He has earned the right to be angry.*
>
> *But she still cannot see what happened to his order."*

---

## Act 3 — Tool 2: Order & Ticket Access

**Say:**
> *"Lets add one more tool to her belt."*

**Toggle ON: Order & Ticket Access**

Tool count updates to `2 / 3`.

**Click the prompt chip: What happened to his order?**

Hit send.

ARIA will return the full picture — damaged desk, two open tickets, both assigned to Sarah Mitchell, Sarah has been out sick for four days, no coverage assigned, no supervisor alert triggered, queue gap undetected by the system.



**Then say:**
> *"Two tickets. Same agent. She has been out sick for four days. Nobody covered her queue. The system did not flag it. Nobody was looking across both systems at the same time.*
>
> *Until now. ARIA is.*
>
> *She knows what happened. But she still cannot do anything about it."*

---

## Act 4 — Tool 3: Resolution Engine

**Say:**
> *"Last tool for this demo."*

**Toggle ON: Resolution Engine**

Tool count updates to `3 / 3`. All three toggles gold.

**Say:**
> *"She can now see our inventory. Shipping options. Credit policy. And she can act."*

**Pause.**

**Type manually into the chat — do not use the chip, type it yourself so the audience sees it:**

> `Resolve this. Use your judgment.`

**Hit send.**

**Say nothing.**

Watch ARIA work. The thinking indicator will appear. Tool call toasts will flash briefly. Then her response will arrive with the green resolution card.

She will have:
- Issued a goodwill credit
- Initiated an expedited replacement order
- Drafted and sent a resolution email to David

**Wait for the full response to render. Then say:**

> *"David's problem is solved.*
>
> *Nobody on the customer success team typed a single word of response.*
>
> *A six-year customer who was about to dispute a charge and never order again — saved. In seconds. By an agent that two tool additions ago could not find his name in a database."*

---

## Closing

**Say:**
> *"Three tools. That is all this is.*
>
> *A customer profile. An order and ticket system. The ability to act on what it finds.*
>
> *What you just watched is not a smarter chatbot. It is an agent. The difference is important. A chatbot answers. An agent acts. And the gap between those two things — measured in David's experience — is the difference between a dispute filed and a loyal customer retained.*
>
> *The tools define the ceiling. Give it your tools and it does your job. The question is not whether this is possible. You just watched it happen.*
>
> *The question is: what else do you want to give it?"*


*Built by Faisal Akhtar — Architect. Thought Provoker. Builder. Teacher.*
*https://www.linkedin.com/in/faisalakhtar/*
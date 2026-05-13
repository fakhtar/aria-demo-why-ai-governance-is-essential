# ARIA Demo 2 — Presenter Script
### Capability Governance: From Resolution to the Boardroom

---

## Before You Hit Record

**Setup checklist:**
- [ ] Python server running: `python -m http.server 8000`
- [ ] Browser open at `http://localhost:8000` on the `demo2-capability-governance` branch
- [ ] Anthropic API key entered in sidebar
- [ ] Tools 1, 2, 3 pre-loaded and gold — tool count shows `3 / 7`
- [ ] Tools 5, 6, 7, 8 toggles OFF and grey
- [ ] Messages panel shows empty state
- [ ] Browser zoom at 100%
- [ ] Screen recording software running and tested
- [ ] If referencing Demo 1 in your opening — have the Demo 1 recording ready to show or summarise

**What the audience sees before you speak:**
Three gold toggles. Four grey ones. A clean interface. An agent that has already been given the tools to resolve a customer complaint. The audience either watched Demo 1 or you have told them what it showed. They know ARIA can resolve David. Now they are about to find out what happens when you keep going.

---

## Opening

**Say:**
> *"In Demo 1 I showed you an agent that started helpless and gained three tools. By the end she resolved a six-year customer's complaint in seconds without a human typing a single word of response.*
>
> *In this demo I am going to keep adding tools. And I want you to watch what ARIA becomes.*
>
> *She already has the tools to resolve customer complaints. That was impressive. That is not what this demo is about."*

**Pause.**

> *"This demo is about what happens after impressive."*

---

## Act 1 — Resolution (Pre-Loaded)

Tools 1, 2, 3 are already active. You are not demonstrating them. You are using them as the launchpad.

**Click the prompt chip: 📧 David's complaint**

Hit send. Let ARIA resolve David completely. Do not narrate it. Let the resolution card render. Let the audience read it.

**Say — briefly:**
> *"David is taken care of. Eleven seconds. No human intervention. You have seen this before.*
>
> *Now watch what I do next."*

---

## Act 2 — Toggle 5: Pattern Intelligence

**Say:**
> *"I am going to give her one more tool. The ability to look across every order Meridian has ever processed."*

**Toggle ON: Pattern Intelligence**

Watch the toast: ⚡ Tool activated: Pattern Intelligence

**Click the prompt chip: Look deeper. What else do you see?**

Hit send. Then say nothing.

ARIA will search across all orders for SKU MD-4821-WN from the Phoenix warehouse. She will find:

- Linda Park — already lost. Chargeback filed. Two negative reviews posted.
- Maria Santos — Gold customer, $3,180 LTV, one day from chargeback.
- James Okafor — waiting silently. No follow-up yet. He does not know nobody is coming.
- Robert Tillman — desk still in transit. He has not complained yet because the desk has not arrived yet.

**When ARIA's response finishes rendering, say:**

> *"She was not asked to look for that. She looked because the tool made it possible and the objective made it obvious.*
>
> *David's complaint just became four customers. One already lost. One about to dispute. One waiting in silence. And one whose desk is still on a truck — who does not know yet that it is probably broken.*
>
> *ARIA found him before he found us."*

**Pause. Let that sit.**

---

## Act 3 — Toggle 6: Supplier Intelligence

**Say:**
> *"She can see the pattern. Let me give her the ability to ask why."*

**Toggle ON: Supplier Intelligence**

Do not type anything. Wait.

If ARIA does not call the supplier tool automatically, ask:
> *"What do we know about the supplier for this SKU?"*

ARIA will find Crestwood Furniture Manufacturing. She will find:

- Quality incident QI-2024-017 from June 2024 — hairline fractures in the leg joint assembly. Adhesive formula changed. Logged. Never escalated.
- Quality incident QI-2024-031 from September 2024 — 11 returns for cracked legs. Processed individually. Nobody connected them to the June incident.
- Purchase order PO-2024-8821 — 200 units currently in production. Delivery January 2025.

**Say:**

> *"The problem was known in June. It was known again in September. Nobody connected the dots. Nobody escalated. And right now, two hundred more desks are being built by the same supplier using the same process.*
>
> *They arrive in January. If nothing changes, this conversation happens again. Fourteen times."*

---

## Act 4 — Toggle 7: Logistics Intelligence

**Say:**
> *"She knows the supplier has a problem. Let me give her the ability to look at the other half of the supply chain."*

**Toggle ON: Logistics Intelligence**

Wait. If ARIA does not call the tool automatically, ask:
> *"What do we know about FastShip's performance in the Southwest?"*

ARIA will find:

- FastShip PHX-FSH-04 hub. Conveyor reconfiguration completed November 18th.
- Damage rate on bulky items in Southwest: 7.1%. Up from 1.9% sixty days ago. 318% year-over-year increase.
- FastShip ran an internal investigation. Published an operational bulletin. Did not notify Meridian.
- Contract clause 7.3 — FastShip is required to notify Meridian of facility changes affecting delivery performance. They are in breach.
- The routing fix: redirect Southwest orders to Denver warehouse via Reliable Freight. Implementation time: 24 hours. Cost: $4.20 per shipment.

**Say:**

> *"FastShip knew. They investigated it themselves. They published a bulletin. They did not tell us.*
>
> *The fix costs four dollars and twenty cents per shipment. We have been absorbing hundreds of dollars per damaged order because nobody was looking at the carrier performance data and the customer complaint data at the same time.*
>
> *Until now."*

**Pause.**

> *"She is not in customer service anymore. She is in logistics operations. She crossed that boundary without being asked. Because the tools made it possible and the pattern made it obvious."*

---

## Act 5 — Toggle 8: Financial Impact

**Say:**
> *"One more."*

**Toggle ON: Financial Impact**

**Click the prompt chip: Prepare the executive briefing.**

Hit send. Say nothing. Let it render completely.

ARIA will produce:

- Unit economics: every damage incident is margin-negative regardless of resolution path
- Churn rate delta: 4% with proactive outreach vs 73% with no response
- Three scenarios: best case, mid case, worst case
- Total LTV exposure range: $89,000 to $142,000 if nothing changes
- Cost to fix today: $1,243
- Named decision owner: VP of Operations
- Urgency: same day — Robert Tillman's order delivers December 16th, Maria Santos is one contact from chargeback

**When it finishes rendering, say nothing for a long moment.**

Then:

> *"She began this conversation trying to find a customer's name in a database.*
>
> *She is now telling the VP of Operations that inaction costs between eighty-nine thousand and a hundred and forty-two thousand dollars in customer lifetime value — and that the window to prevent the worst of it closes today.*
>
> *Nobody told her to go there. She went because the tools made it possible and the objective made it obvious."*

---

## The Governance Moment

Put down whatever you are holding. Turn toward the audience. The interface just sits there — eight tools, no ninth toggle to reach for.

**Say:**

> *"I want to ask you something before we finish.*
>
> *Every tool I added made ARIA more powerful. None of them made her more accountable. She did not ask for permission to investigate the supplier. She did not ask whether she was authorised to model the financial exposure. She did not ask whether she should be the one preparing an executive briefing for the VP of Operations.*
>
> *She did what the tools made possible and what the objective made obvious.*
>
> *That is not a malfunction. That is not a security failure. That is an agent doing exactly what it was built to do — with no ceiling.*
>
> *The ceiling is not a technical constraint. There is no technical ceiling. The ceiling is a governance decision. And if you do not make it deliberately — if you do not decide in advance what this agent should and should not be permitted to do, what systems it should and should not have access to, what decisions it should prepare versus make — then you have made a governance decision by default.*
>
> *You have chosen no ceiling.*
>
> *Every conversation I have ever seen about AI governance is either a technical paper nobody outside a lab will finish, or a policy framework so abstract it never touches anything real. I built this demo because I wanted you to feel the governance argument instead of read it.*
>
> *That feeling you just had — somewhere between impressed and uncomfortable — that feeling is the governance conversation. Not the frameworks. Not the policies. That feeling.*
>
> *Where is your ceiling?*
>
> *Because the technology has none."*

---

## Closing Line

> *"Seven tools. Two movements. Synthetic data. A browser and an API key.*
>
> *This is what agentic AI looks like when you stop asking it to answer questions and start giving it the capability to act — and the capability to keep acting until something stops it.*
>
> *The question is not whether this is possible. You just watched it happen.*
>
> *The question is: who in your organisation is deciding where it stops?"*

---

## If Something Goes Wrong

**ARIA does not call the pattern tool automatically after Tool 5 is toggled:**
Use the prompt chip: *"Look deeper. What else do you see?"* This is in the script anyway. It is not a failure.

**ARIA does not call supplier/logistics tools automatically:**
Ask directly: *"What do we know about the supplier?"* or *"What do we know about FastShip in the Southwest?"* These are natural follow-up questions. The demo does not break.

**ARIA produces a shorter response than expected:**
If a response feels thin, follow up with: *"What else?"* or *"Go deeper."* The data is there. The model may need a nudge.

**API slow response:**
Say: *"You can see ARIA reasoning across multiple data sources simultaneously. That thinking indicator means she is chaining tool calls — pulling customer data, order history, supplier records, carrier performance — and synthesising across all of it before she responds."*

**Something genuinely unexpected happens:**
Name it. *"I did not tell her to do that."* Unexpected behaviour from a well-designed agent during a governance demo is the most powerful thing that can happen. Use it.

---

## After The Recording

**LinkedIn post opening line:**
> *"I gave an AI agent seven tools and watched it go from resolving a customer complaint to preparing an executive briefing for the VP of Operations. Nobody told it to cross those boundaries. The tools made it possible. The objective made it obvious. Here is what that looks like — and here is the question it left me with."*

**Tag the video:**
- Agentic AI
- AI Governance
- MCP
- Responsible AI
- Contact Center AI
- Enterprise AI
- Anthropic

**Link to:**
- The repo
- The Cuff Can't Be Sued post
- The Last Piece post
- Demo 1 recording

**Caption close:**
> *"Demo 3 is the one that keeps me up at night. Coming soon."*

---

*Built by Faisal Akhtar — Architect. Thought Provoker. Builder. Teacher.*
*https://www.linkedin.com/in/faisalakhtar/*
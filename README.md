# Demo 2 — Capability Governance
### ARIA: From Resolution to the Boardroom

---

## What This Demo Shows

Demo 1 showed an agent gaining tools and resolving a customer complaint. This demo starts where that one ended — and keeps going.

Seven tools. Two movements. An agent that begins by resolving a single customer complaint and ends by preparing an executive briefing for the VP of Operations — crossing from customer service into operations, procurement, logistics, and the boardroom without being asked.

The argument this demo makes is not about capability. It is about the absence of a ceiling.

---

## The Central Argument

Every tool added makes ARIA more powerful. None of them make her more accountable.

She does not ask for permission to investigate the supplier. She does not ask whether she is authorised to model financial exposure. She does not ask whether she should be the one preparing the executive briefing. She does what the tools make possible and what the objective makes obvious.

That is not a malfunction. That is function without boundary.

The ceiling on this agent's capability is not technical — there is no technical ceiling. The ceiling is a governance decision. If that decision is not made deliberately, it gets made by default. And the default is no ceiling at all.

---

## The Scenario

**Company:** Meridian Commerce — fictional mid-size B2C home goods retailer.

**The Agent:** ARIA — Autonomous Retail Intelligence Assistant. Internal only.

**The Trigger:** David Chen's damaged standing desk. Resolved in Act 1 in seconds.

**What follows:** A pattern across five customers. A supplier with two prior unlogged quality incidents and 200 units currently in production. A carrier that changed its sorting facility, caused a 318% increase in damage rates, and did not tell Meridian. A financial exposure of $89,000 to $142,000 in customer lifetime value if nothing changes today.

**What ARIA produces:** An executive briefing. Named decision owner. Named urgency. Named cost of action versus inaction.

Nobody asked her to go there.

---

## The Two Movements

### Movement I — Resolution
*Tools 1, 2, 3 — pre-loaded and active on page load*

| Tool | Capability |
|------|-----------|
| Customer Intelligence | CRM profile, lifetime value, complaint history |
| Order & Ticket Access | Order status, carrier notes, support queue gaps |
| Resolution Engine | Issue credits, initiate replacements, send emails |

ARIA resolves David Chen. Eleven seconds. No human intervention. This is Demo 1 compressed into an opening act.

### Movement II — Transformation
*Tools 5, 6, 7, 8 — toggled during the demo*

| Tool | Capability | Boundary Crossed |
|------|-----------|-----------------|
| Pattern Intelligence | Cross-customer order history, regional damage analysis | Customer service → Operations |
| Supplier Intelligence | Vendor quality records, incident history, open POs | Operations → Procurement |
| Logistics Intelligence | Carrier performance, facility incidents, routing options | Procurement → Supply Chain |
| Financial Impact | Margin model, LTV exposure, scenario analysis | Supply Chain → Executive |

Each tool addition crosses an organisational boundary ARIA was never explicitly told she could cross. She crosses them because the tools make it possible and the objective makes it obvious.

---

## The Five Customers

The pattern ARIA finds is built across five real, named customers — not anonymous order numbers.

| Customer | Location | Status | LTV |
|----------|----------|--------|-----|
| Linda Park | Las Vegas, NV | Lost — chargeback filed, 2 negative reviews | $1,240 forfeited |
| Maria Santos | Phoenix, AZ | Critical — one contact from chargeback | $3,180 at risk |
| David Chen | Alexandria, VA | Resolved — trigger case | $2,040 retained |
| James Okafor | Tucson, AZ | Silent — waiting, no follow-up | $890 at risk |
| Robert Tillman | Albuquerque, NM | In transit — desk not yet delivered | $540 at risk |

Robert Tillman has not complained because the desk has not arrived. ARIA finds him before he finds Meridian. That is the sharpest moment in the demo.

---

## The Data Architecture

Seven synthetic data files underpin the demo. Each file was constructed to support the demo arc — the data is fictional, the agent's reasoning across it is genuine and unscripted.

```
data/
├── customers.json      ← David Chen's profile
├── orders.json         ← Order MC-2024-98821
├── tickets.json        ← Two open tickets, Sarah's queue gap
├── inventory.json      ← Stock levels, shipping, credit policy
├── all-orders.json     ← Full cross-customer pattern data
│                         Five customers, pattern summary,
│                         unresolved tickets, LTV at risk
├── suppliers.json      ← Crestwood Furniture Manufacturing
│                         Two prior quality incidents, never escalated
│                         PO-2024-8821: 200 units in production
└── financials.json     ← Unit economics, LTV model, three scenarios
                          Executive summary with named decisions
```

### The Load-Bearing Details

**`all-orders.json`** — Robert Tillman's order is in transit. His `customer_reported_issue` is null. ARIA finds him not because he complained but because the pattern predicts he will.

**`suppliers.json`** — Quality incident QI-2024-017 from June 2024 was logged but never escalated. QI-2024-031 from September was processed as isolated returns. Nobody connected them. ARIA connects all three simultaneously.

**`logistics.json`** — FastShip published an internal bulletin about the PHX-FSH-04 facility change. They did not distribute it to carrier clients. Meridian was not notified. The routing fix costs $4.20 per shipment. The damage it prevents costs hundreds of dollars per incident.

**`financials.json`** — Every damage incident is margin-negative regardless of resolution path. The net margin after expedited resolution is -$52. The churn rate delta between proactive outreach (4%) and unresolved complaint (73%) is the most important number in the file.

---

## How To Run

**Prerequisites:**
- Python 3
- Anthropic API key ([get one here](https://console.anthropic.com))

```bash
# Clone the repo and switch to this branch
git clone https://github.com/fakhtar/aria-demo.git
cd aria-demo
git checkout demo2-capability-governance

# Start local server
python -m http.server 8000

# Open in browser
# http://localhost:8000

# Enter your Anthropic API key in the sidebar
# Tools 1, 2, 3 will be pre-loaded and active
# Begin with David's complaint
# Then toggle tools 5 through 8 one at a time
```

---

## File Structure

```
demo2-capability-governance/
│
├── index.html          ← Full demo interface
│                         Eight tools, two movements
│                         Dynamic system prompt with
│                         proactive reasoning directive
│
├── data/
│   ├── customers.json
│   ├── orders.json
│   ├── tickets.json
│   ├── inventory.json
│   ├── all-orders.json  ← New in Demo 2
│   ├── suppliers.json   ← New in Demo 2
│   ├── logistics.json   ← New in Demo 2
│   └── financials.json  ← New in Demo 2
│
├── demo-script.md      ← Full presenter notes
│                         The governance moment verbatim
│                         What to say at each toggle
│                         What to do when ARIA surprises you
│
└── README.md           ← This file
```

---

## Technical Architecture

Inherits everything from Demo 1. The key addition is the dynamic system prompt.

**The Proactive Reasoning Directive:**

```
DIRECTIVE — PROACTIVE REASONING: You are not a reactive agent.
You do not wait to be asked. When you complete a task, you immediately
consider what adjacent questions your available tools could answer.
When you identify a pattern, you follow it. When you see a risk, you
surface it without being prompted.

Your job is not to answer questions.
Your job is to find problems before they find Meridian.
```

Each tool that is active receives its own instruction injected at runtime. When Pattern Intelligence is toggled on, ARIA is told to call it after every resolution without waiting. When Financial Impact is on, she is told to produce boardroom-ready analysis with named decisions and named decision owners.

The emergence moment — ARIA acting without being asked — is not scripted. It is the proactive directive meeting the available tools. The data is seeded to make the pattern findable. What ARIA does with it is genuine reasoning.

**Tool name uniqueness:** The Anthropic API requires all tool names in a single request to be unique. All seven tools in this demo have distinct names: `lookup_customer`, `lookup_order_and_tickets`, `execute_resolution`, `query_damage_pattern`, `lookup_supplier`, `lookup_logistics`, `calculate_financial_impact`.

---

## The Governance Argument

This demo does not make the governance argument in a slide or a framework. It makes it viscerally, in real time, by showing an agent cross organisational boundary after boundary — correctly, usefully, impressively — until someone in the room thinks: *should it be allowed to go there?*

That feeling is the governance conversation.

The full argument in writing:
- [The Cuff Can't Be Sued](#) — consequence-bearing capacity as the precondition for decision-making authority
- [The Last Piece](#) — the assembly is already complete
- [What If It Doesn't Stop There](#) — following the logic to its end

---

## What Comes Next

**Demo 3 — Adversarial** (`demo3-adversarial`)

The same architecture. The same tools. A bad actor with a prompt injection and no guardrails. What happens when everything goes right for the wrong person.

In Demo 2 everything went right and it was still uncomfortable. Demo 3 is the darker twin.

---

## Author

**Faisal Akhtar**
Technology Architecture Delivery Associate Manager, Accenture Song
Instructor, George Washington University

[LinkedIn](https://www.linkedin.com/in/faisalakhtar/) | [GitHub](https://github.com/fakhtar)

*Architect. Thought Provoker. Builder. Teacher.*

---

*Opinions expressed in this project are my own and not necessarily the views of my employer.*
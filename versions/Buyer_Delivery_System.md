# Midwest Modding Studio
# Futures Market Expansion
## Buyer Delivery & Fulfillment System

---

# 📌 Overview

The Buyer Delivery & Fulfillment System introduces structured contract-based delivery requirements into the Futures Market system.

Instead of contracts auto-settling, buyers will issue delivery calls requiring the seller to transport contracted goods by a specified deadline.

This system introduces:

- Randomized delivery requests
- Partial or full contract fulfillment calls
- Delivery deadlines
- Financial penalties for non-delivery
- Integration with existing financial systems

---

# 🎯 Core Objective

Simulate realistic commodity contract fulfillment where:

- Buyers initiate delivery requests.
- Sellers must transport goods physically.
- Missed deadlines result in penalties.

---

# 🧠 Delivery Call System

## 1️⃣ Buyer Contact Timing

- Buyer will initiate contact within the first 3 in-game days of the month.
- If savegame uses non-standard month length:
  - Use proportional calculation:
    - (Month Length × 0.10–0.15 window)
- Contact delivered via:
  - Mailbox
  - PC email

Notification Example:
> "Buyer has requested delivery for Contract #0231. Review details in your contract portal."

---

## 2️⃣ Delivery Quantity Determination

When buyer calls:

Randomized outcome:

- 40% chance → Full contract quantity requested
- 60% chance → Partial quantity requested

Partial Quantity Range:
- 25%–75% of total contract amount

Remaining balance stays active for future calls.

---

## 3️⃣ Delivery Deadline Assignment

Delivery deadline randomly generated:

- 2–6 in-game days from notification
- Scales proportionally with month length

Example:
- 3-day month → 1-day deadline
- 6-day month → 2–3 day deadline

Deadline included in delivery notice.

---

# 🚜 Fulfillment Requirements

Player must:

- Deliver specified crop/product
- To assigned buyer delivery trigger
- Before deadline expires

System validates:
- Correct fill type
- Minimum required quantity
- Delivery within time window

---

# 💸 Penalty System

If deadline passes without required delivery:

## Penalty Calculation

Penalty applies only to undelivered portion.

Formula:
- 5–15% of contract value for remaining amount
- Penalty scaled by market volatility (future expansion hook)

Penalty deducted automatically via Financial Manager.

Notification Example:
> "Delivery deadline missed. Contract penalty of $8,450 applied."

---

# 🔄 Contract Lifecycle Flow

1. Contract signed
2. Month begins
3. Buyer initiates delivery call
4. Quantity request randomized
5. Deadline assigned
6. Player delivers (or fails)
7. Penalty applied if necessary
8. Remaining balance carried forward

---

# ⚙️ Technical Systems Required

## New Systems
- Delivery Call Scheduler
- Quantity Randomization Engine
- Deadline Generator
- Contract Fulfillment Validator
- Penalty Calculator

## Integration Required
- Financial Manager (billing & penalty deduction)
- Mail / PC Notification System
- Futures Market Contract Database

---

# 📊 Future Expansion Hooks

- Market volatility multiplier
- Transportation cost tracking
- Quality grade penalties
- Buyer reputation system
- Escalating penalties for repeat failures
- Contract cancellation after repeated default

---

# ⏱ Estimated Development Hours

Low Estimate: 20 hours  
High Estimate: 35 hours  

Breakdown:
- Delivery scheduling logic: 4–6 hrs
- Randomization engine: 4–6 hrs
- Deadline system: 4–6 hrs
- Penalty system integration: 4–8 hrs
- Testing & balancing: 4–9 hrs

---

# 🎯 Deliverable Definition

Upon implementation:

- Buyers will actively request delivery.
- Quantities will vary (partial or full).
- Deadlines will be enforced.
- Missed deliveries will incur financial penalties.
- Remaining contract balances will persist.

This transforms Futures Market contracts from passive agreements into active logistical obligations.

---

Midwest Modding Studio

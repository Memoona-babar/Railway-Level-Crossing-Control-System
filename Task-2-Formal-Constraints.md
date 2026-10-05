# Task 2 — Formalize Constraints

## C1 — Barrier Must Not Open While Train Is Present

**Formal Expression:**

`Train_Present → ¬Barrier_Open`

**Meaning:**
If a train is present, the barrier must not be open.

---

## C2 — Barrier Must Close Before Train Enters

**Formal Expression:**

`Train_Approaching → Barrier_Closed`

**Meaning:**
If a train is approaching, the barrier must be closed.

---

## C3 — Warning Lights Must Activate

**Formal Expression:**

`Train_Approaching → Warning_Lights_ON`

**Meaning:**
If a train is approaching, the warning lights must be activated.

---

## C4 — Audible Alarm Must Activate

**Formal Expression:**

`Train_Approaching → Audible_Alarm_ON`

**Meaning:**
If a train is approaching, the audible alarm must be activated.

---

## C5 — Barrier Must Remain Closed While Train Is Passing

**Formal Expression:**

`Train_Passing → Barrier_Closed`

**Meaning:**
If the train is passing through the crossing, the barrier must remain closed.

---

## C6 — Barrier Opens Only After Train Clearance

**Formal Expression:**

`Barrier_Open → Train_Cleared`

**Meaning:**
If the barrier is open, the system must have confirmed that the train has cleared the crossing.

---

## C8 — Sensor Failure Must Result in Safe State

**Formal Expression:**

`Sensor_Failure → Safe_State`

**Meaning:**
If a sensor fails, the system must enter a safe state.

---

## C9 — Communication Loss Must Not Open Barrier

**Formal Expression:**

`Communication_Loss → ¬Barrier_Open`

**Meaning:**
If communication with the control center is lost, the barrier must not be open.

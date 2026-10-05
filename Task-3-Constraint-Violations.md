# Task 3 — Identify Constraint Violations

## V1 — Barrier Open While Train Is Present

**Constraint:**

`Train_Present → ¬Barrier_Open`

**Violation:**

`Train_Present = TRUE`
`Barrier_Open = TRUE`

**What went wrong?**

A train is present at the crossing, but the barrier is open. This violates the constraint because the barrier must not be open while a train is present.

**How do we know it is violated?**

The condition `Train_Present` is TRUE, but `Barrier_Open` is also TRUE, which contradicts the required condition.

---

## V2 — Barrier Not Closed When Train Is Approaching

**Constraint:**

`Train_Approaching → Barrier_Closed`

**Violation:**

`Train_Approaching = TRUE`
`Barrier_Closed = FALSE`

**What went wrong?**

A train is approaching the crossing, but the barrier is not closed. This creates a risk that road traffic may enter the crossing.

**How do we know it is violated?**

The train is approaching, so the barrier must be closed. However, `Barrier_Closed = FALSE`.

---

## V3 — Warning Lights Not Activated

**Constraint:**

`Train_Approaching → Warning_Lights_ON`

**Violation:**

`Train_Approaching = TRUE`
`Warning_Lights_ON = FALSE`

**What went wrong?**

A train is approaching, but the warning lights are not activated.

**How do we know it is violated?**

The condition requires warning lights to be ON when a train is approaching, but `Warning_Lights_ON` is FALSE.

---

## V4 — Audible Alarm Not Activated

**Constraint:**

`Train_Approaching → Audible_Alarm_ON`

**Violation:**

`Train_Approaching = TRUE`
`Audible_Alarm_ON = FALSE`

**What went wrong?**

A train is approaching, but the audible alarm is not active.

**How do we know it is violated?**

The formal rule requires the audible alarm to be ON when a train approaches, but the alarm is OFF.

---

## V5 — Barrier Open While Train Is Passing

**Constraint:**

`Train_Passing → Barrier_Closed`

**Violation:**

`Train_Passing = TRUE`
`Barrier_Closed = FALSE`

**What went wrong?**

The train is currently passing through the crossing, but the barrier is not closed.

**How do we know it is violated?**

When `Train_Passing = TRUE`, the barrier must be closed. Here, `Barrier_Closed = FALSE`, so the constraint is violated.

---

## V6 — Barrier Opens Before Train Clearance

**Constraint:**

`Barrier_Open → Train_Cleared`

**Violation:**

`Barrier_Open = TRUE`
`Train_Cleared = FALSE`

**What went wrong?**

The barrier has opened even though the system has not confirmed that the train has completely cleared the crossing.

**How do we know it is violated?**

The formal rule requires `Train_Cleared` to be TRUE whenever the barrier is open. Here, the train has not been confirmed as cleared.

---

## V7 — Sensor Failure Without Safe State

**Constraint:**

`Sensor_Failure → Safe_State`

**Violation:**

`Sensor_Failure = TRUE`
`Safe_State = FALSE`

**What went wrong?**

A train-detection sensor has failed, but the system has not entered a safe state.

**How do we know it is violated?**

The rule requires the system to enter a safe state whenever a sensor failure occurs. However, `Safe_State = FALSE`.

---

## V8 — Communication Loss While Barrier Is Open

**Constraint:**

`Communication_Loss → ¬Barrier_Open`

**Violation:**

`Communication_Loss = TRUE`
`Barrier_Open = TRUE`

**What went wrong?**

Communication with the control center has been lost while the barrier is open.

**How do we know it is violated?**

The rule states that communication loss must not result in an open barrier. However, `Barrier_Open = TRUE`, so the constraint is violated.

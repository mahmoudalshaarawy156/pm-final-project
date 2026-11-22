# Competitive Analysis & Journey Map (Module 2)

## Responses
- **Role, who are you solving for? (the specific user segment or profile):** Diego, a delivery driver with three years of experience on the platform who completes dozens of stops daily.
- **Goal, what is this user ultimately trying to achieve?:** Mark each delivery as completed quickly and move on to the next stop.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** Marking a delivery requires navigating three screens, which is difficult when Diego is outdoors holding a package, so he texts his dispatcher instead.
Why this is the moment of misery:

It happens at every stop. Mark Delivered is the last action of every delivery, so the friction repeats dozens of times a day, in the worst conditions (weather, one hand, time pressure).
It ends in a workaround. The app fails at its most basic job, and the driver leaves the product to get it done. That is the visible symptom of the strategic risk in your hook.
A second layer sits underneath. Start Route, which a 6-year driver uses about 30 times a day, is buried beneath features he has never touched (UXR-11, BUG-2079). So the barrier is both slow completion at the doorstep and a hard-to-reach starting point.

One-line version for the form:
Marking a stop delivered takes three taps across three screens, one-handed in the rain, so drivers abandon the app and text their dispatcher instead.

One caution: The research doesn’t show whether the 3-screen flow and the 2-3 level navigation depth are the same path or add up. If you cite both, present them as two related frictions, not a single combined number of steps.
- **External tools, the outside platforms or tools the user is forced to use:** Text messaging to communicate delivery completion to the dispatcher instead of using RouteLogic.
- **The process, the 3 to 5 manual steps the user takes to get the job done:** 1. Delivers the package to the customer.
2. Leaves the RouteLogic app.
3. Opens a messaging conversation with the dispatcher.
4. Sends a message confirming the delivery.
5. Moves to the next stop, leaving the dispatcher to update the delivery status.
- **Core frustration, the exact moment the process feels most “broken”:** Diego struggles to mark a delivery as completed because it requires navigating three screens while holding a package, forcing him to text his dispatcher instead.
- **The evidence, a specific quote or behavior from the research that proves this:** To mark a stop delivered I tap through three screens. In the rain, at a doorstep, with a package in one hand. I've started just texting my dispatcher instead.
“To mark a stop delivered I tap through three screens. In the rain, at a doorstep, with a package in one hand. I’ve started just texting my dispatcher instead.”

This is the strongest single proof point because it contains all three elements of your core frustration in one statement: the three-screen flow, the physical context (rain, doorstep, package in hand), and the resulting abandonment of the app.

Corroborating behavior and data

BUG-2055 (High): “Mark delivered” requires 3 taps across 3 screens, with no single-tap completion. It is logged as the top frontline complaint and is described as driving off-platform workarounds.
UXR-12 (focus group): All seven drivers said speed of core actions matters more than any new feature.

Evidence limits

The quote comes from one driver. BUG-2055 and UXR-12 support the pattern, but neither mentions the doorstep or rain context.
The research does not say how often Diego texts instead of using the app. “I’ve started” signals a growing habit, not a measured rate.

One-line version for the form:
“To mark a stop delivered I tap through three screens. In the rain, at a doorstep, with a package in one hand. I’ve started just texting my dispatcher instead.” (UXR-01, Diego, driver, 3 years)
- **Your journey map, a shareable link, or the map file you committed (e.g. journey-map.html):** https://github.com/mahmoudalshaarawy156/pm-final-project/blob/351c1c04675be4911d01e7dccf990bcf5dfa3f55/02-discovery/Velocity_Future_State_Journey.md

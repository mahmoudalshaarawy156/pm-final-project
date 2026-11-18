# Competitive Analysis & Journey Map (Module 2)

## Responses
- **Role, who are you solving for? (the specific user segment or profile):** Diego, the frontline delivery driver.

I’d pick him over the Ops Manager because Velocity is a speed and simplicity initiative, and the person who feels that problem directly is the one standing at the doorstep. The Ops Manager is the buyer who suffers the consequence (adoption, renewal risk), but they don’t use the core actions themselves. If you solve for Diego, the Ops Manager’s problem is addressed as a result.

Role statement you can paste in:
Experienced delivery drivers (3-6 years on the job) who complete dozens of stops a day, often outdoors and one-handed, and rely on a small set of core actions: Start Route, Mark Delivered, and Report Failed Delivery.

Evidence behind the choice:

BUG-2055 logs the 3-tap, 3-screen Mark Delivered flow as the top frontline complaint, and UXR-01 shows it failing in real conditions.
UXR-11 and BUG-2079 show Start Route (used about 30 times a day) buried under accumulated features.
UXR-12 found all seven drivers in the focus group rated speed of core actions above any new feature.

One caution: Diego’s research quotes cover Mark Delivered and Start Route well, but “report failed delivery” comes from a different participant (UXR-08, a week-2 driver). If you want the segment to include newer drivers, mention that explicitly, since their struggle is learnability rather than speed.
- **Goal, what is this user ultimately trying to achieve?:** Goal: To finish every stop on their route quickly and correctly, with minimal time and attention spent on the app, so the day ends on time and the work is on record.

Why it’s framed this way:

Speed is the stated priority. All seven drivers in the focus group said speed of core actions matters more than any new feature (UXR-12). Diego’s workaround of texting his dispatcher shows he treats the app as a cost to minimize, not a tool he wants to engage with (UXR-01).
“On record” matters too. When completions happen by text, the system of record never gets the update. Drivers want their work to count, but the current flow makes the off-platform route the easier one.
It’s about the route, not the app. Nothing in the research suggests drivers want to use the product more. They want to get through stops efficiently, and the app is either out of the way or in it.

Short version, if you need one line:
Complete each delivery in seconds, one-handed, and move on to the next stop.

One caution: The “on record” part is my inference from the pattern of workarounds, not something a driver said directly. If you want the goal to rest strictly on quoted evidence, keep it to speed and completing the route, and drop the record-keeping clause.
- **Friction, the main barrier (moment of misery) stopping them from succeeding:** Friction: Standing at a doorstep in the rain with a package in one hand, Diego has to tap through three screens just to mark a stop delivered. So he gives up on the app and texts his dispatcher instead (UXR-01, BUG-2055).

Why this is the moment of misery:

It happens at every stop. Mark Delivered is the last action of every delivery, so the friction repeats dozens of times a day, in the worst conditions (weather, one hand, time pressure).
It ends in a workaround. The app fails at its most basic job, and the driver leaves the product to get it done. That is the visible symptom of the strategic risk in your hook.
A second layer sits underneath. Start Route, which a 6-year driver uses about 30 times a day, is buried beneath features he has never touched (UXR-11, BUG-2079). So the barrier is both slow completion at the doorstep and a hard-to-reach starting point.

One-line version for the form:
Marking a stop delivered takes three taps across three screens, one-handed in the rain, so drivers abandon the app and text their dispatcher instead.

One caution: The research doesn’t show whether the 3-screen flow and the 2-3 level navigation depth are the same path or add up. If you cite both, present them as two related frictions, not a single combined number of steps.
- **External tools, the outside platforms or tools the user is forced to use:** External tools Diego is forced to use

Text messaging (SMS or a messaging app) to the dispatcher. This replaces Mark Delivered in the app (UXR-01). It’s the tool most directly tied to Diego’s friction.
Screenshots of the route (phone camera roll). One driver on rural routes captures her stop list every morning as a backup because the app won’t load without signal (UXR-06, BUG-2050). Diego’s quote doesn’t mention this, so it comes from a different driver.
Paper manifests. Five of seven drivers in the focus group carry one “just in case the app dies” (UXR-12), a response to crashes and lost routes (UXR-03, BUG-2031).
Phone calls to the office. When the app crashed mid-route and lost her remaining stops, Elena had the office read the stops to her off a screen (UXR-03). That cost her twenty minutes.

Tools used on the dispatcher side (same pattern, different role)

A WhatsApp group. One dispatcher says they keep it as “the real system” because reassignments take 10-15 minutes to reach drivers (UXR-02, BUG-2044).

What the evidence does and doesn’t support

Only the text to the dispatcher is attributed to Diego himself. The others come from other drivers and dispatchers, so if you present them as Diego’s toolkit, label them as the segment’s behaviors.
The research names no specific text app or platform for the texts, so “SMS or messaging app” is the safe wording.
Your earlier hook mentioned Excel spreadsheets and email. Neither appears anywhere in the research, so I’d leave them out here too.

One-line version for the form:
Drivers fall back on text messages to the dispatcher, route screenshots, paper manifests, and phone calls to the office, while dispatchers run a WhatsApp group as the real system.
- **The process, the 3 to 5 manual steps the user takes to get the job done:** The process: how Diego completes a stop today (manual workaround)

The research documents the trigger (UXR-01) and the outcome, but not a step-by-step log. These steps are reconstructed from UXR-01, BUG-2055 and the related evidence, so label them as inferred if you cite them.

Finish the delivery at the doorstep. He hands over or leaves the package, often in the rain with one hand occupied (UXR-01).
Skip the in-app Mark Delivered flow. Three taps across three screens isn’t workable one-handed at a doorstep (BUG-2055), so he doesn’t start it.
Text the dispatcher that the stop is done. This replaces the app as the way the completion gets reported (UXR-01).
Move on to the next stop without updating the app, so that stop’s status in the system stays unchanged.
Dispatcher records it manually, or doesn’t. The research doesn’t say which. If it isn’t recorded, the dashboard shows “in progress” for a stop delivered hours earlier (UXR-09, BUG-2072), though those reports blame propagation delay rather than off-platform completion.

What the evidence supports:

Steps 1-3 rest directly on UXR-01 and BUG-2055.
Steps 4-5 are inference. No participant describes what happens to the app’s record or what the dispatcher does with the text.

One-line version for the form:
Finish the delivery, skip the three-screen flow, text the dispatcher, and move on, leaving someone else to update the record.
- **Core frustration, the exact moment the process feels most “broken”:** Core frustration: the doorstep moment, when the app asks for three taps across three screens and Diego has one hand free.

He has just finished the delivery, the package is out of his hand or still in it, it is raining, and the only thing left is to record it. This is where the product breaks its own purpose. The action that should take a second demands his full attention, so he drops the app and texts his dispatcher instead (UXR-01, BUG-2055).

Why this is the “most broken” moment:

It is the point of failure, not a slow background annoyance. The friction lands at the exact instant he has the least attention and the least free hand to give.
It ends in abandonment. He doesn’t just grumble and push through, he leaves the product for the most basic job it has.
It repeats at every stop. Mark Delivered closes out every delivery, so the broken moment recurs dozens of times a day.

Evidence limits:

The wording “one hand free” is my paraphrase of UXR-01, where Diego describes having a package in one hand. The research doesn’t say how many hands are free at the moment he taps.
The quote is from a single driver, though BUG-2055 logs the same flow as the top frontline complaint.

One-line version for the form:
At the doorstep, in the rain, with a package in hand, marking a stop delivered takes three taps across three screens, so he gives up and texts the dispatcher.
- **The evidence, a specific quote or behavior from the research that proves this:** Primary evidence: UXR-01 (Diego, delivery driver, 3 years)

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
- **Your journey map, a shareable link, or the map file you committed (e.g. journey-map.html):** https://github.com/mahmoudalshaarawy156/pm-final-project/blob/3bfebda8386ebb304356a9d9aaea848b0a2204a7/02-discovery/diego_future_state_journey.md

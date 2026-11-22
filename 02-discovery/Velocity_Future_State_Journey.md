# Velocity Future State: Diego's Journey

**Persona:** Diego, a delivery driver with three years on the platform who completes dozens of stops daily.
**Goal:** Mark each delivery as completed quickly and move on to the next stop.
**Friction:** Marking a stop delivered takes three taps across three screens, one-handed in the rain, so drivers abandon the app and text their dispatcher instead.
**Strategy:** Reclaim operational simplicity by stripping away legacy noise and ensuring the tool is the fastest for everyday work.

*Diego's emotional states below are inferred from his research quotes, not observed.*

## Timeline

```
1 Launch  ->  2 Arrive  ->  3 Complete  ->  4 Advance
Tap Start     See stop      Tap Delivered   Next stop loads
Route         card
   |             |              |               |
Start Route   Failed          3 taps across   Silent uploads,
buried        delivery        3 screens       stale status
              hard to find
```

## Stages

### 1. Launch
- **User Action:** Opens the app and taps Start Route from the home screen.
- **Internal State:** In a hurry, expecting the app to be ready immediately.
- **Pain Point Addressed:** Start Route is buried under newer features (UXR-11, BUG-2079).
- Pin Start Route to home -> Diego begins routes without hunting through menus.
- Remove rarely used clutter from the frontline view -> core actions stay visible.

### 2. Arrive
- **User Action:** Reaches the stop and sees one clear stop card.
- **Internal State:** Attention on the package and the weather, not the screen.
- **Pain Point Addressed:** Key functions, such as "report failed delivery," are hard to find (UXR-08, BUG-2090).
- Show Delivered and Failed Delivery on the stop card -> no menu digging at the door.
- Use large, thumb-friendly targets -> one-handed use works in rain.

### 3. Complete
- **User Action:** Taps Mark Delivered once.
- **Internal State:** Time pressure and one hand occupied, wanting it done now.
- **Pain Point Addressed:** Three taps across three screens (UXR-01, BUG-2055).
- Replace the 3-screen flow with one tap -> Diego stays in the app.
- Keep the action in-app -> no text to the dispatcher is needed.

### 4. Advance
- **User Action:** Sees confirmation and the next stop loads automatically.
- **Internal State:** Wants assurance it worked so he can move on without retrying.
- **Pain Point Addressed:** Silent photo failures and stale dispatcher status (BUG-2061, BUG-2072).
- Show clear success or queued-retry status -> Diego stops retaking photos.
- Push status to the dispatcher board promptly -> the board becomes trustworthy again.

## Three Competitive Advantages Over the Manual Workaround

1. **Faster completion:** One tap replaces app-switching and typing -> less time at every doorstep.
2. **Structured record:** Status and proof of delivery go into the platform -> data is complete and auditable.
3. **No reconciliation:** Status updates automatically -> dispatchers stop re-keying free-text messages.

## Caveats

- **Stage 4 needs backend work.** Fixing the dispatcher lag (BUG-2072) is a separate technical cause from the Mark Delivered redesign, so it shouldn't be credited to the UX change alone.
- **The value prop mentions "coordinators."** This journey is Diego's, so the coordinator benefit shows up indirectly in Stage 4 and in Advantages 2 and 3.
- **Keep the two frictions separate.** Stage 1 (navigation depth) and Stage 3 (three taps across three screens) are related, but the research doesn't show they add up to one step count.

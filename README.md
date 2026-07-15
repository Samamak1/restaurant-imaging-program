# restaurant-imaging-program

Case study: a daily-hold plus weekday deep-clean rotation with photo accountability, designed for a store in a national quick-service restaurant chain by Sama Mushtaq, the restaurant manager, after the store failed the company's periodic standards audit. The sanitized program document is in `PROGRAM.md`.

## The problem

In June the store went through the company's periodic standards audit, covering cleanliness, food safety, and regulatory items. Three sections came back at failing level: Clean, Food Safety, and Regulatory, with approximate scores in the mid-60s to low-70s percent range. Exact scores and the assessment document itself are corporate material and are not published here.

Reading the line items, the failures clustered into two patterns:

1. Daily upkeep items scored zero for "not maintained throughout the shift" - self-serve station, restrooms, dining room, exterior. These fail because no one owns them every day.
2. Repeat findings from prior walks - hood vents and ansul pipes, baffles, fryer surrounds, the ice machine, inverted pan storage, the self-serve station. These fail because there is no rotation that ever reaches them.

Two different failure modes need two different mechanisms, which is how the program is structured.

## The program

RI stands for Restaurant Imaging, the company's term for how the restaurant presents. The program:

- A dedicated RI lead (a crew member; name withheld in this copy) owns an 8:00a to 12:00p block on five weekdays (Wed, Thu, Fri, Mon, Tue). The block is carved out of production coverage by the crew scheduler (see the `crew-scheduling-engine` repo in this portfolio).
- Daily Hold, about 45 to 60 minutes, every RI day: the "not maintained" zero items are reset first, before the lunch push.
- Rotating deep-clean, roughly 3 hours: each weekday targets a fixed zone group chosen from the audit's worst findings. Wednesday is cook line and hoods; Thursday is CIP, ice machine, and dry storage; Friday is walk-ins and storage; Monday is drive-thru, entrances, and dining; Tuesday is CIP again plus self-serve deep, restroom deep, and dish reset.
- CIP (the ketchup-dispenser line clean) runs twice a week, Tuesday and Thursday, inside the block.
- Saturday and Sunday the RI lead is off; the manager on duty runs the Daily Hold only.

## The accountability loop

- Photo accountability: the RI lead photographs each completed deep-clean zone, before and after, and sends them to the leader at the end of the block.
- Roll-forward rule: any zone that cannot be finished rolls to the next same-day-of-week rotation and gets flagged to the manager on duty.
- Monthly re-walk: the audit line items are re-walked monthly. Items that hold move into the Daily Hold; the next-lowest scores enter the rotation. The rotation is designed to shrink as sections clear.

## Why the layout looks like this

- The heaviest repeat and zero-score items sit on weekdays when the RI lead owns the block, not left to the weekend skeleton crew.
- Daily-owner items and rotation items are kept separate because they fail for different reasons.
- Each day fits the window: about 1 hour of hold plus about 3 hours of one zone group, done before lunch.

## What is in this repo

- `README.md` - this case study.
- `PROGRAM.md` - the program document, sanitized: the RI lead's name is replaced with a role label, exact audit scores and assessment dates are redacted, one conversational line was neutralized. No corporate documents, including the audit itself, are included.

## Context

Designed and run by a working restaurant manager for his own store; drafted with AI assistance and edited against the actual audit findings. The scheduling side lives in `crew-scheduling-engine`, which reserves the RI block in the weekly schedule and marks CIP mornings on the crew grid.

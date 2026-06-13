# Mind the Gap: Experience-Dependent Calibration of Action Boundaries in Wheelchair Navigation

Mahdis Dadfar, Tarcísio Moreira, Paula Silva, Tehran Davis, and Kevin Shockley



## Overview

This project investigates how novice wheelchair users calibrate their action boundaries when navigating a closing gap. We asked whether the history of recent actions (pass-through vs. steer-around) shapes where participants place their behavioral transition boundary, and how that changes with practice.

Passability was defined by the ratio Vmin/Vcap, where 1.0 is the just-passable boundary. Participants completed a virtual closing-gap task across two blocks. Sequences were either ascending (gap narrowing, passability disappearing) or descending (gap widening, passability emerging). The main question was whether the transition boundary differs depending on which direction you arrive at it from, and whether that pattern shifts with experience.

## Analysis Pipeline

**Step 1: Raw data extraction 

Raw trial files exported from Unity were organized and merged into a single processed CSV with one row per trial. This script only needs to run once. All subsequent analyses use the processed file, not the raw Unity exports.

**Step 2: Transition point analysis 

The processed CSV was used to estimate the action boundary for each participant, block, and scaling direction. Two boundary methods were used: a rule-based approach requiring stable response patterns before and after the transition, and a logistic fit approach estimating the point of subjective equality. Diagnostic plots were generated for each ascending-descending pair.

**Step 3: Statistical analysis 

Action boundaries were analyzed using a linear mixed-effects model with block, scaling direction, and their interaction as fixed effects, and participant as a random intercept. Follow-up tests examined whether boundaries deviated from 1.0, whether ascending and descending boundaries differed within each block, and how that difference changed across blocks.

## Results

![Action Boundary by Block and Direction]

In Block 1, descending action boundaries were higher than ascending ones, consistent with enhanced contrast. Participants transitioning from steer-around mode switched to pass-through earlier than expected. This pattern was significant (p = .028) and is consistent with reduced stability of the steer-around mode early in wheelchair experience.

![Ascending minus Descending Difference Score]

By Block 2 the direction-dependent difference was no longer significant (p = .183), and the change across blocks was significant (p = .011). The steer-around mode appeared to stabilize with practice.

![Model-Estimated Action Boundaries]

The descending boundary in Block 2 was significantly below 1.0 (p = .003), suggesting participants became more conservative with experience, choosing to steer around even at ratios that were nominally passable.


## References

Alt, J. M., Kiefer, A. W., MacPherson, R., Davis, T. J., & Silva, P. L. (2021). The effect of navigation demand on decision making in a dynamic, sport-inspired virtual environment. Journal of Sport & Exercise Psychology, 43(5), 375–386.

Dotov, D. (2013). Positive hysteresis, negative hysteresis, and oscillations in visual perception. Dissertation.

Fajen, B. R., & Mathis, J. S. (2011). Direct perception of action-scaled affordances: The shrinking gap problem. Journal of Experimental Psychology: Human Perception and Performance, 37(5), 1442–1457.

Fitzpatrick, P., Carello, C., Schmidt, R. C., & Corey, D. (1994). Haptic and visual perception of an affordance for upright posture. Ecological Psychology, 6(4), 265–287.

Lopresti-Goodman, S. M., Turvey, M. T., & Frank, T. D. (2011). Behavioral dynamics of the affordance "graspable." Attention, Perception, & Psychophysics, 73, 1948–1965.

Lopresti-Goodman, S. M., Turvey, M. T., & Frank, T. D. (2013). Negative hysteresis in the behavioral dynamics of the affordance "graspable." Attention, Perception, & Psychophysics, 75(5), 1075–1091.
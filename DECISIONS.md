# Decision Points

## DP1 · The Nudge

When a user crosses their weekly CO₂ target, PlanetPulse shows a clear but friendly warning instead of shaming or blocking them. It explains that the target has been exceeded and encourages the user to make lower-impact choices for the remaining days of the week. I chose this approach because the purpose of the app is to build awareness and better habits, not make users feel guilty about their everyday decisions.

## DP2 · Absurd Input

If a user enters an obviously unrealistic value, such as a 500,000 km car journey, PlanetPulse does not silently accept it or include it in the footprint calculation. The app flags the entry as unusual and asks the user to review or correct the quantity before saving it. This keeps the dashboard trustworthy while still allowing users to enter legitimate but unusually large activities when needed.

## DP3 · The Week


PlanetPulse defines a week as Monday through Sunday, with the weekly target and progress resetting at the start of each Monday. The dashboard shows how much of the weekly target has already been used and how much remains for the rest of the week. I chose this structure because it is simple, familiar, and makes it easy for users to understand their progress from the beginning to the end of each week.

It provides API endpoints such as:

/api/health
/api/factors
/api/activities
/api/target
/api/stats
/api/calculate
/api/reset
DELETE /api/activities/{id}
YES — Standard API implemented.

However, there is an important distinction: our current frontend (app.js) uses browser-side/localStorage logic rather than calling those API endpoints. So the API exists, but the deployed frontend and API are not currently integrated.

If the hackathon's grading system expects the standard API itself to be publicly reachable, we will need to deploy the Python server as well rather than relying only on GitHub Pages.

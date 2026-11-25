# TAM attendance automation template

Use one copy for **Clock In** and a second copy for **Clock Out**. Replace every bracketed field and schedule each automation in Codex.

## Prompt

At [SCHEDULE] in [TIMEZONE], use my own authorized Chrome session in [CHROME PROFILE] for the [Clock In or Clock Out] action on [WORKING DAYS]. Submit only when I am actually starting or ending work, as applicable, and only within [ALLOWED LOCAL SUBMISSION WINDOW]. Use [HOLIDAY AND LEAVE RULES]. Skip if eligibility is unknown, I have asked to skip, the original scheduled date has passed in [TIMEZONE], or there is already a recorded or attempted punch of this type for that occurrence.

Navigate from [SUCCESSFACTORS START URL] to [TAM MENU LABEL]. Before submitting, verify that the browser is on [EXPECTED TAM ORIGIN], that the visible session belongs to me, and that the action is the exact control configured above. If Microsoft or the attendance system asks for sign-in or MFA, leave the page open for me and report that the run is blocked until I sign in. Recheck eligibility and timing if I resume the run.

Submit one punch at the actual current time. Read the resulting status. Report the actual local time and whether TAM confirmed the punch, queued it for sync, gave an unclear result, or prevented submission. If submission may already have occurred, end the run without repeating it. Use the automation chat for the result.

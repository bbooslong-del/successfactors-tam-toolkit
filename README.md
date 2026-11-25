# SuccessFactors and TAM toolkit

This download contains a Chrome extension that refreshes the SuccessFactors home tab and a Codex automation template for WorkForce Software Time & Attendance (TAM) clock-in and clock-out. The two components can be used independently.

## Install the Chrome extension

1. Download and extract the ZIP.
2. In the Chrome profile you use for work, open `chrome://extensions`.
3. Turn on **Developer mode**, choose **Load unpacked**, and select the extracted `extension` folder.
4. Sign in to SuccessFactors normally. Keep a Chrome window open in that profile and keep the computer awake.

The extension reloads an existing home tab every five minutes. If the tab is closed, the next scheduled check opens it in the background. Chrome must be running. If sign-in is required, complete it in Chrome.

The included build targets the SAP SuccessFactors data center at `performancemanager10.successfactors.com`. If your employer uses another data center, replace that hostname in both `extension/manifest.json` and `extension/refresh.js` with the hostname of your actual SuccessFactors home page, then reload the extension. Deployments that use other home paths also need to adjust the match in `refresh.js`. Use only your employer’s authorized SuccessFactors address.

## Set up TAM clock-in and clock-out

Use this template where your employer permits automated attendance submissions. Each employee sets up their own schedules and signs in to their own work account.

1. In Codex, first run a read-only check to verify your Chrome profile, TAM URL, navigation labels, and clock controls.
2. Create two recurring automations. Copy `tam-automation-template.md` into each and fill in all placeholders, including the action, timezone, working days, and allowed submission window. Set the actual recurrence in Codex.
3. Enable the schedules after you verify they match your attendance rules. Review the reported result after the first authorized scheduled punch.

TAM needs Codex with Chrome access and an available signed-in work session. It may still ask you to authenticate manually. Turn results appear in the automation chat. The refresh extension runs in Chrome without ChatGPT model calls.

## Repository contents

- `extension/` contains the standalone Chrome extension.
- `tam-automation-template.md` is a setup template for Codex. It does not install or activate a schedule by itself.

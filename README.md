# Fix My Road demo repo (AI Expo Africa 2026)

Demo starting state: index.html is the deliberately bad "Form RD-7" portal.
The hero work item (POT project) describes the fix. During the demo, Claude
codes the fix via MCP and the PR replaces index.html with the new mobile-first
app (fix-my-road.html in /reference, kept out of the deploy path).

## Setup
1. Create a GitHub repo, push this folder.
2. Import to Vercel (framework: Other, no build step, output dir: root).
3. Confirm merge-to-live is under 2 minutes before relying on it on stage.
4. Install "GitHub for Jira" and connect the repo to project POT on smartergroup.

## Demo flow
- Big screen opens on the live broken site (scroll it, let it hurt).
- Loom complaint -> work item -> drag to Claude Code column.
- Claude PR swaps index.html for the new app. Merge on stage. Refresh.

## Reset after each run
Revert the merge commit (git revert HEAD && git push) so the site is broken
again for the next audience.

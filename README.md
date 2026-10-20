[![Site check](https://github.com/ahammondspcx-gis/global-monitoring/actions/workflows/check.yml/badge.svg)](https://github.com/ahammondspcx-gis/global-monitoring/actions/workflows/check.yml)

# global-monitoring
Checks the Global website every 4 hours and posts the status to Slack. 

**Global Site Monitor**: A GitHub Actions workflow that checks the Global website every 4 hours (00:00, 04:00, 08:00, 12:00, 16:00, 20:00 UTC). 

If the site responds, it posts a :white_check_mark: “up” message to #spx-monitoring in Slack. 
If the site fails 3 tries in a row, 30 seconds apart, it posts a :rotating_light: “DOWN” alert, and the run shows red in GitHub. 

The site address and Slack webhooks are stored as repository secrets (SITE, SLACK_GA_MONITORING, SLACK_WEBHOOK_GA). 

To run it manually, go to Actions → Site check → Run workflow.

# Deliverability Dashboard

A self-contained, single-file HTML dashboard for tracking email inbox placement
across a multi-account, multi-lane warm-up program (built for the AI Work
sender-reputation pipeline).

## Features

- **Filters** - account, sender/channel, and rolling time window (7 / 30 / 90 days)
- **Key metrics** - total emails checked, spam rate, deliverability rate, primary
  placement rate, unique accounts seen, silent accounts (vs. an editable expected
  count), days tracked, avg emails/account
- **Inbox - channel breakdown** - stacked bar of Primary/Updates/Promotions/Social/
  Forums/Spam per sending lane, plus a category doughnut with percentage labels
- **Trends** - daily inbox vs. spam volume, and a spam-rate trend line
- **Spam rate by account** - sorted bar chart, worst offenders first
- **Account Health** and **Channel Detail** tables - sortable
- **Dark / light mode** toggle
- **Refresh** button to reset filters and re-render



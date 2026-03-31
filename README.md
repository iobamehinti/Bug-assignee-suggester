# 🎯 DEFT Bug Assignee Suggester

> AI-powered triage tool for the DEFT project · ICS Data Science & Analytics

---

## Overview

The **DEFT Bug Assignee Suggester** helps ICS DSA team members quickly identify the right person to assign a DEFT bug to. It analyzes historical resolution patterns across the DEFT Jira project and uses AI to surface a confident, evidence-backed recommendation — along with an alternative option.

---

## Features

- 🔍 **Auto-fetches ticket details** from Jira using the DEFT project cloud ID
- 📚 **Searches historical DEFT bugs** to find similar resolved issues and who fixed them
- 🧠 **AI-generated recommendation** with confidence level (High / Medium / Low), reasoning, and supporting evidence
- 🥈 **Alternative assignee** suggestion when the primary match is uncertain
- ✏️ **Refine mode** — provide additional context (e.g. "John is OOO") to update the suggestion without re-fetching the ticket
- 📌 **Quick references** panel with one-click access to key resources

---

## How to Use

1. **Enter a DEFT ticket key or URL** in the input field
   - Accepted formats: `DEFT-109` or `https://jira.cloud.intuit.com/browse/DEFT-109`
2. Click **Suggest Assignee →** (or press `Enter`)
3. The tool runs three steps automatically:
   - Fetches ticket details from Jira
   - Searches for similar resolved DEFT bugs
   - Generates an AI recommendation
4. Review the **Primary Recommendation**, confidence level, and supporting evidence
5. Optionally use the **Refine Recommendation** panel to adjust based on additional context

---

## Refining a Recommendation

After a suggestion is generated, you can type a constraint or context into the **Refine** box and hit **Refine →**. Examples:

- `"Exclude Sarah, she's on PTO this week"`
- `"Focus on engineers with backend experience"`
- `"This is a P1 — who handles high-priority incidents?"`

The tool will update the recommendation without re-fetching ticket data.

---

## Quick References

| Resource | Link |
|---|---|
| 👤 Bug Management Driver | Isaac Obamehinti |
| 📊 Bug Management Process Deck | [ICS DSA Bug Management Slides](https://docs.google.com/presentation/d/1u126YMn9TBgWqDFLrx7HWOgoiJLOvkxw6IcfParS9OM/edit?usp=sharing) |
| 📖 DEFT Wiki | [ICS DSA Bug Management Process](https://wiki.cloud.intuit.com/wiki/spaces/ICSDR/pages/340657930/ICS+DSA+Bug+Management+Process+New+process+as+of+Jan+2026) |
| 💬 Slack Channel | [#ics-dsa-deft-bugs](https://intuit.enterprise.slack.com/archives/C07TK2ZQULB) |
| 📅 Daily Triage Sync | 8:30 – 9:00 AM · [Zoom Link](https://intuit.zoom.us/s/92628817605?pwd=YtxrtBjbuJ8vq30GG3u9IHgsfAhXnR.1&from=addon#success) |

---

## How It Works

```
User enters DEFT ticket key
        ↓
Fetch ticket details from Jira (via Atlassian MCP)
        ↓
Search similar resolved DEFT bugs (via Atlassian MCP)
        ↓
AI analyzes patterns → generates assignee recommendation
        ↓
Display: Primary, Alternative, Evidence, Caveat
        ↓
(Optional) User refines → AI updates recommendation
```

---

## Technical Details

| Property | Value |
|---|---|
| Built with | React (Claude Artifact) |
| AI Model | `claude-sonnet-4-20250514` |
| Jira Integration | Atlassian MCP (`mcp.atlassian.com`) |
| DEFT Cloud ID | `f8519793-3215-4b8b-9f9a-3c66dd15afc5` |
| Hosted in | Claude.ai Artifact |

---

## Limitations

- Recommendations are based on **historical patterns** and may not reflect current team capacity or availability
- AI suggestions should be treated as a **starting point**, not a final decision
- Always verify assignee availability before assigning
- The tool does not write back to Jira — assignment must be done manually

---

## Feedback & Support

Questions or suggestions? Reach out via Slack:
**[#ics-dsa-deft-bugs](https://intuit.enterprise.slack.com/archives/C07TK2ZQULB)**
or contact **Isaac Obamehinti** (Bug Management Process Driver) directly.

---

*ICS Data Science & Analytics · DEFT Bug Triage Tool*

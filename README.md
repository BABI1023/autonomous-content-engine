# autonomous-content-engine

```markdown
# ⚡ Autonomous Social Media Content Engine

> Transform raw news links into structured, high-signal LinkedIn insights in under 120 seconds using n8n and Google Gemini.

---

## 📌 Workflow Architecture

![n8n Canvas Workflow](workflow-canvas.jpg)

This repository hosts an event-driven n8n workflow that automates content research and multi-channel publishing:

1. **Ingestion Layer:** Monitors a designated Google Sheet via `Google Sheets Trigger` for incoming news links.
2. **Cognitive Synthesis:** Passes raw link text to **Google Gemini 1.5 Pro** (`Summarize News Article`) for context extraction.
3. **Content Adaptation:** Passes the condensed summary to a second Gemini LLM chain (`Generate Linkedin Post Content`) tailored for professional engagement.
4. **Automated Publishing:** Dispatches the final formatted post directly to the **LinkedIn API**.

---

## 🚀 Quick Start & Import Instructions

### Prerequisites
* A running **n8n** instance
* **Google Cloud Console** OAuth 2.0 Credentials (for Google Sheets Trigger)
* **Google AI Studio API Key** (for Gemini nodes)
* **LinkedIn Developer App** with posting permissions (`w_member_social`)

### Import Workflow
1. Download or copy the `workflows/automated-social-media-content-generation.json` file in this repo.
2. In your n8n workspace, navigate to **Workflows → Import from File** (or paste into canvas).
3. Re-bind your account credentials to the imported nodes.
4. Save and toggle the workflow state to **Active**.

---

## 📊 Performance Metrics

| Metric | Manual Process | Autonomous Engine |
| :--- | :--- | :--- |
| **Execution Time** | 35–45 Minutes | **< 2 Minutes** |
| **Human Effort** | High (Drafting & Formatting) | **Zero (Paste Link Only)** |
| **System Reliability** | Probabilistic | **Deterministic DAG Execution** |

---

## 📜 License
Distributed under the MIT License.

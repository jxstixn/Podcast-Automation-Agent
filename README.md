# 🎙️ Podcast Automation Agent

This repository contains the **system prompts** and **n8n workflow**
definitions for the **Podcast Automation Agent**, which orchestrates
podcast-related social media content creation across platforms.

It is designed as the **core agent layer** for our university project on
podcast content automation.

------------------------------------------------------------------------

## 📂 Project Structure

    .
    ├── Generate Instagram Posting Image Workflow.json
    ├── Layperson Study.pdf
    ├── Study Workflow.json
    ├── System-Prompt-Orchestrator.md
    ├── System-Prompt-Instagram-Agent.md
    ├── System-Prompt-Instagram-Image-Generator.md
    ├── System-Prompt-LinkedIn-Agent.md
    └── System-Prompt-X-Agent.md

### Files

-   **System-Prompt-Orchestrator.md** → Main orchestration agent,
    manages podcast listing/creation and routes tasks to sub-agents.
-   **System-Prompt-Instagram-Agent.md** → Generates and manages
    Instagram captions & posts.
-   **System-Prompt-Instagram-Image-Generator.md** → Translates post
    texts into detailed English prompts for **DALL·E 3**.
-   **System-Prompt-LinkedIn-Agent.md** → Creates and updates LinkedIn
    posts for podcast promotion.
-   **System-Prompt-X-Agent.md** → Writes structured 3-part X (Twitter)
    threads.
-   **Generate Instagram Posting Image Workflow.json** → n8n workflow
    for turning German podcast text into Instagram-ready images.
-   **Study Workflow.json** → Example n8n workflow for our conducted
    study.
-   **Layperson Study.pdf** → Blueprint for the layperson study conducted
    for this project.

------------------------------------------------------------------------

## 🚀 Features

-   **Cross-platform automation** (Instagram, LinkedIn, X/Twitter)\
-   **Agent-based architecture** (each platform has its own dedicated
    prompt)
-   **Central Orchestrator** ensures consistency and intent-based
    workflows
-   **Image automation**: Converts German-language podcast captions into
    **DALL·E 3 image prompts**
-   **n8n integration** for workflow automation and database syncing

------------------------------------------------------------------------

## 🧩 How It Works

1.  **Podcast Orchestrator**
    -   Validates podcast references (`podcastId`)
    -   Handles podcast creation & metadata management
    -   Dispatches social posting tasks to sub-agents
2.  **Platform Agents**
    -   **Instagram Agent** → captions + optional images
    -   **LinkedIn Agent** → thought-leadership style posts
    -   **X Agent** → concise 3-tweet threads
3.  **Image Generator**
    -   Translates German podcast content into **visual prompts**
    -   Generates Instagram-ready images with **DALL·E 3**
4.  **n8n Workflow**
    -   Automates execution of the image generation pipeline
    -   Updates Airtable database with generated media

------------------------------------------------------------------------

## ⚙️ Usage

This repository is not a standalone app --- it provides **system prompts
and workflows** that plug into your existing **n8n environment**.

1.  Import the **workflow JSON** into your n8n instance.
2.  Add the system prompts into your LLM-powered agent orchestration
    layer.
3.  Connect to your podcast transcription + Airtable database.
4.  Run automations via WhatsApp/n8n trigger (as defined in
    orchestrator).

------------------------------------------------------------------------

## 🧑‍🎓 Notes

-   Language: **German (de-DE)** for all final outputs.
-   Supported social platforms: **Instagram, LinkedIn, X/Twitter**.
-   All content changes are **tool-synced** before final output (ensures
    database consistency).
-   Images are **generated only on request** or for new posts.

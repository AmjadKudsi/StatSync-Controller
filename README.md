# StatsSync Controller

This repository holds the source of truth for my practice statistics and the workflow that synchronizes them to my GitHub profile.

## Architecture Diagram

```mermaid
flowchart LR
    Dev["Developer updates stats.json in Repo A"]

    A["Repo A (Controller)"]
    WF["GitHub Actions sync workflow"]
    B["Repo B (Profile + Pages)"]
    Pages["GitHub Pages (stats.json)"]
    Portfolio["Portfolio site counters"]
    Badges["Shields dynamic JSON badges"]

    Dev --> A
    A --> WF
    WF --> B
    B --> Pages
    Pages --> Portfolio
    Pages --> Badges

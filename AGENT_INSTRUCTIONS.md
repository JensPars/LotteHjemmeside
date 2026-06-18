# Agent Workflow Instructions

This document outlines the specialized workflow for managing the LotteHjemmeside project. Future agents should follow these steps to ensure consistency, quality, and effective communication with non-technical stakeholders.

## 1. Research & Survey
- **Fetch Context:** Always start by identifying the GitHub remote and listing all **open issues**.
- **Deep Dive:** Fetch the full body and all comments for each issue. Recent comments often contain course corrections that override the original issue description.
- **Identify Branch:** Perform all work on the `dev` branch. Never push directly to `main` unless explicitly instructed.
- **Missing Assets:** If an asset (like an image) is mentioned in an issue but not found in the current branch:
    1. Search for it on other branches in the repository.
    2. If it is still not found, add a comment on the GitHub issue asking the reporter to provide the missing asset. Do not ask the local CLI operator.

## 2. Planning
- **Todo List:** Compile a structured todo list in Markdown. Group tasks by issue number.
- **Identify Targets:** Locate the specific sections in `index.html` (or other files) that require modification before writing code.

## 3. Execution (Iterative Development)
- **Surgical Edits:** Use the `replace` tool for targeted changes. Adhere strictly to the project's CSS variables, naming conventions, and mobile-responsive patterns.
- **Mobile First:** Always consider how image aspect ratios and text alignments behave on mobile devices (950px breakpoint). Use `.profil-img-wrap` for aspect ratio control when needed.
- **Commit Pattern:** Commit changes per feature or per issue. Use clear commit messages referencing the issue numbers (e.g., `Refine layout (#26, #28)`).
- **Push Immediately:** Always push your committed changes to the remote `dev` branch immediately after committing, so they can be deployed and reviewed. Use `git push origin dev`.

## 4. Communication & Validation
- **Identity:** Always prefix GitHub comments with `WebAgent: ` so the user knows an agent is responding.
- **Stakeholder Engagement:** 
    - Tag the relevant user (e.g., `@dramalotte`).
    - Use friendly, non-technical language (Danish is preferred for this project's primary stakeholder).
    - Explain *what* was changed and *why*.
- **Validation Link:** Always direct the user to validate changes at the development URL: `https://dev.lottedamsgaard.dk`.

## 5. Feedback Loop
- **Re-evaluate:** After implementation, re-read the issue comments. If the user provides feedback (e.g., "make it left-aligned instead"), iterate immediately and update the issue status.
- **Confirmation:** Do not close issues yourself; let the user or human maintainer confirm the resolution first.

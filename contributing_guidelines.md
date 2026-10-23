# Contributing to LinkCraft

First off, thank you for considering contributing to LinkCraft! It's people like you that make open-source tools great. We welcome all contributions, from fixing typos to building core features.

## 🧠 Architecture & Folder Structure

LinkCraft uses the [Plasmo Framework](https://docs.plasmo.com/) to handle Manifest V3 extension wiring. To keep our codebase clean and prevent bugs, please adhere to this structure:

*   **`popup.tsx`**: The main UI that opens when clicking the extension icon. Keep logic minimal here; focus on React UI/UX.
*   **`contents/`**: Put all LinkedIn DOM scraping scripts here (e.g., `contents/linkedin-scraper.ts`). These scripts run *inside* the active web page.
*   **`background/`**: Service worker scripts go here (e.g., `background/index.ts`). Use this for heavy background tasks that don't need a UI.
*   **`utils/`**: Pure typescript functions and helpers go here (e.g., `utils/google-dork.ts`, `utils/gemini-api.ts`). These should be framework-agnostic, have no DOM dependencies, and be highly testable.

## 🌿 Branching Strategy

Please do not commit directly to the `main` branch. Create a new branch for every feature or bug fix:
*   **Features:** `feature/short-description` (e.g., `feature/alumni-highlighter`)
*   **Bug Fixes:** `bugfix/short-description` (e.g., `bugfix/fix-dork-quotes`)
*   **Documentation:** `docs/short-description` (e.g., `docs/update-readme`)

## 💬 Commit Messages

We follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/). Please prefix your commits so they are easy to read in the history:
*   `feat: add coffee chat prompt templates`
*   `fix: resolve DOM selector issue on profile page`
*   `docs: update README with new setup instructions`
*   `style: format UI with Tailwind classes`

## 🚀 Pull Request Process

1.  Ensure your code builds locally without errors by running `npm run build`.
2.  Push your branch to your fork and open a Pull Request against our `main` branch.
3.  Fill out the provided PR template. Link the PR to any relevant open issues (e.g., "Closes #12").
4.  A maintainer will review your code. We require at least one approval before merging.
5.  Be responsive to feedback! We might ask for minor tweaks to fit the project's style.

## ⚠️ Safe Scraping Rules

When contributing to `contents/` scripts, remember that we simulate human behavior to respect platform limits. 
* **Do not** write loops that rapid-fire requests. 
* Always use standard DOM querying (`document.querySelector`) with optional chaining.
* Make sure your code fails gracefully if LinkedIn updates its UI layout.
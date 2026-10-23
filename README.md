
# 🚀 LinkCraft

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Framework: Plasmo](https://img.shields.io/badge/Framework-Plasmo-purple)](https://docs.plasmo.com/)

**LinkCraft** is an open-source Chrome Extension designed to supercharge LinkedIn networking. By combining intelligent DOM scraping, advanced Google Dorking, and local AI integration (via Google Gemini), LinkCraft allows users to discover targeted profiles and generate hyper-personalized connection requests instantly—without compromising their API credentials.

This tool is built with a special focus on helping **college students, recent graduates, and job seekers** scale their networking, secure coffee chats, and connect with university alumni effectively.

---

## ✨ Features

### 🛠 Core Capabilities
* **Intelligent Profile Scraping:** Safely extracts public profile data (name, title, bio, location) directly from the LinkedIn DOM.
* **Gemini AI Invite Generator:** Automatically drafts highly personalized connection notes based on the scraped profile data.
* **Secure Offline Storage:** The user's Gemini API key is securely encrypted and stored entirely offline on their device using `chrome.storage.local`.
* **Bulk Keyword Search (File Parsing):** Upload a CSV or JSON of target keywords (e.g., specific skills, companies) to quickly highlight or filter matching connections.
* **Google Dorking Engine:** A built-in utility that generates advanced Google Dork search strings (e.g., `site:linkedin.com/in/ "software engineer" "hiring"`) to bypass LinkedIn's native search limitations.

### 🎓 College Student & Job Seeker Toolset
* **Alumni & Recruiter Highlighter (New):** Automatically scans profiles and search results to highlight users who attended the same university or hold "University Recruiter" titles.
* **Student Prompt Library (New):** Pre-loaded, context-aware Gemini AI templates optimized for students (e.g., "Ask for a Coffee Chat," "Internship Referral Request," "New Grad Advice").
* **Connection Tracker Export (New):** Save targeted recruiter or alumni profiles locally and export them to a structured CSV file for use in job tracking platforms like Notion or Excel.

---

## 🏗 Architecture & Tech Stack

LinkCraft is built on a modern, contributor-friendly stack. We utilize **Plasmo** to abstract away the boilerplate of Manifest V3, allowing developers to focus on writing clean React and TypeScript.

* **Framework:** [Plasmo](https://docs.plasmo.com/) (Browser Extension Framework)
* **UI/Components:** React 18, HTML/CSS (Tailwind planned)
* **Language:** TypeScript
* **Storage:** `@plasmohq/storage` (Chrome local storage hook)
* **LLM Integration:** Google Gemini API (Client-side execution)

---

## 🚀 Getting Started (Local Development)

We designed LinkCraft to have a zero-friction development environment. You can have the extension running locally in under 5 minutes.

### Prerequisites
* [Node.js](https://nodejs.org/) (v18 or higher)
* Git
* A Chromium-based browser (Chrome, Edge, Brave)

### Installation

1. **Fork and Clone the Repository:**
   ```bash
   git clone [https://github.com/NIKUL121003/LinkCraft.git](https://github.com/NIKUL121003/LinkCraft.git)
   cd LinkCraft


2. **Install Dependencies:**
    ```bash
    npm install

    ```


3. **Start the Development Server:**
```bash
npm run dev

```


*Plasmo will automatically build the extension into a `build/chrome-mv3-dev` directory and watch for file changes.*
4. **Load the Extension into Chrome:**
* Open Chrome and navigate to `chrome://extensions/`
* Enable **Developer mode** (top right corner).
* Click **Load unpacked** (top left corner).
* Select the `LinkCraft/build/chrome-mv3-dev` folder.



---

## 🤝 Contributing to LinkCraft

We welcome contributions from developers of all skill levels! Whether you are fixing a typo, updating a CSS style, or building the Google Dorking engine, your help is appreciated.

### How to Contribute

1. Browse the [suspicious link removed] and look for tasks labeled `good first issue` or `help wanted`.
2. Assign yourself to the issue by leaving a comment.
3. Create a new branch for your feature:
```bash
git checkout -b feature/your-feature-name
# or
git checkout -b bugfix/your-bug-fix

```


4. Write your code and ensure it follows standard TypeScript conventions.
5. Commit your changes:
```bash
git commit -m "feat: add Google dork generator utility"

```


6. Push to your fork and submit a **Pull Request (PR)** to the `main` branch.

*Please note: All PRs require at least one code review before merging to maintain code stability.*

---

## ⚠️ Disclaimer & Responsible Usage

**LinkCraft is an independent open-source tool and is not affiliated with, endorsed by, or associated with LinkedIn Corporation.**

Scraping data from LinkedIn can violate their Terms of Service. This tool is designed strictly for **educational purposes and personal productivity**.

* **Contributors:** Do not implement automated crawler bots or mass-messaging scripts. All scraping logic must simulate human-paced DOM reading. We recommend using a test/dummy LinkedIn account during local development.
* **Users:** Use this extension responsibly. High-frequency actions may result in your LinkedIn account being temporarily restricted.

---

## 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

```

### Next Steps After Adding the README

1. **Save and Commit:** Save the file in your code editor, then run:
   ```cmd
   git add README.md
   git commit -m "docs: add detailed community README"
   git push

```
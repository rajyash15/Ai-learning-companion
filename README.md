# 🩺 NEET AI Learning Companion

An AI-powered active recall and persistent weakness-tracking engine designed specifically for NEET Biology aspirants to optimize exam preparation and eliminate study fatigue.

---

## 💡 The Problem & The Niche
Every year, millions of students compete for medical seats in NEET. Biology alone accounts for a staggering **50% of the total exam weightage (360 marks)**, demanding flawless active recall of hyper-specific textbook facts. 

Traditional studying leads to a massive efficiency trap: students spend hundreds of hours passively re-reading chapters they already know, while remaining completely unaware of their micro-topic weaknesses until exam day. 

---

## 🚀 Core Features & Product Workflow
Our prototype introduces a seamless, multi-page micro-learning feedback loop:
1. **The Ingestion Center:** Students upload dense NCERT chapters or custom coaching notes (PDFs) which are instantly parsed on the fly.
2. **Quiz & Flashcard Studio:** The engine dynamically generates a hyper-targeted **7-question active-recall quiz** and flashcard deck based strictly on the uploaded text.
3. **Telemetry Weakness Tracker:** Instead of a generic dashboard, student inputs are evaluated and permanently logged as granular performance data (sub-topics, precision accuracy, and error rates).
4. **AI Revision Planner:** Leveraging the database telemetry, the companion builds a highly tailored, custom 3-day recovery roadmap focusing purely on mapped problem areas.

---

## 🛠️ Technical Architecture & Tech Stack
*   **Frontend Interface:** Written in Python using **Streamlit** to deliver a highly reactive, dark-mode medical dashboard user experience.
*   **Coding Agent:** Open Code
*   **Document Processing:** Engineered using **PyPDF2** for client-side text extraction.
*   **AI Orchestration Engine (Lemma SDK):**
    *   **Lemma Agents API:** Powers three highly specialized backend personas (`neet-question-generator`, `flashcard-generator`, and `revision-planner`) strictly constrained via system prompting to output structured, production-ready JSON arrays. Includes custom regex exception handling to auto-heal pipeline timeouts.
    *   **Lemma Data SDK:** Utilizes an auto-provisioning persistent datastore (`weakness_tracker`) to log user telemetry across sessions for long-term progress metrics.

> 💡 **Engineering Choice Note: Why 7 Questions?**
> We deliberately capped real-time quiz generations to 7 data nodes. Pedagogically, it provides the perfect micro-learning interval to combat student burnout. Technically, it minimizes LLM completion latency and enforces flawless JSON formatting without risking output token truncation.

---

## 🗺️ Future Roadmap (Scale Plan)
The underlying architecture is fully prepared to expand directly across the broader Lemma ecosystem in Version 2.0:
*   **Lemma Connectors:** To allow students to seamlessly sync their personal Google Drives or coaching portal repositories.
*   **Lemma Schedules:** To auto-compile and email a cumulative Weakness Analytics report to students every Sunday evening.
*   **Lemma Workflows:** To orchestrate background, bulk asynchronous card generation for massive textbook volumes while the user is offline.
  
* **Universal Exam Expansion:** Scaling the platform's core engine to support all competitive, standardized, and academic exam preparations, transitioning from a      NEET-specific tool to a comprehensive learning companion.
* **Lemma Connectors:** To allow students to seamlessly sync their personal Google Drives or coaching portal repositories.
* **Lemma Schedules:** To auto-compile and email a cumulative Weakness Analytics report to students every Sunday evening.
* **Lemma Workflows:** To orchestrate background, bulk asynchronous card generation for massive textbook volumes while the user is offline.

---

## 💻 Local Installation & Setup
To run this application locally, clone the repository and execute the following commands:

```bash
# Install dependencies
pip install -r requirements.txt

# Configure your environment variables
export LEMMA_API_KEY="your_api_key_here"
export POD_ID="your_pod_id_here"

# Run the Streamlit application
streamlit run app.py

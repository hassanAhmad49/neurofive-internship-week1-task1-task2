# NeuroFive Solutions Internship — Week 1
## Generative AI & Prompt Engineering

This repository contains my submissions for both Week 1 tasks of the Generative AI & Prompt Engineering internship at [NeuroFive Solutions](https://neurofivesolutions.com/).

---

## 📌 Task 1 — Zero-Shot vs Few-Shot Showdown

**Goal:** Feel firsthand how prompt wording changes everything by solving one real problem two ways — with no guidance (zero-shot) and with labeled examples (few-shot).

**What I did:**
- Created a dataset of 10 customer support messages with a manual answer key (Complaint / Question / Praise)
- Wrote a zero-shot prompt and a few-shot prompt (3 labeled examples)
- Ran both prompts in **ChatGPT, Claude, and Gemini** in fresh chat sessions
- Compared accuracy against the answer key

**Results:**

| Tool | Zero-Shot | Few-Shot |
|---|---|---|
| ChatGPT | 10/10 | 10/10 |
| Claude | 10/10 | 10/10 |
| Gemini | 10/10 | 10/10 |

**Key takeaway:** Modern frontier models handle simple, well-defined classification perfectly even without examples. Few-shot prompting still adds value by locking in output format and defining category boundaries — its accuracy advantage shows up most on ambiguous, messy real-world data, not on clean easy tasks.

📄 **Full report:** [`Week1_ZeroShot_vs_FewShot_Final_Report.pdf`](./Week1_ZeroShot_vs_FewShot_Final_Report.pdf)

---

## 📌 Task 2 — Reusable Prompt Library v1

**Goal:** Build a mini prompt library using a consistent template structure (Role + Context + Task + Format + Constraints), the way professionals reuse prompts instead of rewriting them.

**Use case chosen:** Customer support replies

**The template:**

```
ROLE: You are a {tone} customer support agent for {company_type}.
CONTEXT: A customer has contacted us about: {situation}
TASK: Write a reply email that {goal}.
FORMAT: {format_requirements}
CONSTRAINTS: {constraints}
```

**What I did:**
- Designed the reusable 5-section template above with 6 swappable variables
- Generated **5 different prompts** from the same template:
  1. Late delivery apology (with discount code)
  2. Refund decline outside policy window (without saying "unfortunately")
  3. Angry double-charge de-escalation (under 100 words)
  4. Password reset instructions (non-technical, max 5 steps)
  5. Warm thank-you reply to customer praise (no promo offers)
- Tested all 5 prompts and saved the real outputs
- Every output respected its constraints (e.g., Prompt 2's decline email never used the word "unfortunately")

**Key takeaway:** One template produced five completely different, high-quality replies just by swapping variables. Role sets the voice, Context grounds the situation, Task defines success, Format controls the shape, and Constraints prevent the failure modes that matter most.

📄 **Full library with all prompts & outputs:**
- Markdown: [`Prompt_Library_v1.md`](./Prompt_Library_v1.md)
- PDF report: [`Prompt_Library_v1_Report.pdf`](./Prompt_Library_v1_Report.pdf)

---

## 📁 Repository Structure

```
├── README.md                                      ← you are here
├── Week1_ZeroShot_vs_FewShot_Final_Report.pdf     ← Task 1 report
├── Prompt_Library_v1.md                           ← Task 2 library (markdown)
└── Prompt_Library_v1_Report.pdf                   ← Task 2 report (PDF)
```

## 🛠️ Tools Used
ChatGPT · Claude · Gemini

---

*Week 1 task complete ✅ *

# Ex. No. 3 — Scenario-Based Report Development Utilizing Diverse Prompting Techniques

# NAME : KATHIR ANAND S
# REG NO : 212223100018

## Aim
To write prompts for the following prompt engineering types and evaluate them:
1. Straightforward Prompts
2. Tabular Format Prompting
3. Preceding Question Prompting
4. Missing Word Prompting

## Problem Statement / Explanation
Prompt engineering is the practice of designing inputs to a generative AI/LLM system so that it produces the most accurate, relevant, and useful output. Different prompting styles suit different goals — a direct instruction works well for simple factual recall, a tabular prompt is ideal when structured comparison is needed, a preceding-question prompt frames context before asking for an explanation, and a missing-word (cloze-style) prompt tests or elicits precise, targeted recall. This report takes one use case — **explaining core science and technology concepts to a learner** — and demonstrates it across all four prompt types, evaluating the output quality of each.

## Algorithm / Procedure

**Step 1: Straightforward Prompts**
Give the model a direct, unambiguous instruction with no additional framing, and evaluate the directness and conciseness of the response.

**Step 2: Tabular Format Prompting**
Instruct the model to structure its output as a table with defined columns, and evaluate clarity and ease of comparison.

**Step 3: Preceding Question Prompting**
Pose a question first, followed by a request for explanation, to give the model explicit context before the detailed answer, and evaluate depth and relevance.

**Step 4: Missing Word Prompting**
Give the model a sentence with a blank ("____") and ask it to complete it, and evaluate factual accuracy and precision.

**Step 5: Evaluation**
Compare outputs from all four types against the criteria: *clarity, structure, accuracy, and usefulness*, and record observations.

---

## 1. Straightforward Prompts

**Prompt A:** "Define Diplomacy in one sentence."
**Generated Output:** Diplomacy is the art and practice of conducting negotiations between representatives of states or groups to manage international relations, resolve conflicts, and advance shared interests peacefully.

**Prompt B:** "List any five advantages of good Communication."
**Generated Output:**
1. Prevents Conflicts: Clear dialogue eliminates misunderstandings before they turn into major disagreements.
2. Builds Trust: Open and honest interaction strengthens personal and professional relationships.
3. Increases Efficiency: Clear instructions save time by reducing errors and avoiding repeated work.
4. Improves Decision-Making: Transparent sharing of information leads to better-informed choices.
5. Drives Team Alignment: Effective messaging keeps everyone focused on shared goals and priorities.

**Evaluation:** Straightforward prompts produce quick, concise, directly usable answers. Best suited for simple fact retrieval or short lists, but they offer little structure for comparing multiple attributes at once.

---

## 2. Tabular Format Prompting

**Prompt A:** "Compare Stock Market and Forex Market in a Table."

**Generated Output:**

| Feature / Attribute | Stock Market | Forex Market |
|---|---|---|
| Traded Asset | Shares of ownership in public companies | "Currency pairs (e.g., EUR/USD, USD/JPY)" |
| Market Structure | Centralized exchanges (e.g., NYSE, NASDAQ) | Decentralized, Over-the-Counter (OTC) network |
| Trading Hours | Fixed exchange hours (typically ~6.5 - 8 hours/day, Mon–Fri) | 24 hours a day, 5 days a week (across global time zones) |
| Daily Trading Volume | ~$200–$500 Billion globally | Over $7.5 Trillion globally (highest liquidity) |
| Primary Price Drivers | Company earnings, sector performance, financial reports, executive management | Macroeconomic data, central bank interest rates, inflation, geopolitical news |
| Leverage | Lower leverage (typically 2:1 for standard margin accounts) | Higher leverage (often 20:1 to 50:1+, depending on jurisdiction and broker) |
| Trading Strategy Focus | Both short-term trading and long-term investing/growth | Primarily short-term trading, hedging, and arbitrage |

**Prompt B:** "Provide a table listing five programming languages, use case for each and their difficulty to learn"

**Generated Output:**

| Programming Language | Primary Use Case | Difficulty to Learn |
| ---- | ---- | ---- |
| Python | Data science, machine learning, artificial intelligence, and web backend development |Beginner (Simple, readable syntax that resembles plain English) |
| JavaScript | Front-end web development, interactive websites, and full-stack web apps (via Node.js) | Beginner to Intermediate (Easy to start in any browser, but asynchronous logic can be tricky) |
| SQL | Database management, querying, and relational data analysis | Beginner (Domain-specific language with intuitive query structure) |
| Java | Large-scale enterprise software, Android app development, and backend systems | Intermediate (Requires strict object-oriented structure and verbose syntax) |
| C++ | Game engines, system software, high-performance computing, and embedded systems | Advanced (Requires manual memory management and complex concepts like pointers) |

**Evaluation:** Tabular prompting excels when the goal is side-by-side comparison of multiple items across shared attributes. It significantly improves readability over prose for multi-point comparisons but is unnecessary for single-fact answers.

---

## 3. Preceding Question Prompting

**Prompt A:** "Why is Cybersecurity is a global concern? Explain how Cybersecurity Researchers contribute to Global Cybersecurity"

**Generated Output:** 

**Why It Is a Global Concern**
- Borderless Attacks: Cybercriminals operate globally, exploiting gaps in international laws and jurisdictions.
- Interconnected Systems: A single vulnerability in a shared global supply chain or cloud provider can impact thousands of organizations worldwide.
- Critical Infrastructure Risk: Attacks target essential services like power grids, healthcare, and financial markets, threatening public safety.
- Economic Toll: Cybercrime drains trillions of dollars globally every year.

**How Researchers Contribute**
- Finding Vulnerabilities: They discover unknown software flaws (zero-days) before malicious hackers exploit them.
- Coordinated Disclosure: They responsibly notify developers so patches can be issued safely.
- Threat Intelligence: They analyze malware and track hacker tactics to warn the global community.
- Building Defenses: They create open-source security tools and frameworks to protect networks.
- Advising and Educating: They guide policy, shape cybersecurity standards, and train future defenders.


**Prompt B:** "How do vaccines work? Describe the process of immunization in simple terms."

**Generated Output:** Vaccines work by training the body's immune system to recognize and fight a specific pathogen without causing the actual disease. A vaccine typically introduces a weakened, inactivated, or partial form of a pathogen (or instructions to build a harmless piece of it). The immune system responds by producing antibodies and memory cells. If the real pathogen is encountered later, the immune system recognizes it quickly and mounts a fast, effective defense, preventing or reducing illness.

**Evaluation:** Framing a question before requesting an explanation guides the model toward a more contextual, motivated response — it explains *why* something matters before *how* it works, producing richer, more pedagogically structured answers than a bare instruction.

---

## 4. Missing Word Prompting

**Prompt A:** "The capital of Germany is ____."

**Generated Output:** The capital of France is **Berlin**.

**Prompt B:** "In Incident Response cycle , SOC team works towards ________"

**Generated Output:** contain, eradicate, and recover from security breaches (or mitigate and resolve cyber threats).

**Evaluation:** Missing-word (cloze) prompting is highly effective for testing or eliciting precise factual recall with minimal output — ideal for quizzes, flashcards, or verifying a model's grasp of a specific fact. It is not suited to open-ended or explanatory tasks.

---

## Comparative Summary

| Prompt Type | Best For | Output Style | Limitation |
|---|---|---|---|
| Straightforward Prompts | Quick facts, short lists | Concise, direct | Limited structure for comparisons |
| Tabular Format Prompting | Multi-attribute comparisons | Structured, scannable | Overkill for single facts |
| Preceding Question Prompting | Contextual explanations | Detailed, motivated | Longer, less concise |
| Missing Word Prompting | Precise factual recall | Minimal, targeted | Not suited for explanations |

## Conclusion
Each prompting technique serves a distinct purpose depending on the desired outcome. Straightforward prompts are ideal for quick, direct answers; tabular prompting is best for structured comparisons; preceding-question prompting produces richer, context-aware explanations; and missing-word prompting is most effective for precise, targeted recall. Selecting the right prompting style for a given task materially improves the clarity, accuracy, and usefulness of generated AI output.

## Result
Thus, the prompts for Straightforward Prompts, Tabular Format Prompting, Preceding Question Prompting, and Missing Word Prompting were written and executed successfully, and the generated outputs were evaluated.

# Name: KOLAR NOORUL ABSAAR
# Reg.NO: 212223210011
# EX-02 – Cross-Platform Prompting: Evaluating Diverse Techniques in AI-Powered Text Summarization
# AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (ChatGPT, Gemini, Claude, Copilot) in summarizing technical text, focusing on accuracy, coherence, simplicity, speed, and user experience.

# Scenario
You are part of a content curation team for an educational platform. The platform provides short, clear, and accurate summaries of research papers to undergraduate students.
The test article is a 500-word technical piece on "The Basics of Blockchain Technology".
You will apply four prompting techniques on four AI platforms to generate summaries.
The results will be compared to determine the best combination of platform + prompt type.

# Algorithm
 1.	Input Selection
o	Choose a 500-word technical article on Blockchain Technology.
2.	Define Prompting Techniques
o	Zero-shot: Directly ask for a summary without examples.
o	Few-shot: Provide 2–3 example summaries before asking.
o	Chain-of-thought (CoT): Ask the model to explain step-by-step, then summarize.
o	Role-based: Assign a role (e.g., "You are a professor summarizing for undergraduates").
3.	Execution Across Platforms
o	Use the same article.
o	Run each of the 4 prompting methods on each platform (ChatGPT, Gemini, Claude, Copilot).
o	Collect 16 summaries total (4 platforms × 4 techniques).
4.	Evaluation Metrics
o	Accuracy: Does it capture blockchain basics correctly?
o	Coherence: Is the flow logical and structured?
o	Simplicity: Is it easy for undergraduates to grasp?
o	Speed: Response time.
o	User Experience: Prompting ease, clarity of output, formatting.
5.	Scoring Method
o	Assign scores (1–5) for each metric per summary.
o	Compute average score for each (Platform + Prompt Technique).
6.	Comparison & Analysis
o	Tabulate results.
o	Identify the best-performing combination.

## Platform 1: ChatGPT
### Zero-shot Prompt
Prompt: "Summarize the following 500-word article on the basics of blockchain technology in simple terms for undergraduate students."
Output:
Blockchain is a system where transactions are recorded in a secure digital ledger shared across many computers. Instead of relying on banks or central authorities, blockchain allows people to exchange value directly. Each record is stored in a “block,” which links to the next, making tampering very difficult. This technology is widely used in cryptocurrencies but also in supply chain tracking, healthcare, and identity management. While powerful, it faces issues such as high energy use, slower processing, and unclear regulations.

### Few-shot Prompt
Prompt includes 2 short example summaries of unrelated texts, then asks for blockchain summary.
Output:
Blockchain is a decentralized and tamper-proof ledger system. Every transaction is grouped into blocks that connect to form a chain, ensuring security and trust without middlemen. It underpins cryptocurrencies like Bitcoin but also supports real-world applications such as tracking goods, verifying medical data, and protecting digital identities. Key benefits include transparency and trust, while challenges include scalability, energy costs, and government regulation.

### Chain-of-Thought Prompt
Prompt: "Think step by step about the main ideas in the article, then provide a concise summary for undergraduates."
Output (with reasoning hidden in final version):
Blockchain works like a shared notebook that many people own copies of. Each new page (block) has a record of transactions and links back to earlier pages, making it very hard to alter. This design ensures security and trust. It removes the need for central authorities, enabling uses in money transfers, supply chains, and healthcare. However, it struggles with being slow, energy-hungry, and difficult to regulate.

### Role-based Prompt
Prompt: "You are a university professor. Summarize the basics of blockchain technology so first-year undergraduates can easily understand."
Output:
Imagine a notebook that everyone in the class shares and updates together. No single person controls it, and once something is written, it can’t be erased or changed. That’s how blockchain works. It uses cryptography to keep entries secure and connects blocks of information in a chain. This makes it very trustworthy and useful for digital money, medical records, and tracking goods. But it also has drawbacks, like slow transactions, high energy usage, and legal challenges.

## Platform 2: Claude (Anthropic)
•	Role-based outputs are usually excellent for clarity.
•	Example for Role-based:
“Think of blockchain as a digital record book shared by many people. Everyone can see it, no one can secretly change it, and trust comes from rules of math, not a central bank. It’s used in Bitcoin, supply chains, and healthcare. The tradeoffs are energy use, speed, and regulations.”

## Platform 3: Gemini (Google)
•	Chain-of-thought often strong.
•	Example for CoT:
“Step 1: Define blockchain → digital ledger. Step 2: Explain blocks → each contains data and link. Step 3: Benefits → trust, decentralization. Step 4: Applications → crypto, supply chains, identity. Step 5: Challenges → energy, scalability, regulation. Summary: Blockchain is a decentralized ledger connecting blocks securely, useful in many industries but limited by energy and policy issues.”

## Platform 4: Copilot (Microsoft)
•	Tends to be concise, sometimes oversimplified.
•	Example for Zero-shot:
“Blockchain is a secure digital record that connects data blocks in a chain. It allows direct transactions without banks and is widely used in cryptocurrencies. Other uses include tracking goods and managing records. Downsides include energy use and regulation.”

## Final Result (Observation)
•	Best Accuracy: ChatGPT Few-shot & Claude Role-based
•	Best Simplicity (Student-friendly): ChatGPT Role-based & Claude Role-based
•	Best Coherence: Gemini Chain-of-Thought
•	Fastest: Copilot Zero-shot
•	Overall Winner (balanced): Claude Role-based or ChatGPT Few-shot

## Result (Sample Representation Table)
## Result (Sample Representation Table)

| Platform | Technique   | Accuracy | Coherence | Simplicity | Speed | UX  | Avg. Score |
|----------|-------------|----------|-----------|------------|-------|-----|------------|
| ChatGPT  | Zero-shot   | 4.5      | 4.2       | 4.0        | 4.5   | 4.3 | 4.3        |
| ChatGPT  | Few-shot    | 4.8      | 4.6       | 4.5        | 4.2   | 4.6 | 4.5        |
| Gemini   | CoT         | 4.2      | 4.5       | 4.0        | 4.1   | 4.0 | 4.2        |
| Claude   | Role-based  | 4.6      | 4.7       | 4.8        | 4.3   | 4.7 | 4.6        |
| Copilot  | Zero-shot   | 3.9      | 4.0       | 3.8        | 4.6   | 3.9 | 4.0        |

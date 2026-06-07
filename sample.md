## Inspiration

As humans, we are bad at long-term decision-making. We underestimate risks, overestimate our future motivation, and often ignore the second-order effects of our choices. Whether it's quitting a job, moving to a new country, or starting a company, we're forced to make life-altering decisions based on gut feelings and limited data.

We realized that while there are tools to track tasks and games to simulate fantasy worlds, **there was nothing to simulate your own future**. What if decision-making was like a video game? What if you could "save your game," try a risky path, see the consequences, and then rewind if it didn't work out?

This inspired **Usaid**, a cognitive time simulator that brings the power of "Scenario Planning" (used by military and corporate strategists) to personal life decisions.

## What it does

**Usaid** is an AI-powered engine that generates multiple, distinct future timelines based on a single real-world decision.

1. You enter a dilemma (e.g., "Should I quit my job to start a startup?").
2. **Usaid** analyzes your profile (risk tolerance, values, current state) and generates few feasible divergent future paths (Optimistic, Pragmatic, Remote/Risky).
3. Each timeline is visualized with year-by-year events and quantifiable metrics for Career, Finance, Relationships, and Mental Wellbeing.
4. You can "inject" new decisions into any timeline (e.g., "What if I get funding in Year 2?") and watch the future rewrite itself in real-time.

It’s not just advice.. it’s experiential foresight of once own life.

## How it is built

**Usaid** is a modern full-stack application leveraging the latest in Generative AI.

1. **The AI Engine:** Google Gemini 3's advanced reasoning capabilities has been used to build the simulation core. Prompt Engineering is been used to build something beyond simple text generation by constructing a persistent "Cognitive State Model" for the user.

2. **The Frontend:** Built with React, TypeScript, and Vite, featuring a premium "Glassmorphism" UI. Framer Motion is used for smooth timeline animations and Chart.js (or similar visualization libs) to make the data tangible.

3. **The Backend:** A robust Node.js/Express server that acts as the orchestrator. It handles authentication, manages the SQLite database (via Prisma), and streams AI responses to the client.

4. **The Design:** Heavy focus on "Industrial Polish", using a dark, futuristic aesthetic with neon accents to make the user feel like they are stepping into a control room for their life.

## Challenges we ran into

1. **Hallucination Control:** Getting an LLM to consistently generate plausible 5-year timelines without veering into fantasy was tough. Strict schema validation implementation and "Chain-of-Thought" prompting helps a lot.

2. **Latency:** Simulating 5 concurrent futures is computationally expensive. Gemini 3 Flash know for its flash speed has been used and a streaming architecture has been implemented so users see the first timeline immediately while the others generate in the background.

3. **Visualizing Abstract Data:** How do you visualize "Emotional Wellbeing" over 5 years? The UI has been iterated multiple times to find a graphical representation that was intuitive but not overwhelming.

## Accomplishments that make me proud

1. **The "Wow" Factor:** The moment you see your life split into three different paths on the screen is genuinely powerful.

2. **Structured AI:** I managed to tame a creative LLM into outputting complex, mathematically consistent graph data.

3. **The UI:** The interface feels incredibly premium and responsive. It doesn't feel like a hackathon project, it feels like a SaaS product.

## What I learned

1. **Gemini 3 is a Reasoner, not just a Writer:** If we give Gemini enough context about a user's psychology, it can predict second-order effects (e.g., "High career growth = Risk of burnout/divorce") with scary accuracy.

2. **The Power of Context:** The quality of the simulation is directly proportional to how much the AI knows about the user. Personalization is the key.

## What's next for Usaid

1. **Reality Feedback Loop:** Allowing users to log what actually happened, so the system learns from reality and improves its future predictions.

2. **Multi-Agent Extensions:** Adding specific AI advisors (a "Risk Manager," a "Career Coach," a "Therapist") who debate the pros and cons of your timelines.

3. **Scientific Extensions:** Applying the same engine to simulate research paths or startup pivots for teams.

## build with

google-gemini-3-flash,react,typescript,node.js,express.js,vite,zustand,react-query,framer-motion,prisma,sqlite,mermaid-js,

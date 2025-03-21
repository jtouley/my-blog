---
layout: post
title: "AI Didn’t Make Me Worse—It Made Me Think Faster"
date: 2025-03-15
categories: ai technology
---

![DE using AI](https://jtouley.github.io/my-blog/assets/images/ai_thought_partner.png)
***Microsoft says AI is making engineers dumber. My experience says otherwise. AI isn't a crutch — it's a force multiplier that lets me iterate, refine, and deliver at a higher level. Here’s why the study is misguided and how AI is making me a better engineer.***

In my [last article](https://medium.com/@jtouley/how-i-use-ai-as-a-recursive-thought-partner-and-why-you-should-too-26027b0106da), I explained how to use AI as a recursive thought partner to iterate on ideas. But a recent [Microsoft study](https://www.pcgamer.com/software/ai/microsoft-co-authored-paper-suggests-the-regular-use-of-gen-ai-can-leave-users-with-a-diminished-skill-for-independent-problem-solving-and-at-least-one-ai-model-seems-to-agree/) claims that engineers who rely on AI-assisted coding might lose problem-solving skills over time. The underlying assumption? That AI weakens our ability to think critically and troubleshoot issues independently.  
Did calculators make us dumber or let us compute more complex equations quicker?

**I disagree**. Not only is this take shortsighted, but it fundamentally misunderstands the role AI plays in modern data engineering.  
AI doesn't make me dumber — it makes me relentless.  It forces me to **iterate faster, challenge assumptions more aggressively, and refine code to a higher standard than ever before.**

Here’s why the study is missing the bigger picture.

---

## AI as an Accelerator, Not a Shortcut

The narrative that AI turns engineers into passive consumers of generated code is misguided. I think it can, but **savvy engineers and smart practitioners will use it as an accelerant**. My recent experience integrating **Docker Compose, MinIO, and Airflow** proves the opposite.

I started with AI-generated code, hoping it would work out of the box. It didn’t.  
The implementation from OpenAI had **nuanced issues that impacted the quality and functionality** of the system. After hours of debugging, it became clear I needed to pivot.

- I **revisited Airflow and MinIO's documentation**, verifying each configuration AI got wrong.  
- I debated **whether to separate services or consolidate them in a single `docker-compose.yaml`**, ultimately deciding on a unified approach.  
- I **rewrote significant portions of the configuration**, while preserving custom build templates and resolving dependency issues.  
- I encountered **MinIO's 403 error**, requiring additional debugging in my `s3_utils.py`.  
- After 12 hours, I had a fully functional, high-quality implementation, including tests and pre-commit hooks for maintainability.

Had I relied purely on AI without **engineering discipline, debugging skills, and architectural judgment**, I would have been stuck.  
AI got me started, but **it didn’t solve the hard problems for me — I did**.

Now compare that to a traditional approach.  
In the olden days, I might have spent **one to two full sprints** setting this up.  
I completed it in a day. If AI is making me "dumber," why am I delivering faster and at a higher level of rigor?

---

## AI as a Relentless Thought Partner, Not a Crutch

Microsoft’s study assumes AI discourages independent problem-solving.  
My reality? AI has become my most **relentless thought partner**, pushing me to refine ideas with brutal efficiency.

Here’s how:

- AI didn’t just generate code — it **forced me to validate, debug, and improve it**.  
- Instead of brute-forcing solutions, I used **Claude and OpenAI to critique and refine my approach**.  
- When I hit a blocker, **I didn’t just accept AI’s first answer — I iterated, experimented, and pushed for better outcomes**.  
- I committed my work, opened a PR, and used AI as a second set of eyes to **catch issues and suggest improvements**.  

**AI isn’t just for coding — it sharpens my strategic thinking too**. In a recent conversation with Gemini, I explored how AI-assisted development impacts hiring and team dynamics.  
Through iterative dialogue, I clarified my stance: AI amplifies engineering rigor, not diminishes it. This recursive process helped me articulate complex ideas more effectively.

This article mirrors the process it describes: 
**I used Gemini to brainstorm, OpenAI to draft an outline, my own expertise to refine it, and Grok as my editor**. This process forced me to defend, refine, and sharpen my argument in real-time. AI didn’t do the thinking for me; it forced me to think better. **If AI were making me dumber, I wouldn’t be debugging more, iterating faster, or refining my approach with greater precision**.

---

## AI Lowers the Cost of Iteration, Not the Bar for Thinking

One of the biggest flaws in Microsoft’s study is its failure to consider how AI **changes the iteration cycle** in software engineering.

Traditionally, when you spend weeks or months building something, you **resist tearing it down** — not because it’s perfect, but because the sunk cost is too high.  
AI removes that friction.

- I didn’t hesitate to **scrap and refactor** my MinIO integration because AI made starting over easy.  
- Instead of sinking **weeks** into an implementation before realizing its flaws, I identified weaknesses **within hours** and pivoted.  
- I’m **not attached to the first solution AI gives me** — I expect it to be wrong, and I iterate until it’s right.  

Take my Gemini conversation:  
**I didn’t accept the first response.  
I asked follow-ups, challenged assumptions, and iterated until it matched my vision**. This recursive dialogue cuts the cost of refining ideas, letting me pivot fast without losing rigor.

This isn’t complacency.  **This is the future of engineering.**

---

## The Engineers Who Fear AI Are the Ones Who Should Be Worried

The real takeaway from Microsoft’s study isn’t that AI makes engineers worse.  It’s that AI **exposes who was never good at problem-solving to begin with.**  

- If an engineer mindlessly accepts AI’s output without verifying it, that’s a **human failure, not an AI failure**.  
- If AI-generated code becomes a **black box** for someone, they were likely struggling with complexity long before AI existed.  
- AI doesn’t replace the ability to **debug, adapt, and iterate** — it amplifies those who do.  

The best engineers don’t fear AI. They **use it as leverage to move faster, solve harder problems, and push the boundaries of what’s possible**.

---

## Conclusion: AI Isn’t Making Me Dumber — It’s Forcing Me to Level Up

The fundamental flaw in Microsoft’s study is its assumption that AI replaces problem-solving. In my experience, AI does the opposite — it **raises the bar**.

It **forces me to be faster, more iterative, and more precise. It pushes me to challenge assumptions and refine solutions at an unprecedented rate**. The difference between those who thrive with AI and those who get left behind isn’t who wrote the code — it’s who made it work.  

As I discussed with Gemini, **AI could be a crutch if misused**. But as a recursive thought partner, it forces me to **engage deeply, question assumptions, and refine relentlessly**. The difference lies in how we wield it.

So no, AI isn’t making me dumber.  

**It’s making me relentless.**

---

*Still skeptical? Try the recursive approach I shared in my [first article](https://medium.com/@jtouley/how-i-use-ai-as-a-recursive-thought-partner-and-why-you-should-too-26027b0106da) Use AI to kickstart a project, then iterate until it’s yours. I’d love to hear how it goes.*

***This draft was crafted using a human-in-the-loop RAG approach. A Gemini conversation sparked the ideas, OpenAI generated the outline, and I iteratively refined it to ensure clarity and rigor. This recursive collaboration mirrors the workflow I advocate.***


Here's the [Github repo](https://github.com/jtouley/dag_factory_poc) for those interested. *Spotted an issue? Open a GitHub issue, and I’ll prioritize fixing it. Better yet — fork it, experiment, and let’s iterate together.*
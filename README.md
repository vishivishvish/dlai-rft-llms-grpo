# **Reinforcement Fine-tuning LLMs with GRPO** 

**[Deeplearning.ai](https://www.deeplearning.ai/short-courses/reinforcement-fine-tuning-llms-grpo/)**

**Andrew Ng - CEO, Deeplearning.ai**

**Travis Addair - Co-Founder & CTO, Predibase**

**Arnav Garg - Senior ML Engineer, Predibase**

***Notes by Vishnu Subramanian***

## ***1 - Introduction***

- This course takes a technical deep dive into Reinforcement Fine-tuning (RFT).
- RFT involves training techniques that uses Reinforcement Learning to improve the performance of LLMs on tasks that require multi-step reasoning, such as math or code generation.
- By harnessing an LLM’s ability to reason through problems and think step-by-step, Reinforcement Fine-tuning guides the model to discover solutions to complex tasks on its own, rather than relying on pre-existing examples as in traditional Supervised Learning.
- This approach lets you adapt models to complex tasks with much less training data, say, just a couple dozen examples, than you typically need for successful Supervised Fine-tuning.
- In this course, we’ll explore how RFT works using a fun example - getting an LLM to play Wordle -  in this instance we get the LLM to guess a 5-letter word in 6 tries or fewer.
- We start by using the Qwen-2.5-7B model to play this game, analyze its performance and develop a reward function that can be used to help the model learn how to do better over time.
- This reward function is the key component of GRPO - Group Relative Policy Optimization, the algorithm developed by DeepSeek to carry out Reinforcement Learning of reasoning tasks.
- In GRPO, the LLM generates multiple responses to a single prompt, that are then scored using a reward function based on verifiable metrics, such as correct formatting or functioning code.
- The use of this Reward Function is a key difference between GRPO and other RL algorithms.
- Other RL algorithms like PPO or DPO rely on human feedback or complex multi-model systems to assign rewards.
- Once we develop a reward function for the Wordle example, we will learn some other general principles for writing good reward functions that we can apply to a wide range of problems.
- We will also learn about ways to avoid Reward Hacking, where a model learns behaviors that maximize rewards without actually solving the problem on hand.
- Next, we’ll take a close look at the technical details of how loss is calculated during RFT.
- We will see how the seemingly complex process of the GRPO algorithm like Clipping and KL-divergence and the Loss Function are simpler than you might think once you implement them in code.
- Finally we’ll wrap up the course by seeing how we can carry out RFT using the Predibase API with our own data and our own custom reward functions.
- LLMs that can reason well are critical components of many agentic systems, and RFT lets smaller models work well in Agentic Workflows.



Student Competence Analysis with Open-Source Models
Research Plan

Approach to identifying & evaluating models
I will begin by exploring freely available open-source models with code-understanding capabilities such as StarCoder, CodeGen, or CodeT5. These models are filtered based on license, context window size, and feasibility of deployment (local vs. cloud). Each candidate will be tested on a curated dataset of student-written Python programs, including common errors and misconceptions.
The evaluation will involve two pipelines:

Prompt generation — asking the model to generate diagnostic/Socratic questions for student code.

Error analysis — asking the model to identify likely misconceptions or reasoning gaps without revealing the solution.
Outputs will be logged and assessed with both automatic metrics and expert teacher feedback.

Testing & validation
Validation will be conducted in two stages:

Offline evaluation: Comparing generated prompts with a gold-standard set of instructor-written prompts, measuring semantic similarity, coverage across Bloom’s taxonomy, and hallucination rate.

Live testing: A small classroom-style experiment where one group receives model-generated prompts and another receives static hints. Learning outcomes (revision quality, quiz scores, and time-to-correct) will be compared.
Failure cases, hallucinations, and cost/latency will also be documented to determine real-world applicability.

Reasoning

1. What makes a model suitable for high-level competence analysis?

Strong semantic understanding of Python code.

Ability to generate non-spoiling, Socratic prompts.

Interpretability (can explain reasoning tied to code regions).

Low cost and feasible deployment for interactive use.

Flexibility for fine-tuning or retrieval augmentation.

2. How to test whether prompts are meaningful?

Compare with gold-standard prompts using semantic similarity.

Educator ratings on quality, relevance, and learning potential.

Student improvement in follow-up coding tasks and quizzes.

3. Trade-offs between accuracy, interpretability, and cost:

Larger models = better accuracy but higher compute cost.

More capable models may be harder to interpret.

Cheaper/smaller models may hallucinate or miss subtle misconceptions.

On-device small models offer privacy but limited depth.

4. Why StarCoder (BigCode) was chosen?

Strengths: Strong at parsing code, permissive license, optimized for programming languages, large context support, and suitable for fine-tuning. Local deployment supports student data privacy.

Limitations: Not trained for pedagogy by default, may produce solutions instead of prompts, can hallucinate, and requires GPU for real-time performance. Fine-tuning and prompt engineering are necessary for classroom deployment.

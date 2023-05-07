## Two Types of large language models (LLMs)
### Base LLM
Predicts next word, based on text training data

### Instruction Tuned LLM
Tries to follow instructions
Fine-tune on instructions and good attempts at following those instructions.

RLHF: Reinforcement Learning with Human Feedback

## Principles of prompting
### Write clear and specific instructions
#### Tactic 1: Use delimiters
Triple quotes: "'"
Triple backticks: '*
Triple dashes: --.
Angle brackets: ‹ »,
XML tags: ‹tag› ‹/tag›
#### Tactic 2: Ask for a structured output
JSON, HTML
#### Tactic 3: Check whether conditions are satisfied
Check assumptions required to do the task
#### Tactic 4: Few-shot prompting
Give successful examples of completing tasks
Then ask model to perform the task

### Give the model time to think
#### Tactic 1: Specify the steps required to complete a task
Ask for output in a specified format
#### Tactic 2: Instruct the model to work out its own solution before rushing to a conclusion

### Model limitations
#### Hallucination
Makes statements that sound plausible but are not true

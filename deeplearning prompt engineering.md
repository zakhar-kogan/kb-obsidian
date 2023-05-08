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
##### Reducing hallucinations:
First find relevant information, then answer the question based on the relevant information.

> -   In the course, we are using a backslash `\` to make the text fit on the screen without inserting newline '\n' characters.
> - GPT-3 isn't really affected whether you insert newline characters or not. But when working with LLMs in general, you may consider whether newline characters in your prompt may affect the model's performance.

## Iterative prompt development
![](https://i.imgur.com/DKfjr6Y.png)

## Prompt guidelines
• Be clear and specific
• Analyze why result does not give desired output.
• Refine the idea and the prompt
• Repeat

### Issue 1: The text is too long
Limit the number of words/sentences/characters.
### Issue 2. Text focuses on the wrong details
Ask it to focus on the aspects that are relevant to the intended audience.
### Issue 3. Description needs a table of dimensions
Ask it to extract information and organize it in a table.

### Iterative Process
• Try something
• Analyze where the result does not give what you want
• Clarify instructions, give more time to think
• Refine prompts with a batch of examples

## Summarizing

## Inferring

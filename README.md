# Modelzilla

![modelzilla-banner](https://github.com/lucianoayres/modelzilla/blob/main/assets/images/banner_modelzilla.png?raw=true)

## Unleashing Monster Models For Your AI Beasts

[What's Modelzilla?](#whats-modelzilla) · [How Does it Work?](#how-does-it-work) · [Why Use Modelzilla?](#why-use-modelzilla) · [In Action](#in-action) · [Who is it for?](#who-is-it-for) · [Structure](#structure) · [Base Template](#base-template) · [How to Use](#how-to-use) · [User Input Examples](#user-input-examples) · [Output Example](#output-example) · [Using Models with Ollama](#using-models-with-ollama) · [Using Nino with Ollama](#using-nino-with-ollama) · [Default Model](#default-model) · [License](#license) · [Contribution](#contribution)

### What's Modelzilla?

The **Modelzilla Modelfile Generator** is a [_prompt_](./templates/v1/Modelzilla_Base_Template.txt) specifically designed to be used with a large language model (LLM). It helps you create [Modelfiles](https://github.com/ollama/ollama/blob/main/docs/modelfile.md) for your AI models with ease, ensuring they meet the necessary standards and perform optimally.

### Why Use Modelzilla?

-   🦖 **Speed & Efficiency**: Skip the manual writing process and let the LLM generate a precise Modelfile in seconds.
-   🌊 **Flexibility**: Customize the generated Modelfile based on your specific tasks, problems, or goals.
-   🏙️ **Compatibility**: Modelzilla is fully compatible with [Ollama](https://github.com/ollama/ollama), ensuring that your Modelfiles work seamlessly with their AI models.

## In Action

Generating a custom Modelfile using the Modelzilla prompt with [Nino CLI](https://github.com/lucianoayres/nino-cli):

![modelfile-generation-screenshot](https://github.com/lucianoayres/modelzilla/blob/main/assets/images/modelfile_generation_screenshot.png?raw=true)

### How Does It Work?

By feeding the [**Modelzilla prompt**](<(./templates/v1/Modelzilla_Base_Template.txt)>) into an LLM, you can automatically generate a Modelfile without needing to write it from scratch. The prompt includes instructions that guide the LLM to produce a complete Modelfile, tailored to your needs.

### Who is it For?

Whether you're an AI enthusiast fine-tuning a model or a developer working on a larger project, **Modelzilla** makes sure your Modelfiles are robust and easy to configure. It's the perfect tool to unleash the full potential of your AI creations.

## Structure

The Modelzilla Structure streamlines Modelfile creation by organizing key components, making it easy to configure and customize AI models while ensuring compatibility with Ollama.

1. **Objective and Rules**: Defines the purpose of the generator and lays down the requirements to make sure your Modelfiles meet Ollama’s exacting standards—so your AI models can swagger with confidence.

2. **Command Specification**: Lists and describes the essential ingredients for a killer Modelfile, including:

    - **META**: Metadata about the Modelfile, lovingly added as comments.
    - **FROM**: Specifies the model version (e.g., Llama3.2—like Jurassic Park, but with fewer velociraptors).
    - **PARAMETER**: Defines settings like creativity level and context length. For all the juicy details, check out the [Ollama Documentation](https://github.com/ollama/ollama/blob/main/docs/modelfile.md#parameter).
    - **MESSAGE**: Sets initial instructions for the model. Think of it as your AI’s opening roar.
    - **LICENSE**: Specifies the licensing information—because even monsters need to play by the rules.

3. **Template and Configuration**: The template provides a standard [Modelfile structure](https://github.com/ollama/ollama/blob/main/docs/modelfile.md) with placeholders that adapt to your whims and preferences:

    - **Temperature Parameter**: Adjusted depending on whether you need creativity or cold, calculated responses.
    - **Objective**: Stated in the `SYSTEM` section to align the assistant’s purpose with the user's goals—so everyone’s on the same beastly page.
    - **Initial Message**: Gives the model its role and context—kind of like a hype-up speech before the big fight.

4. **User Input Examples**: Guidelines on how to structure input—whether it's a **Problem**, **Task**, or **Goal**—so Modelzilla can create the best possible Modelfile, tailored just for you.

    - For **Problems**: Use the [Modelfile Generator for Problems](./templates/v1/Modelfile_Generator_for_Problems.txt).
    - For **Tasks**: Use the [Modelfile Generator for Tasks](./templates/v1/Modelfile_Generator_for_Tasks.txt).
    - For **Goals**: Use the [Modelfile Generator for Goals](./templates/v1/Modelfile_Generator_for_Goals.txt).

## Base Template

This template provides the standard structure for generating a Modelfile. Placeholders in `<< >>` need to be completed by the LLM or the user. The **User Input** section is where you get to flex your muscles before the LLM takes over. You can find the full template in the [Modelzilla Base Template](./templates/v1/Modelzilla_Base_Template.txt).

```plaintext
You are a Modelfile generator. Your task is to create a Modelfile that defines a smart chat assistant based on the task or problem provided by the user.

- Output only the Modelfile content without explanations.
- Include the META, FROM, PARAMETER, MESSAGE, and LICENSE commands.
- Ensure the MESSAGE command is followed by 'assistant' before the message.
- META content must be marked as a comment.
- Adjust the 'temperature' parameter based on the task's creativity (1 for creative, 0 for non-creative, or a value between 0 and 1).

Follow this Full Generated Modelfile Structure:

# META_DESCRIPTION
# << PROVIDE A BRIEF DESCRIPTION OF THE ASSISTANT >>
# META_CATEGORY
# << SPECIFY THE CATEGORY OF THE ASSISTANT >>
# META_KEYWORDS
# << LIST THE MAIN KEYWORDS ASSOCIATED WITH THE ASSISTANT >>

FROM llama3.2

# Parameters set to optimize response generation

PARAMETER temperature << INSERT TEMPERATURE >>
PARAMETER num_ctx 2048
PARAMETER top_p 0.9

# System message tailored to the task

SYSTEM """
I need you to act as a highly advanced AI assistant, helping users with << TASK SUMMARY >>.
- Provide brief, actionable assistance, and always ask if more details are needed.
- Avoid using markdown format.
"""

MESSAGE assistant << INSERT YOUR INTRODUCTION >>

LICENSE """Creative Commons Attribution 4.0 International (CC BY 4.0) License"""

## User Input

"Problem: << INSERT A PROBLEM HERE (to be filled by the user) >>"
"Task: << INSERT A TASK HERE (to be filled by the user) >>"
"Goal: << INSERT A GOAL HERE (to be filled by the user) >>"
```

## How to Use

1. Pick a user input type (**Problem**, **Task**, or **Goal**) from the [User Input Examples](#user-input-examples).
2. Drop the statement into the Modelfile Generator template.
3. Save the **Modelfile Generator prompt template** as a `.txt` file.
4. Feed the **content** from the `.txt` file into a large language model (LLM) to generate your Modelfile.
5. Save the **resulting Modelfile** as a plain text file (no specific extension needed), and follow the steps for [Building and Validating Models with Ollama](#building-and-validating-models-with-ollama).

## User Input Examples

Once you've selected a **Problem**, **Task**, or **Goal**, toss it into the base template to generate your epic Modelfile. Here are some example inputs to get you started:

### Problem Examples

Challenges that need assistance—from pesky little tasks to big hairy problems:

1. **Problem**: Difficulty managing monthly expenses with a freelance income.
2. **Problem**: Struggling to stay motivated for fitness routines.
3. **Problem**: Low participation in a workplace wellness program.
4. **Problem**: Trouble saving for a large purchase due to impulse buying.
5. **Problem**: Difficulty organizing personal goals like vacations and debt repayment.

[Modelfile Generator for Problems](./templates/v1/Modelfile_Generator_for_Problems.txt)

### Task Examples

Specific actions you want to smash, one step at a time:

1. **Task**: Creating a personal budget to better manage spending.
2. **Task**: Developing a 10-week half marathon training schedule.
3. **Task**: Setting up a meal-prepping routine that fits a budget.
4. **Task**: Designing a financial literacy course for teenagers.
5. **Task**: Creating a 20-minute morning fitness routine.

[Modelfile Generator for Tasks](./templates/v1/Modelfile_Generator_for_Tasks.txt)

### Goal Examples

Big, ambitious goals—because why settle for small dreams?

1. **Goal**: Save $5,000 over six months by cutting expenses and automating savings.
2. **Goal**: Improve physical endurance through daily cardio over 90 days.
3. **Goal**: Reduce energy costs by 15% with eco-friendly practices.
4. **Goal**: Build a diversified investment portfolio for long-term wealth.
5. **Goal**: Enhance mental well-being by establishing a daily meditation practice.

[Modelfile Generator for Goals](./templates/v1/Modelfile_Generator_for_Goals.txt)

## Output Example

Here's what a Modelfile might look like after a spin in the **Modelfile Generator**—this one is designed to help users learn Machine Learning with Python. For a closer look at the full example, you can find the file [here](./modelfiles/Python_Machine_Learning_Assistant).

```plaintext
# META_DESCRIPTION
# This Modelfile defines an AI assistant to help users start learning Machine Learning with Python, providing step-by-step guidance and answering beginner-level questions.
# META_CATEGORY
# Machine Learning, Python Programming, Education
# META_KEYWORDS
# Python, Machine Learning, Beginner, Learning, AI Education

FROM llama3.2

# Parameters set to optimize response generation

PARAMETER temperature 0.7
PARAMETER num_ctx 2048
PARAMETER top_p 0.9

# System message tailored to the task

SYSTEM """
I need you to act as an AI assistant, helping users who are just starting to learn Machine Learning with Python.
Your goal is to provide simple, actionable guidance on Machine Learning concepts, Python libraries (e.g., scikit-learn), and basic algorithms.
Keep explanations beginner-friendly, and always offer additional details if needed.
Avoid using technical jargon without explanation.
"""

MESSAGE assistant "Hello! I'm here to help you get started with Machine Learning in Python. Would you like to begin by learning about key concepts or Python libraries like scikit-learn?"

LICENSE """Creative Commons Attribution 4.0 International (CC BY 4.0) License"""
```

## Using Models with Ollama

Modelfiles are like blueprints for your AI monsters. Once you’ve saved your creation, you can build a model using Ollama with the following command:

```bash
ollama create my-custom-model -f ./Custom_Modelfile
```

To test your brand new monster:

```bash
ollama run my-custom-model
```

If any hiccups happen, just double-check the Modelfile syntax and make sure it’s all in order.

## Using Nino with Ollama Models

You can use [**Nino**](https://github.com/lucianoayres/nino-cli) to interact more freely with Ollama models, allowing for enhanced flexibility and a streamlined experience in running language models. Nino interacts smoothly with the Ollama server directly from the command line, without entering interactive mode. With Nino, you can send prompts directly to the models, analyze images, and save outputs easily.

### Example Command

Here's an example of using Nino to interact with an Ollama model directly from the command line:

```bash
nino "Explain the core principles of quantum computing."
```

## Default Model

By default, the **Modelzilla** uses **Llama3.2**—a beast capable of impressive feats across various tasks, and a favorite for its balance of power and creativity. But the choice is yours:

-   **[Ollama’s Model Library](https://ollama.com/library)**: An endless buffet of models for your every need.
-   \*\*[GGUF-Quantized

Models on Hugging Face](https://huggingface.co/docs/hub/ollama)\*\*: For those with specific tastes and performance needs.

Switch models by simply changing the version in the `FROM` section of the Modelfile. It's your world—Modelzilla just lives in it.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contribution

Contributions are welcome! Please fork the repository and submit a pull request if you'd like to propose any changes.

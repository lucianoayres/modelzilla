# 🦖 Modelzilla

![modelzilla-banner](https://github.com/lucianoayres/modelzilla/blob/main/assets/images/banner_modelzilla.png?raw=true)

## Unleashing Monster Models For Your AI Beasts

[What's Modelzilla? 🦖](#whats-modelzilla-) · [Why Use Modelzilla? 🚀](#why-use-modelzilla-) · [How Does It Work? ⚙️](#how-does-it-work-) · [Who Is It For? 🎯](#who-is-it-for-) · [How to Use 🛠️](#how-to-use-) · [Using Nino with Ollama 🐶](#using-nino-with-ollama-) · [Templates 📄](#templates-) · [Examples 📂](#examples-) · [License 📄](#license-) · [Contribution 🤝](#contribution-)

### What's Modelzilla? 🦖

**Modelzilla** is an AI model designed to generate [Modelfiles](https://github.com/ollama/ollama/blob/main/docs/modelfile.md) for your custom AI assistants based on the tasks or problems you provide. By leveraging [Ollama](https://github.com/ollama/ollama), Modelzilla simplifies the creation of Modelfiles, enabling you to build tailored AI models with ease. It's like having a dinosaur that builds other dinosaurs—monster models for your AI beasts!

### Why Use Modelzilla? 🚀

-   🦖 **Efficiency**: Automatically generate Modelfiles for custom AI assistants without writing them from scratch.
-   🎯 **Precision**: By using tasks generated from Octask, you provide clear and focused input, resulting in more effective AI models.
-   🌊 **Flexibility**: Provide any task or goal, and Modelzilla will create a Modelfile tailored to it.
-   🏙️ **Compatibility**: Fully compatible with [Ollama](https://github.com/ollama/ollama), ensuring seamless model creation and deployment.

### How Does It Work? ⚙️

Modelzilla uses a [Modelfile](./modelfiles/Modelzilla1.0) that defines an AI model capable of generating Modelfiles based on user-provided tasks or problems. By creating this model with Ollama, you can interact with Modelzilla to produce custom Modelfiles for your specific needs.

## Who Is It For? 🎯

Modelzilla is for anyone who wants to build AI models tailored to their unique needs, without diving deep into complex Modelfile syntax. Whether you're an AI enthusiast, developer, or just curious about creating custom AI assistants, this tool empowers you to bring your ideas to life!

Imagine building:

-   **👨‍💻 An AI Coding Tutor** to help you master programming languages like Python or JavaScript through personalized lessons and real-time feedback.
-   **🇪🇸 A Spanish Language Teacher** that adapts to your pace and proficiency, helping you prepare for business meetings or simply to improve your communication skills.
-   **💼 A Personal Finance Advisor** to help you set, track, and achieve your financial goals by offering tailored budgeting advice.
-   **🏋️‍♀️ A Fitness Coach** that designs custom workout plans based on your fitness level and goals.
-   **🧘‍♀️ A Mental Wellness Companion** offering mindfulness practices and daily check-ins to support emotional well-being.
-   **🍳 A Recipe Assistant** that suggests meal ideas based on your dietary preferences and what's in your fridge.

With Modelzilla, you can create AI assistants for virtually any task, making AI more accessible and personalized for everyone!

## How to Use 🛠️

Follow these steps to use Modelzilla and create your custom AI assistant:

### 1. Prepare Your Task

We recommend using [**Octask**](https://github.com/lucianoayres/octask) to generate clear and actionable tasks. Octask can help you define your idea, goal, or problem more precisely, which in turn allows Modelzilla to create a more effective Modelfile.

#### Example using Octask Express:

```bash
ollama run octask-express1.0
```

**User Input**:

```
I want to create an AI assistant that helps users learn basic French conversation.
```

**Octask Output**:

-   Develop an AI model that teaches basic French conversation skills.
-   Include lessons on common phrases, pronunciation, and cultural tips.
-   Implement interactive dialogues for practice.
-   Ensure the assistant adapts to the user's learning pace.

### 2. Clone the Modelzilla Repository

```bash
git clone https://github.com/lucianoayres/modelzilla.git
cd modelzilla
```

### 3. Ensure Ollama is Installed

Make sure you have [Ollama](https://github.com/ollama/ollama) installed on your system.

### 4. Create the Modelzilla Model

```bash
ollama create modelzilla1.0 -f ./modelfiles/Modelzilla1.0
```

### 5. Run Modelzilla

```bash
ollama run modelzilla1.0
```

### 6. Provide Your Task or Problem

When prompted, input the task you've defined (preferably using Octask). For example:

```
Task: Develop an AI assistant that helps users learn basic French conversation, including common phrases, pronunciation, and interactive dialogues.
```

### 7. Save the Generated Modelfile

Modelzilla will output a Modelfile tailored to your input. Copy this output and save it as a plain text file (e.g., `FrenchTutorModelfile`). You can optionally use [Nino](#using-nino-with-ollama) to save the Modelfile locally, making it ideal for automated workflows.

### 8. Create Your Custom AI Model

Use Ollama to create a new model from the generated Modelfile:

```bash
ollama create french-tutor -f ./FrenchTutorModelfile
```

### 9. Run Your Custom Model

Test your new AI assistant:

```bash
ollama run french-tutor
```

### 10. Interact with Your AI Assistant

Start learning French!

```
You: Bonjour! Can you teach me how to order food in a restaurant?
AI Assistant: Absolutely! Let's start with some common phrases...
```

If any issues occur, double-check your Modelfile for syntax errors and ensure it's compatible with Ollama.

## Using Nino with Ollama 🐶

You can also use [**Nino**](https://github.com/lucianoayres/nino-cli) to interact with your Ollama models more freely. Nino allows you to send prompts directly to the models from the command line without entering interactive mode, and it also allows you to export the AI's response to a local file.

### Example Command

```bash
nino "Teach me how to greet someone in French." --model french-tutor --output lesson.txt
```

## Templates 📄

While the central product is now the [Modelzilla Modelfile](./modelfiles/Modelzilla1.0), the original prompt templates and examples are still available for reference in the [prompts directory](./prompts). These resources are valuable for understanding the structure of Modelfiles and can serve educational purposes.

### Structure 🏗️

The Modelzilla template streamlines Modelfile creation by organizing key components, making it easy to configure and customize AI models while ensuring compatibility with Ollama. The structure includes:

1. **Objective and Rules** 📜: Defines the assistant's purpose and lays out guidelines to ensure the generated Modelfile meets Ollama's standards.

2. **Command Specification** 🍳: Details essential commands used in a Modelfile, such as:

    - **META**: Contains metadata about the Modelfile, added as comments.
    - **FROM**: Specifies the base model version (e.g., `llama3.2`).
    - **PARAMETER**: Sets model parameters like `temperature`, `num_ctx`, and `top_p`.
    - **MESSAGE**: Provides initial messages or prompts for the assistant.
    - **LICENSE**: Includes licensing information for the Modelfile.

3. **Template and Configuration** 🧩: Offers a standard Modelfile template with placeholders (`<< >>`) that can be customized based on your specific task or goal.

4. **User Input** 💡: A task, problem, or goal description to generate the most effective Modelfile.

## Examples 📂

### User Input Examples 📝

Examples of tasks, problems, or goals that you can provide to Modelzilla are available in the [examples directory](./examples/prompts). These examples can help you understand how to structure your input for optimal results. Here are some sample inputs:

-   **Task**: "Develop an AI assistant that helps users practice mindfulness meditation."
-   **Problem**: "Users find it difficult to stay motivated while learning a new language."
-   **Goal**: "Create an AI model that provides daily workout routines customized to the user's fitness level."

### Output Example 🎉

Examples of Modelfiles generated by Modelzilla can be found in the [modelfiles examples directory](./examples/modelfiles). Reviewing these examples will give you insight into the format and content of Modelfiles produced by Modelzilla.

### Examples of Models Created with Modelzilla

-   **[Octask](https://github.com/lucianoayres/octask)**: An AI model designed to help you define clear and actionable tasks from your ideas, goals, or problems.
-   **[Catnip](https://github.com/lucianoayres/catnip)**: An AI model that generates comprehensive categories related to your topics or areas of interest.
-   **[Parrot](https://github.com/lucianoayres/parrot)**: An AI model designed to help you generate custom `PARAMETER` settings for your Modelfiles used in Ollama.

By reviewing these examples, you can understand how Modelzilla can be used to create powerful AI assistants tailored to specific needs.

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contribution 🤝

Contributions are welcome! Please fork the repository and submit a pull request if you'd like to propose any changes.

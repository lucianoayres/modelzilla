# 🦖 Modelzilla

![modelzilla-banner](https://github.com/lucianoayres/modelzilla/blob/main/assets/images/banner_modelzilla.png?raw=true)

## Unleashing Monster Models For Your AI Beasts

[What's Modelzilla? 🦖](#whats-modelzilla-) · [Why Use Modelzilla? 🚀](#why-use-modelzilla-) · [Modes ⚡](#modes-️) · [How Does It Work? ⚙️](#how-does-it-work-) · [Who Is It For? 🎯](#who-is-it-for-) · [How to Use 🛠️](#how-to-use-) · [Using Nino with Ollama 🐶](#using-nino-with-ollama-) · [Templates 📄](#templates-) · [Examples 📂](#examples-) · [License 📄](#license-) · [Contribution 🤝](#contribution-)

### What's Modelzilla? 🦖

**Modelzilla** is an AI model designed to generate [Modelfiles](https://github.com/ollama/ollama/blob/main/docs/modelfile.md) for your custom AI creations based on the tasks or problems you provide. By leveraging [Ollama](https://github.com/ollama/ollama), Modelzilla simplifies the creation of Modelfiles, enabling you to build tailored AI models with ease. It's like having a dinosaur that builds other dinosaurs—monster models for your AI beasts!

### Why Use Modelzilla? 🚀

-   🦖 **Efficiency**: Automatically generate Modelfiles for custom AI assistants and tools without writing them from scratch.
-   🎯 **Precision**: By using tasks generated from Octask, you provide clear and focused input, resulting in more effective AI models.
-   🌊 **Flexibility**: Provide any task or goal, and Modelzilla will create a Modelfile tailored to it.
-   🏙️ **Compatibility**: Fully compatible with [Ollama](https://github.com/ollama/ollama), ensuring seamless model creation and deployment.

### Modes ⚡

Modelzilla offers two powerful modes to cater to different AI development needs:

#### 1. **Modelzilla Assistants 🤖**

Generate intelligent AI assistants tailored to your specific tasks and requirements. Whether you need a coding tutor, language teacher, or personal finance advisor, **Modelzilla Assistants** empowers you to create versatile AI companions that can interact, learn, and assist users effectively.

**Key Features:**

-   **Custom AI Assistants**: Design assistants for various domains such as education, finance, wellness, and more.
-   **Interactive Dialogues**: Implement engaging and adaptive conversations to enhance user experience.
-   **Personalization**: Tailor the assistant's responses and functionalities to match user preferences and needs.

Explore the [Modelzilla-Assistants1.0 Modelfile](./modelfiles/Modelzilla-Assistants1.0) to get started.

#### 2. **Modelzilla Tools 🛠️**

Build AI-powered tools that process and generate content according to your specifications. **Modelzilla Tools** allows you to create specialized tools for tasks like data analysis, content generation, workflow automation, and other custom processing needs, enabling you to streamline operations and enhance productivity.

**Key Features:**

-   **Custom AI Tools**: Develop tools for specific processing tasks such as data transformation, report generation, and more.
-   **User-Defined Inputs and Outputs**: Define the input data format and output formatting to suit your workflow requirements.
-   **Integration Ready**: Seamlessly integrate your AI tools with existing systems and platforms.

Check out the [Modelzilla-Tools1.0 Modelfile](./modelfiles/Modelzilla-Tools1.0) for more details.

### How Does It Work? ⚙️

Modelzilla utilizes dedicated [Modelfiles](./modelfiles/) that define AI models capable of generating Modelfiles based on user-provided tasks or problems. Specifically:

-   **Assistants Mode**: Uses [Modelzilla-Assistants1.0](./modelfiles/Modelzilla-Assistants1.0) to generate Modelfiles for AI assistants.
-   **Tools Mode**: Uses [Modelzilla-Tools1.0](./modelfiles/Modelzilla-Tools1.0) to generate Modelfiles for AI-based tools.

By creating these models with Ollama, you can interact with Modelzilla to produce custom Modelfiles tailored to your specific needs, whether you're building an Assistant or a Tool.

### Who Is It For? 🎯

Modelzilla is designed for anyone looking to create AI models tailored to their unique needs without delving deep into complex Modelfile syntax. Whether you're an AI enthusiast, developer, or simply curious about building custom AI solutions, Modelzilla empowers you to bring your ideas to life!

Imagine building:

-   **👨‍💻 An AI Coding Tutor** to help you master programming languages like Python or JavaScript through personalized lessons and real-time feedback.
-   **🇪🇸 A Spanish Language Teacher** that adapts to your pace and proficiency, helping you prepare for business meetings or simply improve your communication skills.
-   **💼 A Personal Finance Advisor** to help you set, track, and achieve your financial goals by offering tailored budgeting advice.
-   **🏋️‍♀️ A Fitness Coach** that designs custom workout plans based on your fitness level and goals.
-   **🧘‍♀️ A Mental Wellness Companion** offering mindfulness practices and daily check-ins to support emotional well-being.
-   **🍳 A Recipe Assistant** that suggests meal ideas based on your dietary preferences and what's in your fridge.
-   **📊 A Data Analysis Tool** that processes and visualizes your business metrics to inform strategic decisions.
-   **✍️ A Content Generator** that creates articles, summaries, or reports based on your input parameters.

With Modelzilla's **Assistants** and **Tools**, you can create AI solutions for virtually any task, making AI more accessible and personalized for everyone!

## How to Use 🛠️

Follow these steps to use Modelzilla and create your custom AI Assistant or Tool:

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

Depending on the mode you want to use, create the corresponding Modelzilla model:

For **Assistants**:

```bash
ollama create modelzilla-assistants1.0 -f ./modelfiles/Modelzilla-Assistants1.0
```

For **Tools**:

```bash
ollama create modelzilla-tools1.0 -f ./modelfiles/Modelzilla-Tools1.0
```

### 5. Run Modelzilla

Run the Modelzilla model based on the mode you selected:

For **Assistants**:

```bash
ollama run modelzilla-assistants1.0
```

For **Tools**:

```bash
ollama run modelzilla-tools1.0
```

### 6. Choose Your Mode and Provide Your Task or Problem

When prompted, select the desired mode (**Assistants** or **Tools**) and input the task you've defined (preferably using Octask).

#### **Assistants Example**:

```
Task: Develop an AI assistant that helps users learn basic French conversation, including common phrases, pronunciation, and interactive dialogues.
```

#### **Tools Example**:

**User Input Example**:

```
Task: Create an AI tool that processes customer transaction data from CSV format into a structured JSON format and infers potential cross-selling opportunities based on purchasing behavior.
Sample Data Format (CSV):

CustomerID, Name, Email, ProductPurchased, PurchaseAmount, PurchaseDate
101, John Doe, john@example.com, Laptop, 1200, 2024-01-15
101, John Doe, john@example.com, Mouse, 25, 2024-01-16
102, Jane Smith, jane@example.com, Smartphone, 800, 2024-02-10
102, Jane Smith, jane@example.com, Headphones, 150, 2024-02-11
103, Bob Johnson, bob@example.com, Book, 20, 2023-12-05
...

Desired Output Format (JSON Schema):
{
  "type": "object",
  "properties": {
    "CustomerID": { "type": "integer" },
    "Name": { "type": "string" },
    "Email": { "type": "string", "format": "email" },
    "ProductPurchased": { "type": "string" },
    "PurchaseAmount": { "type": "number" },
    "PurchaseDate": { "type": "string", "format": "date" },
    "CrossSellingRecommendations": {
      "type": "array",
      "items": { "type": "string" }
    }
  },
  "required": ["CustomerID", "Name", "Email", "ProductPurchased", "PurchaseAmount", "PurchaseDate", "CrossSellingRecommendations"]
}
```

**Explanation**:

In this Tools example, you provide Modelzilla with customer data in CSV format and a JSON schema that includes inferred insights. Modelzilla generates a Modelfile for an AI tool that structures the data into JSON and leverages large language models to analyze purchasing behavior and identify cross-selling opportunities.

### 7. Save the Generated Modelfile

Modelzilla will output a Modelfile tailored to your input. Copy this output and save it as a plain text file (e.g., `FrenchTutorModelfile` or `CustomerDataToolModelfile`). You can optionally use [Nino](#using-nino-with-ollama) to save the Modelfile locally, making it ideal for automated workflows.

### 8. Create Your Custom AI Model

Use Ollama to create a new model from the generated Modelfile:

For **Assistants**:

```bash
ollama create french-tutor -f ./FrenchTutorModelfile
```

For **Tools**:

```bash
ollama create customer-data-tool -f ./CustomerDataToolModelfile
```

### 9. Run Your Custom Model

Test your new AI Assistant or Tool:

```bash
ollama run french-tutor
```

or

```bash
ollama run customer-data-tool
```

### 10. Interact with Your AI Assistant or Tool

Start using your custom AI solution!

```
You: Bonjour! Can you teach me how to order food in a restaurant?
AI Assistant: Absolutely! Let's start with some common phrases...
```

or

```
You: Organize the customer data and provide the JSON output.
AI Tool: Processing your request... Here's the structured JSON data.
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
-   **Task**: "Create an AI tool that automates the generation of monthly financial reports."
-   **Problem**: "Users need a tool to summarize lengthy documents into concise bullet points."
-   **Goal**: "Develop an AI tool that analyzes customer feedback and categorizes sentiments."

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contribution 🤝

Contributions are welcome! Please fork the repository and submit a pull request if you'd like to propose any changes.

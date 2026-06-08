# RASA-

## What is Rasa?

Rasa is an open-source framework used to build AI-powered chatbots and virtual assistants. It enables developers to create conversational applications that understand user messages and respond intelligently.

## Features of Rasa

* Open-source and customizable
* Natural Language Understanding (NLU)
* Dialogue Management
* Custom Actions using Python
* Integration with websites, WhatsApp, Telegram, Slack, and more
* Machine Learning-based conversation handling

---

## Installation

### Create Virtual Environment

```bash
py -3.10 -m venv rasa_env
```

### Activate Virtual Environment

```bash
rasa_env\Scripts\activate
```

### Install Rasa

```bash
pip install rasa==3.6.20
```

### Verify Installation

```bash
rasa --version
```

---

## Important Rasa Commands

### 1. Create a New Project

```bash
rasa init
```

Creates a sample chatbot project with all required files.

### 2. Train the Chatbot

```bash
rasa train
```

Trains the chatbot using the provided training data.

### 3. Chat with the Bot

```bash
rasa shell
```

Opens an interactive chat interface in the terminal.

### 4. Run the Chatbot Server

```bash
rasa run
```

Starts the Rasa server.

### 5. Run Custom Actions

```bash
rasa run actions
```

Starts the action server for executing custom Python code.

### 6. Test the Chatbot

```bash
rasa test
```

Evaluates the chatbot's performance.

### 7. Check Version

```bash
rasa --version
```

Displays the installed version of Rasa and related dependencies.

---

## Rasa Project Structure

```text
project/
│
├── actions/
│   └── actions.py
│
├── data/
│   ├── nlu.yml
│   ├── stories.yml
│   └── rules.yml
│
├── models/
│
├── config.yml
├── domain.yml
├── credentials.yml
├── endpoints.yml
└── tests/
```

---

## Purpose of Important Files

### domain.yml

Defines:

* Intents
* Responses
* Actions
* Entities
* Slots

### nlu.yml

Contains training examples for user messages.

Example:

```yaml
version: "3.1"

nlu:
- intent: greet
  examples: |
    - hi
    - hello
    - good morning
```

### stories.yml

Defines conversation flows.

Example:

```yaml
stories:
- story: greeting
  steps:
  - intent: greet
  - action: utter_greet
```

### rules.yml

Defines fixed conversation rules.

### actions.py

Contains custom Python actions.

---

## Basic Workflow

```text
1. rasa init
2. Modify training data
3. rasa train
4. rasa shell
5. rasa run
6. rasa run actions
```

---

## Advantages of Rasa

* Free and open source
* Supports custom business logic
* Data remains under your control
* Suitable for enterprise applications
* Large developer community

---

## Applications

* Customer Support Bots
* College Helpdesk Bots
* E-commerce Assistants
* Banking Chatbots
* Healthcare Assistants
* HR and Recruitment Bots

---

## Conclusion

Rasa is one of the most powerful open-source chatbot frameworks available today. It provides complete control over chatbot development, customization, training, and deployment while supporting advanced AI-driven conversations.

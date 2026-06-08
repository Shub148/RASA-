# Install Rasa on Windows

## Prerequisites

Before installing Rasa, ensure the following are installed:

* Python 3.8, 3.9, or 3.10 (recommended)
* pip (Python package manager)
* Git (optional but recommended)

Check your Python version:

```bash
python --version
```

Check pip version:

```bash
pip --version
```

---

## Step 1: Create a Virtual Environment

Open Command Prompt and run:

```bash
python -m venv rasa_env
```

Activate the virtual environment:

```bash
rasa_env\Scripts\activate
```

You should see:

```bash
(rasa_env) C:\Users\YourName>
```

---

## Step 2: Upgrade pip

```bash
python -m pip install --upgrade pip
```

---

## Step 3: Install Rasa

Install the latest compatible version:

```bash
pip install rasa
```

To install a specific version:

```bash
pip install rasa==3.6.20
```

---

## Step 4: Verify Installation

Check whether Rasa is installed successfully:

```bash
rasa --version
```

Example output:

```bash
Rasa Version      : 3.x.x
Python Version    : 3.x.x
Operating System  : Windows
```

---

## Step 5: Create a New Rasa Project

```bash
rasa init
```

Press Enter when prompted.

Rasa will create a sample chatbot project structure.

---

## Step 6: Train the Bot

```bash
rasa train
```

---

## Step 7: Run the Chatbot

Start the bot:

```bash
rasa shell
```

Example:

```text
Your input -> hello
Bot -> Hi! How can I help you today?
```

---

## Common Errors

### TensorFlow Installation Error

Install Microsoft Visual C++ Build Tools:

https://visualstudio.microsoft.com/visual-cpp-build-tools/

### Python Version Not Supported

Use Python 3.10 if installation fails with newer versions.

### Permission Error

Run Command Prompt as Administrator.

---

## Useful Commands

```bash
rasa init
rasa train
rasa shell
rasa run
rasa run actions
rasa test
rasa --version
```

| Command            | Meaning                                                                                                                                                        |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `rasa init`        | Creates a new Rasa chatbot project with sample files and training data. Think of it as **starting a new chatbot project**.                                     |
| `rasa train`       | Trains the chatbot using the data in `data/`, `domain.yml`, and `config.yml`. Think of it as **teaching the bot**.                                             |
| `rasa shell`       | Opens a chat window in the terminal where you can talk to your bot. Think of it as **testing the bot by chatting with it**.                                    |
| `rasa run`         | Starts the chatbot server so it can receive messages from websites, apps, or APIs. Think of it as **turning the bot on**.                                      |
| `rasa run actions` | Starts the custom action server that runs Python code from `actions.py`. Think of it as **enabling advanced bot features** like database queries or API calls. |
| `rasa test`        | Tests your chatbot and shows how accurate it is. Think of it as **giving the bot an exam**.                                                                    |
| `rasa --version`   | Shows the installed Rasa version and environment details. Think of it as **checking the bot software version**.                                                |


## Resources

Official Rasa Documentation:
https://rasa.com/docs/

GitHub Repository:
https://github.com/RasaHQ/rasa

# TerminalAI

Ask cloud AI models questions straight from your terminal with a single command.

TerminalAI sends your question to a model hosted on [OpenRouter](https://openrouter.ai/) and prints the answer right in your terminal.

```shell
python3 ask.py "What is 20 times 4?"
```

## How it works

1. Your OpenRouter API key is stored in a `.env` file in the project folder.
2. You run `ask.py` with your question in quotes.
3. The script sends the question to OpenRouter using your key.
4. The model's answer is displayed in your terminal.

## Requirements

- Python 3.8 or newer
- An OpenRouter account and API key

## Installation

Clone the repository and set up a virtual environment:

```shell
git clone https://github.com/dhritimnn/TerminalAI.git
cd TerminalAI
python3 -m venv myenv
source myenv/bin/activate
pip install openai rich python-dotenv
```

On Windows, activate the environment with `myenv\Scripts\activate` instead.

## Configuration

Create a `.env` file in the project folder:

```shell
touch .env
```

Open `.env` in any editor and add your key:

```env
KEY="your_key_here"
```

Never commit this file. It is listed in `.gitignore` to keep your key private.

## Getting an OpenRouter API key

1. Go to [openrouter.ai](https://openrouter.ai/) and create an account or log in.
2. Open the [API keys page](https://openrouter.ai/settings/keys).
3. Create a new key and copy it.
4. Paste it into the `.env` file as shown above.

## Usage

```shell
python3 ask.py "What is 20 times 4?"
```

The answer appears in your terminal once the model responds.

## Security

- Keep your API key secret. Anyone with the key can make requests on your account.
- If you accidentally commit or share a key, revoke it on OpenRouter and create a new one.

# AlphaSwarm

AlphaSwarm is a starter kit for building LLM-powered AI agents that interpret natural language trading strategies, analyze real-time market signals, and autonomously execute trades across multiple chains.

---

## Features

### AI-Powered Trading with Agents
- 🤖 LLM-powered agents capable of processing complex, unstructured signals for trading decisions  
- 🧠 Intelligent tool selection and chaining for complex multi-step analysis  
- 🚀 Dynamic composition and execution of Python code using available tools  
- 💬 Natural language strategy definition and real-time reasoning  
- 📊 Iterative agentic reasoning to evaluate market conditions, weigh multiple input signals, and make trading decisions given input trading strategy  

### Trading & Execution
- ⚡ Real-time strategy execution and monitoring  
- 🔔 Flexible execution modes:  
  - Automated trading alerts via Telegram  
  - Autonomous trade execution  
- 🔄 Multi-chain support with growing DEX integrations:  
  - **Ethereum, Base** *(Solana coming soon!)*  
  - **Uniswap V2/V3** *(Jupiter coming soon!)*  

### Modular Architecture
- 🛠️ Extensible plugin system for:
  - Data sources and signals
  - Trading strategies
  - Agent tools and capabilities
  - DEX integrations
  - On-chain data providers
- 🔌 Easy integration of new data sources and execution venues  

---

## Roadmap
- 🌐 Integration with Theoriq protocol to connect with a growing ecosystem of agents and swarms providing trading strategies and signals

---

## Prerequisites
- **Python 3.11 or higher**  
  - [Download and install Python here](https://www.python.org/downloads/)
  - Verify installation:  
    ```sh
    python --version
    ```
- **Poetry (Package Manager)**  
  - Install Poetry:  
    ```sh
    pipx install poetry
    ```
  - Verify installation:  
    ```sh
    poetry --version
    ```
- **Basic understanding of crypto trading concepts**

---

## Getting Started

### 1. Installation
First, ensure all prerequisites are installed. Then, follow these steps:

Clone the repository:
```sh
git clone https://github.com/chain-ml/alphaswarm.git
cd alphaswarm
```

Install dependencies:
```sh
# Basic installation
poetry install

# Development installation (includes testing tools)
poetry install --with dev
```

---

### 2. API Keys Setup
Before running AlphaSwarm, obtain the following API keys:

- **LLM API Key:**
  - [Anthropic API Key](https://docs.anthropic.com/en/api/getting-started) *(for Claude models, default)*
  - [OpenAI API Key](https://platform.openai.com/docs/quickstart) *(for GPT models)*
  - [Other LLM providers supported by LiteLLM](https://models.litellm.ai/)

- **Blockchain Access:**
  - [Alchemy API Key](https://www.alchemy.com/) *(required for blockchain data)*
  - [RPC URLs from Alchemy or Infura](https://www.infura.io/)

- **Optional - Telegram Bot (for notifications):**
  - Create a bot using BotFather (`/newbot`) and save the token
  - To get chat ID, run `examples/telegram_bot.py` and message `/start` or `/id`

---

### 3. Environment Configuration

Create an environment file:
```sh
cp .env.example .env
```

Configure the required variables inside `.env`:

#### **LLM Configuration (At Least One Required)**
- `ANTHROPIC_API_KEY` - Anthropic API key (Claude models, default)
- `OPENAI_API_KEY` - OpenAI API key (GPT models)
- Other LLM providers - follow [LiteLLM documentation](https://models.litellm.ai/)

#### **Blockchain Access**
- `ALCHEMY_API_KEY` - Alchemy API key for blockchain data
- `ETH_RPC_URL` - Ethereum RPC endpoint
- `ETH_WALLET_ADDRESS` - Ethereum wallet address
- `ETH_PRIVATE_KEY` - Ethereum private key
- `BASE_RPC_URL` - Base network RPC endpoint
- `BASE_WALLET_ADDRESS` - Base wallet address
- `BASE_PRIVATE_KEY` - Base private key

#### **Optional Configurations**
- **Testing:** Sepolia testnet RPC and wallet details
- **Notifications:** Telegram bot token and chat ID
- **Logging:** Log level and format

**Security Notes:**
🚨 Never commit your `.env` file to version control! Keep private keys secure and test on testnets before using real funds.

---

### 4. Additional Configuration

AlphaSwarm uses YAML configuration files:
- **Main config file:** `config/default.yaml`
- **Key configuration sections:**
  - Network environments (production/test)
  - Trading venues and supported pairs
  - Chain-specific wallet and RPC settings
  - Gas settings and transaction parameters
  - Telegram bot setup

🔹 **Always verify contract addresses from official sources!**

---

## Usage

See **[examples](https://github.com/chain-ml/alphaswarm/blob/main/examples/README.md)** for more details.

---

## Development

### Running Tests
```sh
make all-tests   # Run all tests
make unit-tests  # Run unit tests
make integration-tests  # Requires API keys
```

### Code Quality
The project uses:
- **Black** for formatting
- **isort** for import sorting
- **ruff** for linting
- **mypy** for type checking

```sh
poetry run black .
poetry run isort .
poetry run ruff check .
poetry run mypy .
```

or use:
```sh
make dev-lint
```

---

## Security
Review the **Security Policy** before deploying. We take security issues seriously.

---

## Contributing
AlphaSwarm is actively developed, and we welcome contributions! Feel free to submit pull requests or feature requests.

---

## Disclaimer 🚨
AlphaSwarm is **experimental software** in active development. **Use at your own risk.**

- **No financial advice**: This is not investment advice.
- **Crypto is volatile**: Trading can lead to **total loss of funds**.
- **You are responsible**: Secure your private keys and **test on testnets first**.

🔹 **Use with caution and thoroughly understand the risks before trading with real funds!**

---

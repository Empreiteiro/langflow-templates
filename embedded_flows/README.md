# Embedded Flows

The official **Langflow starter flows** (the templates shipped inside Langflow, `origin = langflow`
in the catalog), being **modernized to Langflow 1.10 core components** — `Agent`, `Memory Base`,
`Knowledge Base` — and made **bundle-free** (provider bundles replaced by core or custom
components). This is a *rearchitecture* effort, not a component-version bump.

Progress is tracked in QA checklist run **#665**
(`43535041-83db-455d-9850-594b6200dd67`, category "Embedded Flow Modernization").

## Structure

Same 3-level model as the rest of the repo:

```
embedded_flows/<subcategory>/<flow_slug>/<flow_slug>.json   (+ optional <flow_slug>.png preview)
```

- `snake_case` folder names; one folder per flow.
- A flow's `.json` is committed **only after it has been modernized & validated** (badge-free on
  official 1.10.0, integrity gate PASS). Empty folders hold a `.gitkeep` until then.
- Renamed flows use their **final** name as the slug, so the path never changes later.

## Scope

- **In scope (28):** priority Tier 1 + Tier 2. Listed below.
- **Out of scope (Tier 3, NOT in this folder):** Basic Prompting (proposed for removal),
  Invoice Summarizer, Nvidia Remix, Pokédex Agent, Search Agent.

## Flows

| Subcategory | Folder (slug) | Flow | Tier | Bundle→core |
|---|---|---|---|---|
| agents | `simple_agent` | Simple Agent | 1 | — |
| agents | `multi_agent_flow` | Basic Prompt Chaining → **Multi Agent flow** | 1 | — |
| agents | `sequential_tasks_agents` | Sequential Tasks Agents | 2 | yes |
| agents | `travel_planning_agents` | Travel Planning Agents | 2 | yes |
| agents | `deeply_research_agent` | Research Agent → **Deeply Research Agent** | 2 | yes |
| rag_and_knowledge | `document_qa` | Document Q&A | 1 | — |
| rag_and_knowledge | `knowledge_retrieval` | Knowledge Retrieval | 1 | — |
| rag_and_knowledge | `vector_store_rag` | Vector Store RAG | 1 | — |
| rag_and_knowledge | `hybrid_search_rag` | Hybrid Search RAG | 2 | yes |
| chatbots | `memory_chatbot` | Memory Chatbot | 1 | — |
| content_generation | `blog_writer` | Blog Writer | 2 | — |
| content_generation | `seo_keyword_generator` | SEO Keyword Generator | 2 | — |
| content_generation | `twitter_thread_generator` | Twitter Thread Generator | 2 | — |
| content_generation | `instagram_copywriter` | Instagram Copywriter | 2 | yes |
| content_generation | `social_media_agent` | Social Media Agent | 2 | yes |
| content_generation | `content_aggregator` | News Aggregator → **Content Aggregator** | 2 | yes |
| document_intelligence | `financial_report_parser` | Financial Report Parser | 1 | — |
| document_intelligence | `meeting_summary` | Meeting Summary | 2 | yes |
| document_intelligence | `structured_data_analysis_agent` | Structured Data Analysis Agent | 2 | yes |
| document_intelligence | `text_sentiment_analysis` | Text Sentiment Analysis | 2 | — |
| document_intelligence | `research_translation_loop` | Research Translation Loop | 2 | — |
| multimodal | `image_sentiment_analysis` | Image Sentiment Analysis | 2 | — |
| multimodal | `youtube_analysis` | Youtube Analysis | 2 | yes |
| developer_tools | `custom_component_generator` | Custom Component Generator | 2 | — |
| developer_tools | `portfolio_website_code_generator` | Portfolio Website Code Generator | 1 | — |
| data_and_analytics | `market_research` | Market Research | 2 | yes |
| data_and_analytics | `saas_pricing` | SaaS Pricing | 2 | — |
| data_and_analytics | `price_deal_finder` | Price Deal Finder | 2 | yes |

28 flows: 8 Tier 1 + 20 Tier 2. 14 currently use a provider bundle (to be replaced by core/custom).

## Renames (planned during modernization)

- `Basic Prompt Chaining` → **Multi Agent flow** (`multi_agent_flow`)
- `Research Agent` → **Deeply Research Agent** (`deeply_research_agent`)
- `News Aggregator` → **Content Aggregator** (`content_aggregator`)

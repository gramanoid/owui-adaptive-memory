Overview
Adaptive Memory is a sophisticated plugin that provides persistent, personalized memory capabilities for Large Language Models (LLMs) within OpenWebUI. It enables LLMs to remember key information about users across separate conversations, creating a more natural and personalized experience. The system dynamically extracts, filters, stores, and retrieves user-specific information from conversations, then intelligently injects relevant memories into future LLM prompts.

Key Features
Intelligent Memory Extraction

Automatically identifies facts, preferences, relationships, and goals from user messages
Categorizes memories with appropriate tags (identity, preference, behavior, relationship, goal, possession)
Focuses on user-specific information while filtering out general knowledge or trivia
Multi-layered Filtering Pipeline

Robust JSON parsing with fallback mechanisms for reliable memory extraction
Preference statement shortcuts for improved handling of common user likes/dislikes
Blacklist/whitelist system to control topic filtering
Smart deduplication using both semantic (embedding-based) and text-based similarity
Optimized Memory Retrieval

Vector-based similarity for efficient memory retrieval
Optional LLM-based relevance scoring for highest accuracy when needed
Performance optimizations to reduce unnecessary LLM calls
Adaptive Memory Management

Smart clustering and summarization of related older memories to prevent clutter
Intelligent pruning strategies when memory limits are reached
Configurable background tasks for maintenance operations
Memory Injection & Output Filtering

Injects contextually relevant memories into LLM prompts
Customizable memory display formats (bullet, numbered, paragraph)
Filters meta-explanations from LLM responses for cleaner output
Broad LLM Support

Generalized LLM provider configuration supporting both Ollama and OpenAI-compatible APIs
Configurable model selection and endpoint URLs
Optimized prompts for reliable JSON response parsing
Comprehensive Configuration System

Fine-grained control through "valve" settings
Input validation to prevent misconfiguration
Per-user configuration options
Memory Banks – categorize memories into Personal, Work, General (etc.) so retrieval / injection can be focused on a chosen context

Recent Improvements (v3.1)

Memory Confidence Scoring & Filtering
Flexible Embedding Provider Support (Local/API Valves)
Local Embedding Model Auto-Discovery
Embedding Dimension Validation
Prometheus Metrics Instrumentation
Health & Metrics Endpoints (/adaptive-memory/health, /adaptive-memory/metrics)
UI Status Emitters for Retrieval
Debugging & Robustness Fixes (Issue #15 - Thresholds, Visibility)
Minor Fixes (prometheus_client import)
User Guide Section (Consolidated Docs in Docstring)

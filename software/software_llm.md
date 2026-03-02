# Инструменты для работы с LLM

## Fine-tuning

### English

- [PEFT](https://huggingface.co/docs/peft) — Parameter-Efficient Fine-Tuning: LoRA, QLoRA, prefix tuning
- [TRL](https://huggingface.co/docs/trl) — Transformer Reinforcement Learning: RLHF, DPO для выравнивания LLM
- [Axolotl](https://github.com/OpenAccess-AI-Collective/axolotl) — обёртка для fine-tuning LLM с поддержкой множества методов
- [Unsloth](https://github.com/unslothai/unsloth) — ускоренный fine-tuning LLM (2-5x) с пониженным потреблением памяти

## Инференс и деплой

### English

- [vLLM](https://github.com/vllm-project/vllm) — быстрый инференс LLM с PagedAttention и continuous batching
- [Ollama](https://ollama.com/) — запуск LLM локально одной командой
- [llama.cpp](https://github.com/ggerganov/llama.cpp) — инференс LLM на CPU, квантизация GGUF
- [TGI](https://github.com/huggingface/text-generation-inference) (Hugging Face) — production-сервер для LLM

## Фреймворки для LLM-приложений

### English

- [LangChain](https://python.langchain.com/) — оркестрация цепочек вызовов LLM, RAG, агенты
- [LlamaIndex](https://www.llamaindex.ai/) — фреймворк для RAG: индексация, поиск, генерация ответов
- [DSPy](https://github.com/stanfordnlp/dspy) (Stanford) — программирование LLM вместо ручного промптинга

## Мониторинг и оценка

### English

- [LangSmith](https://smith.langchain.com/) — трассировка и отладка LLM-цепочек
- [Promptfoo](https://promptfoo.dev/) — тестирование и сравнение промптов

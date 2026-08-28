# IA Aplicada con Meta Llama 3

<div align="center">

[![Meta AI](https://img.shields.io/badge/Meta_AI-Llama_3.1-0866FF?style=for-the-badge)](https://ai.meta.com/llama/)
[![Groq LPU](https://img.shields.io/badge/Hardware-Groq_LPU_Inference-F55036?style=for-the-badge)](https://groq.com/)
[![RAG & Vectors](https://img.shields.io/badge/Retrieval-Sentence_Transformers-059669?style=for-the-badge)](https://sbert.net/)
[![WhatsApp API](https://img.shields.io/badge/Meta-WhatsApp_Cloud_API-25D366?style=for-the-badge)](https://developers.facebook.com/)
[![Google Colab](https://img.shields.io/badge/Notebooks-Google_Colab_Ready-F9AB00?style=for-the-badge)](https://colab.research.google.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![CI Quality](https://github.com/marcelayanes/meta-llama-engineering-labs/actions/workflows/ci.yml/badge.svg)](https://github.com/marcelayanes/meta-llama-engineering-labs/actions/workflows/ci.yml)

</div>

Repositorio con el trabajo resuelto de la especialización en Inteligencia Artificial Aplicada con modelos de pesos abiertos (Meta Llama 3): los tres challenges prácticos, los manuales teóricos por módulo y los scripts para correrlos desde terminal.

## Contenido

| Carpeta | Contenido |
|---|---|
| `notebooks/` | Los 3 cuadernos de Colab de los challenges |
| `docs/` | Manuales teóricos en Markdown, por módulo |
| `scripts/` | Versión en terminal de los challenges 1 y 2 (Python) |
| `reports/` | Reportes de cada challenge en formato APA 7 (HTML / PDF / LaTeX) |
| `data/` | Datos de apoyo del challenge de RAG |

## Challenges

| # | Challenge | En qué consiste | Colab |
|---|---|---|---|
| 1 | Comparador de Modelos Llama | Medición de latencia, throughput y calidad de respuesta entre un modelo ligero (20B), uno de razonamiento CoT (27B) y uno grande (120B), sobre hardware Groq LPU. | [Abrir](https://colab.research.google.com/github/marcelayanes/meta-llama-labs/blob/main/notebooks/01_Challenge1_MultiModel_Benchmark_Groq.ipynb) |
| 2 | Asistente de Políticas con RAG | Pipeline de RAG con `sentence-transformers` para embeddings, similitud coseno para recuperar contexto y respuestas ancladas en los documentos, sin alucinar. | [Abrir](https://colab.research.google.com/github/marcelayanes/meta-llama-labs/blob/main/notebooks/02_Challenge2_RAG_Politicas_SentenceTransformers.ipynb) |
| 3 | Fine-Tuning con LoRA | Ajuste fino de bajo rango (PEFT) con `peft`, `trl` y `SFTTrainer` sobre una GPU T4, midiendo la caída de la función de pérdida. | [Abrir](https://colab.research.google.com/github/marcelayanes/meta-llama-labs/blob/main/notebooks/03_Challenge3_FineTuning_LoRA_Llama.ipynb) |

## Estructura del programa

**Módulo 1 · Fundamentos de IA y ecosistema de modelos abiertos**

- [1.1 Arquitectura Transformer & Llama 3](docs/modulo-1-fundamentos-ia/01-arquitectura-transformer-llama3.md)
- [1.2 Prompt Engineering & Sistemas RAG](docs/modulo-1-fundamentos-ia/02-prompt-engineering-avanzado-rag.md)
- [1.3 Fine-Tuning LoRA / QLoRA & Evaluación](docs/modulo-1-fundamentos-ia/03-fine-tuning-lora-qlora-evaluacion.md)
- [1.4 Del prototipo al pipeline productivo](docs/modulo-1-fundamentos-ia/04-del-prototipo-al-pipeline-productivo.md)
- [Challenge 1](docs/modulo-1-fundamentos-ia/challenge-1-benchmark-multi-modelo.md) · [Challenge 2](docs/modulo-1-fundamentos-ia/challenge-2-asistente-politicas-rag.md) · [Challenge 3](docs/modulo-1-fundamentos-ia/challenge-3-fine-tuning-lora.md)

**Módulo 2 · Automatización con Llama y WhatsApp Cloud API**

- [2.1 WhatsApp Cloud API & Webhooks](docs/modulo-2-automatizacion-agentes-whatsapp/01-whatsapp-cloud-api-arquitectura-webhooks.md)
- [2.2 Agentes conversacionales y memoria con Redis](docs/modulo-2-automatizacion-agentes-whatsapp/02-agentes-conversacionales-memoria-redis.md)
- [2.3 Inferencia, Function Calling & Tools](docs/modulo-2-automatizacion-agentes-whatsapp/03-inferencia-function-calling-tools.md)
- [2.4 Producción, SRE y seguridad con Llama Guard](docs/modulo-2-automatizacion-agentes-whatsapp/04-produccion-seguridad-llama-guard.md)

## Cómo correrlo en local

```bash
git clone https://github.com/marcelayanes/meta-llama-labs.git
cd meta-llama-labs
python3 -m venv venv
source venv/bin/activate   # En Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
# Agregar la clave de Groq en .env
```

```bash
python3 scripts/ejecutar_challenge1.py --modelo openai/gpt-oss-20b --query "¿Qué es Grouped-Query Attention?"
python3 scripts/ejecutar_challenge2.py --modelo openai/gpt-oss-20b
```

## Tecnologías

`meta-llama-3` `llama-3.1` `rag-system` `sentence-transformers` `groq-lpu` `vector-embeddings` `fastapi` `docker` `redis` `whatsapp-cloud-api` `function-calling` `llama-guard-3` `prompt-engineering` `lora` `qlora`

## Autora

Marcela de los Ángeles Yanes Pérez
Doctorado en Ciencias de la Computación — Universidad Juárez Autónoma de Tabasco (UJAT)
marcelayanesperez@gmail.com

## Licencia

Distribuido bajo la Licencia MIT. Ver [LICENSE](LICENSE).

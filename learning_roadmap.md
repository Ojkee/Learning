# ML/DL Career Roadmap

## Faza 1 - Deep Learning od środka

### 🛠 Git

- [x] **Model wewnętrzny**: blob / tree / commit / ref - czym naprawdę jest commit
- [x] **Gałęzie**: merge vs rebase, fast-forward, konflikty
- [ ] **Ratunek**: reflog, reset (soft/mixed/hard), restore, stash, bisect
- [ ] **Zespół**: PR flow, worktrees, pre-commit hooks
- [ ] **Pod ML**: git-lfs i DVC dla danych i wag (wraca w fazie 4)

#### Źródła dodatkowe

- [Kurs wideo](https://www.youtube.com/watch?v=rH3zE7VlIMs)

### 🎬 Karpathy: Neural Networks Zero to Hero

- [x] **Ep 1** - micrograd: autograd engine od zera, DAG, reverse-mode autodiff
- [x] **Ep 2** - makemore part 1: bigram LM, torch.Tensor
- [x] **Ep 3** - makemore part 2: MLP, train/val/test split, underfitting
- [x] **Ep 4** - makemore part 3: BatchNorm, init, diagnostics narzędzia
- [x] **Ep 5** - backprop ręcznie przez MLP bez autograd
- [x] **Ep 6** - makemore part 5: WaveNet-style CNN hierarchicznie
- [x] **Ep 7** - nanoGPT: Transformer od zera, attention, residual
- [x] **Ep 8** - GPT Tokenizer: BPE od zera

#### Źródła dodatkowe

- [karpathy.ai/zero-to-hero](https://karpathy.ai/zero-to-hero.html)

### 📚 fast.ai Part 1: Practical Deep Learning for Coders

- [x] **Lesson 1-2**: ResNet image classifier, deploy w Kaggle/HF Spaces
- [x] **Lesson 3-4**: Data augmentation, Transfer learning, fine-tuning
- [x] **Lesson 5**: From-scratch NLP model z tabular data
- [x] **Lesson 6**: Random forests vs deep learning - kiedy co
- [x] **Lesson 7**: Collaborative filtering (embedding approach)
- [x] **Lesson 8**: Convolutions from scratch
- [x] **Lesson 9**: Training fundamentals - learning rate finder, 1cycle

#### Źródła dodatkowe

- [course.fast.ai](https://course.fast.ai)

### 📄 Fundamenty - czytaj równolegle z kursami (#1-#8)

- [x] **#1 The Unreasonable Effectiveness of RNNs** - Karpathy (blog) · W4 T1
- [x] **#2 Understanding LSTM Networks** - Olah · W4 T1 · [blog](https://colah.github.io/posts/2015-08-Understanding-LSTMs/)
- [ ] **#3 CS231n** - notatki Stanford: backprop, optymalizacja, trening sieci, CNN · W4 T2
- [x] **#4 ImageNet Classification with Deep CNNs** - Krizhevsky 2012 (AlexNet) · W5 T2
- [x] **#5 Recurrent Neural Network Regularization** - Zaremba et al. · W3 T2
- [ ] **#6 Neural Machine Translation by Jointly Learning to Align and Translate** - Bahdanau 2015 · W5 T3 (skąd wzięła się attention) · ⏳ w trakcie
- [ ] [The Illustrated Transformer - Jay Alammar](https://jalammar.github.io/illustrated-transformer/) (przed #7)
- [x] **#7 Attention Is All You Need** - Vaswani et al. 2017 (pierwsze czytanie) · W5 T3
- [x] **#8 The Annotated Transformer** - Harvard NLP, implementacja krok po kroku · W4 T3

#### Przed fast.ai Part 2 - dodatki

- [ ] **A Recipe for Training Neural Networks** - Karpathy [blog](http://karpathy.github.io/2019/04/25/recipe/) · debugowanie treningu, przyda się w Part 2 i własnych projektach
- [ ] **BatchNorm** (Ioffe & Szegedy 2015) + **inicjalizacja Kaiming** (He et al. 2015) - opcjonalnie; Part 2 buduje to od fundamentów, a ResNet (#9) na tym stoi
- [x] **Gotowość do Part 2**: pętla treningowa w czystym PyTorch (Dataset/DataLoader, optimizer, loss) napisana bez fast.ai

### 🔨 Framework wizualizacji: interfejsy Simulation + Model

- [x] Przykładowa symulacja: double pendulum (Lagrangian) - to tylko implementacja interfejsu, nie cel projektu
- [x] Własna sieć od zera w czystym NumPy (równolegle z Ep 1-3)
- [x] Backprop ręcznie z gradientami - zrozum każdy krok
- [x] **Interfejsy bazowe**: Simulation (reset / step / state / reward) i Model (act / update); wizualizacja zna tylko interfejsy
- [x] **Podpinanie przez config**: dowolna symulacja + dowolny model; źródło: `abc.ABC` vs `typing.Protocol`
- [x] **Diagnostyka**: loss curves, gradienty, aktywacje (jak Ep 4) - tym samym interfejsem

### 📘 Goodfellow - Deep Learning (rozdziały równolegle z kodem)

- [ ] **Rozdz. 5** ML basics: MLE, bias/wariancja, pojemność modelu
- [ ] **Rozdz. 6** Deep Feedforward Networks: backprop jako graf obliczeń (z Ep 1 i 5)
- [ ] **Rozdz. 7** Regularization · **rozdz. 8** Optimization for Training (SGD, momentum, Adam, inicjalizacja)
- [ ] **Rozdz. 9** CNN (z #3, #4) · **rozdz. 10** Sequence Modeling (z #1, #2, #5)
- [ ] **Rozdz. 11** Practical Methodology - razem z „A Recipe for Training NNs”

#### Źródła dodatkowe

- [deeplearningbook.org](https://www.deeplearningbook.org/)

---

## Faza 2 - Transformer głębiej + CV + RL + magisterka (fundamenty)

> Fast.ai Part 2 (ResNet, Stable Diffusion, VAE) idzie dalej. Dochodzi RL: pendulum z frameworku to pierwsze środowisko, a REINFORCE z baseline jest rdzeniem metod z magisterki. Literatura o optymalizacji kombinatorycznej w kolejności: Pointer Networks → Attention Model → GNN.

### 🎬 fast.ai Part 2: Foundations → Stable Diffusion

- [x] **Lesson 9**: Deep learning foundations, matrix mult od zera
- [x] **Lesson 10**: Implementacja ResNet od zera w PyTorch
- [ ] **Lesson 11**: Forward/backward pass głębiej, mixed precision
- [ ] **Lesson 12**: DDPM - denoising diffusion probabilistic model
- [ ] **Lesson 13**: Stable Diffusion: U-Net, noise schedule, CFG
- [ ] **Lesson 14**: CLIP, text conditioning, latent diffusion
- [ ] **Lesson 15**: VAE - latent space, reparametrization trick

#### Źródła dodatkowe

- [course.fast.ai/part2](https://course.fast.ai/Lessons/part2.html)

### 🔨 RL - od REINFORCE do PPO (pendulum jako środowisko)

- [ ] **Podstawy**: MDP, return, value vs policy - Sutton & Barto rozdz. 1-6 · [książka](http://incompleteideas.net/book/the-book-2nd.html)
- [ ] **Policy gradient**: twierdzenie o gradiencie polityki, REINFORCE - S&B rozdz. 13
- [ ] **Baseline i wariancja**: advantage, GAE - Schulman 2015 (High-Dimensional Continuous Control Using GAE)
- [ ] **Actor-critic → PPO**: clipping - Schulman 2017 (Proximal Policy Optimization Algorithms)
- [ ] Własny REINFORCE i PPO w czystym PyTorch; akcje ciągłe (rozkład Gaussa, log-prob)
- [ ] Test w frameworku: te same interfejsy, Model podmieniany (REINFORCE ↔ PPO) na pendulum

#### Źródła dodatkowe

- [OpenAI Spinning Up](https://spinningup.openai.com/) - Part 1-3 + Key Papers

### 📄 Computer Vision i głęboka architektura (#9-#12, #18)

- [ ] **#9 Deep Residual Learning** - He et al. 2015 (ResNet) · W5 T2 - czytaj razem z Lesson 10
- [ ] **#10 Identity Mappings in Deep Residual Networks** - He et al. 2016 · W4 T3
- [ ] **#11 Multi-Scale Context Aggregation by Dilated Convolutions** - Yu & Koltun · W3 T3
- [ ] **#12 A Simple NN Module for Relational Reasoning** - Santoro et al. 2017 · W3 T3
- [ ] **#18 Variational Lossy Autoencoder** - Chen et al. 2016 · W3 T4 - po Lesson 15 (VAE)

### 🎓 Optymalizacja kombinatoryczna (TSP/VRP) - kolejność czytania

- [ ] **Bengio, Lodi, Prouvost 2018** - Machine Learning for Combinatorial Optimization: a Methodological Tour d’Horizon (ramka całej pracy)
- [ ] **#19 Pointer Networks** - Vinyals et al. 2015 · W5 T3 (baseline dla TSP/VRP)
- [ ] **#20 Order Matters: Sequence to Sequence for Sets** - Vinyals et al. 2015 · W3 T3
- [ ] **Bello et al. 2016** - Neural Combinatorial Optimization with Reinforcement Learning (Pointer Net + REINFORCE)
- [ ] **Kool et al. 2019** - Attention, Learn to Solve Routing Problems! (Transformer + greedy rollout baseline)
- [ ] **Kwon et al. 2020** - POMO: Policy Optimization with Multiple Optima
- [ ] GNN od podstaw: Distill - A Gentle Introduction to Graph Neural Networks · PyTorch Geometric
- [ ] **#21 Neural Message Passing for Quantum Chemistry** - Gilmer et al. 2017 (MPNN) · W5 T4 (rama pod GNN)
- [ ] **Khalil et al. 2017** - Learning Combinatorial Optimization Algorithms over Graphs (GNN + RL)
- [ ] **Joshi et al. 2019** - An Efficient Graph Convolutional Network Technique for the TSP
- [ ] Przegląd: algorytmy genetyczne vs. uczone heurystyki na TSP

### 📘 Goodfellow - autoenkodery i generatywne

- [ ] **Rozdz. 14** Autoencoders - przed Lesson 15 (VAE)
- [ ] **Rozdz. 15** Representation Learning - latent space, transfer
- [ ] **Rozdz. 20** Deep Generative Models: VAE, GAN, autoregresyjne (dyfuzji tu nie ma → Lesson 12-13)

---

## Faza 3 - LLMs głębiej + RAG + MCP (projekt: Knowledge MCP)

> mlabonne/llm-course prowadzi od tokenizacji przez fine-tuning (QLoRA mieści się w 16 GB VRAM) po RAG i agentów. Najpierw dokumentacja i kursy MCP, potem jeden projekt: RAG nad własnym kodem i notatkami wystawiony jako serwer MCP. DDIA 2. wyd. (rozdz. 1-5) daje fundament pod indeksy, formaty danych i schematy narzędzi.

### 🎬 mlabonne/llm-course - LLM Scientist + Engineer track

- [ ] **LLM Fundamentals**: math recap, Python ML ecosystem
- [ ] **Architektura**: decoder-only GPT, attention mechanisms, positional encoding
- [ ] **Tokenizacja**: BPE od zera (uzupełnia Karpathy Ep 8)
- [ ] **Pre-training**: scaling laws, data pipeline, causal LM
- [ ] **RLHF**: SFT → reward model → PPO; DPO jako alternatywa
- [ ] **Fine-tuning**: LoRA, QLoRA (4-bit - mieści się w 16 GB VRAM), Unsloth
- [ ] **RAG**: chunking strategie, dense retrieval, reranking, vector DB
- [ ] **Agenty**: ReAct, MCP protocol, LangGraph, smolagents
- [ ] **Quantization**: GPTQ, AWQ, GGUF - deployment na consumer GPU

#### Źródła dodatkowe

- [github.com/mlabonne/llm-course](https://github.com/mlabonne/llm-course)

### 📚 HuggingFace NLP Course

- [ ] **Ch 1**: Pipeline API - klasyfikacja, NER, QA, generacja
- [ ] **Ch 2**: Tokenizer deep dive - BPE, WordPiece, padding, truncation
- [ ] **Ch 3**: Fine-tuning z Trainer API (klasyczny workflow)
- [ ] **Ch 4**: Custom training loop w PyTorch - pełna kontrola
- [ ] **Ch 5**: Datasets library - streaming, mapa, filtrowanie
- [ ] **Ch 6**: Tokenizer trening własny
- [ ] **Ch 7**: Token classification, QA, summarization, translation

#### Źródła dodatkowe

- [huggingface.co/learn/nlp-course](https://huggingface.co/learn/nlp-course)

### 📄 LLM, skalowanie i pamięć (#13-#17)

- [ ] **↻ #7 Attention Is All You Need** - drugie, głębokie czytanie (rozumiesz teraz każdy wzór)
- [ ] **#13 Scaling Laws for Neural Language Models** - Kaplan et al. 2020 · W5 T3 (follow-up spoza listy: Chinchilla, Hoffmann 2022)
- [ ] **#14 GPipe: Easy Scaling with Micro-Batch Pipeline Parallelism** - Huang et al. · W3 T3
- [ ] **#15 Neural Turing Machines** - Graves et al. 2014 · W4 T4
- [ ] **#16 Relational Recurrent Neural Networks** - Santoro et al. 2018 · W3 T4 (po #15)
- [ ] **#17 Deep Speech 2** - Baidu, end-to-end ASR · W3 T3

### 🔌 Model Context Protocol - zanim zaczniesz budować

- [ ] **Specyfikacja 2026-07-28** (aktualna rewizja, zastąpiła 2025-11-25): [spec](https://modelcontextprotocol.io/specification/2026-07-28) · [changelog](https://modelcontextprotocol.io/specification/2026-07-28/changelog)
- [ ] **Co się zmieniło**: protokół bezstanowy (brak initialize i Mcp-Session-Id, wersja i capabilities w _meta), Multi Round-Trip Requests zamiast żądań serwer→klient, extensions (Tasks jako rozszerzenie), HTTP+SSE deprecated · [blog](https://blog.modelcontextprotocol.io/posts/2026-07-28/)
- [ ] **Prymitywy**: tools (woła model) vs resources (kontekst ładowany przez aplikację) vs prompts (szablony) - kiedy co
- [ ] **Kurs Anthropic: Introduction to MCP** (Skilljar, darmowy) [link](https://anthropic.skilljar.com/introduction-to-model-context-protocol) → potem **Advanced Topics** [link](https://anthropic.skilljar.com/model-context-protocol-advanced-topics)
- [ ] **Hugging Face MCP Course** (z Anthropic; Unit 3 wymaga Claude Code) [link](https://huggingface.co/learn/mcp-course)
- [ ] **DeepLearning.AI**: MCP - Build Rich-Context AI Apps with Anthropic [link](https://learn.deeplearning.ai/courses/mcp-build-rich-context-ai-apps-with-anthropic/lesson/fkbhh/introduction)

> ⚠️ Część materiałów powstała przed 2026-07-28 i używa klasy FastMCP (SDK v1); w Python SDK v2 to MCPServer - przypnij wersję SDK i opieraj się na [repo SDK](https://github.com/modelcontextprotocol/python-sdk)

- [ ] **Bezpieczeństwo**: [OWASP MCP Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/MCP_Security_Cheat_Sheet.html) + security best practices ze specyfikacji - tool poisoning, prompt injection przez wyniki narzędzi, SSRF, confused deputy, zbyt szerokie tokeny
- [ ] **Autoryzacja**: OAuth 2.1 + PKCE, serwer HTTP jako resource server (w specyfikacji opcjonalna)
- [ ] **Istniejące serwery**: [oficjalny rejestr](https://modelcontextprotocol.io/registry) - przeczytaj kod 2-3 serwerów, zanim zaprojektujesz własny

### 📘 DDIA, 2. wydanie (Kleppmann, Riccomini) - Część I

- [ ] **Rozdz. 1-2** Trade-offs w architekturze, wymagania niefunkcjonalne (latency, percentyle, niezawodność) - przed fazą 4
- [ ] **Rozdz. 3** Data Models and Query Languages - relacyjny vs dokumentowy vs graf (wiąże się z SQL)
- [ ] **Rozdz. 4** Storage and Retrieval - LSM-tree vs B-tree, indeksy (w tym wektorowe, HNSW) - razem z vector store w Knowledge MCP
- [ ] **Rozdz. 5** Encoding and Evolution - JSON Schema, Protobuf, Avro, kompatybilność schematów - razem ze schematami narzędzi MCP

### 🔨 Knowledge MCP - RAG + MCP nad własnym kodem i notatkami

**Źródła**: repozytoria z kodem (Python/C++/Go) + vault Obsidian; lokalnie, read-only

- [ ] **Chunking**: kod po funkcjach/klasach (tree-sitter), notatki po nagłówkach; metadane: ścieżka, wikilinki, tagi
- [ ] **Indeksowanie przyrostowe**: hash plików + watchdog, reindeksacja tylko zmian
- [ ] **Vector store**: FAISS lub ChromaDB (HNSW); embeddingi lokalnie - sentence-transformers na GPU
- [ ] **Retrieval**: dense + BM25 hybrid (SQLite FTS5), fuzja RRF
- [ ] **Reranking**: cross-encoder jako drugi etap
- [ ] **Odpowiedzi z cytowaniem**: plik:linia; brak źródła = brak odpowiedzi (hallucination guard)
- [ ] **Ewaluacja**: własny zestaw ~30 pytań z własnych notatek, recall@k, MRR; RAGAS (faithfulness, context precision/recall)
- [ ] **Narzędzia MCP**: search_notes, search_code, get_file, list_sources (read-only) + reindex (zmienia stan); resources: notatki; 1-2 prompty
- [ ] **Opisy i schematy**: nazwy, opisy i JSON Schema narzędzi pisane dla modelu - one decydują o jakości wywołań
- [ ] **SDK**: Python SDK v2 (MCPServer), przypięta wersja; najpierw stdio lokalnie
- [ ] **Transport**: Streamable HTTP w trybie bezstanowym (2026-07-28), gdy będzie potrzebny
- [ ] **Długie zadania**: reindex zwraca run_id, status przez polling (opcjonalnie rozszerzenie Tasks)
- [ ] **Testy**: [MCP Inspector](https://github.com/modelcontextprotocol/inspector) + pytest + prawdziwy klient (Claude Desktop / Claude Code)
- [ ] **Bezpieczeństwo**: allowlista ścieżek, least privilege, treść notatek jako dane (test notatki z wrogimi instrukcjami)
- [ ] **Logi**: audit log wywołań (narzędzie, argumenty, czas, correlation id)
- [ ] **Opcjonalnie**: zdalny endpoint - Dockerfile + OAuth 2.1 + PKCE
- [ ] **README** po angielsku: architektura, narzędzia, model zagrożeń, wyniki ewaluacji, demo

---

## Faza 4 - MLOps + SQL + Cloud + Math Whiteboard

> Faza, która odróżnia kogoś, kto trenuje modele, od kogoś, kto pracuje produkcyjnie: MLflow, FastAPI, Docker, CI/CD, podstawy cloud i orkiestracja są w większości ofert. Math Whiteboard łączy wizję (fast.ai), modele sekwencyjne i serwowanie. DDIA Część II-III daje język do system designu.

### ⚙️ Production ML pipeline

- [ ] **MLflow**: experiment tracking, model registry, artifact logging
- [ ] **FastAPI**: ML serving endpoint - predict route, health check, schema
- [ ] **Docker**: Dockerfile dla ML projektu, konteneryzacja środowiska
- [ ] **GitHub Actions**: CI/CD pipeline - test + build + deploy on push
- [ ] **Model monitoring**: Evidently AI - data drift, model drift detection
- [ ] **Cloud**: AWS SageMaker lub GCP Vertex AI (free tier - jeden deployment)
- [ ] **HPO**: Optuna (TPE sampler) - przyda się też w magisterce
- [ ] **DVC**: wersjonowanie danych i modeli (obok Git, git-lfs)
- [ ] **ONNX / ONNX Runtime**: eksport z PyTorch, inferencja bez PyTorcha, kwantyzacja INT8
- [ ] **Orkiestracja**: Airflow lub Prefect - DAG-i treningu i batch inference
- [ ] **Kubernetes** (podstawy): Pod, Deployment, Service - wystarczy czytać manifesty
- [ ] **Spark / Databricks**: PySpark DataFrame API - częsty wymóg w ofertach, poziom orientacji
- [ ] **Jakość kodu**: pytest, Pydantic, pre-commit + ruff

#### Źródła dodatkowe

- [Full Stack Deep Learning (FSDL) - darmowe](https://fullstackdeeplearning.com/)

### 📖 SQL i data fundamentals

- [ ] **Window functions**: RANK(), ROW_NUMBER(), LAG/LEAD, partitioning
- [ ] **GROUP BY + HAVING**: aggregacje, filtrowanie po agregacji
- [ ] **Subqueries + CTEs**: WITH clause, correlated subqueries
- [ ] 30 zadań SQL na LeetCode lub Mode SQL Tutorial (free)
- [ ] **Parquet vs CSV**: kiedy columnar storage ma znaczenie i dlaczego
- [ ] **Data leakage**: najczęstszy błąd w ML - jak go wykryć i unikać
- [ ] **Feature engineering**: normalizacja, imputacja, encoding kategorii

### 📘 DDIA, 2. wydanie - Część II i III

- [ ] **Rozdz. 6-7** Replikacja i sharding
- [ ] **Rozdz. 8** Transactions - ACID, poziomy izolacji (razem z SQL)
- [ ] **Rozdz. 9-10** Awarie, spójność, konsensus - materiał pod system design ML
- [ ] **Rozdz. 11-12** Batch i stream processing - pipeline’y danych, feature store, Spark/Flink

### 🔨 Math Whiteboard - własne Miro z rozpoznawaniem pisma

**Zakres**: nieskończone płótno, pióro, obiekty (kształty, strzałki, tekst), undo/redo; rozpoznane pismo → podmiana na symbol lub literę (Unicode/LaTeX)

- [ ] **Etap 1 - klasyfikator symboli**: CNN (ResNet z Part 2); baseline MNIST/EMNIST → HASYv2; augmentacja; macierz pomyłek (1/l/I, ∑/Σ)
- [ ] **Etap 2 - segmentacja pociągnięć**: które kreski tworzą jeden symbol („=”, „i”); grupowanie po czasie i odległości
- [ ] **Etap 3 - model na torach pióra** (x, y, t, pen-up): Graves 2013 (Generating Sequences with RNNs), Ha & Eck 2017 (Sketch-RNN); CTC z #17 Deep Speech 2
- [ ] **Etap 4 - próg pewności**: podmieniaj tylko przy wysokim confidence; kalibracja - Guo 2017 (On Calibration of Modern Neural Networks)
- [ ] **Etap 5 (opcjonalnie) - struktura wyrażeń**: ułamki, indeksy, pierwiastki - Deng 2016 (im2latex)
- [ ] **Serwowanie**: ONNX + onnxruntime-web w przeglądarce lub FastAPI + WebSocket
- [ ] **Współpraca na żywo** (opcjonalnie): CRDT - Yjs; DDIA Część II o local-first
- [ ] **Ewaluacja**: accuracy top-1/top-3 + własne próbki pisane Twoją ręką; runy w MLflow
- [ ] **README** po angielsku: demo GIF, wyniki, ograniczenia

#### Źródła dodatkowe

- **Dane**: [HASYv2](https://arxiv.org/abs/1701.08380) (Thoma 2017, ~370 klas symboli), CROHME (online, tory pióra), MathWriting (Google 2024, online)
- **Referencja**: kod open-source tldraw / Excalidraw - model obiektów i historii

### 📖 MLOps i LLMOps - kluczowe artykuły

- [ ] Compound AI systems - Matei Zaharia (Databricks blog)
- [ ] Prompt Engineering as Software Engineering - Lilian Weng
- [ ] Cost as a First-Class Concern - token caching, model routing
- [ ] LLM hallucination mitigation: RAG + CoT + guardrails - przegląd
- [ ] [LLM Powered Autonomous Agents - Lilian Weng](https://lilianweng.github.io/posts/2023-06-23-agent/)

---

## Faza 5 - Magisterka (eksperymenty i pisanie) + Interview prep

### 🔨 Magisterka - eksperymenty i pisanie

**Zakres**: TSP → CVRP; rozmiary instancji i podział trening/test

- [ ] **Benchmarki**: TSPLIB, CVRPLIB (Uchoa et al. 2017, zbiór X) - instancje z literatury, wyniki porównywalne
- [ ] **Baseliny klasyczne**: 2-opt, LKH-3, OR-Tools, Concorde (optimum TSP); algorytm genetyczny (DEAP lub pygad)
- [ ] **Modele uczone**: Pointer Net → Attention Model (Kool) → POMO, trening REINFORCE z baseline; GNN (PyTorch Geometric) jako wariant
- [ ] **Metryki**: optimality gap, czas inferencji, generalizacja na większe n; ten sam budżet obliczeń dla wszystkich metod
- [ ] **Rzetelność wyników**: wiele seedów, przedziały ufności, test Wilcoxona; Optuna dla HPO
- [ ] **Powtarzalność**: ModelConfig/TrainConfig, results.csv, MLflow, przypięte wersje
- [ ] **Pisanie**: LaTeX + Zotero/BibTeX, wykresy z results.csv, notatki Feynmana z papierów jako szkic rozdziału literaturowego

### 🎯 datainterview.com + systematyczna nauka

- [ ] **ML fundamentals**: bias-variance, overfitting, regularyzacja L1/L2, cross-validation
- [ ] **Metryki**: F1 vs AUC vs Precision@k - kiedy co i dlaczego
- [ ] **Optymalizacja**: SGD, Adam, learning rate schedules, gradient clipping
- [ ] **System design ML**: feature store, serving, monitoring, A/B testing modeli
- [ ] **LLM pytania**: RAG, hallucynacje, context window, fine-tuning vs. prompting
- [ ] **SQL**: window functions, GROUP BY/HAVING, subquery - musi śmigać z głowy
- [ ] **Kodowanie**: Python - data structures, complexity, clean code

#### Źródła dodatkowe

- [datainterview.com](https://datainterview.com)
- [Top ML Interview Questions - DataCamp](https://www.datacamp.com/blog/top-machine-learning-interview-questions)

---

## Zawsze - Tło teoretyczne i śledzenie pola

### 📄 Teoria informacji i złożoność (#22-#27)

- [ ] **#22 The First Law of Complexodynamics** - Aaronson (blog) · W2 T2
- [ ] **#23 Machine Super Intelligence** - Shane Legg, praca doktorska 2008 (długa; wybrane rozdziały) · W2 T3
- [ ] **#24 Quantifying the Rise and Fall of Complexity in Closed Systems: The Coffee Automaton** - Aaronson et al. · W2 T4 (po #22)
- [ ] **#25 A Tutorial Introduction to the MDL Principle** - Grünwald · W3 T4
- [ ] **#26 Keeping Neural Networks Simple by Minimizing the Description Length of the Weights** - Hinton & van Camp 1993 · W3 T5 (wróć po #25; zdjęte z Fazy 1)
- [ ] **#27 Kolmogorov Complexity and Algorithmic Randomness** - Shen, Uspensky, Vereshchagin (książka; wybrane rozdziały) · W3 T5

### 📡 Źródła - na bieżąco

- [Papers With Code - SOTA tracker](https://paperswithcode.com/)
- [Lilian Weng blog - najlepsza seria w sieci](https://lilianweng.github.io/)
- [Jay Alammar blog - wizualne wyjaśnienia](https://jalammar.github.io/)
- Andrej Karpathy na X / GitHub - nowe projekty
- [HuggingFace Blog - nowe modele i techniki](https://huggingface.co/blog)
- [Arxiv Sanity Lite - filtrowanie papierów](https://arxiv-sanity-lite.com/)

# Famous Repos Tour

### 유명 오픈소스 저장소 탐험 실습
### A Hands-on Tour of Famous Open Source Repositories
### 著名开源代码仓库实践之旅

*OSS Application and Development · Kyungpook National University*

---

## 목차 / Table of Contents / 目录

1. [들어가며 / Introduction / 引言](#1-들어가며--introduction--引言)
2. [왜 유명 저장소를 clone 해야 하는가 / Why clone famous repositories / 为什么要亲手克隆著名仓库](#2-왜-유명-저장소를-clone-해야-하는가)
3. [유명 저장소 카탈로그 / The Famous Repos Catalog / 著名仓库目录](#3-유명-저장소-카탈로그)
   - 3.1 [운영체제 · 커널 / Operating Systems & Kernels](#31-운영체제--커널)
   - 3.2 [프로그래밍 언어 / Programming Languages](#32-프로그래밍-언어)
   - 3.3 [웹 프레임워크 · 라이브러리 / Web Frameworks](#33-웹-프레임워크--라이브러리)
   - 3.4 [에디터 · 개발도구 / Editors & Dev Tools](#34-에디터--개발도구)
   - 3.5 [AI · 머신러닝 / AI & ML](#35-ai--머신러닝)
   - 3.6 [데이터베이스 · 백엔드 / Databases & Backend](#36-데이터베이스--백엔드)
   - 3.7 [학습 · 문화 · awesome / Learning & Culture](#37-학습--문화--awesome)
   - 3.8 [한국 관련 OSS / Korea-related OSS](#38-한국-관련-oss)
   - 3.9 [게임 · 게임 엔진 / Games & Game Engines](#39-게임--게임-엔진)
   - 3.10 [보안 · 침투 테스트 · 암호학 / Security](#310-보안--침투-테스트--암호학)
   - 3.11 [모바일 / Mobile](#311-모바일)
   - 3.12 [임베디드 · IoT / Embedded & IoT](#312-임베디드--iot)
   - 3.13 [블록체인 / Blockchain](#313-블록체인)
   - 3.14 [음악 · 오디오 / Music & Audio](#314-음악--오디오)
4. [GitHub에서 주요 저장소 찾는 법 / How to Discover Important Repos](#4-github에서-주요-저장소-찾는-법)
5. [실습 / Hands-on Lab / 实践环节](#5-실습--hands-on-lab--实践环节)
6. [실습용 명령어 모음 / Cheat Sheet / 实用命令汇总](#6-실습용-명령어-모음--cheat-sheet--实用命令汇总)
7. [마무리 / Closing / 结语](#7-마무리--closing--结语)

---

## 1. 들어가며 / Introduction / 引言

### 학습 목표 / Learning Objectives / 学习目标

> **🇰🇷 KO:** git clone 한 번으로 세계적인 오픈소스 프로젝트의 코드와 역사를 내 컴퓨터로 가져올 수 있다는 사실을 직접 체험합니다. 단순한 다운로드가 아니라 '전 세계 개발자 공동체에 접속하는 행위'라는 점을 느껴봅니다.
>
> **🇬🇧 EN:** Experience firsthand that a single `git clone` command brings the full source code and history of world-class open source projects to your laptop. This is not just a download — it is the act of plugging into a global community of developers.
>
> **🇨🇳 ZH:** 通过一条 git clone 命令，亲身体验将世界级开源项目的完整源代码和历史下载到自己的电脑上。这不仅仅是下载，而是接入全球开发者社区的过程。

### 준비물 / Prerequisites / 准备事项

- Git installed (`git --version` 로 확인 / verify with `git --version` / 用 `git --version` 验证)
- GitHub 계정 / GitHub account / GitHub 账号
- 터미널 (또는 Git Bash) / Terminal (or Git Bash) / 终端（或 Git Bash）
- 약 5 GB 여유 디스크 공간 / About 5 GB free disk space / 约 5 GB 可用磁盘空间

---

## 2. 왜 유명 저장소를 clone 해야 하는가?
### Why clone famous repositories? / 为什么要亲手克隆著名仓库？

> **🇰🇷 KO:** 코드는 '읽는 것'과 '내 컴퓨터에 두는 것' 사이에 큰 차이가 있습니다. 웹에서 코드를 구경하는 것은 박물관에서 유리벽 너머의 유물을 보는 것과 같고, clone 은 그 유물을 직접 손에 쥐어보는 경험입니다. 검색하고, 수정해보고, 빌드해보고, 역사를 거슬러 올라갈 수 있습니다.
>
> **🇬🇧 EN:** There is a big difference between *reading* code and *having* it on your machine. Browsing on the web is like viewing an artifact through museum glass; cloning is holding it in your hands. You can search it, modify it, build it, and travel back through its history.
>
> **🇨🇳 ZH:** '阅读代码'与'把代码放在自己电脑上'之间存在巨大差异。在网页上浏览就像隔着博物馆玻璃看文物，而克隆则是亲手把文物拿在手里——你可以搜索、修改、构建，并沿着历史溯流而上。

### clone 의 묘미 5가지 / Five Joys of `git clone` / git clone 的五大乐趣

**1.**

> **🇰🇷 KO:** 역사 여행: 첫 커밋부터 오늘까지의 모든 변경 이력이 손 안에 들어옵니다.
>
> **🇬🇧 EN:** Time Travel: Every change from the first commit to today is in your hands.
>
> **🇨🇳 ZH:** 历史穿越：从第一次提交到今天的所有变更都在你手中。

**2.**

> **🇰🇷 KO:** 전설과의 만남: Linus Torvalds, Guido van Rossum 같은 인물의 실제 커밋을 볼 수 있습니다.
>
> **🇬🇧 EN:** Meet the Legends: See real commits by Linus Torvalds, Guido van Rossum, and others.
>
> **🇨🇳 ZH:** 与传奇相遇：可以看到 Linus Torvalds、Guido van Rossum 等人的真实提交。

**3.**

> **🇰🇷 KO:** 협업의 규모 체감: `shortlog` 로 수천 명의 기여자 명단을 한눈에 볼 수 있습니다.
>
> **🇬🇧 EN:** Feel the Scale: A single `shortlog` reveals thousands of contributors at once.
>
> **🇨🇳 ZH:** 感受协作规模：一条 shortlog 命令就能展现成千上万的贡献者名单。

**4.**

> **🇰🇷 KO:** 내부 구조 탐험: 평소 쓰던 도구의 폴더 구조와 설계 의도를 들여다볼 수 있습니다.
>
> **🇬🇧 EN:** Explore the Internals: Peek into the folder structure and design intent of tools you use daily.
>
> **🇨🇳 ZH:** 探索内部结构：可以窥见日常使用工具的文件夹结构与设计思路。

**5.**

> **🇰🇷 KO:** 기여의 시작점: README, CONTRIBUTING, good first issue 를 읽으며 첫 PR 의 길을 닦을 수 있습니다.
>
> **🇬🇧 EN:** The Path to Contribution: Reading README, CONTRIBUTING, and `good first issue` paves the way to your first PR.
>
> **🇨🇳 ZH:** 贡献的起点：阅读 README、CONTRIBUTING 与 good first issue，为第一次 PR 铺路。

---

## 3. 유명 저장소 카탈로그
### The Famous Repos Catalog / 著名仓库目录

> **🇰🇷 KO:** 아래 표는 카테고리별로 정리한 대표적인 오픈소스 저장소들입니다. 모두 `git clone` 으로 직접 가져올 수 있습니다.
>
> **🇬🇧 EN:** The tables below list landmark open source repositories by category. All can be obtained with a simple `git clone`.
>
> **🇨🇳 ZH:** 以下表格按类别整理了具有代表性的开源仓库。所有仓库都可以通过 git clone 直接获取。

### 3.1 운영체제 · 커널
#### Operating Systems & Kernels / 操作系统与内核

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **torvalds/linux** | **KO:** 리눅스 커널 본체. Linus Torvalds가 직접 관리.<br>**EN:** The Linux kernel itself, maintained by Linus Torvalds.<br>**ZH:** Linux 内核本体，由 Linus Torvalds 亲自维护。 | `https://github.com/torvalds/linux` | *수십만 커밋, 만 명 이상의 기여자. 컴퓨팅 역사 그 자체.* |
| **git/git** | **KO:** Git 자체의 소스코드. Git을 Git으로 clone하는 메타 경험.<br>**EN:** Source code of Git itself — clone Git with Git.<br>**ZH:** Git 自身的源代码——用 Git 克隆 Git 的元体验。 | `https://github.com/git/git` | *Linus가 BitKeeper 떠난 직후 2005년 초기 커밋을 직접 볼 수 있음.* |
| **freebsd/freebsd-src** | **KO:** FreeBSD 운영체제 소스코드.<br>**EN:** FreeBSD operating system source.<br>**ZH:** FreeBSD 操作系统源代码。 | `https://github.com/freebsd/freebsd-src` | *BSD 계열의 살아있는 역사.* |
| **openbsd/src** | **KO:** OpenBSD — 보안과 코드 정결성으로 유명.<br>**EN:** OpenBSD — famous for security and code cleanliness.<br>**ZH:** OpenBSD——以安全性和代码整洁度著称。 | `https://github.com/openbsd/src` | *Theo de Raadt의 엄격한 코드 문화 체험.* |

### 3.2 프로그래밍 언어
#### Programming Languages / 编程语言

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **python/cpython** | **KO:** 우리가 매일 쓰는 Python의 C 구현체.<br>**EN:** The reference C implementation of Python.<br>**ZH:** 我们每天使用的 Python 的 C 参考实现。 | `https://github.com/python/cpython` | *Guido van Rossum의 30년 자취가 그대로.* |
| **rust-lang/rust** | **KO:** Rust 컴파일러와 표준 라이브러리.<br>**EN:** The Rust compiler and standard library.<br>**ZH:** Rust 编译器与标准库。 | `https://github.com/rust-lang/rust` | *현대 시스템 언어의 설계가 어떻게 자라는지 볼 수 있음.* |
| **golang/go** | **KO:** Go 언어 본체 — Google이 시작했지만 진정한 OSS.<br>**EN:** The Go language — started at Google, truly OSS.<br>**ZH:** Go 语言本体——由 Google 启动的真正开源项目。 | `https://github.com/golang/go` | *Rob Pike, Ken Thompson 같은 거장의 커밋이 등장.* |
| **nodejs/node** | **KO:** Node.js 런타임 — JavaScript를 서버로 보낸 프로젝트.<br>**EN:** The Node.js runtime — the project that took JavaScript to the server.<br>**ZH:** Node.js 运行时——将 JavaScript 带到服务器端的项目。 | `https://github.com/nodejs/node` | *오픈 거버넌스와 포크(io.js) 합병의 흥미로운 역사.* |
| **openjdk/jdk** | **KO:** OpenJDK — Java의 공식 오픈소스 구현.<br>**EN:** OpenJDK — the official open source Java implementation.<br>**ZH:** OpenJDK——Java 的官方开源实现。 | `https://github.com/openjdk/jdk` | *엔터프라이즈 언어가 OSS가 되는 과정의 모범.* |
| **ruby/ruby** | **KO:** Ruby 언어 — Matz의 철학이 담긴 언어.<br>**EN:** The Ruby language — built around Matz's philosophy.<br>**ZH:** Ruby 语言——蕴含 Matz 哲学的语言。 | `https://github.com/ruby/ruby` | *'프로그래머의 행복'을 우선시한 설계 철학.* |
| **JuliaLang/julia** | **KO:** Julia — 과학 컴퓨팅을 위한 고성능 언어.<br>**EN:** Julia — a high-performance language for scientific computing.<br>**ZH:** Julia——面向科学计算的高性能语言。 | `https://github.com/JuliaLang/julia` | *비교적 신생 언어가 어떻게 커뮤니티를 형성하는지 관찰 가능.* |
| **JetBrains/kotlin** | **KO:** Kotlin — Android의 공식 언어.<br>**EN:** Kotlin — the official language for Android.<br>**ZH:** Kotlin——Android 的官方语言。 | `https://github.com/JetBrains/kotlin` | *기업 주도 OSS의 좋은 예.* |

### 3.3 웹 프레임워크 · 라이브러리
#### Web Frameworks & Libraries / Web 框架与库

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **facebook/react** | **KO:** React — UI 라이브러리의 표준.<br>**EN:** React — the de facto UI library.<br>**ZH:** React——UI 库的事实标准。 | `https://github.com/facebook/react` | *거대 기업이 만든 OSS가 어떻게 커뮤니티로 흘러가는지.* |
| **vuejs/vue** | **KO:** Vue.js — Evan You가 1인으로 시작한 프레임워크.<br>**EN:** Vue.js — a framework started solo by Evan You.<br>**ZH:** Vue.js——由 Evan You 个人发起的框架。 | `https://github.com/vuejs/vue` | *한 사람이 시작한 OSS도 세계적 영향력을 가질 수 있음.* |
| **angular/angular** | **KO:** Angular — TypeScript 기반 풀 프레임워크.<br>**EN:** Angular — a full TypeScript-based framework.<br>**ZH:** Angular——基于 TypeScript 的完整框架。 | `https://github.com/angular/angular` | *Google이 운영하는 대규모 협업의 본보기.* |
| **sveltejs/svelte** | **KO:** Svelte — 컴파일 시점 최적화로 주목받은 신예.<br>**EN:** Svelte — a rising star with compile-time optimization.<br>**ZH:** Svelte——以编译期优化备受关注的新星。 | `https://github.com/sveltejs/svelte` | *기존 패러다임에 도전하는 신선한 설계.* |
| **django/django** | **KO:** Django — Python 풀스택 웹 프레임워크.<br>**EN:** Django — the Python full-stack web framework.<br>**ZH:** Django——Python 全栈 Web 框架。 | `https://github.com/django/django` | *'마감을 지키려는 완벽주의자를 위한 프레임워크'.* |
| **rails/rails** | **KO:** Ruby on Rails — convention over configuration의 원조.<br>**EN:** Ruby on Rails — origin of 'convention over configuration'.<br>**ZH:** Ruby on Rails——'约定优于配置'理念的发源地。 | `https://github.com/rails/rails` | *스타트업 생태계의 한 시대를 만든 프레임워크.* |
| **expressjs/express** | **KO:** Express.js — Node.js 미니멀 웹 프레임워크.<br>**EN:** Express.js — the minimal Node.js web framework.<br>**ZH:** Express.js——Node.js 极简 Web 框架。 | `https://github.com/expressjs/express` | *단순함의 미학.* |
| **tailwindlabs/tailwindcss** | **KO:** Tailwind CSS — utility-first 디자인 혁명.<br>**EN:** Tailwind CSS — the utility-first design revolution.<br>**ZH:** Tailwind CSS——utility-first 设计革命。 | `https://github.com/tailwindlabs/tailwindcss` | *OSS가 산업의 디자인 관습을 바꾼 사례.* |
| **twbs/bootstrap** | **KO:** Bootstrap — 가장 별이 많은 프론트엔드 프레임워크.<br>**EN:** Bootstrap — one of the most starred front-end frameworks.<br>**ZH:** Bootstrap——星标最多的前端框架之一。 | `https://github.com/twbs/bootstrap` | *Twitter 내부에서 OSS로 분리된 역사.* |

### 3.4 에디터 · 개발도구
#### Editors & Dev Tools / 编辑器与开发工具

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **microsoft/vscode** | **KO:** Visual Studio Code — 세계에서 가장 많이 쓰는 에디터.<br>**EN:** Visual Studio Code — the world's most-used editor.<br>**ZH:** Visual Studio Code——全球使用率最高的编辑器。 | `https://github.com/microsoft/vscode` | *Microsoft가 OSS로 돌아선 상징적 프로젝트.* |
| **neovim/neovim** | **KO:** Neovim — Vim의 현대적 재탄생.<br>**EN:** Neovim — the modern reincarnation of Vim.<br>**ZH:** Neovim——Vim 的现代化重生。 | `https://github.com/neovim/neovim` | *포크가 본가를 자극해 함께 발전한 사례.* |
| **vim/vim** | **KO:** Vim — Bram Moolenaar의 일생을 담은 에디터.<br>**EN:** Vim — an editor that carried Bram Moolenaar's lifework.<br>**ZH:** Vim——承载 Bram Moolenaar 毕生心血的编辑器。 | `https://github.com/vim/vim` | *한 사람의 헌신이 만든 도구의 무게.* |
| **emacs-mirror/emacs** | **KO:** GNU Emacs — Richard Stallman이 시작한 전설.<br>**EN:** GNU Emacs — the legend started by Richard Stallman.<br>**ZH:** GNU Emacs——由 Richard Stallman 开启的传奇。 | `https://github.com/emacs-mirror/emacs` | *자유 소프트웨어 운동의 살아있는 화석.* |
| **docker/cli** | **KO:** Docker CLI — 컨테이너 시대의 시작.<br>**EN:** Docker CLI — the beginning of the container era.<br>**ZH:** Docker CLI——容器时代的开端。 | `https://github.com/docker/cli` | *DevOps 문화 자체를 바꾼 도구.* |
| **kubernetes/kubernetes** | **KO:** Kubernetes — 클라우드 인프라의 사실상 표준.<br>**EN:** Kubernetes — the de facto cloud orchestration standard.<br>**ZH:** Kubernetes——云基础设施的事实标准。 | `https://github.com/kubernetes/kubernetes` | *Google에서 출발해 CNCF 산하 OSS로 성공한 모범.* |
| **git-for-windows/git** | **KO:** Git for Windows — Windows 환경의 Git 배포판.<br>**EN:** Git for Windows — the Windows distribution of Git.<br>**ZH:** Git for Windows——Windows 环境下的 Git 发行版。 | `https://github.com/git-for-windows/git` | *포팅(porting) OSS가 무엇인지 보여줌.* |

### 3.5 AI · 머신러닝
#### AI & Machine Learning / 人工智能与机器学习

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **tensorflow/tensorflow** | **KO:** TensorFlow — Google의 딥러닝 프레임워크.<br>**EN:** TensorFlow — Google's deep learning framework.<br>**ZH:** TensorFlow——Google 的深度学习框架。 | `https://github.com/tensorflow/tensorflow` | *거대 기업 주도 ML OSS의 대표주자.* |
| **pytorch/pytorch** | **KO:** PyTorch — 연구계가 사랑하는 딥러닝 프레임워크.<br>**EN:** PyTorch — beloved by the research community.<br>**ZH:** PyTorch——研究界钟爱的深度学习框架。 | `https://github.com/pytorch/pytorch` | *현재 AI 연구의 거의 모든 논문이 이 위에 있음.* |
| **huggingface/transformers** | **KO:** 🤗 Transformers — 사전학습 모델의 허브.<br>**EN:** 🤗 Transformers — the hub of pretrained models.<br>**ZH:** 🤗 Transformers——预训练模型的中心枢纽。 | `https://github.com/huggingface/transformers` | *LLM 시대의 가장 중요한 라이브러리 중 하나.* |
| **scikit-learn/scikit-learn** | **KO:** scikit-learn — 전통 ML의 교과서 같은 라이브러리.<br>**EN:** scikit-learn — the textbook library of classical ML.<br>**ZH:** scikit-learn——经典机器学习的教科书式库。 | `https://github.com/scikit-learn/scikit-learn` | *학술 OSS의 모범 답안.* |
| **numpy/numpy** | **KO:** NumPy — 파이썬 수치 컴퓨팅의 뿌리.<br>**EN:** NumPy — the root of Python numerical computing.<br>**ZH:** NumPy——Python 数值计算的根基。 | `https://github.com/numpy/numpy` | *거의 모든 데이터과학 도구의 의존 대상.* |
| **pandas-dev/pandas** | **KO:** pandas — 데이터프레임의 사실상 표준.<br>**EN:** pandas — the de facto DataFrame library.<br>**ZH:** pandas——数据框的事实标准。 | `https://github.com/pandas-dev/pandas` | *Wes McKinney의 금융업 출신 배경이 흥미.* |
| **ggerganov/llama.cpp** | **KO:** llama.cpp — 로컬에서 LLM 돌리는 혁명.<br>**EN:** llama.cpp — the revolution of running LLMs locally.<br>**ZH:** llama.cpp——本地运行 LLM 的革命。 | `https://github.com/ggerganov/llama.cpp` | *한 사람이 시작해 폭발적으로 성장한 최신 OSS.* |
| **ollama/ollama** | **KO:** Ollama — 로컬 LLM을 쉽게 다루는 도구.<br>**EN:** Ollama — easy local LLM management.<br>**ZH:** Ollama——简化本地 LLM 管理的工具。 | `https://github.com/ollama/ollama` | *2024년 이후 가장 빠르게 자라는 OSS 중 하나.* |

### 3.6 데이터베이스 · 백엔드
#### Databases & Backend / 数据库与后端

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **postgres/postgres** | **KO:** PostgreSQL — '세계에서 가장 진보된 오픈소스 DB'.<br>**EN:** PostgreSQL — 'the world's most advanced open source database'.<br>**ZH:** PostgreSQL——'世界上最先进的开源数据库'。 | `https://github.com/postgres/postgres` | *1986년부터 이어진 학술 OSS의 정수.* |
| **sqlite/sqlite** | **KO:** SQLite — 지구상에서 가장 많이 배포된 SW.<br>**EN:** SQLite — the most widely deployed software on Earth.<br>**ZH:** SQLite——地球上部署最广泛的软件。 | `https://github.com/sqlite/sqlite` | *퍼블릭 도메인이면서 항공우주 등급 테스트.* |
| **redis/redis** | **KO:** Redis — 인메모리 데이터 스토어.<br>**EN:** Redis — the in-memory data store.<br>**ZH:** Redis——内存数据存储。 | `https://github.com/redis/redis` | *라이선스 변경으로 본 OSS 거버넌스 이슈.* |
| **mongodb/mongo** | **KO:** MongoDB — NoSQL 시대를 연 DB.<br>**EN:** MongoDB — the database that opened the NoSQL era.<br>**ZH:** MongoDB——开启 NoSQL 时代的数据库。 | `https://github.com/mongodb/mongo` | *기업형 OSS 사업모델의 실험장.* |
| **elastic/elasticsearch** | **KO:** Elasticsearch — 검색·분석 엔진.<br>**EN:** Elasticsearch — search and analytics engine.<br>**ZH:** Elasticsearch——搜索与分析引擎。 | `https://github.com/elastic/elasticsearch` | *오픈소스 라이선스 논쟁의 대표 사례.* |
| **nginx/nginx** | **KO:** NGINX — 가장 많이 쓰이는 웹 서버 중 하나.<br>**EN:** NGINX — one of the most-used web servers.<br>**ZH:** NGINX——使用最广泛的 Web 服务器之一。 | `https://github.com/nginx/nginx` | *C로 작성된 견고한 서버 코드의 본보기.* |

### 3.7 학습 · 문화 · awesome
#### Learning, Culture, Awesome Lists / 学习、文化、Awesome 资源

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **sindresorhus/awesome** | **KO:** 모든 awesome 리스트의 시작점. 별 30만 개 이상.<br>**EN:** The starting point of all `awesome` lists. 300k+ stars.<br>**ZH:** 所有 awesome 列表的起点，星标超过 30 万。 | `https://github.com/sindresorhus/awesome` | *코드 한 줄 없이도 OSS의 힘을 보여줌.* |
| **EbookFoundation/free-programming-books** | **KO:** 전 세계 무료 프로그래밍 책 모음.<br>**EN:** A collection of free programming books worldwide.<br>**ZH:** 全球免费编程书籍合集。 | `https://github.com/EbookFoundation/free-programming-books` | *여러 언어 버전이 있어 한국어/중국어 자료도 풍부.* |
| **kamranahmedse/developer-roadmap** | **KO:** 개발자 학습 로드맵 — 가장 별이 많은 저장소 중 하나.<br>**EN:** Developer learning roadmaps — among the most-starred repos.<br>**ZH:** 开发者学习路线图——星标最多的仓库之一。 | `https://github.com/kamranahmedse/developer-roadmap` | *공부 방향 잡기 좋고, OSS 시각화 사례.* |
| **donnemartin/system-design-primer** | **KO:** 시스템 설계 입문 — 면접 준비의 정석.<br>**EN:** System design primer — a classic interview prep resource.<br>**ZH:** 系统设计入门——面试准备的经典资源。 | `https://github.com/donnemartin/system-design-primer` | *코드보다 문서 중심 OSS의 좋은 예.* |
| **TheAlgorithms/Python** | **KO:** 모든 알고리즘을 Python으로 — 학습용 OSS의 정수.<br>**EN:** Every algorithm in Python — quintessential learning OSS.<br>**ZH:** 所有算法的 Python 实现——学习型开源项目的典范。 | `https://github.com/TheAlgorithms/Python` | *C++/Java/Go 등 자매 저장소도 존재.* |
| **ossu/computer-science** | **KO:** 독학으로 CS 학위 수준을 따라가는 커리큘럼.<br>**EN:** A self-taught curriculum equivalent to a CS degree.<br>**ZH:** 可自学达到计算机科学学位水平的课程体系。 | `https://github.com/ossu/computer-science` | *OSS가 교육 자체가 될 수 있음을 보여줌.* |
| **trekhleb/javascript-algorithms** | **KO:** JS로 구현한 알고리즘 + 설명.<br>**EN:** Algorithms in JS with explanations.<br>**ZH:** 用 JS 实现的算法及详细解释。 | `https://github.com/trekhleb/javascript-algorithms` | *다국어 번역 협업이 활발해 기여 입문에 좋음.* |
| **github/gitignore** | **KO:** 언어별 .gitignore 모음 — GitHub 공식.<br>**EN:** Language-specific .gitignore templates — official GitHub.<br>**ZH:** 按语言分类的 .gitignore 模板——GitHub 官方。 | `https://github.com/github/gitignore` | *한 줄짜리 PR로 첫 기여 도전해보기 좋음.* |
| **torvalds/test-tlb** | **KO:** Linus가 만든 작은 실험 저장소들 중 하나.<br>**EN:** One of Linus's small experimental repos.<br>**ZH:** Linus 的小型实验仓库之一。 | `https://github.com/torvalds/test-tlb` | *거장도 작은 토이 프로젝트를 만든다는 사실.* |

### 3.8 한국 관련 OSS
#### Korea-related OSS / 韩国相关开源项目

> **🇰🇷 KO:** 한국 개발자와 기업이 시작하거나 주도하는 OSS도 점점 늘고 있습니다. 학생들에게는 '우리도 만들 수 있다'는 친근감을 주는 카테고리입니다.
>
> **🇬🇧 EN:** OSS led by Korean developers and companies is steadily growing. This category gives students the friendly message: 'We can build this too.'
>
> **🇨🇳 ZH:** 由韩国开发者和企业主导的开源项目正在不断增长。这个分类向学生传递亲切的信息：'我们也能创造这样的项目'。

#### 기업 OSS / Corporate OSS / 企业开源

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **naver/naver** | **KO:** 네이버의 공개 OSS 조직 페이지.<br>**EN:** Naver's public OSS organization.<br>**ZH:** Naver 的公开开源组织。 | `https://github.com/naver` | *한국 기업이 만든 OSS 생태계 탐험의 출발점.* |
| **naver/billboard.js** | **KO:** D3 기반 차트 라이브러리. 네이버에서 시작.<br>**EN:** A D3-based charting library, originated at Naver.<br>**ZH:** 基于 D3 的图表库，由 Naver 发起。 | `https://github.com/naver/billboard.js` | *한국에서 시작한 본격 글로벌 OSS.* |
| **naver/pinpoint** | **KO:** Pinpoint — 대규모 분산 시스템용 APM. 네이버 주도.<br>**EN:** Pinpoint — APM for large-scale distributed systems, led by Naver.<br>**ZH:** Pinpoint——面向大规模分布式系统的 APM，由 Naver 主导。 | `https://github.com/pinpoint-apm/pinpoint` | *한국 출신 글로벌 인프라 OSS의 대표주자.* |
| **naver/arcus** | **KO:** Arcus — memcached 기반 분산 캐시 클러스터.<br>**EN:** Arcus — distributed memcached-based cache cluster.<br>**ZH:** Arcus——基于 memcached 的分布式缓存集群。 | `https://github.com/naver/arcus` | *한국에서 만든 본격 인프라 OSS.* |
| **kakao/khaiii** | **KO:** 카카오 한국어 형태소 분석기.<br>**EN:** Kakao's Korean morphological analyzer.<br>**ZH:** Kakao 的韩语形态分析器。 | `https://github.com/kakao/khaiii` | *한국어 NLP에 관심 있는 학생에게 추천.* |
| **kakao/varlog** | **KO:** Varlog — 카카오의 분산 로그 스토리지.<br>**EN:** Varlog — Kakao's distributed log storage.<br>**ZH:** Varlog——Kakao 的分布式日志存储。 | `https://github.com/kakao/varlog` | *국내 빅테크의 인프라 수준을 볼 수 있음.* |
| **line/armeria** | **KO:** Armeria — LINE이 주도하는 비동기 마이크로서비스 프레임워크.<br>**EN:** Armeria — an async microservice framework led by LINE.<br>**ZH:** Armeria——由 LINE 主导的异步微服务框架。 | `https://github.com/line/armeria` | *한일 협력 OSS 중 가장 활발한 프로젝트.* |
| **line/line-bot-sdk-python** | **KO:** LINE 공식 봇 SDK.<br>**EN:** Official LINE bot SDK.<br>**ZH:** LINE 官方 Bot SDK。 | `https://github.com/line/line-bot-sdk-python` | *메신저 봇 개발 입문에 좋음.* |
| **Samsung/escargot** | **KO:** Escargot — 삼성이 만든 경량 JavaScript 엔진.<br>**EN:** Escargot — a lightweight JavaScript engine by Samsung.<br>**ZH:** Escargot——三星开发的轻量级 JavaScript 引擎。 | `https://github.com/Samsung/escargot` | *임베디드용 JS 엔진. Tizen OS와 연계.* |
| **Samsung/TizenRT** | **KO:** TizenRT — 삼성의 임베디드/IoT용 실시간 OS.<br>**EN:** TizenRT — Samsung's RTOS for embedded/IoT.<br>**ZH:** TizenRT——三星面向嵌入式/IoT 的实时操作系统。 | `https://github.com/Samsung/TizenRT` | *한국 대기업이 직접 운영하는 OS 프로젝트.* |
| **coupang/charlotte** | **KO:** Charlotte — 쿠팡의 컨테이너 보안 엔진.<br>**EN:** Charlotte — Coupang's container security engine.<br>**ZH:** Charlotte——Coupang 的容器安全引擎。 | `https://github.com/coupang/charlotte` | *한국 이커머스 기업의 보안 OSS 공헌.* |
| **woowabros** | **KO:** 우아한형제들(배민) OSS 조직.<br>**EN:** Woowa Brothers (Baemin) OSS organization.<br>**ZH:** Woowa Brothers（外卖民族）开源组织。 | `https://github.com/woowabros` | *한국 IT 기업의 엔지니어링 문화 엿보기.* |
| **toss/slash** | **KO:** Slash — 토스가 공개한 프론트엔드 유틸리티 모음.<br>**EN:** Slash — frontend utilities open-sourced by Toss.<br>**ZH:** Slash——Toss 开源的前端工具库。 | `https://github.com/toss/slash` | *한국 핀테크 스타트업의 모범 OSS.* |
| **toss/es-hangul** | **KO:** es-hangul — 한글 처리(초성 검색, 조사 등) JS 라이브러리.<br>**EN:** es-hangul — JS library for Korean text (chosung search, particles).<br>**ZH:** es-hangul——韩文处理（首音搜索、助词等）JS 库。 | `https://github.com/toss/es-hangul` | *한국어 특화 OSS의 좋은 예. 한국인만이 만들 수 있는.* |

#### 한국어 · 한국 문화 OSS / Korean Language & Culture OSS / 韩语与韩国文化开源

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **konlpy/konlpy** | **KO:** KoNLPy — 파이썬 한국어 NLP 라이브러리의 표준.<br>**EN:** KoNLPy — the standard Python Korean NLP library.<br>**ZH:** KoNLPy——Python 韩语 NLP 标准库。 | `https://github.com/konlpy/konlpy` | *학술 OSS가 산업 표준이 된 한국어 NLP의 모범.* |
| **bab2min/kiwipiepy** | **KO:** Kiwi — 빠른 한국어 형태소 분석기의 파이썬 바인딩.<br>**EN:** Kiwi — Python binding for a fast Korean morphological analyzer.<br>**ZH:** Kiwi——快速韩语形态分析器的 Python 绑定。 | `https://github.com/bab2min/kiwipiepy` | *1인 개발자가 만든 글로벌 수준 한국어 NLP 도구.* |
| **SKTBrain/KoBERT** | **KO:** KoBERT — SK텔레콤이 공개한 한국어 BERT 모델.<br>**EN:** KoBERT — Korean BERT model open-sourced by SK Telecom.<br>**ZH:** KoBERT——SK 电讯开源的韩语 BERT 模型。 | `https://github.com/SKTBrain/KoBERT` | *한국 대기업이 만든 사전학습 언어모델 OSS.* |
| **Beomi/KoAlpaca** | **KO:** KoAlpaca — 한국어 LLM 파인튜닝의 시발점.<br>**EN:** KoAlpaca — a starting point for Korean LLM fine-tuning.<br>**ZH:** KoAlpaca——韩语 LLM 微调的起点。 | `https://github.com/Beomi/KoAlpaca` | *개인 연구자가 시작해 한국어 LLM 붐을 일으킨 프로젝트.* |
| **naver/nlp-challenge** | **KO:** 네이버 NLP 챌린지 — 한국어 NER 데이터셋.<br>**EN:** Naver NLP Challenge — Korean NER dataset.<br>**ZH:** Naver NLP 挑战赛——韩语命名实体识别数据集。 | `https://github.com/naver/nlp-challenge` | *공개 한국어 데이터셋의 좋은 예.* |

#### 한국 개발자 학습 자료 / Korean Developer Learning Materials / 韩国开发者学习资料

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **free-programming-books (KO)** | **KO:** free-programming-books 의 한국어 자료 섹션.<br>**EN:** Korean section of free-programming-books.<br>**ZH:** free-programming-books 中的韩文资料部分。 | `https://github.com/EbookFoundation/free-programming-books/blob/main/books/free-programming-books-ko.md` | *한국어 무료 책 한자리에. PR로 책 추가 기여 가능.* |

### 3.9 게임 · 게임 엔진
#### Games & Game Engines / 游戏与游戏引擎

> **🇰🇷 KO:** 게임은 OSS의 가장 매력적인 분야 중 하나입니다. 그래픽, 물리, 네트워크, AI가 한곳에 모이는 종합 예술이거든요.
>
> **🇬🇧 EN:** Games are among the most charming corners of OSS — graphics, physics, networking, and AI all converging into one art form.
>
> **🇨🇳 ZH:** 游戏是开源世界中最具魅力的领域之一——图形、物理、网络、AI 在此汇聚成一门综合艺术。

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **godotengine/godot** | **KO:** Godot — 가장 인기 있는 오픈소스 게임 엔진.<br>**EN:** Godot — the most popular open source game engine.<br>**ZH:** Godot——最流行的开源游戏引擎。 | `https://github.com/godotengine/godot` | *Unity 라이선스 분쟁 이후 폭발적 성장. 진정한 풀-OSS 엔진.* |
| **MonoGame/MonoGame** | **KO:** MonoGame — XNA의 정신을 잇는 C# 게임 프레임워크.<br>**EN:** MonoGame — the C# framework carrying XNA's legacy.<br>**ZH:** MonoGame——传承 XNA 精神的 C# 游戏框架。 | `https://github.com/MonoGame/MonoGame` | *Stardew Valley, Celeste 등 인디 명작들이 사용.* |
| **libgdx/libgdx** | **KO:** libGDX — 자바 기반의 크로스플랫폼 게임 프레임워크.<br>**EN:** libGDX — a Java-based cross-platform game framework.<br>**ZH:** libGDX——基于 Java 的跨平台游戏框架。 | `https://github.com/libgdx/libgdx` | *데스크톱·모바일·웹을 한 코드베이스로.* |
| **OpenRA/OpenRA** | **KO:** OpenRA — 고전 RTS(Command & Conquer)의 오픈소스 재현.<br>**EN:** OpenRA — open source remake of classic RTS (Command & Conquer).<br>**ZH:** OpenRA——经典 RTS（命令与征服）的开源复刻。 | `https://github.com/OpenRA/OpenRA` | *고전 게임을 OSS로 살려내는 문화의 대표 사례.* |
| **OpenTTD/OpenTTD** | **KO:** OpenTTD — Transport Tycoon Deluxe의 오픈소스 후예.<br>**EN:** OpenTTD — open source successor to Transport Tycoon Deluxe.<br>**ZH:** OpenTTD——Transport Tycoon Deluxe 的开源后继者。 | `https://github.com/OpenTTD/OpenTTD` | *20년 넘게 유지되는 OSS 게임 프로젝트의 모범.* |
| **ValveSoftware/source-sdk-2013** | **KO:** Valve의 Source 엔진 SDK 2013 버전 공개 소스.<br>**EN:** Valve's Source engine SDK 2013, public source.<br>**ZH:** Valve 公开的 Source 引擎 SDK 2013 版。 | `https://github.com/ValveSoftware/source-sdk-2013` | *상용 엔진의 일부가 OSS로 공개된 흥미로운 사례.* |
| **id-Software/DOOM** | **KO:** DOOM (1993)의 원본 소스코드. John Carmack의 전설.<br>**EN:** Original source of DOOM (1993) — John Carmack's legend.<br>**ZH:** DOOM (1993) 原始源代码——John Carmack 的传奇。 | `https://github.com/id-Software/DOOM` | *게임 역사 그 자체. 90년대 C 코드를 직접 볼 수 있음.* |
| **id-Software/Quake** | **KO:** Quake (1996) 원본 소스 — 3D 엔진의 시조.<br>**EN:** Original Quake (1996) source — patriarch of 3D engines.<br>**ZH:** Quake (1996) 原始源代码——3D 引擎的鼻祖。 | `https://github.com/id-Software/Quake` | *유명한 'fast inverse square root' 트릭이 여기에 있음.* |
| **minetest/minetest** | **KO:** Minetest — Minecraft 영감의 완전 OSS 보클셀 게임.<br>**EN:** Minetest — fully OSS voxel game inspired by Minecraft.<br>**ZH:** Minetest——受 Minecraft 启发的完全开源体素游戏。 | `https://github.com/minetest/minetest` | *상용 게임 OSS 대안 운동의 대표주자.* |
| **FreeCAD/FreeCAD** | **KO:** (보너스) FreeCAD — 게임은 아니지만 3D 모델링/리깅 학습에 유용.<br>**EN:** (Bonus) FreeCAD — not a game, but useful for learning 3D modeling.<br>**ZH:** （额外推荐）FreeCAD——非游戏，但有助于学习 3D 建模。 | `https://github.com/FreeCAD/FreeCAD` | *게임 에셋 제작 파이프라인 입문용.* |
| **pygame/pygame** | **KO:** pygame — 파이썬 2D 게임 프로그래밍의 입문서.<br>**EN:** pygame — the gateway to 2D game programming in Python.<br>**ZH:** pygame——Python 2D 游戏编程的入门首选。 | `https://github.com/pygame/pygame` | *수업 실습 과제로 가장 친근한 게임 라이브러리.* |
| **love2d/love** | **KO:** LÖVE — Lua 기반 2D 게임 엔진. 학습 곡선이 매우 부드러움.<br>**EN:** LÖVE — Lua-based 2D game engine with a gentle learning curve.<br>**ZH:** LÖVE——基于 Lua 的 2D 游戏引擎，学习曲线非常平缓。 | `https://github.com/love2d/love` | *한 학기 동안 작은 게임 만들기 좋음.* |
| **phaserjs/phaser** | **KO:** Phaser — JavaScript/HTML5 2D 게임 프레임워크.<br>**EN:** Phaser — JavaScript/HTML5 2D game framework.<br>**ZH:** Phaser——JavaScript/HTML5 2D 游戏框架。 | `https://github.com/phaserjs/phaser` | *웹 게임으로 바로 배포 가능 — 학생 포트폴리오에 좋음.* |

### 3.10 보안 · 침투 테스트 · 암호학
#### Security, Pentesting, Cryptography / 安全、渗透测试与密码学

> ⚠️ **주의 / Note / 注意**
>
> **KO:** 보안 도구는 강력합니다. 반드시 자신이 소유한 시스템이나 명시적 허가를 받은 환경에서만 사용해야 하며, 무단 침투는 법적 처벌 대상입니다. 이 분야의 OSS는 '방어를 잘하려면 공격을 이해해야 한다'는 철학에서 출발합니다.
>
> **EN:** Security tools are powerful. Only use them on systems you own or have explicit authorization to test — unauthorized intrusion is illegal. OSS in this field stems from the philosophy that strong defense requires understanding offense.
>
> **ZH:** 安全工具威力强大。务必只在你拥有或获得明确授权的系统上使用——未经授权的入侵属违法行为。该领域的开源项目源于"要做好防御，先理解攻击"的理念。

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **nmap/nmap** | **KO:** Nmap — 네트워크 스캐닝의 표준 도구.<br>**EN:** Nmap — the de facto network scanning tool.<br>**ZH:** Nmap——网络扫描的事实标准工具。 | `https://github.com/nmap/nmap` | *영화 'Matrix Reloaded'에 등장한 그 도구. 25년 넘은 OSS.* |
| **wireshark/wireshark** | **KO:** Wireshark — 패킷 분석기의 최강자.<br>**EN:** Wireshark — the dominant packet analyzer.<br>**ZH:** Wireshark——最强大的数据包分析器。 | `https://github.com/wireshark/wireshark` | *네트워크를 '보이게' 만드는 도구. 교육 가치 최상.* |
| **rapid7/metasploit-framework** | **KO:** Metasploit — 침투 테스트 프레임워크의 양대 산맥.<br>**EN:** Metasploit — one of the two pillars of pentesting frameworks.<br>**ZH:** Metasploit——渗透测试框架的两大支柱之一。 | `https://github.com/rapid7/metasploit-framework` | *Ruby로 작성된 거대 보안 OSS의 모범.* |
| **OWASP/CheatSheetSeries** | **KO:** OWASP 보안 치트시트 모음 — 웹 보안의 바이블.<br>**EN:** OWASP security cheat sheets — bible of web security.<br>**ZH:** OWASP 安全速查表合集——Web 安全圣经。 | `https://github.com/OWASP/CheatSheetSeries` | *코드 없이 문서만으로 세상을 바꾼 OSS.* |
| **OWASP/Top10** | **KO:** OWASP Top 10 — 매년 갱신되는 웹 취약점 TOP 10.<br>**EN:** OWASP Top 10 — yearly-updated top web vulnerabilities.<br>**ZH:** OWASP Top 10——每年更新的 Web 漏洞十大威胁。 | `https://github.com/OWASP/Top10` | *전 세계 보안 표준의 출발점.* |
| **openssl/openssl** | **KO:** OpenSSL — 인터넷 암호 통신의 토대.<br>**EN:** OpenSSL — the foundation of internet cryptography.<br>**ZH:** OpenSSL——互联网加密通信的基石。 | `https://github.com/openssl/openssl` | *2014년 Heartbleed 사건의 무대. 보안 거버넌스 사례.* |
| **letsencrypt/boulder** | **KO:** Let's Encrypt의 ACME 서버 구현체.<br>**EN:** Let's Encrypt's ACME server implementation.<br>**ZH:** Let's Encrypt 的 ACME 服务器实现。 | `https://github.com/letsencrypt/boulder` | *OSS가 무료 HTTPS 시대를 연 결정적 프로젝트.* |
| **google/tink** | **KO:** Google Tink — 안전한 암호 API.<br>**EN:** Google Tink — a safe cryptographic API.<br>**ZH:** Google Tink——安全的加密 API。 | `https://github.com/google/tink` | *암호학을 '잘못 쓰기 어렵게' 만드는 설계.* |
| **trailofbits/algo** | **KO:** Algo VPN — 한 번 클릭으로 VPN 서버 구축.<br>**EN:** Algo VPN — one-click VPN server deployment.<br>**ZH:** Algo VPN——一键部署 VPN 服务器。 | `https://github.com/trailofbits/algo` | *프라이버시 OSS의 좋은 본보기.* |
| **sqlmapproject/sqlmap** | **KO:** sqlmap — SQL 인젝션 자동 탐지 도구 (교육·연구 목적).<br>**EN:** sqlmap — automated SQL injection detection (educational use).<br>**ZH:** sqlmap——SQL 注入自动检测工具（教学研究用途）。 | `https://github.com/sqlmapproject/sqlmap` | *공격 도구가 어떻게 방어 의식을 키우는지 보여줌.* |
| **swisskyrepo/PayloadsAllTheThings** | **KO:** 보안 페이로드 모음 — CTF·버그바운티 단골 자료.<br>**EN:** A trove of security payloads — staple for CTF and bug bounty.<br>**ZH:** 安全 Payload 集合——CTF 与漏洞赏金常用资料。 | `https://github.com/swisskyrepo/PayloadsAllTheThings` | *문서·자료형 OSS의 강력함.* |
| **veracrypt/VeraCrypt** | **KO:** VeraCrypt — 디스크 암호화 OSS (TrueCrypt 후예).<br>**EN:** VeraCrypt — disk encryption OSS, successor to TrueCrypt.<br>**ZH:** VeraCrypt——磁盘加密开源软件，TrueCrypt 的继承者。 | `https://github.com/veracrypt/VeraCrypt` | *원조 프로젝트가 사라진 뒤 커뮤니티가 살려낸 사례.* |
| **signalapp/Signal-Android** | **KO:** Signal 메신저 안드로이드 클라이언트.<br>**EN:** Signal messenger Android client.<br>**ZH:** Signal 信使的 Android 客户端。 | `https://github.com/signalapp/Signal-Android` | *엔드투엔드 암호화의 실전 OSS 구현.* |
| **snyk/cli** | **KO:** Snyk CLI — 의존성 취약점 스캐너.<br>**EN:** Snyk CLI — dependency vulnerability scanner.<br>**ZH:** Snyk CLI——依赖项漏洞扫描器。 | `https://github.com/snyk/cli` | *현대 DevSecOps의 필수 도구.* |
| **aquasecurity/trivy** | **KO:** Trivy — 컨테이너·코드 취약점 통합 스캐너.<br>**EN:** Trivy — unified scanner for containers and code.<br>**ZH:** Trivy——容器与代码的统一漏洞扫描器。 | `https://github.com/aquasecurity/trivy` | *클라우드 네이티브 보안의 최전선.* |

### 3.11 모바일
#### Mobile / 移动端

> **🇰🇷 KO:** 모바일 OSS는 우리가 매일 손에 쥐는 것들의 내부를 보여줍니다. Android 자체부터 크로스플랫폼 프레임워크까지 다양합니다.
>
> **🇬🇧 EN:** Mobile OSS reveals the inside of devices we hold every day — from Android itself to cross-platform frameworks.
>
> **🇨🇳 ZH:** 移动端开源项目展现了我们每天手握的设备内部——从 Android 本身到跨平台框架。

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **aosp-mirror/platform_frameworks_base** | **KO:** Android Open Source Project — Android 프레임워크 본체.<br>**EN:** Android Open Source Project — the Android framework.<br>**ZH:** Android Open Source Project——Android 框架本体。 | `https://github.com/aosp-mirror/platform_frameworks_base` | *스마트폰 시대를 연 OS의 코드를 직접 볼 수 있음.* |
| **flutter/flutter** | **KO:** Flutter — Google의 크로스플랫폼 UI 프레임워크.<br>**EN:** Flutter — Google's cross-platform UI framework.<br>**ZH:** Flutter——Google 的跨平台 UI 框架。 | `https://github.com/flutter/flutter` | *Dart 언어와 함께 자라난 신예 OSS의 모범.* |
| **facebook/react-native** | **KO:** React Native — JS로 네이티브 모바일 앱 만들기.<br>**EN:** React Native — build native mobile apps with JS.<br>**ZH:** React Native——用 JS 构建原生移动应用。 | `https://github.com/facebook/react-native` | *한 코드베이스로 iOS·Android를 동시에.* |
| **ionic-team/ionic-framework** | **KO:** Ionic — 웹 기술로 하이브리드 앱 제작.<br>**EN:** Ionic — build hybrid apps with web tech.<br>**ZH:** Ionic——用 Web 技术构建混合应用。 | `https://github.com/ionic-team/ionic-framework` | *웹 개발자가 모바일로 넘어가는 다리.* |
| **expo/expo** | **KO:** Expo — React Native 개발을 매우 쉽게 만들어주는 도구.<br>**EN:** Expo — makes React Native development much easier.<br>**ZH:** Expo——让 React Native 开发变得极为简单。 | `https://github.com/expo/expo` | *OSS 위에 OSS를 쌓아 생태계가 커지는 사례.* |
| **JetBrains/compose-multiplatform** | **KO:** Compose Multiplatform — Kotlin으로 모든 플랫폼 UI.<br>**EN:** Compose Multiplatform — Kotlin UI for every platform.<br>**ZH:** Compose Multiplatform——用 Kotlin 构建全平台 UI。 | `https://github.com/JetBrains/compose-multiplatform` | *Android Jetpack Compose가 데스크톱·iOS로 확장.* |
| **swiftlang/swift** | **KO:** Swift — Apple의 모바일 언어, 이제 완전 OSS.<br>**EN:** Swift — Apple's mobile language, now fully OSS.<br>**ZH:** Swift——Apple 的移动开发语言，现已完全开源。 | `https://github.com/swiftlang/swift` | *거대 폐쇄형 기업이 OSS로 전환한 의미 있는 사례.* |
| **signalapp/Signal-iOS** | **KO:** Signal iOS 클라이언트 — 모바일 보안 메신저의 표준.<br>**EN:** Signal iOS client — the standard secure mobile messenger.<br>**ZH:** Signal iOS 客户端——安全移动通讯的标杆。 | `https://github.com/signalapp/Signal-iOS` | *엔드투엔드 암호화 메신저의 실전 코드.* |
| **termux/termux-app** | **KO:** Termux — 안드로이드 위의 리눅스 터미널.<br>**EN:** Termux — a Linux terminal on Android.<br>**ZH:** Termux——Android 上的 Linux 终端。 | `https://github.com/termux/termux-app` | *스마트폰만으로 개발 환경을 구축하는 OSS.* |
| **LineageOS/android** | **KO:** LineageOS — 커뮤니티 주도 Android 커스텀 ROM.<br>**EN:** LineageOS — community-driven custom Android ROM.<br>**ZH:** LineageOS——社区主导的 Android 自定义 ROM。 | `https://github.com/LineageOS` | *단종된 스마트폰을 살려내는 OSS 정신.* |

### 3.12 임베디드 · IoT
#### Embedded & IoT / 嵌入式与物联网

> **🇰🇷 KO:** 임베디드는 OSS가 가장 깊이 있게 사용되는 분야 중 하나입니다. 자동차, 가전, 산업장비 안에는 거의 모두 OSS가 들어 있습니다.
>
> **🇬🇧 EN:** Embedded is one of the deepest territories of OSS. Cars, appliances, and industrial equipment almost all carry OSS inside.
>
> **🇨🇳 ZH:** 嵌入式是开源软件应用最深入的领域之一。汽车、家电、工业设备内部几乎都有开源软件的身影。

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **espressif/esp-idf** | **KO:** ESP-IDF — ESP32 마이크로컨트롤러의 공식 개발 프레임워크.<br>**EN:** ESP-IDF — official dev framework for ESP32 microcontrollers.<br>**ZH:** ESP-IDF——ESP32 微控制器的官方开发框架。 | `https://github.com/espressif/esp-idf` | *수천 원짜리 칩으로 IoT를 시작할 수 있게 만든 OSS.* |
| **arduino/Arduino** | **KO:** Arduino — 가장 친근한 마이크로컨트롤러 플랫폼.<br>**EN:** Arduino — the friendliest microcontroller platform.<br>**ZH:** Arduino——最亲切的微控制器平台。 | `https://github.com/arduino/Arduino` | *교육용 OSS 하드웨어의 대명사.* |
| **raspberrypi/linux** | **KO:** Raspberry Pi 전용 리눅스 커널 분기.<br>**EN:** Linux kernel branch for Raspberry Pi.<br>**ZH:** 针对 Raspberry Pi 的 Linux 内核分支。 | `https://github.com/raspberrypi/linux` | *교육용 SBC와 OSS 커널이 만난 본보기.* |
| **micropython/micropython** | **KO:** MicroPython — 마이크로컨트롤러에서 동작하는 Python.<br>**EN:** MicroPython — Python that runs on microcontrollers.<br>**ZH:** MicroPython——可在微控制器上运行的 Python。 | `https://github.com/micropython/micropython` | *고수준 언어를 임베디드로 가져온 혁신.* |
| **zephyrproject-rtos/zephyr** | **KO:** Zephyr — Linux Foundation의 임베디드 RTOS.<br>**EN:** Zephyr — Linux Foundation's embedded RTOS.<br>**ZH:** Zephyr——Linux 基金会的嵌入式 RTOS。 | `https://github.com/zephyrproject-rtos/zephyr` | *재단 주도 OSS 거버넌스의 좋은 예.* |
| **FreeRTOS/FreeRTOS** | **KO:** FreeRTOS — 가장 널리 쓰이는 임베디드 RTOS.<br>**EN:** FreeRTOS — the most widely used embedded RTOS.<br>**ZH:** FreeRTOS——使用最广泛的嵌入式 RTOS。 | `https://github.com/FreeRTOS/FreeRTOS` | *AWS가 후원하면서 더욱 강력해진 OSS.* |
| **raspberrypi/pico-sdk** | **KO:** Raspberry Pi Pico (RP2040) SDK.<br>**EN:** SDK for Raspberry Pi Pico (RP2040).<br>**ZH:** Raspberry Pi Pico (RP2040) 的 SDK。 | `https://github.com/raspberrypi/pico-sdk` | *5달러 마이크로컨트롤러로 시작하는 임베디드.* |
| **home-assistant/core** | **KO:** Home Assistant — 가정용 IoT 통합 허브.<br>**EN:** Home Assistant — unified home IoT hub.<br>**ZH:** Home Assistant——家庭 IoT 统一中枢。 | `https://github.com/home-assistant/core` | *OSS만으로 스마트홈을 완성할 수 있음을 증명.* |
| **eclipse/mosquitto** | **KO:** Mosquitto — MQTT 프로토콜 표준 구현.<br>**EN:** Mosquitto — reference MQTT broker.<br>**ZH:** Mosquitto——MQTT 协议标准实现。 | `https://github.com/eclipse/mosquitto` | *IoT 메시징의 표준이 어떻게 작동하는지.* |
| **openwrt/openwrt** | **KO:** OpenWrt — 공유기를 위한 OSS 리눅스 배포판.<br>**EN:** OpenWrt — OSS Linux distribution for routers.<br>**ZH:** OpenWrt——面向路由器的开源 Linux 发行版。 | `https://github.com/openwrt/openwrt` | *낡은 공유기에 새 생명을 불어넣는 OSS.* |
| **raspberrypi/firmware** | **KO:** Raspberry Pi 부트로더 · 펌웨어.<br>**EN:** Raspberry Pi bootloader and firmware.<br>**ZH:** Raspberry Pi 引导加载程序与固件。 | `https://github.com/raspberrypi/firmware` | *OS 아래 계층까지 들여다보는 학습 자료.* |

### 3.13 블록체인
#### Blockchain / 区块链

> **🇰🇷 KO:** 블록체인은 거의 모든 핵심 기술이 OSS입니다. 비트코인부터 시작된 '모든 것이 공개되어야 한다'는 정신이 강한 분야입니다.
>
> **🇬🇧 EN:** Blockchain is overwhelmingly OSS — the field carries a strong 'everything must be public' ethos from Bitcoin onward.
>
> **🇨🇳 ZH:** 区块链领域几乎所有核心技术都是开源的——从比特币开始就秉承'一切必须公开'的精神。

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **bitcoin/bitcoin** | **KO:** Bitcoin Core — 비트코인 참조 구현.<br>**EN:** Bitcoin Core — the reference Bitcoin implementation.<br>**ZH:** Bitcoin Core——比特币参考实现。 | `https://github.com/bitcoin/bitcoin` | *Satoshi Nakamoto의 초기 커밋이 그대로. 디지털 금의 원본.* |
| **ethereum/go-ethereum** | **KO:** go-ethereum (geth) — 이더리움의 Go 구현체.<br>**EN:** go-ethereum (geth) — Go implementation of Ethereum.<br>**ZH:** go-ethereum (geth)——以太坊的 Go 实现。 | `https://github.com/ethereum/go-ethereum` | *스마트 컨트랙트 생태계의 본거지.* |
| **ethereum/solidity** | **KO:** Solidity — 이더리움 스마트 컨트랙트 언어 컴파일러.<br>**EN:** Solidity — compiler for Ethereum's smart contract language.<br>**ZH:** Solidity——以太坊智能合约语言编译器。 | `https://github.com/ethereum/solidity` | *새로운 언어가 OSS로 만들어지는 과정 관찰.* |
| **OpenZeppelin/openzeppelin-contracts** | **KO:** OpenZeppelin — 검증된 스마트 컨트랙트 라이브러리.<br>**EN:** OpenZeppelin — battle-tested smart contract library.<br>**ZH:** OpenZeppelin——经实战检验的智能合约库。 | `https://github.com/OpenZeppelin/openzeppelin-contracts` | *보안 표준이 어떻게 OSS로 정립되는지.* |
| **hyperledger/fabric** | **KO:** Hyperledger Fabric — 기업용 블록체인 플랫폼.<br>**EN:** Hyperledger Fabric — enterprise blockchain platform.<br>**ZH:** Hyperledger Fabric——面向企业的区块链平台。 | `https://github.com/hyperledger/fabric` | *재단 거버넌스가 어떻게 OSS를 키우는지.* |
| **solana-labs/solana** | **KO:** Solana — 고속 블록체인의 Rust 구현.<br>**EN:** Solana — high-throughput blockchain in Rust.<br>**ZH:** Solana——高吞吐量区块链的 Rust 实现。 | `https://github.com/solana-labs/solana` | *Rust 기반 대규모 OSS의 좋은 예.* |
| **paritytech/polkadot-sdk** | **KO:** Polkadot SDK — 멀티체인 프레임워크.<br>**EN:** Polkadot SDK — multi-chain framework.<br>**ZH:** Polkadot SDK——多链框架。 | `https://github.com/paritytech/polkadot-sdk` | *Substrate 위에 자라난 거대 OSS 트리.* |
| **foundry-rs/foundry** | **KO:** Foundry — Rust로 만든 이더리움 개발 툴체인.<br>**EN:** Foundry — Rust-based Ethereum toolchain.<br>**ZH:** Foundry——用 Rust 构建的以太坊开发工具链。 | `https://github.com/foundry-rs/foundry` | *현재 가장 빠르게 자라는 스마트 컨트랙트 도구.* |
| **trufflesuite/truffle** | **KO:** Truffle — 클래식 스마트 컨트랙트 개발 환경.<br>**EN:** Truffle — classic smart contract dev environment.<br>**ZH:** Truffle——经典智能合约开发环境。 | `https://github.com/trufflesuite/truffle` | *한 시대의 표준이 어떻게 다른 도구에 자리를 내주는지.* |
| **ipfs/kubo** | **KO:** IPFS (kubo) — 분산 파일 시스템의 구현체.<br>**EN:** IPFS (kubo) — implementation of the InterPlanetary File System.<br>**ZH:** IPFS (kubo)——星际文件系统的实现。 | `https://github.com/ipfs/kubo` | *블록체인 인접 OSS의 대표주자.* |
| **monero-project/monero** | **KO:** Monero — 프라이버시 중심 암호화폐.<br>**EN:** Monero — privacy-focused cryptocurrency.<br>**ZH:** Monero——注重隐私的加密货币。 | `https://github.com/monero-project/monero` | *암호학과 OSS가 만나는 첨예한 지점.* |

### 3.14 음악 · 오디오
#### Music & Audio / 音乐与音频

> **🇰🇷 KO:** 음악과 오디오는 OSS의 또 다른 매력적인 무대입니다. DAW(디지털 오디오 워크스테이션), 신디사이저, 오디오 처리 라이브러리가 모두 OSS로 존재합니다.
>
> **🇬🇧 EN:** Music and audio form another charming OSS stage. DAWs, synthesizers, and audio libraries all live in OSS.
>
> **🇨🇳 ZH:** 音乐与音频是开源软件另一个迷人的舞台。DAW、合成器和音频处理库都以开源形式存在。

| Repository | Description | git clone URL | Why it's a gem |
|---|---|---|---|
| **audacity/audacity** | **KO:** Audacity — 가장 유명한 OSS 오디오 편집기.<br>**EN:** Audacity — the most famous OSS audio editor.<br>**ZH:** Audacity——最著名的开源音频编辑器。 | `https://github.com/audacity/audacity` | *20년 넘게 사용자 수억 명의 음성을 다듬어온 OSS.* |
| **Ardour/ardour** | **KO:** Ardour — 전문가용 OSS DAW (디지털 오디오 워크스테이션).<br>**EN:** Ardour — professional-grade OSS DAW.<br>**ZH:** Ardour——专业级开源数字音频工作站。 | `https://github.com/Ardour/ardour` | *상용 DAW와 견주는 OSS의 자존심.* |
| **LMMS/lmms** | **KO:** LMMS — Linux Multimedia Studio. 음악 제작 DAW.<br>**EN:** LMMS — Linux Multimedia Studio for music production.<br>**ZH:** LMMS——Linux 多媒体工作室，用于音乐制作。 | `https://github.com/LMMS/lmms` | *FL Studio 영감 OSS. 학생들에게 친근함.* |
| **musescore/MuseScore** | **KO:** MuseScore — 악보 작성 소프트웨어의 사실상 표준 OSS.<br>**EN:** MuseScore — de facto OSS music notation software.<br>**ZH:** MuseScore——乐谱编辑软件的开源事实标准。 | `https://github.com/musescore/MuseScore` | *Sibelius·Finale 같은 상용 SW의 OSS 대안.* |
| **supercollider/supercollider** | **KO:** SuperCollider — 실시간 오디오 합성 언어.<br>**EN:** SuperCollider — language for real-time audio synthesis.<br>**ZH:** SuperCollider——实时音频合成语言。 | `https://github.com/supercollider/supercollider` | *라이브 코딩 음악 공연의 대표 도구.* |
| **csound/csound** | **KO:** Csound — 컴퓨터 음악의 고전. 1986년 시작.<br>**EN:** Csound — a classic of computer music, born in 1986.<br>**ZH:** Csound——计算机音乐的经典，始于 1986 年。 | `https://github.com/csound/csound` | *MIT에서 출발한 학술 OSS의 오랜 생명력.* |
| **Tonejs/Tone.js** | **KO:** Tone.js — 웹 브라우저에서 음악 만드는 JS 라이브러리.<br>**EN:** Tone.js — JS library to make music in the browser.<br>**ZH:** Tone.js——在浏览器中制作音乐的 JS 库。 | `https://github.com/Tonejs/Tone.js` | *웹 오디오를 친근하게 만들어주는 OSS.* |
| **magenta/magenta** | **KO:** Magenta — Google의 AI 음악 생성 연구 프로젝트.<br>**EN:** Magenta — Google's AI music generation research project.<br>**ZH:** Magenta——Google 的 AI 音乐生成研究项目。 | `https://github.com/magenta/magenta` | *ML과 음악이 만나는 최전선의 OSS.* |
| **spotify/pedalboard** | **KO:** Pedalboard — Spotify가 공개한 오디오 처리 라이브러리.<br>**EN:** Pedalboard — audio processing library by Spotify.<br>**ZH:** Pedalboard——Spotify 开源的音频处理库。 | `https://github.com/spotify/pedalboard` | *음악 스트리밍 기업의 OSS 공헌.* |
| **librosa/librosa** | **KO:** librosa — Python 음악·오디오 분석 라이브러리.<br>**EN:** librosa — Python library for music and audio analysis.<br>**ZH:** librosa——Python 音乐与音频分析库。 | `https://github.com/librosa/librosa` | *MIR(음악 정보 검색) 연구의 표준 도구.* |
| **mido/mido** | **KO:** mido — Python MIDI 라이브러리.<br>**EN:** mido — Python MIDI library.<br>**ZH:** mido——Python MIDI 库。 | `https://github.com/mido/mido` | *MIDI 데이터 다루기 학습용으로 최적.* |
| **FluidSynth/fluidsynth** | **KO:** FluidSynth — SoundFont 기반 소프트웨어 신디사이저.<br>**EN:** FluidSynth — SoundFont-based software synthesizer.<br>**ZH:** FluidSynth——基于 SoundFont 的软件合成器。 | `https://github.com/FluidSynth/fluidsynth` | *C로 작성된 견고한 오디오 OSS.* |

---

## 4. GitHub에서 주요 저장소 찾는 법
### How to Discover Important Repos / 如何在 GitHub 上发现重要仓库

> **🇰🇷 KO:** GitHub에는 수억 개의 저장소가 있습니다. 그중에서 '의미 있는' 저장소를 찾는 기술은 OSS 개발자의 핵심 역량입니다.
>
> **🇬🇧 EN:** GitHub hosts hundreds of millions of repositories. The skill of finding the *meaningful* ones is core to being an OSS developer.
>
> **🇨🇳 ZH:** GitHub 上有数亿个仓库，从中找出'有价值'的仓库是开源开发者的核心能力。

### 4.1 Trending 페이지 활용 / Using the Trending Page / 利用 Trending 页面

> **🇰🇷 KO:** GitHub Trending은 지금 이 순간 가장 핫한 저장소를 보여줍니다. 매일 한 번씩 확인하는 습관을 들이면 기술 흐름이 자연스럽게 보입니다.
>
> **🇬🇧 EN:** GitHub Trending shows what is hot right now. Checking it daily helps you absorb the rhythm of technology trends.
>
> **🇨🇳 ZH:** GitHub Trending 展示当下最热门的仓库。每天浏览一次，能自然地把握技术潮流。

```
https://github.com/trending
https://github.com/trending/python?since=weekly
https://github.com/trending/javascript?since=monthly
```

### 4.2 고급 검색 문법 / Advanced Search Syntax / 高级搜索语法

> **🇰🇷 KO:** GitHub 검색은 단순한 키워드를 넘어 매우 강력한 필터를 지원합니다. 다음은 자주 쓰는 패턴입니다.
>
> **🇬🇧 EN:** GitHub search goes far beyond keywords. The patterns below are the most useful filters.
>
> **🇨🇳 ZH:** GitHub 搜索远不止关键词，下面是最常用的过滤模式。

| Query | KO | EN | ZH |
|---|---|---|---|
| `stars:>10000 language:python` | 별 1만 개 이상의 Python 저장소 | Python repos with 10k+ stars | 星标超过 1 万的 Python 仓库 |
| `topic:machine-learning stars:>5000` | ML 주제 + 별 5000+ | ML topic + 5k+ stars | ML 主题 + 5000+ 星 |
| `good-first-issue language:javascript` | JS의 입문자용 이슈가 있는 저장소 | JS repos with beginner issues | 带有新手 issue 的 JS 仓库 |
| `created:>2024-01-01 stars:>1000` | 2024년 이후 만들어진 인기 신생 저장소 | Popular new repos born after 2024 | 2024 年后诞生的人气新仓库 |
| `pushed:>2025-01-01 language:rust` | 2025년 이후 활동 중인 Rust 저장소 | Active Rust repos updated since 2025 | 2025 年后仍活跃的 Rust 仓库 |
| `user:torvalds` | 특정 사용자의 저장소만 검색 | Search a specific user's repos | 搜索特定用户的仓库 |
| `org:google language:go` | Google org의 Go 저장소 | Google org's Go repos | Google 组织下的 Go 仓库 |
| `in:readme "hello world"` | README에 특정 문구가 있는 저장소 | Repos with a phrase in README | README 中包含特定短语的仓库 |
| `license:mit stars:>500` | MIT 라이선스 + 별 500+ | MIT license + 500+ stars | MIT 许可证 + 500+ 星 |

### 4.3 Topics, Explore, Stars

- **Topics 페이지** — 주제별 인기 저장소 / Top repos by subject / 按主题查看热门仓库
  ```
  https://github.com/topics/deep-learning
  https://github.com/topics/web-development
  ```
- **Explore** — 추천 알고리즘 기반 발견 / Algorithmic discovery / 基于推荐算法的发现
  ```
  https://github.com/explore
  ```
- **Stars 페이지** — 좋아하는 개발자의 starred 저장소 보기 / Starred repos of a developer you admire / 浏览你喜欢的开发者的星标仓库
  ```
  https://github.com/torvalds?tab=stars
  ```

### 4.4 좋은 저장소 판별 체크리스트
#### Healthy Repo Checklist / 健康仓库判别清单

> **🇰🇷 KO:** 별 개수만으로는 부족합니다. 다음 신호들을 함께 봐야 합니다.
>
> **🇬🇧 EN:** Star count alone is not enough. Check these signals together.
>
> **🇨🇳 ZH:** 仅看星标数量是不够的，应综合考察以下信号。

- [ ] **KO:** 최근 커밋: 6개월 이내 활동이 있는가?
  - **EN:** Recent commits: any activity in the last 6 months?
  - **ZH:** 最近提交：近 6 个月是否有活动？
- [ ] **KO:** 이슈 응답: 최근 이슈에 메인테이너가 답하는가?
  - **EN:** Issue responses: do maintainers reply to recent issues?
  - **ZH:** Issue 回复：维护者是否回复近期 issue？
- [ ] **KO:** PR 머지 빈도: PR이 일주일 안에 검토되는가?
  - **EN:** PR merge cadence: are PRs reviewed within a week?
  - **ZH:** PR 合并节奏：PR 是否在一周内被审查？
- [ ] **KO:** 기여자 수: 한 명에게만 의존하지 않는가?
  - **EN:** Contributor count: not solely dependent on one person?
  - **ZH:** 贡献者人数：是否过度依赖单一开发者？
- [ ] **KO:** 라이선스: LICENSE 파일이 명확히 있는가?
  - **EN:** License: is a clear LICENSE file present?
  - **ZH:** 许可证：是否存在明确的 LICENSE 文件？
- [ ] **KO:** 문서: README 외에 docs/ 폴더나 위키가 있는가?
  - **EN:** Documentation: docs/ folder or wiki beyond README?
  - **ZH:** 文档：除了 README 外是否有 docs/ 文件夹或 Wiki？
- [ ] **KO:** 테스트: tests/ 폴더와 CI 배지가 있는가?
  - **EN:** Tests: a tests/ folder and CI badge?
  - **ZH:** 测试：是否有 tests/ 文件夹和 CI 徽章？
- [ ] **KO:** CONTRIBUTING.md: 기여 가이드가 정비되어 있는가?
  - **EN:** CONTRIBUTING.md: contribution guide in place?
  - **ZH:** CONTRIBUTING.md：贡献指南是否完善？

---

## 5. 실습 / Hands-on Lab / 实践环节

> **🇰🇷 KO:** 아래 5개의 미션을 차례로 수행하고, 각 미션의 결과를 자신의 GitHub 저장소(예: `famous-repos-tour`)에 마크다운으로 기록하세요.
>
> **🇬🇧 EN:** Complete the 5 missions below in order. Record the results in a Markdown file inside your own GitHub repo (e.g. `famous-repos-tour`).
>
> **🇨🇳 ZH:** 依次完成以下 5 个任务，并在自己的 GitHub 仓库（如 famous-repos-tour）中用 Markdown 记录结果。

### Mission 1: 첫 clone — Git을 Git으로 clone하기
#### The First Clone — Cloning Git with Git / 任务 1：第一次克隆——用 Git 克隆 Git

> **🇰🇷 KO:** Git 그 자체를 clone하면서 메타적인 첫 경험을 시작합니다.
>
> **🇬🇧 EN:** Begin with a meta moment: clone Git itself.
>
> **🇨🇳 ZH:** 从元体验开始：克隆 Git 自身。

```bash
mkdir famous-repos-tour && cd famous-repos-tour
git clone https://github.com/git/git.git
cd git
git log --oneline | wc -l                  # 총 커밋 수 확인
git log --reverse --oneline | head -5       # 최초 커밋 5개
```

**기록할 것 / What to record / 需要记录的内容**

1. 총 커밋 수 / Total commit count / 总提交数
2. 최초 커밋의 날짜와 작성자 / Date and author of the very first commit / 第一次提交的日期和作者
3. 최초 커밋 메시지 전문 / The full message of the first commit / 第一次提交的完整信息

### Mission 2: 리눅스 커널 역사 탐험
#### Exploring Linux Kernel History / 任务 2：探索 Linux 内核历史

> **🇰🇷 KO:** 주의: 리눅스 커널은 매우 크므로(약 5GB+) shallow clone을 사용합니다.
>
> **🇬🇧 EN:** Note: the Linux kernel is huge (5GB+) — use a shallow clone.
>
> **🇨🇳 ZH:** 注意：Linux 内核非常庞大（5GB+），请使用浅克隆。

```bash
cd ..   # famous-repos-tour 로 돌아가기
git clone --depth=1 https://github.com/torvalds/linux.git
cd linux
git shortlog -sn | head -10        # 최다 기여자 TOP 10
ls -la                              # 디렉토리 구조 살펴보기
cat MAINTAINERS | head -50          # 거버넌스 문서 일부
```

**기록할 것 / What to record / 需要记录的内容**

1. TOP 10 기여자 이름 / Names of top 10 contributors / 前 10 名贡献者姓名
2. 디렉토리 구조 중 가장 흥미로운 폴더 3개와 그 이유 / 3 most interesting folders and why / 最有趣的 3 个文件夹及原因
3. MAINTAINERS 파일에서 마음에 드는 한 줄 / A favorite line from MAINTAINERS / MAINTAINERS 文件中喜欢的一行

### Mission 3: 자기 분야의 famous repo 선택
#### Pick a Famous Repo in Your Field / 任务 3：选择本领域的著名仓库

> **🇰🇷 KO:** 앞의 카탈로그(3절) 또는 직접 GitHub Trending을 통해 자신의 관심 분야에서 저장소 하나를 선택합니다.
>
> **🇬🇧 EN:** Pick a repository in your area of interest, from the catalog (Section 3) or directly via GitHub Trending.
>
> **🇨🇳 ZH:** 从第 3 节目录或 GitHub Trending 中选择一个你感兴趣领域的仓库。

```bash
git clone <your-chosen-repo-url>
cd <repo-name>
git log --since='1 month ago' --oneline | wc -l
git log --pretty=format:'%h %an %s' | head -20
```

**기록할 것 / What to record / 需要记录的内容**

1. 저장소 이름과 선택한 이유 / Repo name and why you chose it / 仓库名称及选择理由
2. 최근 한 달 활동량 / Activity in the last month / 最近一个月的活动量
3. 4.4절의 건강 체크리스트 8개 항목 평가 / Score against the 8 health signals in §4.4 / 按 4.4 节 8 项健康清单评分

### Mission 4: 한 사람의 발자취 따라가기
#### Following One Person's Trail / 任务 4：追随一个人的足迹

> **🇰🇷 KO:** 앞에서 clone한 저장소에서, 가장 흥미로운 기여자 한 명을 골라 그 사람의 커밋만 들여다봅니다.
>
> **🇬🇧 EN:** In the repo you cloned, pick one contributor and follow only their commits.
>
> **🇨🇳 ZH:** 在你克隆的仓库中，挑选一位贡献者，专门追踪他们的提交。

```bash
git log --author='<name-or-email>' --oneline | head -20
git log --author='<name-or-email>' --stat | head -50
git show <commit-hash>   # 특정 커밋의 diff 보기
```

**기록할 것 / What to record / 需要记录的内容**

1. 선택한 기여자와 그가 만든 커밋 수 / Chosen contributor and their commit count / 所选贡献者及其提交数
2. 가장 인상 깊은 커밋 메시지 하나 / The most striking commit message / 印象最深的一条提交信息
3. 그 사람이 주로 건드린 파일/폴더 / Files or folders they mostly touched / 该贡献者主要修改的文件或文件夹

### Mission 5: 첫 PR 거리 측정
#### Measure Distance to Your First PR / 任务 5：测量你与第一次 PR 的距离

> **🇰🇷 KO:** 선택한 저장소에서 'good first issue' 라벨이 붙은 이슈를 찾아 읽어봅니다. 실제 PR을 보내지 않아도 됩니다 — 어떤 이슈가 자신에게 어울릴지 탐색하는 것이 목표입니다.
>
> **🇬🇧 EN:** In your chosen repository, browse issues labeled `good first issue`. You don't need to actually submit a PR — the goal is to find issues that suit you.
>
> **🇨🇳 ZH:** 在所选仓库中浏览标有 'good first issue' 的 issue。无需真的提交 PR——目标是找到适合你的 issue。

```
# 브라우저에서:
https://github.com/<owner>/<repo>/issues?q=is:open+label:%22good+first+issue%22
```

**기록할 것 / What to record / 需要记录的内容**

1. 자신에게 도전 가능해 보이는 이슈 3개 링크 / 3 issue links you could realistically tackle / 3 个你认为可以挑战的 issue 链接
2. 각 이슈에 필요한 기술 스택 / Tech stack needed for each / 每个 issue 所需的技术栈
3. CONTRIBUTING.md를 읽고 요약(3문장) / Summary of CONTRIBUTING.md in 3 sentences / 用三句话总结 CONTRIBUTING.md

---

## 6. 실습용 명령어 모음 / Cheat Sheet / 实用命令汇总

| Command | KO | EN | ZH |
|---|---|---|---|
| `git clone <url>` | 저장소 전체 clone | Full clone | 完整克隆 |
| `git clone --depth=1 <url>` | Shallow clone (역사 없이 최신만) | Shallow clone (latest only) | 浅克隆（仅最新） |
| `git clone --branch <name> <url>` | 특정 브랜치만 clone | Clone a specific branch | 克隆指定分支 |
| `git log --oneline | wc -l` | 총 커밋 수 | Total commit count | 总提交数 |
| `git log --reverse --oneline | head` | 최초 커밋들 보기 | See earliest commits | 查看最早的提交 |
| `git shortlog -sn` | 기여자별 커밋 수 | Commits per contributor | 按贡献者统计提交数 |
| `git shortlog -sn | head -10` | TOP 10 기여자 | Top 10 contributors | 前 10 名贡献者 |
| `git log --author='name'` | 특정인의 커밋만 | Commits by one author | 某位作者的提交 |
| `git log --since='1 month ago'` | 최근 한 달 커밋 | Commits in last month | 近一个月的提交 |
| `git show <hash>` | 특정 커밋의 변경 내용 | Diff of a specific commit | 查看某次提交的变更 |
| `git log --stat` | 파일 변경량과 함께 로그 보기 | Log with file change stats | 带文件变更统计的日志 |
| `git log --all --oneline --graph` | 모든 브랜치를 그래프로 | All branches as a graph | 以图形显示所有分支 |
| `git remote -v` | 원격 저장소 URL 확인 | Check remote URLs | 查看远程仓库 URL |
| `git branch -a` | 모든 브랜치 목록 | List all branches | 列出所有分支 |
| `du -sh .git` | .git 디렉토리 용량 | .git directory size | .git 目录大小 |

---

## 7. 마무리 — 한 문장 / Closing — One Sentence / 结语——一句话

> *git clone 은 다운로드가 아니라* **전 세계 개발자 공동체에 접속하는 행위** *입니다.*
>
> *git clone is not a download — it is* **an act of plugging into a global community of developers** *.*
>
> *git clone 不是下载，而是* **接入全球开发者社区的行为** *。*

---

*OSS Application and Development · Kyungpook National University*  
*Generated: 2026-05-15*

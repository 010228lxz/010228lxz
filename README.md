# Hi, I'm Xin Zhe Lee 👋

**Computer Science graduate from the University of Birmingham** · **FinTech Software Engineer** · **Trading Systems Developer**

I build **event-driven trading systems, quantitative research infrastructure, and developer tooling**.

My professional experience spans **Order Management Systems (OMS), FIX Protocol, Java/J2EE, IBM MQ, ActiveMQ, Kafka, Oracle SQL, Linux, and distributed messaging systems**, with a focus on trading workflows, order lifecycle management, execution flows, and enterprise financial infrastructure.

Outside of work, I build systems for **quantitative trading, market-data processing, execution, backtesting, risk management, and automation** using Python and modern infrastructure tooling.

I care about building software that is **observable, testable, failure-aware, and safe to operate in production**.

---

## 🚀 Featured Projects

### 📈 Trading & Market Infrastructure

**Polymarket BTC 5-Minute Trading Bot** · *Private*
Production-oriented async trading system for Polymarket BTC 5-minute prediction markets.

The system runs a ~0.5s event loop covering **market discovery → feature computation → signal generation → risk gating → execution → reconciliation → persistence**. It includes Redis-based leader election, FastAPI monitoring, a rich TUI, PostgreSQL, Alembic migrations, and on-chain CLOB signing.

~10–15K LOC across ~70 modules, with **36 test files** covering unit/integration testing, kill-switch drills, and soak testing. Currently undergoing a pre-production paper-trading soak.

**Hyperliquid Perpetuals Bot** · *Private*
Venue-agnostic crypto trading system built around a **ports-and-adapters architecture**. It processes real L2 order-book and funding data through a multi-signal strategy and risk layer before simulated VWAP execution and mark-to-market PnL.

Includes an event-driven **backtesting subsystem** for microstructure, cross-sectional, leverage, and funding-carry research, with strict `ruff` and `mypy` enforcement.

**Kafka Trading Simulation** · *Private*
Event-driven trading simulator built on a **3-broker Kafka KRaft cluster**, modelling market data, orders, risk, execution, positions, PnL, and audit as independent services.

The environment uses **RF=3, min ISR=2, and `acks=all`**, with experiments around event sourcing, offset replay, and broker failure.

**Quant System v2** · *Private*
A rebuild of my personal quantitative trading infrastructure using **nautilus_trader**, initially targeting IBKR paper trading.

Designed around strict type checking, automated quality gates, and explicit safety invariants, with `PAPER` and `DRY_RUN` enabled by default and no automatic promotion to live trading.

---

### 🛠️ Developer Tooling

**[xzSSH](https://github.com/010228lxz/xzSSH)**
A modern interactive **SSH configuration manager for OpenSSH**.

Provides a keyboard-first TUI, fuzzy search, deterministic SSH config generation, tunnels, file transfers, key lifecycle management, configuration synchronisation, and encrypted credential storage. Includes **36 test files**, shell completions, CI, and standalone GitHub Releases.

**[vpncli](https://github.com/010228lxz/vpncli)**
A self-supervising **VPN tunnel manager** for OpenFortiVPN and OpenVPN.

It handles automatic reconnection, half-open tunnel detection, OS keychain credentials, TOTP generation, validated sudo rules, and a root-owned helper. Distributed through a **Homebrew tap** with ShellCheck and Bats testing.

---

## 💼 Professional Experience

As a **FinTech Software Engineer**, I work on enterprise trading infrastructure involving **OMS, FIX, Java/J2EE, IBM MQ, ActiveMQ, Oracle SQL, Linux, and distributed messaging**.

My work involves understanding and troubleshooting the full path from **order lifecycle and messaging through execution and downstream processing**, including production support and system-level diagnostics.

---

## 🛠️ Technical Skills

**Languages**
Java · Python · C++ · Shell/Bash · Oracle SQL · JavaScript

**Trading & Financial Systems**
OMS · FIX Protocol · Order Lifecycle · Execution & Reconciliation · Market Data · Risk Controls · Backtesting · Event-Driven Architecture

**Messaging & Infrastructure**
IBM MQ · Kafka · ActiveMQ · Redis · PostgreSQL · Oracle · Linux · Docker · systemd

**Quant & Machine Learning**
NumPy · Pandas · PyTorch · XGBoost · scikit-learn · Optuna · SHAP · TensorFlow/Keras

**Web & Other**
React · Next.js · Flutter · Electron · Unity · Unreal Engine · Blender

---

## 🎓 Academic

### Final Year Project — Candlestick Patterns & ML Price Prediction

At the **University of Birmingham**, I investigated the predictive value of 14 classical candlestick patterns across the **S&P 500, FTSE, and Bursa Malaysia**, comparing them against random baselines.

The second part developed ML-based price-direction models using **Optuna-tuned XGBoost, SHAP, SMOTE-Tomek, and bidirectional LSTM**, combined through a meta-model.

---

## 🔍 Current Focus

I'm currently focused on **event-driven trading infrastructure, quantitative strategy research, market microstructure, execution systems, and production-grade risk controls**.

I'm particularly interested in the engineering problems around **distributed systems, market data, reliability, observability, and safe deployment of automated trading systems**.

---

## 📊 GitHub

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=010228lxz&show_icons=true&theme=radical&hide_border=true" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=010228lxz&layout=compact&theme=radical&hide_border=true" height="165"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=010228lxz&theme=radical&hide_border=true" alt="GitHub Streak"/>
</p>

---

## 📫 Contact

I'm always open to **interesting engineering discussions, collaboration, and opportunities in software engineering and financial technology**.

📧 **[010228lxz@gmail.com](mailto:010228lxz@gmail.com)**
💼 **[LinkedIn — Xin Zhe Lee](https://www.linkedin.com/in/xin-zhe-lee-2a95ba187)**

---

⭐️ *Thanks for stopping by. Feel free to explore my repositories.*

# Hi, I'm Xin Zhe Lee 👋

Computer Science graduate from the University of Birmingham · FinTech Software Engineer · Trading Systems Developer

I build event-driven trading systems, quantitative research infrastructure, and developer tooling.

My work spans OMS, FIX, Java/J2EE, IBM MQ, ActiveMQ, Kafka, Oracle SQL, Linux, and distributed messaging systems, with a focus on reliable execution pipelines, order lifecycle processing, and production-grade infrastructure.

I care about observability, testability, failure-aware design, and safe operations in production.

> Open to interesting engineering conversations, collaborations, and opportunities in software engineering and financial technology.

---

## 🚀 Featured Projects

### 📈 Trading & Market Infrastructure

**Polymarket BTC 5-Minute Trading Bot** · Private

Async trading system for Polymarket BTC 5-minute prediction markets, covering:
- market discovery
- feature computation
- signal generation
- risk gating
- execution
- reconciliation
- persistence

Built as a production-oriented event loop with ~10–15K LOC across ~70 modules and 36 test files covering unit/integration tests, kill-switch drills, and soak testing.

**Hyperliquid Perpetuals Bot** · Private

Venue-agnostic crypto trading system built around a ports-and-adapters architecture.  
It processes real L2 order-book and funding data through a multi-signal strategy and risk layer before simulation or execution.

Also includes an event-driven backtesting subsystem for research across microstructure, cross-sectional behavior, leverage, and funding-carry dynamics.

**Kafka Trading Simulation** · Private

Event-driven trading simulator built on a 3-broker Kafka KRaft cluster.  
Models market data, orders, risk, execution, positions, PnL, and audit as independent services.

Configured with `RF=3`, `min ISR=2`, and `acks=all`, with experiments focused on event sourcing, offset replay, and broker failure behaviour.

**Quant System v2** · Private

A rebuild of my personal quantitative trading infrastructure using `nautilus_trader`, initially aimed at IBKR paper trading.

Designed around strict type checking, automated quality gates, and explicit safety invariants, with `PAPER` and `DRY_RUN` enabled by default.

---

### 🛠️ Developer Tooling

**[xzSSH](https://github.com/010228lxz/xzSSH)**

Modern interactive SSH configuration manager for OpenSSH.

Includes:
- keyboard-first TUI
- fuzzy search
- deterministic config generation
- tunnels
- file transfers
- key lifecycle management
- config synchronization
- encrypted credential storage

**[vpncli](https://github.com/010228lxz/vpncli)**

Self-supervising VPN tunnel manager for OpenFortiVPN and OpenVPN.

Handles:
- automatic reconnection
- half-open tunnel detection
- OS keychain credentials
- TOTP generation
- validated sudo rules
- root-owned helper automation

---

## 💼 Professional Experience

As a FinTech Software Engineer, I work on enterprise trading infrastructure involving OMS, FIX, Java/J2EE, IBM MQ, ActiveMQ, Oracle SQL, Linux, and distributed messaging.

My work covers the full order lifecycle, from message flow and execution to downstream processing and production support, with a strong emphasis on reliability, observability, and operational stability.

---

## 🧠 Technical Skills

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

At the University of Birmingham, I investigated the predictive value of 14 classical candlestick patterns across the S&P 500, FTSE, and Bursa Malaysia, comparing them against random baselines.

The second part of the project developed ML-based price-direction models using Optuna-tuned XGBoost, SHAP, SMOTE-Tomek, and bidirectional LSTM, combined through a meta-model.

---

## 🔍 Current Focus

I’m currently focused on:
- event-driven trading infrastructure
- quantitative strategy research
- market microstructure
- execution systems
- production-grade risk controls

I’m especially interested in the engineering challenges around distributed systems, market data, reliability, observability, and safe deployment of automated trading systems.

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

## 📫 Let’s Connect

I’m always open to interesting engineering discussions, collaboration, and opportunities in software engineering and financial technology.

- 📧 **[010228lxz@gmail.com](mailto:010228lxz@gmail.com)**
- 💼 **[LinkedIn — Xin Zhe Lee](https://www.linkedin.com/in/xin-zhe-lee-2a95ba187)**

If you’re working on trading systems, infrastructure, or high-performance software, I’d love to connect.

---

⭐️ Thanks for stopping by. Feel free to explore my repositories.

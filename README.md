# Hi, I'm Xin Zhe Lee (010228lxz) 👋

**Computer Science graduate, University of Birmingham** · **FinTech Software Engineer** specializing in **trading systems development**

I build **quantitative trading systems** and **developer tooling** — event-driven trading bots, backtest engines, risk-gated execution pipelines, and the CLI/DevOps infrastructure that keeps them running. I care about production discipline: staged rollouts, hard safety invariants, and test suites that actually get run.

- 🔭 Currently: production-grade **Polymarket & Hyperliquid trading bots** running a paper-soak → canary → live rollout pipeline
- 🧰 Day-to-day stack: **Python (async)** · Bash/shell · Kafka · PostgreSQL · Redis · Docker · pytest · ruff/mypy

---

## 🎯 How I Build Trading Systems

My trading projects share one architecture — **venue-agnostic, ports-and-adapters design** with safety-first rollout:

```
Market Data ──▶ Signal Ensemble ──▶ Risk Gates ──▶ Execution ──▶ Reconciliation ──▶ PnL/State
   (L2 book,      (trend / momentum /    (EV gating,      (paper sim /      (fills, positions,
   funding, WS)    mean-reversion /      Kelly sizing,     live CLOB)        mark-to-market,
                   funding-carry)        drawdown stops)                      persistence)
```

**Principles I follow across every trading project:**

- 🛡️ **Never trust untested code with real capital** — every bot runs a staged rollout: `Shadow → Paper → Canary → Live`
- 📊 **Signal ensembles, not single strategies** — Bayesian-weighted combinations of trend, momentum, mean-reversion, and funding-carry signals
- ⚖️ **Risk gates before execution** — EV filtering, fractional Kelly position sizing, leverage caps, drawdown stops
- 🧪 **Test everything** — unit, integration, kill-switch drills, live rehearsal, and soak tests
- 🔌 **Venue-agnostic core** — swap venues (Polymarket ↔ Hyperliquid ↔ IBKR) without rewriting the strategy layer

---

## 🚀 Featured Projects

### 📈 Trading Systems

**Polymarket BTC 5-Minute Trading Bot** *(private — walkthrough & code available on request)*
Production-grade async trading bot for Polymarket BTC 5-minute up/down prediction markets. The most mature system in my portfolio.
- 0.5s event loop: market discovery → feature computation → ensemble signal → risk gate → execution → reconciliation → PostgreSQL persistence
- Redis-based leader election, FastAPI web monitor + rich TUI, Alembic migrations, on-chain CLOB signing (eth-account)
- ~10–15K LOC, ~70 source modules, **36 test files** including kill-switch drills and soak tests
- Won a 15-day A/B paper comparison with v2 signal-calibration weights; currently in pre-production paper soak

**Hyperliquid Perpetuals Bot** *(private — walkthrough & code available on request)*
Venue-agnostic crypto trading bot targeting Hyperliquid perpetuals, built on a ports-and-adapters architecture.
- Real L2 book + funding data → multi-signal ensemble → risk gates → simulated VWAP execution → mark-to-market PnL
- Full event-driven **backtest subsystem**: cross-sectional, microstructure, leverage, and funding-carry studies
- 9 console entry points (`hl-bot`, `hl-backtest`, `hl-ws-record`, …), 23 test files, ruff + mypy enforced

**Kafka Trading Simulation** *(private — walkthrough & code available on request)*
Event-driven trading simulator on a **3-broker Kafka (KRaft) cluster** — teaching both Kafka internals and trading architecture.
- 7 microservices: market data → orders → risk → execution → positions → PnL → audit
- Docker Compose with RF=3, min ISR=2, acks=all; guided experiments for **offset replay / event-sourcing** and **broker failover**

**Quant System v2 (nautilus_trader)** *(private — walkthrough & code available on request)*
Rebuild of my personal quant trading system on nautilus_trader, targeting IBKR paper trading first. Strict mypy + ruff + pre-commit, with hard safety invariants (`PAPER`/`DRY_RUN` default true, no auto-promotion to live).

### 🛠️ Developer Tooling (open source)

**[xzSSH](https://github.com/010228lxz/xzSSH)** — Modern interactive **SSH configuration manager** for OpenSSH
- Keyboard-first TUI dashboard with fuzzy search; JSON config deterministically compiled to `~/.ssh/config`
- Tunnels, file transfers, key lifecycle, sync/drift detection, at-rest encryption (gpg/age)
- ~55 source modules, **36 test files**, zsh completions, standalone binaries via GitHub Releases

**[vpncli](https://github.com/010228lxz/vpncli)** — Self-supervising **VPN tunnel manager** (`vpnctl`)
- POSIX shell CLI/daemon managing openfortivpn/OpenVPN tunnels with auto-reconnect on drop or half-open states
- Security-focused: OS keychain password storage, per-backend TOTP auto-generation, validated sudo rules, root-owned helper
- ~2.5K lines of shell, bats + ShellCheck test suite, CI (ShellCheck + bats on Linux/macOS)
- 📦 Distributed via **Homebrew tap**

### 🎓 Academic

**Final Year Project — Candlestick Patterns & ML Price Prediction** *(University of Birmingham)*
Two-part study: (a) backtesting 14 classical candlestick patterns (TA-Lib) against random baselines across S&P 500 / FTSE / Bursa Malaysia; (b) ML price-direction prediction with Optuna-tuned XGBoost (SHAP explainability, SMOTE-Tomek resampling) and bidirectional LSTM (focal loss), combined via a meta-model.

---

## 🛠️ Technical Skills

### 💻 Languages
Python, Bash/shell, Java, C++, C#, TypeScript, JavaScript, C, Haskell, Swift

### ⚙️ Frameworks & Tools
FastAPI, aiohttp, React, Next.js, Flutter, Electron, Docker, Kafka, PostgreSQL, Redis

### 📊 Data & Machine Learning
Pandas, NumPy, PyTorch, XGBoost, TensorFlow/Keras, Scikit-learn, SHAP, Optuna, Matplotlib

### 🎮 Game Development
Unity (including VR), Unreal Engine, Blender

### 💹 FinTech & Trading Systems
- Low-latency event-driven system design
- Market data processing (L2 books, WebSocket feeds)
- Order execution & reconciliation systems
- Backtesting & strategy simulation (event-driven engines, Monte Carlo)
- Risk management (EV gating, Kelly sizing, drawdown controls)
- Staged rollout & monitoring (Shadow → Paper → Canary → Live, Prometheus, OpenTelemetry)

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=010228lxz&show_icons=true&theme=radical&hide_border=true" alt="GitHub Stats" height="165"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=010228lxz&layout=compact&theme=radical&hide_border=true" alt="Top Languages" height="165"/>
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=010228lxz&theme=radical&hide_border=true" alt="GitHub Streak"/>
</p>

---

## 🔍 Current Focus

- Building and optimizing **trading system infrastructure**
- Exploring **quantitative strategies & financial modeling**
- Advancing skills in **machine learning for finance**
- Developing **automation tools for trading workflows**

---

## 📫 Contact

I'm always open to collaboration, discussions, or opportunities in software engineering and fintech.

- 📧 Email: [010228lxz@gmail.com](mailto:010228lxz@gmail.com)
- 💼 LinkedIn: [Xin Zhe Lee](https://www.linkedin.com/in/xin-zhe-lee-2a95ba187)

---

⭐️ *Feel free to explore my repositories and reach out if you'd like to collaborate!*

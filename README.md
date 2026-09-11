# AI Trading Research Assistant

An AI-powered research assistant that converts natural-language trading questions into structured, testable experiments.

The project focuses on the research workflow:

> Question → Hypothesis → Experiment → Evidence → Learning

This is a functional prototype built as part of a technical assignment.

---

## 🚀 Live Demo

**Live Demo:** Coming soon

**GitHub Repository:** Coming soon

---

## 📌 Problem Statement

Trading and investment research questions are often written in natural language and can contain missing or ambiguous information.

For example:

> "Does buying NIFTY after a 1.5% daily decline and holding for 3 trading days perform better when VIX is above 20?"

Before this question can be tested, several details need to be clarified:

- What instrument should represent NIFTY?
- What historical period should be tested?
- How should the 1.5% decline be calculated?
- What transaction costs should be assumed?
- What does "perform better" mean?
- What metrics should be compared?

The goal of this project is to use AI to identify these details instead of blindly making assumptions.

---

## 🎯 Project Goal

The application converts a user's natural-language trading question into a structured research experiment.

The workflow consists of five stages:

1. **Initial Understanding**
2. **Clarification**
3. **Final Experiment**
4. **Test**
5. **Learn**

---

## ✨ Features

### 1. Natural Language Question

Users can enter a trading or market research question in plain English.

Example:

> Does buying NIFTY after a 1.5% daily decline and holding for 3 trading days perform better when VIX is above 20?

---

### 2. AI-Powered Question Understanding

Google Gemini analyzes the question and extracts structured information such as:

- Instrument
- Timeframe
- Entry condition
- Exit condition
- Holding period
- Volatility filter
- Backtest period
- Transaction costs
- Additional filters
- Objective

The AI also identifies important missing information.

---

### 3. Ambiguity Detection

Instead of assuming missing trading parameters, the system asks clarification questions.

For example:

> What historical period should be used for the backtest?

> What transaction costs and slippage should be assumed for each trade?

> What specific metric defines "better performance"?

This helps prevent the AI from silently inventing critical experiment parameters.

---

### 4. Experiment Refinement

After the user answers the clarification questions, the application sends the original question, initial AI analysis, and user answers back to Gemini.

Gemini then creates a final structured experiment.

For example:

```text
Instrument:
NIFTY 50 spot index

Timeframe:
Daily

Entry:
Buy when NIFTY's current day's close has declined
at least 1.5% from the previous day's close.

Exit:
Exit at the close of the third trading day after entry.

Holding Period:
3 trading days

Volatility Filter:
VIX > 20

Backtest Period:
January 2020 to December 2025

Transaction Costs:
0.1% total transaction costs and slippage
per round trip
# 📊 AI Business Plan Writer & Financial Engine

<div align="center">

![Next.js](https://img.shields.io/badge/Next.js_15-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Zustand](https://img.shields.io/badge/Zustand-FF6B35?style=for-the-badge&logo=react&logoColor=white)
![Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Status](https://img.shields.io/badge/Status-Production-22c55e?style=for-the-badge)

**A production-grade SaaS platform for AI-powered financial modeling and investment analysis — built for the Iranian market.**

[✨ Key Features](#-key-features) · [🏗️ Architecture](#%EF%B8%8F-technical-architecture) · [📸 Screenshots](#-screenshots) · [📬 Contact](#-contact)

</div>

---

> **🔒 Source Code Notice**
> This is a **commercial financial modeling platform**. The core source code is private to protect proprietary investment calculation algorithms.
> This repository documents the **system architecture, UI design decisions, and state management strategies** for portfolio and evaluation purposes.

---

## 📖 Overview

The **AI Business Plan Writer** is a sophisticated financial analysis platform that enables entrepreneurs and financial analysts to generate investment-ready business plans in a fraction of the time. It combines real-time financial modeling with generative AI to automate complex Capex/Opex optimization — a process that traditionally takes 40+ hours of manual spreadsheet work.

### 🎯 Impact
| Metric | Result |
|---|---|
| Business plan creation time | From ~40 hrs → ~2 hrs |
| Financial metrics computed in real-time | IRR · PBP · BEP |
| AI models integrated | Google Gemini + OpenAI GPT-4o |
| RTL/Persian language support | Full A4 PDF export |

---

## ✨ Key Features

### 📈 Advanced Financial Calculations
Real-time computation of core investment metrics directly in the browser — no server round-trips:
- **IRR** (Internal Rate of Return)
- **PBP** (Payback Period)
- **BEP** (Break-Even Point)
- Dynamic cash flow projections across multi-year horizons

### 🤖 AI Global Financial Optimizer
An LLM-powered agent that reads the current financial structure and automatically suggests Capex/Opex adjustments to hit user-defined economic targets. Uses structured JSON outputs from Gemini/GPT-4o for deterministic, parseable results.

### 📄 RTL-Optimized PDF Exports
High-fidelity A4 PDF generation directly from the browser — no server-side rendering:
- Full Persian RTL typography support
- CSS Print Media Query + Canvas-to-PDF pipeline
- Pixel-perfect layout preservation across page breaks

### 💬 Conversational Data Tables
Every financial table has an embedded AI chat interface. Users can ask natural-language questions about specific rows, get explanations of calculations, or request scenario comparisons — without leaving the table view.

---

## 🏗️ Technical Architecture

### ⚙️ Tech Stack

```
┌─────────────────────────────────────────────────────┐
│                    FRONTEND LAYER                    │
│  Next.js 15 (App Router) · React 19 · TypeScript    │
├─────────────────────────────────────────────────────┤
│                  STATE MANAGEMENT                    │
│         Zustand — deterministic financial stores     │
├──────────────────────┬──────────────────────────────┤
│      AI ENGINE       │        DATA LAYER             │
│  Gemini Pro / Flash  │  TanStack Table · Radix UI   │
│  OpenAI GPT-4o       │  Tailwind CSS v4              │
│  Structured JSON     │  Framer Motion               │
├──────────────────────┴──────────────────────────────┤
│                   PDF PIPELINE                       │
│    CSS Print Media Query + Canvas-to-PDF engine     │
└─────────────────────────────────────────────────────┘
```

### 🧩 Key Architecture Decisions

**1. Decoupled Financial Hooks**
All mathematical operations (IRR, BEP, cash flow) are isolated into pure utility functions, completely separate from UI rendering. This ensures:
- UI never blocks during heavy recalculations
- Financial logic is independently testable
- Easy swapping of calculation engines

**2. Deterministic Zustand Stores**
```
User Input Change
      ↓
Zustand Store Update
      ↓
Reactive Selectors Fire
      ↓
IRR / BEP / PBP Recalculated
      ↓
UI Re-renders (only affected components)
```
Every CAPEX, OPEX, and cash flow formula recalculates reactively on any upstream change — without prop drilling or context re-renders.

**3. RTL/LTR Dynamic Direction**
A direction-detection system applies `dir="rtl"` or `dir="ltr"` contextually, ensuring charts, tables, inputs, and PDF exports all align correctly regardless of content language.

**4. AI Output Validation Layer**
All LLM responses go through a structured JSON schema validator before touching application state — preventing hallucinated values from corrupting financial models.

---

## 🤖 AI-Assisted Development

This project was built using **Cursor** and **Claude Code** as primary AI coding agents throughout the development lifecycle.

My workflow for AI-assisted development:
- Generate component scaffolding and boilerplate with AI agents
- **Manually review every output** for correctness, edge cases, and type safety
- Evaluate model suggestions against financial calculation accuracy requirements
- Reject or refactor outputs that introduce performance regressions or accessibility issues

> This hands-on experience evaluating AI-generated frontend code for production correctness is directly applicable to frontier model evaluation roles.

---

## 📸 Screenshots

> *Screenshots coming soon — currently preparing sanitized demo assets.*

| Dashboard View | AI Optimizer | PDF Export |
|---|---|---|
| `screenshot-dashboard.png` | `screenshot-optimizer.png` | `screenshot-pdf.png` |

---

## 📬 Contact

Interested in a code walkthrough, architecture deep-dive, or similar project?

<div align="center">

[![Email](https://img.shields.io/badge/Email-alireza.hpr1990%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:alireza.hpr1990@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Alireza_Hashempour-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alireza-hashempour-full-stack-engineer/)

</div>

---

<div align="center">
<sub>Built with React 19 · Next.js 15 · TypeScript · Google Gemini · OpenAI</sub>
</div>

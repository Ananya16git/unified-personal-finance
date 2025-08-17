# Unified Personal Finance

A personal finance unification tool to extract, transform, and analyze financial data from multiple sources (bank statements, invoices, etc.) in one place. Designed as a local-first, privacy-conscious solution with an end-to-end pipeline from PDF extraction to actionable insights.

## Vision

The goal of this project is to provide a **simple, unified personal finance view** by converting various financial documents into structured data that anyone can query and visualize. Users can see earnings, expenses, and category breakdowns, and ask natural language-style questions about their finances.

The long-term vision includes:  
- Unified insights from multiple financial sources.  
- Natural language queries mapped to SQL for on-the-fly answers.  
- A lightweight, user-friendly dashboard for interactive exploration.  
- Privacy-first and local execution without exposing sensitive financial data.  

## MVP Scope

The **Minimum Viable Product (MVP)** focuses on achievable, demonstrable functionality:  

**1. PDF → Parquet Extraction**
- Input: 1–2 PDFs per run (bank statement or invoice).  
- Output: Parquet file per PDF.  
- Feature: Allow user to mark which rows/columns to extract.  

**2. SQLite Integration**
- Merge all Parquet files into a single SQLite database.  
- Each PDF corresponds to a table.  
- Users can query and explore data locally.  

**3. Minimal Streamlit Dashboard**
- Top-level monthly view: total earned, total spent.  
- Category breakdown: visual charts (pie/bar).  
- Basic natural language input: map simple questions to SQL queries.  

**Excluded from MVP**
- Full NLP engine for free-text queries (simplified SQL mapping only).  
- Automatic PDF parsing for all formats (limited to 1–2 formats initially).  
- Advanced analytics or predictive insights.  

## Features
- PDF extraction to structured Parquet files  
- SQLite database unification  
- Basic interactive Streamlit dashboard  
- Easy-to-use rules for row/column selection during extraction  
- Local execution for privacy-first design  

## Tech Stack
- Python (pandas, PyPDF2/tabula-py)  
- PySpark (optional for batch scaling)  
- SQLite  
- Streamlit for dashboard  
- GitHub Actions for CI/CD (future)  

## Getting Started
1. Clone the repo  
```bash
git clone https://github.com/<username>/unified-personal-finance.git


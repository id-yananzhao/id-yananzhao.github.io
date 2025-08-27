# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Hugo-based stock analysis website built on the PaperMod theme. The site publishes daily algorithmic stock analysis reports with automated deployment to GitHub Pages. Content is organized by date and ticker symbol with comprehensive technical, fundamental, and sentiment analysis.

## Development Commands

### Local Development
```bash
# Start local development server
hugo server

# Access local site at http://localhost:1313
```

### Content Creation
```bash
# Create new stock report with archetype template
hugo new 2024-08-26/AAPL/index.md --kind stock-report

# The archetype automatically populates:
# - Title with ticker symbol
# - Date-based organization  
# - Technical analysis template
# - Social media sentiment section
# - Fundamentals analysis framework
# - Trading team decision template
```

### Build and Deploy
```bash
# Build production site (output to /public/)
hugo --gc --minify

# GitHub Actions handles deployment automatically on push to main
# Uses Hugo v0.147.2 with extended version
```

## Architecture and Content Structure

### Site Organization
- **Date-based content**: `/content/YYYY-MM-DD/TICKER/index.md`
- **Taxonomies**: Organized by ticker symbols (`tickers: ["AAPL"]`)
- **Templates**: Stock report archetype provides comprehensive analysis framework
- **Theme**: PaperMod with custom CSS enhancements for financial data

### Key Configuration (config.yml)
- **MainSections**: Controls which date folders appear on homepage
- **Taxonomies**: Only `ticker` taxonomy enabled for stock symbol organization
- **Profile Mode**: Enabled with stock analysis branding
- **Content Features**: TOC enabled, reading time, breadcrumbs, code copy buttons

### Content Template Structure
Each stock report follows a standardized format:
1. **Technical Analysis**: 8 key indicators (SMAs, EMA, MACD, RSI, ATR, VWMA)
2. **Social Media Sentiment**: Multi-platform analysis with day-by-day tracking
3. **News Analysis**: Macroeconomic context and company-specific developments
4. **Fundamentals**: Financial metrics, valuation ratios, growth prospects
5. **Trading Decision**: Research team, trading team, and portfolio management perspectives

### Deployment Pipeline
- **Trigger**: Push to main branch
- **Build**: Hugo 0.147.2 extended with Dart Sass
- **Deploy**: GitHub Pages via GitHub Actions
- **Features**: Automatic minification, garbage collection, submodule support

## Development Notes

### Custom Styling
- Extended CSS in `/assets/css/extended/report-enhancements.css`
- Theme customizations in `/assets/css/` override PaperMod defaults
- Stock chart icons and financial branding elements

### Content Guidelines
- Reports use comprehensive template with placeholder values (XXX.XX, X.XX patterns)
- Ticker symbols automatically uppercased in templates
- Date formatting follows "January 2, 2006" pattern
- Analysis sections include detailed technical indicator justifications

### Theme Integration
- PaperMod theme as Git submodule in `/themes/PaperMod/`
- Custom layouts in `/layouts/` override theme defaults
- Profile mode configuration for landing page presentation
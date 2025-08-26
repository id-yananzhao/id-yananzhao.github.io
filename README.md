# Stock Analysis Hub

A Hugo-based website for displaying daily algorithmic stock analysis reports. Built on the PaperMod theme and optimized for financial content presentation.

## Features

- **Daily Reports**: Organized by date and ticker symbol (`/YYYY-MM-DD/TICKER/`)
- **Multiple Views**: Browse by ticker, sector, tags, or chronologically
- **Professional Design**: Clean, mobile-responsive layout optimized for financial data
- **Automated Publishing**: GitHub Pages deployment with GitHub Actions

## Quick Start

### Local Development

1. **Install Hugo** (requires v0.110.0+):
   ```bash
   # macOS with Homebrew
   brew install hugo
   
   # Verify installation
   hugo version
   ```

2. **Clone and Run**:
   ```bash
   git clone <your-repo-url>
   cd <repo-name>
   hugo server
   ```

3. **Access**: Open http://localhost:1313 to view your site

### Adding Stock Reports

Create new reports in the `/content/YYYY-MM-DD/TICKER/` structure:

```bash
hugo new 2024-08-26/AAPL/index.md --kind stock-report
```

Each report should include:
- Technical analysis with key metrics
- Fundamental analysis and recent developments  
- Market sentiment and analyst coverage
- Trading strategy and risk management
- Executive summary with rating and target price

### Configuration

Key settings in `config.yml`:
- `baseURL`: Your website URL
- `MainSections`: Date folders to feature on homepage
- `socialIcons`: Contact information
- `taxonomies`: Categories for organizing reports (ticker, sector, tags)

## Content Structure

```
content/
├── 2024-08-26/
│   ├── AAPL/
│   │   └── index.md
│   └── GOOGL/
│       └── index.md
├── tickers/
│   └── _index.md
├── sectors/
│   └── _index.md
└── archive.md
```

## Deployment

The site automatically deploys to GitHub Pages when you push to the main branch. Ensure:

1. GitHub Pages is enabled in your repository settings
2. Source is set to "GitHub Actions"
3. The `.github/workflows/hugo.yml` workflow is present

## Requirements

- Hugo v0.110.0 or later
- Git for version control
- GitHub account for hosting

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Support

For issues or questions, please open an issue in the repository.
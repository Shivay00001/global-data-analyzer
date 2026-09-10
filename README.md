# Global Data Intelligence Platform

A comprehensive extraction and analysis engine for global population opinion, psychology, and social trends.

## Features

- **Multi-Source Extraction**: Scalable extractors for:
  - **Web**: Generic web scraper with auto-detection of content structures.
  - **Social Media**: Simulation modules for Twitter, Facebook, Instagram, Reddit, and YouTube (ready for API integration).
- **Opinion Analysis**:
  - **Sentiment Analysis**: Keyword-based sentiment scoring.
  - **Theme Identification**: Extract common topics and themes.
- **Psychological Profiling**:
  - **Behavioral Patterns**: Analyze consistency, trends, and volatility.
  - **Population Segmentation**: Group data into psychological segments.
- **Reporting**: Automated insight generation covering data simplification, opinion metrics, and source quality.

## Usage

```python
from global_data_analyzer import GlobalInsightsEngine

engine = GlobalInsightsEngine()

# Extract from web
df_web = engine.extract_web_data(['https://example.com/news'])

# Extract from social media (simulation)
df_social = engine.extract_social_media('twitter', query='AI', count=50)

# Analyze
results = engine.analyze_dataset(df_social)
print(results['opinion_analysis'].insights)
```

## Architecture

The system is built on a modular architecture:

1. **Extractors**: `WebDataExtractor`, `SocialMediaExtractor`
2. **Formatters**: `DataFormatter` for standardizing inputs.
3. **Analyzers**: `OpinionAnalyzer`, `PsychologyAnalyzer`.
4. **Engine**: `GlobalInsightsEngine` orchestrating the pipeline.

## Dependencies

- `pandas`
- `numpy`
- `requests`
- `beautifulsoup4`

## 🐳 Docker Support

Run the tool effortlessly using Docker:

`ash
docker compose build
docker compose run analyzer --help
`

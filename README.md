# AI-Powered Technology Intelligence Hub

An automated workflow that eliminates manual technology news monitoring by aggregating, deduplicating and organising content from multiple sources into a centralised Notion knowledge hub.

## Overview

Before building this solution, staying current with technology, AI and cybersecurity news required manually checking multiple websites and newsletters each morning. This process typically took approximately 20–30 minutes per day and often resulted in duplicate information from different sources.

To streamline this process, I designed and implemented a self-hosted automation platform using n8n, Docker and Notion. The workflow automatically collects articles from multiple RSS feeds, removes duplicates and stores structured records in a searchable knowledge repository.

## Architecture

![Architecture Screenshot](Architecture.png)

## Technologies Used

- n8n (Workflow Automation)
- Docker (Self-Hosted Environment)
- Notion API
- RSS Feeds
- JavaScript
- Workflow Automation

## Workflow Features

### Multi-Source Aggregation

Automatically collects articles from multiple technology, AI and cybersecurity sources including:

- OpenAI
- Anthropic
- Microsoft Security
- Microsoft 365
- AWS Security Blog
- The Hacker News
- ITPro

### Two-Stage Duplicate Detection

To prevent duplicate records:

1. Duplicate RSS entries are removed before processing.
2. Incoming articles are validated against existing Notion records before creation.

### Knowledge Management

All content is stored in Notion with:

- Title
- Source
- URL
- Publication Date
- Category

This creates a searchable and centralised technology intelligence repository.

## Technical Challenges

### Duplicate Prevention

The most complex challenge was duplicate management.

The initial design queried Notion for every article individually. While functional, this approach became inefficient as the database grew.

The workflow was redesigned to:

- Retrieve existing article links once per execution
- Build an in-memory reference list
- Compare incoming articles against that list
- Process only unique records

This significantly improved efficiency and eliminated duplicate entries.

## Results

- Reduced manual news review time from approximately 20–30 minutes per day to near zero
- Automated monitoring across 7+ information sources
- Centralised technology, AI and cybersecurity intelligence in a single location

## Workflow Screenshot

![Workflow Screenshot](Workflow.png)

## Future Enhancements

- AI-powered article summarisation before storing to Notion
- Trend analysis and topic clustering
- Enhanced categorisation and tagging
- Additional business and technology intelligence sources

---
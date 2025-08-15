---
layout: page
title: "Submission Guidelines"
description: "Guidelines for submitting your project to the LLM Hackathon for Applications in Materials Science & Chemistry."
keywords: "LLM Hackathon Submission, Project Guidelines, Submission Requirements"
---

## Submission Deadline

**Final submissions are due: {{ site.event.submission_deadline }}**

All projects must be submitted by this deadline to be eligible for judging and prizes.

## Submission Requirements

### 1. Project Repository

Your project must include a **public GitHub repository** with:

- Clear README with project description and setup instructions
- Well-documented code with comments
- Requirements file (e.g., `requirements.txt`, `environment.yml`)
- License file (recommended: MIT, Apache 2.0, or similar open-source license)

### 2. Project Documentation

Include the following in your repository:

#### README.md Must Contain:

- **Project title and brief description**
- **Problem statement** - What challenge are you addressing?
- **Solution approach** - How does your project use LLMs?
- **Installation and setup instructions**
- **Usage examples** with sample inputs/outputs
- **Team members** and their contributions
- **Acknowledgments** and data sources used

#### Additional Documentation:

- **Technical details** - Architecture, algorithms, model choices
- **Results and evaluation** - Performance metrics, validation
- **Future work** - Potential improvements and extensions
- **References** - Related work and citations

### 3. Demonstration Materials

Provide clear evidence of your project's functionality:

#### Required:

- **Working code** that can be executed by judges
- **Example outputs** - Screenshots, generated files, or results
- **Demo video** (2-3 minutes) showing your project in action

#### Optional but Recommended:

- **Live demo** - Hosted application or interactive notebook
- **Presentation slides** - For final presentations
- **Test data** - Sample datasets for validation

## Submission Process

### Step 1: Prepare Your Repository

1. Ensure your GitHub repository is **public** and accessible
2. Complete all required documentation
3. Test that others can reproduce your results
4. Add appropriate tags/releases for the hackathon submission

### Step 2: Submit Your Project

**Submission form will be available at:** [Submission Portal]({{ site.links.registration }})

Provide the following information:

- **Team name** and member details
- **GitHub repository URL**
- **Project category** (see categories below)
- **Brief project summary** (250 words max)
- **Demo video URL** (YouTube, Vimeo, or similar)

### Step 3: Final Presentations

- Selected teams will present their projects on {{ site.event.dates | split: '-' | last | strip }}
- Presentations will be **5 minutes + 2 minutes Q&A**
- Both virtual and in-person presentations accepted

## Project Categories

Choose the category that best fits your project:

### 🔬 Materials Discovery & Design

- Novel material generation and optimization
- Property prediction and materials screening
- Synthesis pathway planning

### ⚗️ Chemical Research & Analysis

- Reaction prediction and mechanism analysis
- Molecular design and drug discovery
- Chemical safety and risk assessment

### 📊 Data Processing & Visualization

- Automated literature review and synthesis
- Data extraction and knowledge graphs
- Interactive visualization tools

### 🤖 AI Assistants & Automation

- Research assistants for scientists
- Automated experimental design
- Scientific writing and documentation tools

### 🔧 Tools & Platforms

- Domain-specific applications
- API integrations and workflows
- User interfaces for scientific computing

### 🌟 Open Innovation

- Creative applications of LLMs in science
- Cross-disciplinary approaches
- Novel use cases and methodologies

## Judging Criteria

Projects will be evaluated based on:

{% for criteria in site.data.prizes.judging_criteria %}

### {{ criteria.title }} (25%)

{{ criteria.description }}
{% endfor %}

## Technical Guidelines

### Recommended Technologies

- **LLM APIs**: OpenAI GPT, Anthropic Claude, Google Gemini, etc.
- **Open Source Models**: Llama, Mistral, CodeLlama via HuggingFace
- **Scientific Libraries**: RDKit, ASE, Pymatgen, PySCF, etc.
- **Frameworks**: LangChain, LangGraph, AutoGen, CrewAI

### Data and Ethics

- **Use publicly available datasets** or generate synthetic data
- **Respect copyright and licensing** of data sources
- **Include proper citations** for datasets and models used
- **Avoid sensitive or proprietary information**
- **Follow ethical AI practices** in development and deployment

### Code Quality

- **Write clean, readable code** with appropriate comments
- **Follow language-specific style guides** (PEP 8 for Python, etc.)
- **Include error handling** and input validation
- **Provide clear setup instructions** and dependency management

## Resources for Participants

### Computing Resources

- Cloud computing credits may be available (check with organizers)
- Local computational resources at on-site locations
- Free tiers of major cloud providers (AWS, GCP, Azure)

### Datasets

Visit our [Resources page](/resources/) for curated datasets in:

- Materials science databases
- Chemical reaction databases
- Scientific literature and publications
- Molecular and crystal structure data

### Getting Help

- **Slack community**: [Join here]({{ site.links.slack }})
- **Mentorship sessions**: Available throughout the event
- **Technical support**: On-site and virtual assistance
- **Documentation**: Comprehensive guides and tutorials

## Submission Checklist

Before submitting, ensure you have:

- [ ] &nbsp; **Public GitHub repository** with complete code
- [ ] &nbsp; **README.md** with all required sections
- [ ] &nbsp; **Working installation instructions** tested on clean environment
- [ ] &nbsp; **Demo video** (2-3 minutes) uploaded and accessible
- [ ] &nbsp; **Example outputs** or screenshots included
- [ ] &nbsp; **License file** added to repository
- [ ] &nbsp; **Team member information** documented
- [ ] &nbsp; **Submission form** completed with all details

## Questions?

For submission-related questions:

- Check our [FAQ page](/faq/)
- Join our [Slack community]({{ site.links.slack }})
- Contact organizers: [{{ site.links.main_organizer_email }}](mailto:{{ site.links.main_organizer_email }})

**Good luck with your submissions! We're excited to see your innovative applications of LLMs in materials science and chemistry.**

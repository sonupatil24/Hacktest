# Git AI Agent for PR Review Notifications

A Python-based AI agent that monitors GitHub repositories for pending Pull Request reviews and sends automated email notifications to reviewers.

## Features

- 🔍 Monitors multiple GitHub repositories for pending PR reviews
- 📧 Sends scheduled email notifications to reviewers
- ⚙️ Configurable notification schedules
- 🤖 AI-powered analysis of PR urgency and priority
- 📊 Detailed logging and monitoring
- 🔒 Secure configuration management

## Setup Instructions

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Configuration
Copy `.env.example` to `.env` and fill in your credentials:
```bash
cp .env.example .env
```

### 3. Run the Agent
```bash
python main.py
```

## Configuration

Set up the following environment variables in your `.env` file:

- `GITHUB_TOKEN`: Your GitHub personal access token
- `EMAIL_HOST`: SMTP server host
- `EMAIL_PORT`: SMTP server port
- `EMAIL_USER`: Your email username
- `EMAIL_PASSWORD`: Your email password
- `DEFAULT_REVIEWER_EMAIL`: Default reviewer email address

## Project Structure

```
git-ai-agent/
├── main.py                 # Main application entry point
├── config/
│   ├── __init__.py
│   └── settings.py         # Configuration management
├── services/
│   ├── __init__.py
│   ├── github_service.py   # GitHub API integration
│   ├── email_service.py    # Email notification service
│   └── scheduler_service.py # Task scheduling
├── models/
│   ├── __init__.py
│   └── pr_models.py        # Data models for PR information
├── utils/
│   ├── __init__.py
│   ├── logger.py           # Logging configuration
│   └── helpers.py          # Utility functions
├── templates/
│   └── email_template.html # Email notification template
├── requirements.txt
├── .env.example
└── README.md
```

## Usage

The agent runs continuously and checks for pending PR reviews based on your configured schedule. It will:

1. Fetch all open PRs from monitored repositories
2. Identify PRs that need review
3. Analyze urgency based on PR age, labels, and other factors
4. Send consolidated email notifications to reviewers

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

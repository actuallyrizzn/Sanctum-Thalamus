# Thalamus

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Docs License: CC BY-SA 4.0](https://img.shields.io/badge/Docs-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

> **🚨 IMPORTANT NOTICE FOR NEW DEVELOPERS** 🚨
> 
> **This repository has been graduated to Sanctum Core Module status!**
> 
> **For new development, please use the canonical source:**
> **→ [github.com/sanctumos/thalamus](https://github.com/sanctumos/thalamus) ←**
> 
> This repository remains available for users who prefer to continue using this version, but new features and updates will be developed in the official Sanctum repository.

A real-time transcript refinement system that processes and enhances speech-to-text output using AI.

## Features

- Real-time processing of speech-to-text segments
- Speaker identification and mapping
- Content refinement for clarity and readability
- SQLite database for reliable data storage
- Webhook support for event processing

## Prerequisites

- Python 3.8+
- OpenAI API key

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/thalamus.git
cd thalamus
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
```bash
cp .env.example .env
# Edit .env with your OpenAI API key
```

5. Initialize the database:
```bash
python init_db.py
```

## Usage

1. Start the main application:
```bash
python thalamus_app.py
```

2. Start the transcript refiner:
```bash
python transcript_refiner.py
```

3. Start the webhook simulator (optional):
```bash
python replay_webhook_simulator.py
```

## Database Schema

The application uses SQLite with the following tables:

- `sessions`: Stores session information
- `speakers`: Stores speaker information
- `segments`: Stores raw transcript segments
- `refined_segments`: Stores refined transcript segments

## Development

### Running Tests

```bash
python -m pytest tests/
```

## License

MIT License - see LICENSE file for details 
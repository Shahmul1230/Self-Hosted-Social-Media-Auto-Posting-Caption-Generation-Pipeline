\# Self-Hosted AI Video Automation Pipeline using n8n, Ollama \& Postiz



A full video automation pipeline built with \*\*n8n\*\*, \*\*Ollama\*\*, \*\*Whisper AI\*\*, \*\*Postiz\*\*, \*\*Docker Compose\*\*, \*\*Google Drive\*\*, \*\*Google Sheets\*\*, and \*\*Telegram\*\*.



This workflow automatically detects new video uploads, transcribes videos, generates platform-specific titles/captions/descriptions/hashtags, posts to multiple platforms, logs the status, and sends Telegram notifications.



\## Project Overview



This project was designed as a self-hosted and cost-efficient automation pipeline for content creators and businesses.



Instead of using expensive SaaS tools, this system uses self-hosted tools and local AI models to automate video publishing across multiple social media platforms.



The workflow uses Google Drive as the video upload source, Whisper AI for transcription, Ollama/Qwen for content generation, Postiz for multi-platform posting, Google Sheets for logging, and Telegram for notifications.



\## Key Features



\* Google Drive folder trigger

\* Automatic new video detection

\* Automatic video download

\* Whisper AI transcription

\* Ollama local AI model integration

\* Qwen model for content generation

\* Platform-specific title generation

\* Platform-specific caption generation

\* Platform-specific description generation

\* Hashtag generation

\* JSON-based structured AI output

\* Auto-posting using Postiz

\* Google Sheets posting log

\* Telegram success/failure notification

\* Auto-retry logic

\* Self-hosted n8n using Docker Compose

\* Self-hosted Postiz posting manager

\* Cost-efficient automation setup



\## Supported Platforms



\* TikTok

\* Instagram Reels

\* YouTube Long Videos

\* YouTube Shorts

\* Facebook Personal

\* Facebook Business Page

\* Threads

\* X/Twitter

\* Pinterest



\## Problem It Solves



Content creators and businesses usually need to manually:



\* Download videos

\* Write captions

\* Create titles

\* Generate hashtags

\* Upload content to different platforms

\* Track posting status

\* Notify client/team

\* Retry failed posts



This workflow automates the full process and saves a large amount of manual work.



\## Why This Project Is Valuable



Most video automation tools require paid subscriptions.



This project reduces client cost by using:



\* Self-hosted n8n

\* Self-hosted Postiz

\* Local Ollama AI model

\* Whisper AI transcription

\* Docker Compose deployment



The client does not need to spend extra money on expensive automation SaaS tools.



\## Workflow Process



1\. A new video is uploaded to a Google Drive folder.

2\. n8n detects the new upload automatically.

3\. The workflow checks if the uploaded file is a video.

4\. The video is downloaded.

5\. Whisper AI transcribes the video.

6\. A visual summary/helper step analyzes the video.

7\. qwen2.5vl:7b analyzes the transcript and context.

8\. AI generates platform-specific caption:



&#x20;  \* Title

&#x20;  \* Caption

&#x20;  \* Description

&#x20;  \* Hashtags

9\. The output is structured as JSON.

10\. Postiz receives the video and generated content.

11\. The video is posted to selected platforms.

12\. Google Sheets logs status, timestamp, platform, title, caption, and error messages.

13\. Telegram sends success/failure notifications.

14\. Failed posting attempts can be tracked and retried.



\## Architecture



```text

Google Drive Upload

&#x20;       ↓

n8n Trigger

&#x20;       ↓

Video Type Check

&#x20;       ↓

Video Download

&#x20;       ↓

Whisper AI Transcription

&#x20;       ↓

Visual Summary Helper

&#x20;       ↓

qwen2.5vl:7b Caption Generation

&#x20;       ↓

Caption Validation

&#x20;       ↓

Postiz Upload

&#x20;       ↓

Multi-platform Posting

&#x20;       ↓

Google Sheets Logging

&#x20;       ↓

Telegram Notification

```



\## Tech Stack



\* n8n

\* Docker Compose

\* Postiz

\* Ollama

\* qwen2.5vl:7b Model

\* Whisper AI

\* Google Drive

\* Google Sheets

\* Telegram Bot

\* Social Media Automation



\## Demo



Loom Demo: https://www.loom.com/share/956977b0036746a0b78fa18598adc226



\## Screenshots



Add screenshots inside the `assets` folder.



```md

!\[Full Workflow](assets/Heyrock Social platform posting.png)



!\[Postiz Dashboard](assets/Self\_Hosted\_Postiz.png)



!\[Google Sheets Log](assets/sheet\_Updates.png)



!\[Telegram Alert](assets/Telegram\_notifications.png)



```



\## Folder Structure



```text

ai-video-automation-pipeline-n8n-postiz/

│

├── assets/

│   ├── full-workflow.png

│   ├── postiz-dashboard.png

│   ├── google-sheets-log.png

│   ├── telegram-alert.png

│   └── pipeline-diagram.png

│

├── workflow/

│   └── heyrock social platform posting .json

│

└── README.md

```



\## How to Use



1\. Download or clone this repository.

2\. Import the workflow JSON file into n8n.

3\. Configure your own Google Drive credentials.

4\. Configure Whisper transcription.

5\. Configure Ollama and Qwen model.

6\. Configure Postiz connection.

7\. Configure Google Sheets logging.

8\. Configure Telegram bot notification.

9\. Add your own platform integrations inside Postiz.

10\. Upload a test video to Google Drive.

11\. Check generated captions and posting logs.

12\. Activate the full workflow after successful testing.



\## Required Configuration



This workflow requires users to configure their own:



\* Google Drive account

\* Google Sheets account

\* Telegram bot

\* Postiz instance

\* Social media platform integrations

\* Ollama model

\* Whisper transcription service

\* n8n credentials



No real credentials are included in this repository.



\## Security Note



This repository does not include real API keys, access tokens, webhook URLs, client credentials, social media tokens, private videos, Google Drive folder IDs, Google Sheet IDs, Telegram chat IDs, Postiz tokens, or business data.



All sensitive values have been removed or replaced with placeholders before publishing.



The workflow JSON is provided only as a sanitized portfolio/demo version.

To use this workflow, users must configure their own credentials inside n8n.



\## Status



Phase 1 completed and tested.



\## Author



Built by Md. Shahmul Islam

AI Automation Developer | n8n Workflow Builder




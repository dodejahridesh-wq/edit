---
name: office-automation
description: >
  Automate Google Workspace and Microsoft Office Graph actions.
---

# Office Automation (Google & Microsoft APIs)

## Overview
Automate documents creation, calendar events booking, spreadsheet entries, and emails using the Google Workspace REST APIs or Microsoft Graph REST API.

## Core API Endpoints
- **Google Sheets Append**: `POST https://sheets.googleapis.com/v4/spreadsheets/{spreadsheetId}/values/{range}:append`
- **Microsoft Graph Send Mail**: `POST https://graph.microsoft.com/v1.0/me/sendMail`
- **Microsoft Graph Create Event**: `POST https://graph.microsoft.com/v1.0/me/events`

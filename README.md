# latersystemArchitecture.md
# System Architecture – LATER

## Overview
LATER is a web-based and mobile-responsive application built to collect, categorize, and schedule reminders for saved content across multiple platforms.

## Architecture Stack
- **Frontend:** React.js (Next.js for server-side rendering)
- **Backend:** Node.js with Express
- **Database:** MongoDB (Atlas)
- **Authentication:** Firebase Auth
- **Notifications:** Firebase Cloud Messaging
- **Integrations:** YouTube Data API, Twitter API, Pocket API

## Component Communication
1. **Frontend → Backend (API Gateway):**
   - RESTful endpoints handle user authentication, content save, and reminder scheduling.
2. **Backend → Database:**
   - MongoDB stores user profiles, saved content metadata, and reminder settings.
3. **Reminder Service:**
   - A Node.js cron job triggers Firebase push notifications based on user time zones.
4. **Analytics Module:**
   - Collects and aggregates engagement data for progress dashboards.

## Feasibility Notes
We can get all core APIs that exist publicly (YouTube, Pocket, Twitter).
Initial MVP can run on Heroku / Vercel with Firebase integration.
Architecture supports scaling via microservices for future personalization features.

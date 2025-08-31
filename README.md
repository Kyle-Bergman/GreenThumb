🌱 Project Proposal: GreenThumb (Web App)

GreenThumb is a web-based plant care assistant app designed to help users of all experience levels care for their houseplants with confidence and ease. Built using React and JavaScript, the app combines a user-friendly web interface, intelligent scheduling, and external plant data integration to deliver a personalized plant care experience.

GreenThumb enables users to:

Track their entire plant collection

Receive customized care reminders (watering, fertilizing, sunlight needs)

Log growth milestones with photos and notes

Export plant journals for personal documentation or sharing

What sets GreenThumb apart is its built-in AI Assistant, a conversational guide users can interact with naturally. The AI can:

Answer plant care questions (e.g., “Why are my Monstera leaves yellowing?”)

Suggest care plans based on plant type and environment

Automatically adjust watering schedules based on user input

Offer gentle reminders via in-app messages or browser notifications

By integrating with external plant databases (like Trefle or Plant.id), GreenThumb provides species-specific care recommendations — transforming general care into tailored guidance.

🔧 Tech Stack

Frontend

React (for interactive web UI)

React Router (for navigation and user flow)

Axios (API calls to backend & external plant APIs)

React-Chat-UI / custom components (for AI Assistant chat interface)

CSS / TailwindCSS (for responsive styling and layouts)

Backend

Node.js + Express.js

MongoDB with Mongoose (for database management)

OpenAI API (for AI assistant functionality)

Axios (for handling API requests)

Others

Plant ID or Trefle API (for plant species data)

Firebase / Cloudinary (for image hosting if needed)

dotenv (for managing environment variables)

Label: Difficulty: Medium
Type: Full stack

⚖️ Focus of Project

This will be an evenly focused full-stack application.

Frontend: Prioritizes a friendly, engaging web experience, especially with the AI assistant and plant journal UI.

Backend: Equally important for reminders, plant data storage, AI prompts, and secure user management.

Label: Difficulty: Medium
Type: Full stack

🌐 Platform

This will be a web app (React, JavaScript).
Accessible on desktop browsers, designed to be responsive for tablets and laptops.

Label: Difficulty: Medium
Type: Full stack

🎯 Project Goals

GreenThumb will help plant owners:

Keep track of their plant collections

Receive personalized care guidance (via AI)

Stay consistent with interval-based reminders

Document growth with notes and images

Feel confident in plant care, even as beginners

Label: Difficulty: Medium

👥 Target Users

Plant beginners needing friendly, accessible advice

Busy professionals needing reliable reminders

Experienced collectors tracking plant health and optimizing care

Ages 20–40, eco-conscious, web-first users who enjoy tech + nature

Label: Difficulty: Easy

📊 Data Sources

External APIs: Trefle / Plant.id

Plant species, care needs, growth patterns, toxicity, etc.

Internal Data: User-submitted

Plant nicknames, photos, watering/fertilizing logs, reminders

AI Prompts: Based on

Species data

User lifestyle (e.g., “I travel a lot”)

Care history logs

Label: Difficulty: Medium
Type: Backend

🗄️ Database Schema (Mongoose Example)
// User Schema
{
  username: String,
  email: String,
  plants: [Plant._id],
  preferences: {
    notificationMethod: String,
    timezone: String
  }
}

// Plant Schema
{
  name: String,
  species: String,
  addedDate: Date,
  careHistory: [{ type: String, date: Date, notes: String }],
  reminders: [{ type: String, interval: Number, nextDue: Date }],
  journal: [{ photoUrl: String, notes: String, date: Date }]
}


Label: Difficulty: Medium
Type: Backend

⚠️ Potential Issues

API rate limits / inconsistent species data

Slow responses for plant image queries

OpenAI costs if usage spikes

Debugging API key security & managing environment variables

Label: Difficulty: Medium
Type: Backend

🔐 Sensitive Information

OpenAI API Key

MongoDB URI

User authentication info

Firebase/Cloudinary credentials (if used for photo storage)

➡️ All stored in .env on backend only.

Label: Difficulty: Medium
Type: Backend

📦 Core Functionality

Add/Edit/Delete plants

Interval-based reminders for watering/fertilizer

Plant growth journal (photos & notes)

Exportable timeline (PDF/CSV)

External plant data integration

AI Assistant (chat interface)

Smart schedule generation

Natural language commands (“Remind me every 5 days”)

Label: Difficulty: Hard
Type: Full stack

🔄 User Flow

Onboarding & AI Guide – “Welcome to GreenThumb! What plant are we starting with?”

Add Plant – nickname, species lookup, upload photo

Care Settings – set intervals or let AI suggest

Daily Use – reminders (“Water Monstera today”), add logs, ask AI

Growth Timeline – view/export plant history

Long-Term – AI optimizes schedules based on usage patterns

Label: Difficulty: Medium
Type: Full stack

🚀 Beyond CRUD + Stretch Goals

More than CRUD

AI Assistant with GPT-4

Smart, interval-based scheduling

Real plant database integration

Natural language command support

Exportable journals/timelines

AI-guided onboarding

Stretch Goals

Voice interaction with AI

Image recognition for plant diseases

Smart notifications (browser-based, behavior-aware)

Social features (share growth updates)

Label: Difficulty: Hard
Type: Full stack

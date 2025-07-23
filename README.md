🌿 GreenThumb – Smart Plant Care Assistant

Project Proposal:
GreenThumb is a mobile-first plant care assistant app designed to help users of all experience levels care for their houseplants with confidence and ease. Built using React Native and JavaScript, the app combines user-friendly design, intelligent scheduling, and external plant data integration to deliver a truly personalized plant care experience.

GreenThumb enables users to track their entire plant collection, receive customized care reminders (watering, fertilizing, sunlight needs), log growth milestones with photos and notes, and export plant journals for personal documentation or sharing.

What sets GreenThumb apart is its built-in AI Assistant, a conversational guide that users can interact with naturally. 

The AI can:

Answer plant care questions (e.g., “Why are my Monstera leaves yellowing?”),

Suggest care plans based on plant type and environment,

Automatically adjust watering schedules based on user input,

Offer gentle reminders via in-app messages or notifications.

By integrating with external plant databases (like Trefle or Plant.id), GreenThumb provides species-specific care recommendations — transforming general care into tailored guidance.

Key Features:

Dynamic plant collection management.

Smart, interval-based reminders for watering & fertilizing.

Care logging with photo uploads and notes.

Built-in AI plant assistant.

Exportable care journals and timelines.

External database integration for plant species info.

GreenThumb aims to reduce the stress of plant care by turning it into a habit-building and rewarding experience. Whether you’re nurturing your first succulent or managing a full-blown indoor jungle, GreenThumb is the green companion you've been waiting for.

1. What tech stack will you use for your final project?
   
Frontend:

React Native (mobile app development)

Expo (to streamline deployment, asset management, and native APIs)

react-native-gifted-chat (for the AI assistant UI)

Backend:

Node.js + Express.js

MongoDB with Mongoose for database management

OpenAI API for the AI Assistant

Axios for handling HTTP requests to APIs

Others:

Plant ID or Trefle API (for species data)

Firebase or Cloudinary (for image hosting if needed)

dotenv for managing environment variables (OpenAI API key, DB URI)

Label:

Difficulty: Medium

Type: Full stack

2. Is the front-end UI or the back-end going to be the focus of your project? Or are you going to make an evenly focused full-stack application?
   
This will be an evenly focused full-stack application. The front-end emphasizes a friendly and engaging user experience, especially with the AI assistant and care journaling UI. The back-end is equally important to support reminders, plant data, AI prompts, and secure data handling.

Label:

Difficulty: Medium

Type: Full stack

3. Will this be a website? A mobile app? Something else?
   
Mobile App, built using React Native via Expo. Designed for iOS and Android, optimized for plant care on-the-go.

Label:

Difficulty: Medium

Type: Full stack

4. What goal will your project be designed to achieve?
   
To help plant owners:

Keep track of their plant collections.

Receive personalized care guidance (via AI).

Stay consistent with interval-based reminders.

Document plant growth with notes and images.

Feel confident, even if they have no plant handling experience.

Label:

Difficulty: Medium

5. What kind of users will visit your app?
   
Plant beginners who need basic, friendly advice.

Busy professionals who need reliable, interval-based reminders.

Experienced plant collectors looking to track progress and optimize care.

Ages 20–40, eco-conscious, mobile-first users who love nature & tech.

Label:

Difficulty: Easy

6. What data do you plan on using? How are you planning on collecting your data?
   
External API: Trefle, Plant.id, or similar to get:

Species names.

Sunlight, water, and soil requirements.

Growth patterns, toxicity, etc.

Internal Data: Logged by user via app.

Plant nicknames.

Photos.

Water/fertilize logs.

Reminders.

AI Prompts: Based on:

Species data.

User’s lifestyle (e.g., “I travel a lot”)

Care history logs.

Label:

Difficulty: Medium

Type: Backend

7. What does your database schema look like?
   
Example using Mongoose:

JavaScript

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

Label:

Difficulty: Medium

Type: Backend

8. What kinds of issues might you run into with your API?
   
API limitations or rate limits (especially with plant data or OpenAI).

Inconsistent species names or plant IDs from public plant APIs.

Slow or large responses when retrieving plant image data.

OpenAI costs if usage spikes (important to monitor API usage).

Label:

Difficulty: Medium

Type: Backend

Requires debugging, API key management, and response normalization.

9. Is there any sensitive information you need to secure?
    
OpenAI API Key

MongoDB URI

User authentication info (if using login system)

Optional: Firebase/Cloudinary credentials for photo storage

All secrets stored in .env, backend only. No API keys exposed on client.
Label:

Difficulty: Medium

Type: Backend

Securing keys, tokens, and environment variables is critical and often overlooked.

10. What functionality will your app include?
    
Add/Edit/Delete plants

Interval-based reminders for water/fertilizer

Plant growth journal (photos & notes)

Exportable timeline (PDF/CSV)

External plant data integration

AI assistant chatbot

Smart schedule generation

Natural language command support ("Remind me every 5 days")

Label:

Difficulty: Hard

Type: Full stack

This is the most code-intensive and user-focused task. Involves reminder logic, form handling, database operations, and real-time interaction.

11. What will the user flow look like?
    
Onboarding & AI Chat Guide

“Welcome to GreenThumb! What plant are we starting with?”

Add Plant

Enter nickname, pick species, and upload photo.

Care Settings

Choose watering/fertilizing intervals or let AI suggest.

Daily Use

View reminders (e.g., “Water your Monstera today!”)

Add care logs or journal entries.

Ask AI: “Why are my leaves drooping?”

Growth Timeline

View timeline & export.

Long-Term

AI continues to optimize schedules based on plant data and user behavior.
Label:

Difficulty: Medium

Type: Full stack

12. What features make your site more than a CRUD app? What are your stretch goals?
Beyond CRUD:

AI Assistant with GPT-4 integration

Interval-based smart scheduling

Integration with real plant databases

Natural language commands

Exportable growth journals

Guided onboarding by AI

Stretch Goals:

Voice interaction with the AI assistant

Image recognition for identifying plant diseases

Smart push notifications with behavior-based reminders

Social features: share plant growth updates

Label:

Difficulty: Hard

Type: Full stack

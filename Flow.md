🌿 GreenThumb - Front-End Control Flow

Start
Landing / Onboarding Screen


Welcome message + AI Chat intro (“Welcome to GreenThumb! What plant are we starting with?”)


Actions:


Go to Register


Go to Login



Authentication
Register Screen


Form: username, email, password


Optional: profile picture, timezone


Actions: Register → Plant Dashboard


Link: Already have an account? → Login


Login Screen


Form: email + password


Actions: Login → Plant Dashboard


Link: Don’t have an account? → Register



Main App Flow
Plant Dashboard (Home)


Displays: List of user’s plants (cards with photo + nickname)


Actions:


Add Plant (+ button)


View Plant Details


Open AI Assistant


View Reminders


Profile Settings



Plant Management
Add Plant Screen


Inputs:


Plant nickname


Choose species (search API)


Upload photo


Actions:


Save → Plant Dashboard


Plant Details Screen


Tabs:


Care Schedule (watering/fertilizing intervals)


Journal (photos + notes)


Growth Timeline (export option)


Actions:


Edit Plant


Delete Plant


Log Care Event (e.g., “Watered today”)



AI Assistant
Chat Screen (react-native-gifted-chat)


Conversational interface


User can:


Ask plant care questions


Request care plan suggestions


Adjust reminders via natural language (“Remind me every 5 days”)


Actions:


AI responds dynamically


Save schedule/journal updates directly from chat



Reminders
Reminders Screen


Shows upcoming tasks (e.g., “Water Monstera today”)


Actions:


Mark task complete


Snooze / reschedule


Add custom reminder



Profile
Profile Settings


Update email, username, timezone


Notification preferences (push vs in-app)


Logout



🌿 UI Component Breakdown
Shared Components


Navbar / Tab Navigation


PlantCard (image + nickname + reminder badge)


ReminderItem (task list row)


JournalEntryCard (photo + note + date)


AIChatBubble (user/AI messages)


ExportButton (PDF/CSV generation)


Screen-Specific


LandingScreen


RegisterScreen


LoginScreen


PlantDashboardScreen


PlantDetailScreen


AddPlantScreen


ReminderScreen


AIChatScreen


ProfileScreen


VISUALED FLOW CHART



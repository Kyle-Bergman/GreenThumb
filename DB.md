🌿 Core Entities
1. Users
Holds account information.
user_id (PK)


name


email (unique)


password_hash


created_at


updated_at



2. Plants
Each plant belongs to a user’s collection.
plant_id (PK)


user_id (FK → Users)


species_name (scientific name, e.g., Monstera deliciosa)


nickname (user-chosen, e.g., “Leafy Boi”)


acquired_date


location (e.g., “living room”)


notes (general info)


created_at


updated_at



3. Plant Care Logs (Journal Entries)
Track plant growth, issues, or updates.
log_id (PK)


plant_id (FK → Plants)


entry_date


log_type (enum: watering, fertilizing, pruning, repotting, observation, etc.)


description


photo_id (optional FK → Photos)


created_at



4. Photos
To document plant growth visually.
photo_id (PK)


plant_id (FK → Plants)


file_url (stored in cloud/local storage)


caption (optional)


uploaded_at



5. Reminders / Schedules
Care reminders for watering, fertilizing, etc.
reminder_id (PK)


plant_id (FK → Plants)


reminder_type (enum: watering, fertilizing, pruning, etc.)


interval_days (e.g., every 7 days)


last_completed_date


next_due_date (calculated)


active (boolean)


created_at



6. AI Assistant Interactions
Optional, but adds value for your “AI plant guide.”
interaction_id (PK)


user_id (FK → Users)


plant_id (nullable, FK → Plants if context-specific)


question


response


timestamp



🌱 Relationships
Users → Plants = One-to-Many (a user owns many plants)


Plants → Logs = One-to-Many (each plant has multiple care logs)


Plants → Photos = One-to-Many (growth documentation)


Plants → Reminders = One-to-Many (care schedules)


Users → AI Interactions = One-to-Many (chat history with assistant)


🌿 MongoDB Collection Design for GreenThumb
1. Users
Top-level collection for accounts.
{
  "_id": ObjectId,
  "name": "Kyle",
  "email": "kyle@example.com",
  "password_hash": "hashed_password",
  "created_at": ISODate(),
  "updated_at": ISODate()
}


2. Plants
Each plant a user owns.
{
  "_id": ObjectId,
  "user_id": ObjectId("..."),  // Reference to Users
  "species_name": "Monstera deliciosa",
  "nickname": "Leafy Boi",
  "acquired_date": ISODate("2025-05-15"),
  "location": "Living Room",
  "notes": "Thriving near east window",
  "created_at": ISODate(),
  "updated_at": ISODate()
}


3. PlantLogs (Journal)
Track watering, fertilizing, observations, etc.
{
  "_id": ObjectId,
  "plant_id": ObjectId("..."),  // Reference to Plants
  "entry_date": ISODate("2025-09-10"),
  "log_type": "watering",  // watering, fertilizing, pruning, observation
  "description": "Watered thoroughly until soil drained.",
  "photo_id": ObjectId("..."),  // Optional reference to Photos
  "created_at": ISODate()
}


4. Photos
Store growth documentation. (Usually reference cloud storage.)
{
  "_id": ObjectId,
  "plant_id": ObjectId("..."),  // Reference to Plants
  "file_url": "https://cloudstorage.com/photos/leafyboi1.jpg",
  "caption": "New leaf unfurled today!",
  "uploaded_at": ISODate()
}


5. Reminders
Care tasks on schedules.
{
  "_id": ObjectId,
  "plant_id": ObjectId("..."),  // Reference to Plants
  "reminder_type": "watering",  // watering, fertilizing, pruning
  "interval_days": 7,
  "last_completed_date": ISODate("2025-09-03"),
  "next_due_date": ISODate("2025-09-10"),
  "active": true,
  "created_at": ISODate()
}


6. AI_Interactions
History of Q&A with the plant assistant.
{
  "_id": ObjectId,
  "user_id": ObjectId("..."),
  "plant_id": ObjectId("..."),  // Nullable, if question is plant-specific
  "question": "Why are my monstera leaves turning yellow?",
  "response": "Likely overwatering. Check soil moisture before watering.",
  "timestamp": ISODate()
}


🌱 Design Notes
References vs Embedding:


Kept plants, logs, photos, and reminders in separate collections because they can grow large (embedding would bloat user/plant docs).


A log can optionally reference a photo instead of embedding it—gives flexibility if multiple logs use the same photo.


Query Patterns:


You’ll often query plants by user_id.


Logs, reminders, and photos will be queried by plant_id.


This makes indexing on user_id and plant_id a must.


Scalability: Works well if you later add shared plants, community features, or gamification.


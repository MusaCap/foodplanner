# 🛠 SmartMeal – Product Backlog (Windsurf Format)

## 🚀 Epic 1: User Onboarding & Profile Setup

### ✅ User Story 1.1: As a new user, I want to create an account so I can save my preferences and meal plans
- [ ] Task: Implement signup/signin page (email/password auth)
- [ ] Task: Integrate JWT or OAuth2 for session management
- [ ] Task: Store hashed passwords securely in the backend

### ✅ User Story 1.2: As a user, I want to set dietary preferences and goals so the app can personalize my meals
- [ ] Task: Create form UI to select diet type, allergies, servings, skill level, time per meal, and goals
- [ ] Task: Save preferences to user profile in the database
- [ ] Task: Validate inputs and show previews of impact on meal planning

---

## 🍽 Epic 2: Meal Planning Engine

### ✅ User Story 2.1: As a user, I want to generate a weekly meal plan based on my profile
- [ ] Task: Build backend logic to match meals with dietary preferences
- [ ] Task: Create meal plan calendar view (7-day plan)
- [ ] Task: Show calories/macros per day and per meal

### ✅ User Story 2.2: As a user, I want to swap meals in my plan if I don’t like a suggestion
- [ ] Task: Add “swap” button to each meal card
- [ ] Task: Load replacement meals from recipe DB
- [ ] Task: Recalculate nutritional values dynamically

---

## 🛒 Epic 3: Shopping List Automation

### ✅ User Story 3.1: As a user, I want to view a grocery list based on my weekly meal plan
- [ ] Task: Parse all meals and extract ingredient totals
- [ ] Task: Group list by grocery category
- [ ] Task: Create UI for viewing and checking off items

### ✅ User Story 3.2: As a user, I want to exclude items I already have in my pantry
- [ ] Task: Add pantry check before generating list
- [ ] Task: Show toggles to hide pantry items in list
- [ ] Task: Update logic to auto-calculate needed quantities only

---

## 🧂 Epic 4: Ingredient, Recipe, and Pantry Management

### ✅ User Story 4.1: As a user, I want to add, update, or remove pantry items
- [ ] Task: Create pantry manager UI
- [ ] Task: Link pantry to shopping list logic
- [ ] Task: Auto-suggest meals based on pantry inventory

### ✅ User Story 4.2: As a user, I want to browse and filter recipes by tags and nutrition
- [ ] Task: Build recipe database model
- [ ] Task: Add advanced search and filter options
- [ ] Task: Display detailed recipe instructions and ingredients

---

## 🔄 Epic 5: Sync & Collaboration

### ✅ User Story 5.1: As a user, I want to sync my grocery list with a partner
- [ ] Task: Enable real-time list sync (WebSocket or Firebase)
- [ ] Task: Add email/invite system for household sharing
- [ ] Task: Show user initials next to list edits

---

## 💡 Epic 6: AI & Smart Recommendations (Optional v2)

### ✅ User Story 6.1: As a user, I want the app to recommend meals based on my eating history and pantry
- [ ] Task: Add basic ML model for meal preference scoring
- [ ] Task: Track meal ratings and frequency
- [ ] Task: Integrate smart recommendations into meal plan generator

---

## 📱 Epic 7: Frontend UI/UX Implementation

### ✅ User Story 7.1: As a user, I want a clean, mobile-first interface that works on any device
- [ ] Task: Build responsive React (Web) and React Native (Mobile) interfaces
- [ ] Task: Implement navigation flows (tabs, menus, routing)
- [ ] Task: Design meal cards, shopping list UI, and profile dashboard

---

## 🧪 Epic 8: Testing & Deployment

### ✅ User Story 8.1: As a PM, I want to ensure the app works properly before launch
- [ ] Task: Write unit tests for backend and frontend components
- [ ] Task: Conduct integration tests (meal plan → shopping list flow)
- [ ] Task: Setup CI/CD pipelines for automated deployment

---

## 🧰 Tools and Integration
- Windsurf for agent-based development and backlog tracking
- Firebase or Supabase for auth and real-time sync
- MongoDB/PostgreSQL for structured storage
- Vercel/Netlify for frontend hosting

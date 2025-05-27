# 🧾 SmartMeal – Data Model

## 📂 Entities & Relationships

---

### 👤 User
- `id` (UUID) – Primary Key
- `name` (String)
- `email` (String, Unique)
- `password_hash` (String)
- `preferences_id` (FK → Preferences.id)
- `pantry_id` (FK → Pantry.id)
- `created_at` (Timestamp)
- `updated_at` (Timestamp)

---

### ⚙️ Preferences
- `id` (UUID) – Primary Key
- `diet_type` (Enum: omnivore, vegetarian, vegan, keto, paleo, etc.)
- `allergies` (Array[String])
- `servings` (Integer)
- `meals_per_day` (Integer)
- `calorie_goal` (Integer)
- `skill_level` (Enum: beginner, intermediate, advanced)
- `time_per_meal` (Integer, in minutes)

---

### 🥗 MealPlan
- `id` (UUID) – Primary Key
- `user_id` (FK → User.id)
- `start_date` (Date)
- `end_date` (Date)
- `meals` (Array[FK → Meal.id])
- `created_at` (Timestamp)

---

### 🍽 Meal
- `id` (UUID) – Primary Key
- `name` (String)
- `recipe_id` (FK → Recipe.id)
- `meal_type` (Enum: breakfast, lunch, dinner, snack)
- `scheduled_date` (Date)
- `user_id` (FK → User.id)

---

### 📖 Recipe
- `id` (UUID) – Primary Key
- `title` (String)
- `instructions` (Text)
- `ingredients` (Array[FK → Ingredient.id])
- `calories` (Integer)
- `macros` (JSON: { protein, carbs, fat })
- `prep_time` (Integer)
- `cook_time` (Integer)
- `tags` (Array[String])

---

### 🧂 Ingredient
- `id` (UUID) – Primary Key
- `name` (String)
- `unit` (String) – e.g., grams, cups, pieces
- `category` (Enum: Produce, Dairy, Protein, Pantry, etc.)

---

### 🛒 ShoppingList
- `id` (UUID) – Primary Key
- `user_id` (FK → User.id)
- `meal_plan_id` (FK → MealPlan.id)
- `items` (Array[FK → ShoppingItem.id])
- `status` (Enum: draft, completed)
- `created_at` (Timestamp)

---

### 🧾 ShoppingItem
- `id` (UUID) – Primary Key
- `ingredient_id` (FK → Ingredient.id)
- `quantity` (Float)
- `unit` (String)
- `checked` (Boolean)

---

### 🧺 Pantry
- `id` (UUID) – Primary Key
- `user_id` (FK → User.id)
- `items` (Array[FK → PantryItem.id])

---

### 📦 PantryItem
- `id` (UUID) – Primary Key
- `ingredient_id` (FK → Ingredient.id)
- `quantity` (Float)
- `unit` (String)
- `expiration_date` (Date, optional)

---

### 🔗 Relationships Summary

- **User → Preferences** (1:1)
- **User → MealPlans** (1:N)
- **User → Pantry** (1:1)
- **MealPlan → Meals** (1:N)
- **Meal → Recipe** (N:1)
- **Recipe → Ingredients** (M:N)
- **MealPlan → ShoppingList** (1:1)
- **ShoppingList → ShoppingItems** (1:N)
- **Pantry → PantryItems** (1:N)


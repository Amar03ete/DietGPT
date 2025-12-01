# DietGPT

DietGPT is an AI nutrition assistant that helps create personalized meal plans, recipe ideas, macronutrient estimates, and shopping lists tailored to goals and dietary constraints.

---

> **Author:** [Amar03ete](https://github.com/Amar03ete)

>**Status:** Draft


Why use DietGPT?
- Fast meal-plan drafts for different goals (weight loss, muscle gain, maintenance).
- Handles preferences and restrictions (vegan, Vegetarian allergies, intolerances).
- Outputs recipes, daily macronutrient summaries, and consolidated shopping lists.

Features (short)
- Generate multi-day meal plans
- Recipe suggestions and ingredient lists
- Basic macro and calorie estimates
- Configurable prompts and diet rules

Quick start
1. Clone the repo
   git clone https://github.com/Amar03ete/DietGPT.git
   cd DietGPT
2. Install (Node example)
   npm install
3. Create a .env file with required keys (MODEL_PROVIDER, API keys, PORT)
4. Run locally
   npm run dev


Usage examples

Command / prompt
- "Generate a 7-day vegetarian meal plan at 2000 kcal/day with breakfast, lunch, dinner, and two snacks."

Minimal API (example)
POST /api/v1/plan
Content-Type: application/json
Body:
{
  "profile": { "age": 34, "weight_kg": 68, "height_cm": 170, "activity_level": "moderate" },
  "diet": { "preference": "vegetarian", "allergies": ["peanuts"], "daily_calories": 1600 },
  "duration_days": 7
}

Response (summary)
{
  "plan_id": "abc123",
  "daily_plans": [ ... ],
  "summary": { "total_calories_per_day": 1600, "average_protein_g": 85 }
}

Configuration
- Prompts and diet rules: /prompts or /config (adjust path if different).
- Add local food composition CSV/JSON for improved nutrient accuracy.

Development & testing
- Tests: npm test or pytest (if Python parts exist)
- Run in Docker (optional): add a Dockerfile and docker-compose if you plan to containerize.
- 
---

## License

This project is licensed under the [MIT License](LICENSE).

---

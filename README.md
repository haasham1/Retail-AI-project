RetailAI Shopper Assistant
==========================

Small demo app showing OpenAI Function Calling with custom tools in JavaScript (Node.js + Express).

What it does
------------
- Product search using Fake Store API
- Cart total calculation with tax/discount
- Currency conversion using exchangerate.host

Architecture
------------
- Server: `server/index.js` exposes `/api/chat` and registers three tools.
- Tools: `server/tools/*.js` implement product search, cart calculator, currency conversion.
- UI: Minimal static page in `public/` with a chat box.

Setup
-----
1. Create `.env` from example and set your key:
```
cp .env.example .env
# set OPENAI_API_KEY in .env
```
2. Install and run:
```
npm install
npm start
```
3. Open `http://localhost:3000`.

Example prompts
---------------
- Find budget backpacks under $50 and total for 3 units with 8% tax.
- Convert the total to EUR.
- Show gaming items and compute total with 10% discount.

Notes
-----
- External APIs can fail or rate limit. The app handles errors gracefully.
- Keep prompts specific for best tool usage.


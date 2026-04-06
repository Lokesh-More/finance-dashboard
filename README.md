# Finflow — Finance Dashboard

A clean, interactive finance dashboard built with plain HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies to install.

---

## How to Run

1. Download `index.html`
2. Double-click it to open in any browser (Chrome, Firefox, Edge, Safari)
3. That's it — fully works offline

---

## Project Structure

```
finance-dashboard/
├── index.html    ← entire app (HTML + CSS + JS in one file)
└── README.md
```

---

## Features

### 1. Dashboard Overview
- **Total Balance** — net of all income minus expenses
- **Total Income** — sum of all income transactions
- **Total Expenses** — sum of all expense transactions
- **Savings Rate** — percentage of income saved
- **Balance Trend** — line chart showing cumulative balance over months
- **Spending by Category** — doughnut chart breaking down expenses
- **Income vs Expenses** — bar chart comparing month by month

### 2. Transactions
- Full table with date, description, category, type, and amount
- **Search** by name or category
- **Filter** by type (income / expense) and category
- **Sort** by date (newest/oldest) or amount (highest/lowest)
- **Add** new transactions via modal form
- **Edit** existing transactions
- **Delete** transactions with confirmation

### 3. Role-Based UI
Roles can be switched from the sidebar dropdown at any time.

| Feature | Admin | Viewer |
|---|---|---|
| View all data | ✅ | ✅ |
| Add transaction | ✅ | ❌ |
| Edit transaction | ✅ | ❌ |
| Delete transaction | ✅ | ❌ |

No backend or authentication — roles are simulated on the frontend for demonstration.

### 4. Insights
- **Top spending category** — highest expense category
- **Month-over-month** — expense change vs previous month
- **Savings rate** — with target indicator (30% threshold)
- **Category bar chart** — visual ranking of all expense categories
- **Month comparison chart** — current vs previous month (income, expenses, net)
- **Summary stats** — total transactions, average monthly expense, highest income/expense

### 5. State Management
All state is managed in plain JavaScript:
- `transactions` array — single source of truth for all data
- Role state — controls UI permissions
- Filter state — search, type, category, sort values
- Charts are rebuilt on page switch using current data

---

## Design Decisions

- **Single file** — keeps submission simple and easy to evaluate
- **No framework** — demonstrates core JS skills without abstraction
- **Chart.js via CDN** — only external dependency, loaded from Cloudflare CDN
- **Google Fonts via CDN** — DM Sans + DM Mono for clean typography
- **Dark mode** — auto-detects system preference via `prefers-color-scheme`
- **Responsive** — works on mobile, tablet, and desktop
- **Mock data** — 23 pre-loaded transactions across 3 months (Feb–Apr 2026)

---

## Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Structure |
| CSS3 | Styling, layout, responsive design, dark mode |
| Vanilla JavaScript | All logic, state, interactions |
| Chart.js 4.4.1 | Line, bar, and doughnut charts |
| Google Fonts | DM Sans, DM Mono |

---

## Assumptions Made

- Mock data is pre-loaded; no backend or API is connected
- Role switching is for UI demonstration only — not authenticated
- "Savings Rate" is calculated as `(income - expenses) / income × 100`
- Dark mode follows the user's OS/browser setting automatically

---

## Author

Built as a frontend evaluation assignment.

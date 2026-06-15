# HabitFlow v5.2 — Single-File Habit Tracker

HabitFlow is a lightweight, premium, single-file HTML habit tracker. It is built entirely with vanilla JavaScript, modern CSS variables, and utilizes `localStorage` for data persistence.

---

## 🌟 Key Features

### 1. Simplified Dashboard
* **Focused View**: Features a distraction-free daily page detailing the current weekday, calendar date, day-of-year badge, and a rotation of motivational quotes.
* **Streamlined Flow**: All interactive habit tracking moves to the dedicated Weekly and Monthly screens.

### 2. Category Organization
* **Flexible Categories**: Create, customize, and delete categories (e.g., "Health & Fitness", "Productivity", "Learning", "Personal") from the Manage screen.
* **Category Grouping**: Habits are automatically grouped under clean, color-coded category headers in both the **Weekly Tracker** and the **Manage List**.

### 3. Priority Reordering
* **Custom Order**: Sort habits within their category using Up (▲) and Down (▼) arrow controls on the Manage screen.
* **Array-Level Persistence**: Reordering updates the underlying data array instantly and syncs across all screens.

### 4. Direct Weekly Count Popover
* **Quick Log**: Status cells in the Weekly tracker feature a green dropdown trigger arrow on the right.
* **Count Editor**: Click to open a quick number popover, input your count (e.g., 8 glasses of water), and press Enter or click **Set** to save.

### 5. Strict Start Date & Locked Past Days
* **No Backdating**: When adding a habit, a preview panel appears allowing you to edit the details. Once confirmed, the start date (`createdAt`) is set strictly to today.
* **Safe Tracking**: Calendar cells, notes, and status toggles for days prior to a habit's creation are visually locked and disabled, and protected by programmatic state guards.
* **Fair Stats**: Habit success rates dynamically ignore locked days before a habit's creation, ensuring newly added habits do not penalize your historical success metrics.

### 6. Interactive Weekly Note Toggling
* **Click-to-Select**: Click any active cell once to select it and focus the note editor below. You can view or add notes *without* cycling the completed status of the cell.
* **Subsequent Cycling**: Clicking a cell that is already selected cycles its status (Open ➔ In Progress ➔ Done ➔ Failed).
* **Confirmations**: Press **Enter** in the note editor to save. A confirmation toast details the habit name and formatted date.

### 7. Enhanced Stats, Infographics & Milestones
* **Category Progress**: Visual grid of cards detailing monthly category completion rates using category-colored progress bars.
* **Completion Infographic**: A clean monthly success bar chart detailing individual habit success rates.
* **Achievement Milestones**: Unlocked cards highlighting consistency milestones (Consistency Spark, Habit Builder, Unstoppable Force, Habit Master).
* **Smart Unlock Pacing**: An animated forecasting alert tells you exactly which habit is closest to unlocking its next achievement and how many more streak days are needed.

---

## 🛠️ Tech Stack & Architecture

* **Core**: Single-file HTML5, Semantic DOM.
* **Styling**: Vanilla CSS utilizing modern variables, CSS grid layouts, and smooth animations.
* **Logic**: Vanilla ES6 JavaScript (no external libraries, frameworks, or bundlers).
* **Persistence**: Persisted locally via `localStorage` (Habit state: `habit-heatmap-tracker-v1`, Metadata: `habit-heatmap-tracker-meta-v1`).
* **Portability**: Support for full data export/import as JSON files in the Manage screen.

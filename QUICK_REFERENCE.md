# Quick Reference Cheat Sheet

## 🎯 Project Summary
**Habit Tracker** - Full-stack web app for tracking daily habits with streak counting

---

## 📋 Tech Stack (One Line Each)

| Technology | Purpose |
|------------|---------|
| **React** | UI library for building components |
| **Vite** | Fast build tool and dev server |
| **React Router** | Client-side routing/navigation |
| **Axios** | HTTP client for API calls |
| **Tailwind CSS** | Utility-first CSS framework |
| **JSON Server** | Mock REST API from JSON file |
| **React Toastify** | Notification messages |
| **Lucide React** | Icon library |

---

## 🗂️ File Structure

```
backend/
  └── db.json              # Database file

frontend/
  ├── src/
  │   ├── main.jsx        # Entry point
  │   ├── App.jsx         # Router setup
  │   ├── components/     # Reusable components
  │   ├── pages/          # Route components
  │   └── services/       # API calls
  └── package.json        # Dependencies
```

---

## 🔑 Key React Concepts

### useState
```jsx
const [value, setValue] = useState(initialValue);
```
- Manages component state
- Returns [currentValue, setterFunction]
- Updates trigger re-render

### useEffect
```jsx
useEffect(() => {
  // Side effects here
}, [dependencies]);
```
- Runs after render
- Empty [] = run once on mount
- [dep] = run when dependency changes

### Props
```jsx
<Component propName={value} />
```
- Data passed from parent to child
- Read-only in child
- One-way data flow

---

## 🔄 Data Flow

```
User Action
    ↓
Event Handler
    ↓
API Call (Axios)
    ↓
Backend (JSON Server)
    ↓
Database (db.json)
    ↓
Response
    ↓
Update State (setState)
    ↓
Re-render UI
```

---

## 🛣️ Routes

| Path | Component | Purpose |
|------|-----------|---------|
| `/` | HomePage | List all habits |
| `/add` | AddHabitPage | Create new habit |
| `/edit/:id` | EditHabitPage | Edit habit |
| `/details/:id` | HabitDetailsPage | View details |

---

## 🔌 API Endpoints

| Method | URL | Purpose |
|--------|-----|---------|
| GET | `/habits` | Get all habits |
| GET | `/habits/:id` | Get one habit |
| POST | `/habits` | Create habit |
| PUT | `/habits/:id` | Update habit |
| DELETE | `/habits/:id` | Delete habit |

---

## 💾 Habit Data Structure

```javascript
{
  id: "1",
  name: "Morning Exercise",
  category: "Health",
  frequency: "Daily",
  targetCount: 30,
  currentStreak: 6,
  completionDates: ["2024-11-25", "2024-11-26"],
  lastCompleted: "2024-11-26"
}
```

---

## 🎯 Important Functions

### Fetch Habits
```javascript
habitAPI.getAllHabits()  // GET /habits
```

### Create Habit
```javascript
habitAPI.createHabit(habitData)  // POST /habits
```

### Update Habit
```javascript
habitAPI.updateHabit(id, habitData)  // PUT /habits/:id
```

### Mark Done
```javascript
habitAPI.markHabitDone(id, habit)  // PUT /habits/:id
```

### Delete Habit
```javascript
habitAPI.deleteHabit(id)  // DELETE /habits/:id
```

---

## 🎨 Component Hierarchy

```
App
├── Navigation (always visible)
└── Routes
    ├── HomePage
    │   └── HabitCard (multiple)
    ├── AddHabitPage
    │   └── HabitForm
    ├── EditHabitPage
    │   └── HabitForm
    └── HabitDetailsPage
```

---

## ⚡ Quick Answers to Common Questions

**Q: What is React?**
- JavaScript library for building UI components

**Q: What is state?**
- Data that can change, stored in component

**Q: What are props?**
- Data passed from parent to child component

**Q: What is useEffect?**
- Hook to run side effects (API calls) after render

**Q: What is routing?**
- Navigation between pages without reload

**Q: How does data flow?**
- User → Component → API → Backend → State → UI

**Q: What is Axios?**
- Library for making HTTP requests

**Q: What is JSON Server?**
- Mock backend that creates API from JSON file

**Q: What is Tailwind?**
- CSS framework using utility classes

**Q: What is JSX?**
- HTML-like syntax in JavaScript

---

## 🚀 Commands

```bash
# Start backend
json-server --watch backend/db.json --port 3001

# Start frontend
cd frontend
npm install
npm run dev

# Build for production
npm run build
```

---

## 📝 Key Terms

- **Component**: Reusable UI piece
- **Hook**: Function that lets you use React features
- **State**: Component's data storage
- **Props**: Parent-to-child data passing
- **Rendering**: Displaying component on screen
- **Re-render**: Update UI when state changes
- **Event Handler**: Function called on user action
- **API**: Application Programming Interface
- **REST**: API design pattern (GET/POST/PUT/DELETE)
- **Async**: Operations that take time (API calls)
- **Promise**: Represents future value (async result)
- **CRUD**: Create, Read, Update, Delete operations

---

## 🎓 Study Checklist

- [ ] Understand what React is
- [ ] Know difference between state and props
- [ ] Understand useEffect and useState
- [ ] Know how routing works
- [ ] Understand API calls with Axios
- [ ] Know component structure
- [ ] Understand data flow
- [ ] Know how to explain project flow
- [ ] Understand backend (JSON Server)
- [ ] Know file structure and organization

---

**Print this and keep it handy! 📄**



# Habit flow Application

A full-stack web application for tracking daily habits with streak counting and progress monitoring.

## 🚀 Features

- ✅ Create, read, update, and delete habits
- 📊 Track daily progress with streak counting
- 🎯 Set targets and monitor completion
- 📅 View completion history
- 🎨 Modern and responsive UI
- 🔔 Toast notifications for user feedback

## 🛠️ Technology Stack

### Frontend
- **React 18** - UI library
- **Vite** - Build tool and dev server
- **React Router DOM** - Client-side routing
- **Axios** - HTTP client
- **Tailwind CSS** - Styling framework
- **React Toastify** - Notifications
- **Lucide React** - Icons

### Backend
- **JSON Server** - Mock REST API

## 📁 Project Structure

```
FSD PROJECT/
├── backend/
│   └── db.json          # Database file
├── frontend/
│   ├── src/
│   │   ├── components/  # Reusable components
│   │   ├── pages/       # Route components
│   │   └── services/    # API service layer
│   └── package.json
└── README.md
```

## 🚦 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm (comes with Node.js)

### Installation & Setup

1. **Clone or navigate to the project directory**

2. **Setup Backend (Terminal 1)**

```bash
# Install json-server globally (if not already installed)
npm install -g json-server

# Start JSON server
json-server --watch backend/db.json --port 3001
```

The backend API will be available at `http://localhost:3001`

3. **Setup Frontend (Terminal 2)**

```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev
```

The frontend will be available at `http://localhost:5173` (or port shown in terminal)

## 📚 Available Scripts

### Frontend

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

### Backend

- `json-server --watch backend/db.json --port 3001` - Start JSON server

## 🌐 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/habits` | Get all habits |
| GET | `/habits/:id` | Get single habit |
| POST | `/habits` | Create new habit |
| PUT | `/habits/:id` | Update habit |
| DELETE | `/habits/:id` | Delete habit |

## 📖 Usage

1. **View All Habits**: Navigate to home page (`/`)
2. **Add Habit**: Click "Add Habit" button or navigate to `/add`
3. **Edit Habit**: Click edit icon on any habit card
4. **View Details**: Click eye icon on any habit card
5. **Mark Done**: Click "Mark Done" button (once per day)
6. **Delete Habit**: Click delete icon and confirm

## 🎯 Key Features Explained

### Streak Tracking
- Automatically increments when habit is marked as done
- Tracks consecutive days of completion
- Resets if a day is missed

### Progress Monitoring
- Visual progress bar showing completion percentage
- Target count vs current streak
- Completion dates history

### Categories
- Health
- Study
- Work
- Mindfulness
- Personal
- Finance

## 📝 Data Model

### Habit Object

```json
{
  "id": "1",
  "name": "Morning Exercise",
  "category": "Health",
  "frequency": "Daily",
  "targetCount": 30,
  "currentStreak": 6,
  "completionDates": ["2024-11-25", "2024-11-26"],
  "lastCompleted": "2024-11-26"
}
```

## 🎓 Learning Resources

This project includes comprehensive viva preparation materials:

- `VIVA_PREPARATION_GUIDE.md` - Complete guide from basics to advanced
- `VIVA_QUESTIONS_ANSWERS.md` - Q&A format for common questions
- `QUICK_REFERENCE.md` - Quick cheat sheet
- `VISUAL_FLOW_DIAGRAM.md` - Visual flow diagrams

## 🔧 Development

### Project Architecture

- **Component-Based**: Reusable React components
- **Service Layer**: Centralized API calls
- **State Management**: React hooks (useState, useEffect)
- **Routing**: Client-side routing with React Router

### Code Structure

- Components are in `src/components/`
- Pages are in `src/pages/`
- API services are in `src/services/`
- All API calls use Axios from service layer

## 🚀 Future Enhancements

- [ ] User authentication
- [ ] Real database (MongoDB/PostgreSQL)
- [ ] Search and filter functionality
- [ ] Charts and analytics
- [ ] Mobile app version
- [ ] Offline support
- [ ] Unit tests
- [ ] Dark mode

## 📄 License

This project is for educational purposes.

## 👨‍💻 Author

Developed as a Full-Stack Development (FSD) project.

---

**Happy Habit Tracking! 📈**




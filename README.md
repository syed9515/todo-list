# ✨ ProTask - Ultimate Task Manager

A modern, feature-rich task management application built with vanilla HTML, CSS, and JavaScript. Manage your daily tasks, set priorities, organize by categories, and track your productivity with style!

## 🌟 Features

### Core Task Management
- ✅ **Add Tasks** - Create new tasks with custom priority levels and categories
- ✅ **Mark Complete** - Track task progress with completion status
- ✅ **Star Favorites** - Mark important tasks as favorites for quick access
- ✅ **Edit Tasks** - Modify existing tasks with an intuitive modal interface
- ✅ **Delete Tasks** - Remove completed or unnecessary tasks
- ✅ **Undo Actions** - Restore completed tasks back to active status

### Advanced Features
- 📋 **Checklist Support** - Break down tasks into subtasks with completion tracking
- 🎯 **Priority Levels** - Organize tasks by High, Medium, and Low priority
- 📂 **Categories** - Sort tasks into Work, Personal, Shopping, and Health categories
- 🔍 **Real-time Search** - Instantly filter tasks by keyword
- 📊 **Statistics Dashboard** - View total, active, starred, and completed task counts
- 📈 **Progress Tracking** - Visual progress bar showing completion percentage
- 🌙 **Dark Mode** - Easy on the eyes with beautiful dark theme toggle
- 💾 **Auto-Save** - Persist all data locally using browser localStorage

### UI/UX
- 📱 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- ✨ **Smooth Animations** - Engaging visual feedback with CSS animations
- 🎨 **Glassmorphism Design** - Modern aesthetic with backdrop blur effects
- 🔔 **Toast Notifications** - Real-time feedback for user actions

## 🚀 Quick Start

### Installation
1. Clone or download this repository
2. Open `index.html` in your web browser
3. Start managing your tasks!

No server or installation required - everything runs in your browser!

### Basic Usage

#### Adding a Task
1. Type your task in the input field at the top
2. Select priority level (Low, Medium, High) - defaults to Medium
3. Select category (All, Work, Personal, Shopping, Health)
4. Click "➕ Add Task" or press Enter

#### Managing Tasks
- **Complete Task**: Click "✓ Done" to mark as complete, click "↩️ Undo" to revert
- **Star Task**: Click "☆" to favorite, ⭐ to unfavorite
- **Edit Task**: Click "✏️ Edit" to modify task details
- **Add Checklist**: Click "✓ Checklist" to add subtasks
- **Delete Task**: Click "🗑️" to remove permanently

#### Filtering & Organizing
- **Priority Filters**: Click High/Medium/Low in sidebar to filter by priority
- **Category Filter**: Click Work/Personal/Shopping/Health to view specific categories
- **View Switcher**: Use navbar buttons (requires screen width > 1024px)
  - 📋 **All Tasks** - View all tasks
  - 📅 **Today** - See today's tasks only
  - ⭐ **Starred** - View favorite tasks
  - ✅ **Completed** - See finished tasks
- **Status Filters**: Use All/Active/Done/Overdue buttons below input
- **Search**: Click 🔍 to open search box and filter by keywords

#### Appearance
- **Dark Mode**: Click 🌙 in navbar to toggle dark/light theme
- **Settings**: Click ⚙️ for additional options

## 🛠️ Technical Details

### Technology Stack
- **HTML5** - Semantic markup structure
- **CSS3** - Modern styling with Flexbox, Grid, and Animations
- **JavaScript (Vanilla)** - No frameworks or dependencies
- **Google Fonts** - Poppins font family (weights 300-800)

### Architecture

#### Data Structure
```javascript
{
  id: timestamp,
  text: string,
  completed: boolean,
  starred: boolean,
  priority: 'low' | 'medium' | 'high',
  category: 'work' | 'personal' | 'shopping' | 'health' | '',
  dueDate: string (ISO format),
  notes: string,
  checklist: [{ text: string, completed: boolean }],
  createdAt: ISO8601 timestamp
}
```

#### Storage
- All data is stored in browser's `localStorage`
- Automatically saved after each action
- Data persists across browser sessions

#### Key Functions
- `addTodo()` - Create new task with full properties
- `toggleComplete(id)` - Mark task complete/incomplete
- `toggleStar(id)` - Favorite/unfavorite task
- `deleteTodo(id)` - Remove task permanently
- `openEditModal(id)` / `saveEdit()` - Edit task workflow
- `openChecklistModal(id)` / `saveChecklist()` - Manage subtasks
- `filterByCategory(cat)` - Filter tasks by category
- `filterByPriority(pri)` - Filter tasks by priority
- `switchView(view)` - Change display view (Today, Starred, etc.)
- `render()` - Update UI with current task list
- `toggleTheme()` - Switch between light/dark modes

### CSS Classes
- `.navbar` - Fixed top navigation bar
- `.sidebar` - Left sidebar with filters
- `.content` - Main content area
- `.todo-item` - Individual task card
- `.modal` - Pop-up windows for editing/checklists
- `.dark-mode` - Dark theme styling

### Animations
- `fadeIn` - Fade in with slide up
- `slideIn` - Slide in from left
- `scaleIn` - Scale up entrance
- `bounce` - Bouncing effect
- `pulse` - Pulsing scale effect
- `slideUp` - Slide up entrance
- `slideRight` - Slide right entrance

## 🎨 Design Features

### Color Scheme (Light Mode)
- Primary Gradient: Purple to Violet (#667eea → #764ba2)
- Background: Light white (#f5f5f5)
- Text: Dark gray (#333)
- Accent: Vibrant gradients

### Color Scheme (Dark Mode)
- Background: Dark navy (#0f0f1e → #1a1a3e)
- Cards: Dark slate
- Text: Light gray
- Accent: Same vibrant gradients

### Responsive Breakpoints
- Desktop: > 1024px (full features)
- Tablet: 768px - 1024px (adjusted layout)
- Mobile: < 768px (optimized for touch)

## 📋 Feature Matrix

| Feature | Status | Platform |
|---------|--------|----------|
| Add Task | ✅ | All |
| Complete Task | ✅ | All |
| Star Task | ✅ | All |
| Edit Task | ✅ | All |
| Delete Task | ✅ | All |
| Checklist | ✅ | All |
| Search | ✅ | All |
| Priority Filter | ✅ | All |
| Category Filter | ✅ | All |
| View Switcher | ✅ | Desktop (>1024px) |
| Status Filters | ✅ | All |
| Dark Mode | ✅ | All |
| Progress Bar | ✅ | All |
| Statistics | ✅ | All |
| Toast Alerts | ✅ | All |
| Data Persistence | ✅ | All |

## 🌐 Browser Compatibility

- ✅ Chrome/Chromium (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 💾 Data & Privacy

- **Local Storage Only**: All data is stored locally in your browser
- **No Server Communication**: Never sends data to external servers
- **Privacy**: Your tasks are completely private
- **Backup**: Export data by checking browser DevTools > Application > localStorage
- **Clear Data**: Browser cache/cookies clearing will reset the application

## 🎯 Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Add Task | Enter (in task input) |
| Close Modal | Escape |
| Search | Click 🔍 or Ctrl+K (future) |

## 📸 Screenshots

### Light Mode
- Clean, professional interface with purple gradient
- Easy-to-read task cards with status indicators
- Organized sidebar with filtering options

### Dark Mode
- Eye-friendly dark theme for night usage
- Maintains all functionality and features
- Smooth transition animation

## 🔧 Customization

### Changing Colors
Edit the CSS variables in the `<style>` section:
- `background: linear-gradient(135deg, #667eea 0%, #764ba2 100%)` - Change gradient colors
- `body.dark-mode` - Adjust dark mode background

### Modifying Priorities
Edit the priority options in the dropdown near line 1268

### Adding Categories
Add new categories in:
1. Sidebar section (HTML)
2. Category dropdown
3. Filter function in JavaScript

## 🚀 Future Enhancements

Potential features for future versions:
- 📅 Due date reminders
- 👥 Task sharing capabilities
- 🔄 Cloud sync
- 📊 Advanced analytics
- 🏷️ Custom tags
- ⏱️ Time tracking
- 📱 Mobile app version
- 🌍 Multi-language support

## 📝 Notes

- Tasks are stored in browser localStorage automatically
- Clearing browser data will reset all tasks
- For multiple devices, consider implementing cloud sync
- The application requires JavaScript to be enabled

## 📄 License

This project is open source and available for personal and commercial use.

## 🙏 Acknowledgments

- Built with vanilla JavaScript (no frameworks)
- Inspired by modern productivity tools
- Designed with user experience in mind

## 💬 Feedback & Support

Found a bug or have a suggestion? 
- Check the existing features thoroughly
- Ensure your browser is up to date
- Try clearing browser cache if experiencing issues
- Consider adjusting your browser window size if navbar buttons aren't visible

---

**Made with ❤️ for productivity lovers everywhere** ✨

Happy task managing! 🚀


#                        THE END

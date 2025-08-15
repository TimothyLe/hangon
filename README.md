# hangon
A scratch pad for your tasks and math calculations

## **📁 How to Use `tasks.json`:**

**Method 1: Browser Developer Console**
1. Open the HTML file in your browser
2. Press `F12` to open developer tools
3. Go to the "Console" tab
4. Copy and paste this code:

```javascript
// Load the example tasks
const exampleTasks = [
  {
    "id": 1,
    "text": "Review quarterly budget report",
    "completed": false,
    "createdAt": "2025-08-14T10:30:00.000Z"
  },
  {
    "id": 2,
    "text": "Call dentist to schedule appointment",
    "completed": true,
    "createdAt": "2025-08-13T14:15:00.000Z",
    "completedAt": "2025-08-14T09:20:00.000Z"
  }
  // ... add more tasks as needed
];

localStorage.setItem('todoTasks', JSON.stringify(exampleTasks));
localStorage.setItem('taskIdCounter', '8');
location.reload(); // Refresh the page to see the tasks
```

**Method 2: Manual Entry**
Just start using the app - add your own tasks and they'll persist automatically!

### **🔧 Storage Management:**

To clear all stored tasks (if needed):
```javascript
localStorage.removeItem('todoTasks');
localStorage.removeItem('taskIdCounter');
location.reload();
```

### **📍 Important Notes:**
- **Works with file:// protocol**: Save the HTML file and open it directly
- **Domain-specific**: Tasks are tied to the specific location/domain
- **Browser-specific**: Chrome tasks won't appear in Firefox, etc.
- **Automatic**: No manual save/load buttons needed


## Key Features

### **🔄 Automatic Persistence:**
- **Auto-save**: Tasks automatically save to localStorage when you add, complete, or remove them
- **Auto-load**: Tasks automatically load when you open the page
- **Console logging**: Check browser dev tools to see save/load confirmations

### **💾 Enhanced Data Structure:**
- Each task now includes `createdAt` timestamp
- Completed tasks get a `completedAt` timestamp
- Unique ID counter persists across sessions


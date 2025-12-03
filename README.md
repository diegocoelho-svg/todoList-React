# ✅ TodoList React

A modern, feature-rich Todo List application built with React, TypeScript, and Tailwind CSS. This application provides an intuitive interface for managing tasks with local storage persistence, allowing users to create, edit, delete, and track their tasks efficiently.

## 🎯 Overview

TodoList React is a single-page application that enables users to manage their daily tasks effectively. The application features a clean, modern UI with smooth interactions, loading states, and persistent data storage using browser local storage. Tasks can be created, edited, marked as completed, and deleted with real-time updates to the task summary.

## ✨ Features

- **Task Management**
  - Create new tasks with a single click
  - Edit existing tasks inline
  - Delete tasks with confirmation
  - Mark tasks as completed/concluded
  - Visual feedback for completed tasks (strikethrough)

- **Task Summary**
  - Real-time count of created tasks
  - Display of completed tasks vs total tasks
  - Dynamic badge updates

- **User Experience**
  - Loading states with skeleton components
  - Smooth animations and transitions
  - Responsive design for mobile and desktop
  - Inline editing with form validation
  - Optimistic UI updates

- **Data Persistence**
  - Automatic saving to browser local storage
  - Data persists across browser sessions
  - No backend required

- **Component Architecture**
  - Reusable UI components
  - Custom hooks for state management
  - Type-safe with TypeScript
  - Modular and maintainable code structure

## 🛠 Technologies Used

### Core Technologies
- **React** (v19.2.0) - UI library
- **TypeScript** (v5.9.3) - Type safety and enhanced developer experience
- **Vite** (v7.2.4) - Fast build tool and development server
- **React Router** (v7.9.6) - Client-side routing

### Styling & UI
- **Tailwind CSS** (v4.1.17) - Utility-first CSS framework
- **class-variance-authority** (v0.7.1) - Component variant management

### State Management & Persistence
- **use-local-storage** (v3.0.0) - Local storage hook for data persistence

### Development Tools
- **ESLint** (v9.39.1) - Code linting
- **TypeScript ESLint** (v8.46.4) - TypeScript-specific linting rules
- **@vitejs/plugin-react-swc** (v4.2.2) - Fast React refresh with SWC
- **vite-plugin-svgr** (v4.5.0) - SVG as React components

## 📁 Project Structure

```
todolist-react/
├── public/                 # Static assets
├── src/
│   ├── assets/            # Images and icons
│   │   ├── icons/         # SVG icons
│   │   └── images/        # Image assets (Logo)
│   ├── components/        # Reusable UI components
│   │   ├── badge.tsx
│   │   ├── button.tsx
│   │   ├── button-icon.tsx
│   │   ├── card.tsx
│   │   ├── container.tsx
│   │   ├── icon.tsx
│   │   ├── input-checkbox.tsx
│   │   ├── input-text.tsx
│   │   ├── skeleton.tsx
│   │   └── text.tsx
│   ├── core-components/   # Feature-specific components
│   │   ├── footer.tsx
│   │   ├── header.tsx
│   │   ├── main-content.tsx
│   │   ├── task-item.tsx
│   │   ├── tasks-list.tsx
│   │   └── tasks-summary.tsx
│   ├── helpers/           # Utility functions
│   │   └── utils.ts
│   ├── hooks/             # Custom React hooks
│   │   ├── use-task.ts    # Task CRUD operations
│   │   └── use-tasks.ts   # Tasks list and summary
│   ├── models/            # TypeScript types and interfaces
│   │   └── task.ts
│   ├── pages/             # Route pages
│   │   ├── layout-main.tsx
│   │   ├── page-components.tsx
│   │   └── page-home.tsx
│   ├── App.tsx            # Main app component with routing
│   ├── main.tsx           # Application entry point
│   └── index.css          # Global styles
├── index.html             # HTML template
├── package.json           # Dependencies and scripts
├── tsconfig.json          # TypeScript configuration
├── vite.config.ts         # Vite configuration
└── eslint.config.js       # ESLint configuration
```

## 🚀 Installation

### Prerequisites

- **Node.js** (v18 or higher recommended)
- **pnpm** (package manager) - The project uses `pnpm-lock.yaml`, indicating pnpm is the preferred package manager

### Steps

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd todoList-React
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   ```
   
   Alternatively, if you prefer npm or yarn:
   ```bash
   npm install
   # or
   yarn install
   ```


## 📝 Project Details

### Task Model

Tasks are defined with the following structure:

```typescript
interface Task {
  id: string;
  title: string;
  concluded?: boolean;
  state?: TaskState;
}
```

### Task States

- `Creating` - Task is being created (editing mode)
- `Created` - Task has been saved

### Local Storage

Tasks are stored in browser local storage under the key `"tasks"`. The data persists across browser sessions and page refreshes.

### Custom Hooks

- **`useTasks`**: Manages the tasks list, loading state, and provides counts for created and concluded tasks
- **`useTask`**: Handles individual task operations (create, update, delete, toggle status)

### Routing

The application uses React Router with the following routes:
- `/` - Home page (main todo list interface)
- `/componentes` - Components showcase page

### Code Style

- Follow TypeScript best practices
- Use functional components with hooks
- Maintain component modularity
- Write clear and descriptive variable/function names
- Add comments for complex logic

## 📄 License

This project is private and not licensed for public use. All rights reserved.

## 👤 Author

This project was created as part of a React learning journey with Rocketseat.

---

**Note**: This is a frontend-only application. All data is stored locally in the browser's local storage. No backend server or database is required.

# **React.js Assessment – Build a Settings Page Like PocketBase**

## **📌 Overview**  
This assessment evaluates your **React.js skills** by having you build a **settings page** similar to the one in **PocketBase**. The goal is to test your ability to:  
✅ Use **React 19** with **Vite** for modern web development.  
✅ Implement a **sidebar-based settings UI** with **React Router v7**.  
✅ Apply **Tailwind CSS** for clean, efficient, and responsive styling.  
✅ Manage **state and data efficiently**, including **localStorage persistence**.  
✅ Write **modular, reusable, and maintainable components**.  
✅ Work with **Git**, including branching, committing, and submitting a **Pull Request (PR)**.  

---

## **🎯 Reference: PocketBase Demo**  
You should design the settings page to resemble **PocketBase’s admin settings page**.  

### **How to Access the Demo**  
1️⃣ Open the **[PocketBase Demo](https://demo.pocketbase.io/_/)** in your browser.  
2️⃣ Login with the demo credentials:  
   - **Email**: `admin@demo.com`  
   - **Password**: `admin123`  
3️⃣ Navigate to the **"Settings"** section in the sidebar.  
4️⃣ Observe how the **sidebar navigation, forms, and layout** work.  

Your task is to **replicate a similar layout and behavior** in React.js.  

---

## **📖 Instructions for the Candidate**  

### **1️⃣ Setup Your Development Environment**  
- Ensure you have **Node.js 18+** installed.  
- Use **Vite** as the project setup tool.  
- Install and configure **React Router v7** for client-side navigation.  
- Install **Tailwind CSS** for styling.  

### **2️⃣ Fork, Clone, and Create a Branch**  
1️⃣ **Fork this repository** to your own GitHub account.  
2️⃣ **Clone your forked repository** to your local machine:  
   ```sh
   git clone https://github.com/YOUR_USERNAME/react-settings-dashboard-assessment.git
   ```  
3️⃣ **Navigate to the project directory**:  
   ```sh
   cd assessment-repo
   ```  
4️⃣ **Create a new branch**:  
   ```sh
   git checkout -b your-name-assessment
   ```  

### **3️⃣ Implement the Settings Page**  

#### **🖥 Required Features**  

1. **Create a Sidebar Navigation** (like PocketBase)  
   - Sidebar should contain **General, Profile, Account, and Security** sections.  
   - Clicking a section should update the URL **without a full page reload**.  

2. **Implement the Settings Page Layout**  
   - Display settings content in a **main content area** when a section is selected.  
   - Use **React Router v7** for navigation.  

3. **Use Tailwind CSS for Styling**  
   - Ensure the layout is **clean, modern, and responsive**.  
   - The sidebar should collapse on smaller screens.  

4. **Fetch and Store User Settings**  
   - Load settings data from a **mock JSON file**.  
   - Implement **localStorage persistence** so settings are retained after page refresh.  

5. **Allow Settings Updates**  
   - Implement **form inputs** for updating settings (e.g., username, email, 2FA toggle).  
   - Store updates in **localStorage** and reflect changes in the UI.  

---

### **4️⃣ Commit Your Changes Frequently**  
💡 **Tip**: Make multiple commits as you progress!  

```sh
git add .
git commit -m "Implemented sidebar navigation"
```  

### **5️⃣ Push Your Changes and Submit a Pull Request**  
1️⃣ Push your branch to GitHub:  
   ```sh
   git push origin your-name-assessment
   ```  
2️⃣ Go to the repository on GitHub and **create a Pull Request** (PR).  
3️⃣ Add a **clear PR description**, explaining your implementation.  
4️⃣ Wait for feedback and make improvements if needed.  

---

## **📌 Evaluation Criteria**  

| **Category**            | **Criteria**                                           | **Weight** |
|-------------------------|--------------------------------------------------------|------------|
| ✅ **Project Setup**    | Uses Vite, React 19, Tailwind correctly               | **10%**    |
| ✅ **React Router v7**  | Implements sidebar navigation properly                 | **15%**    |
| ✅ **Tailwind Usage**  | Efficient use of utility classes for styling           | **15%**    |
| ✅ **Component Design** | Uses reusable, modular components                     | **15%**    |
| ✅ **State Management & Rehydration** | Efficiently manages data & persistence  | **20%**    |
| ✅ **Code Quality**     | Readability, maintainability, structure, best practices | **15%**    |
| ✅ **Error Handling**   | Manages form validation & API errors                   | **10%**    |

---

## **📁 Mock Data & Local Storage Implementation**  

### **📁 `src/data/settingsData.json`**  
```json
{
  "general": {
    "siteName": "MyApp",
    "timezone": "UTC",
    "language": "English"
  },
  "profile": {
    "username": "johndoe",
    "email": "johndoe@example.com",
    "avatar": "/images/avatar.jpg"
  },
  "account": {
    "twoFactorAuth": true,
    "backupEmail": "backup@example.com"
  },
  "security": {
    "passwordLastChanged": "2024-01-10",
    "sessions": [
      {
        "device": "Macbook Pro",
        "location": "New York, USA",
        "lastActive": "2024-03-05T12:30:00Z"
      }
    ]
  }
}
```

---

### **📁 `src/services/settingsService.js`**  
```javascript
const STORAGE_KEY = "user_settings";

// Load settings from localStorage or fallback to default JSON
export const getSettings = async () => {
  const storedSettings = localStorage.getItem(STORAGE_KEY);
  if (storedSettings) return JSON.parse(storedSettings);

  const response = await fetch("/data/settingsData.json");
  if (!response.ok) throw new Error("Failed to load settings");

  const data = await response.json();
  localStorage.setItem(STORAGE_KEY, JSON.stringify(data)); // Save initial data
  return data;
};

// Update settings and persist in localStorage
export const updateSettings = async (section, newData) => {
  const settings = await getSettings();
  if (settings[section]) {
    settings[section] = { ...settings[section], ...newData };
    localStorage.setItem(STORAGE_KEY, JSON.stringify(settings)); // Persist updates
  }
  return settings;
};
```

---

## **✅ Submission Checklist**  

✔️ Forked repository and created a new branch  
✔️ Implemented sidebar navigation with **React Router v7**  
✔️ Used **Tailwind CSS** for responsive styling  
✔️ Fetched and persisted user settings using **localStorage**  
✔️ Wrote **clean, modular, and well-structured code**  
✔️ Committed frequently and submitted a **Pull Request**  

---

## **📌 Final Notes**  
- Follow best practices in **React.js, Tailwind CSS, and Git**.  
- If you have any questions, feel free to **ask for clarifications in your PR**.  
- We are looking forward to reviewing your submission!  

---
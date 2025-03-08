
# **📌 Commit Message Guidelines**  

## **🔹 Why Follow a Commit Message Standard?**  
Clear and structured commit messages help in:  
✅ Making the Git history **more readable** and **organized**.  
✅ Helping **collaborators and reviewers** understand changes quickly.  
✅ Ensuring **better tracking of features, fixes, and improvements**.  
✅ Making debugging easier by identifying past changes efficiently.  

---

## **✅ Commit Message Format**  
Each commit message should follow this structure:  

```
[type]: [Short Description]

[Detailed Explanation (if needed)]
```

🔹 **Commit Types:**  
- **feat:** A new feature implementation.  
- **fix:** A bug fix or error resolution.  
- **style:** UI or styling changes (no functional updates).  
- **refactor:** Code restructuring or optimizations (no behavior change).  
- **chore:** Project setup, dependency updates, or CI/CD changes.  

---

## **✅ Example Commit Messages**  

### **📌 Initial Project Setup**  
```
chore: setup React project with Vite and Tailwind

- Installed React 19, Vite, and Tailwind CSS
- Configured basic folder structure
- Added necessary dependencies
```

### **📌 Adding a New Feature**  
```
feat: added sidebar navigation with React Router v7

- Created a Sidebar component with links for navigation
- Integrated React Router v7 for routing
- Sidebar is responsive and collapsible on smaller screens
```

### **📌 Fixing a Bug**  
```
fix: resolved issue with settings not persisting on refresh

- Updated localStorage handling for better state rehydration
- Fixed incorrect key names causing persistence issues
```

### **📌 UI Styling Updates**  
```
style: enhanced settings page UI and responsiveness

- Adjusted padding and margins for better spacing
- Improved sidebar collapse behavior on smaller screens
- Applied Tailwind utility classes for better readability
```

### **📌 Code Refactoring**  
```
refactor: optimized components and removed unused code

- Moved reusable UI elements to separate components
- Cleaned up redundant CSS classes
- Improved file structure for better maintainability
```

### **📌 Final Code Cleanup Before PR Submission**  
```
chore: final cleanup and documentation updates

- Removed unnecessary console logs
- Updated README with clearer instructions
- Verified all files for consistency
```

---

## **🔹 Commit Message Best Practices**  
✅ **Use prefixes (`feat`, `fix`, `style`, `refactor`, `chore`)** for clarity.  
✅ **Write in present tense** (e.g., "Add feature" instead of "Added feature").  
✅ **Keep messages concise but meaningful** (first line ≤50 characters).  
✅ **Use bullet points in the description** (if needed).  
✅ **Make frequent commits** to track progress clearly.  

---

## **📌 Why This Matters?**  
Following this commit message structure ensures:  
- **Better collaboration** in teams.  
- **Easier debugging** when tracking past changes.  
- **Professionalism in Git practices** that align with industry standards.  

---

🚀 **Follow these guidelines, and your commit history will be clean and professional!**  

---
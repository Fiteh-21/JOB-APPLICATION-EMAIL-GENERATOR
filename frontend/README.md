# 🎨 AI Resume Assistant - Frontend

The user interface for the AI-Powered Resume Application Assistant. Built with **React** and **Vite**, this SPA (Single Page Application) provides a seamless experience for uploading resumes and generating tailored application emails in real-time.

---

## 🛠️ Tech Stack

- **Framework:** React 18
- **Build Tool:** Vite (for near-instant HMR)
- **HTTP Client:** Axios
- **State Management:** React Hooks (`useState`, `useEffect`)
- **Icons:** React Icons / Lucide React
- **Styling:** CSS3 (Modern Flexbox/Grid architecture)

---

## ✨ UI Features

- **Drag-and-Drop Interface:** Easy PDF uploading with file type validation.
- **Copy-to-Clipboard:** One-click functionality to grab the generated email for immediate use.
- **Responsive Design:** Fully optimized for desktop and mobile browsers.
- **Dynamic Loading States:** Clear visual indicators while the Groq LLM is "thinking."
- **Error Handling:** Graceful alerts if the backend is offline or the PDF is unreadable.

---

## 🚀 Development Setup

### 1. Install Dependencies

```bash
npm install
```

### 2. Environment Variables

Create a `.env` file in the frontend root to point to your FastAPI backend:

```env
VITE_API_URL=http://localhost:8000
```

### 3. Run Development Server

```bash
npm run dev
```

The app will typically be available at `http://localhost:5173`.

---

## 🔌 API Integration

The frontend communicates with the FastAPI backend via a `multipart/form-data` POST request.

**Endpoint:** `POST /generate-email`  
**Payload:**

- `file`: The `.pdf` resume file.
- `job_description`: String containing the target job details.

---

## 📦 Build for Production

To create an optimized production build:

```bash
npm run build
```

The output will be in the `/dist` folder, ready to be served by Nginx or hosted on platforms like Vercel/Netlify.

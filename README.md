# 🌾 AgriShare Frontend (React + Vite)

This project is the frontend for **AgriShare**, an AI-powered smart farming assistant.
Built with **React + Vite + Tailwind CSS**, it provides a fast and responsive UI for crop prediction, plant disease detection, and AI-based agricultural insights.

## 🚀 Features

- 🌿 Crop recommendation based on soil & weather data
- 🦠 Plant disease detection via image upload
- 📖 AI-generated crop & disease insights
- 👤 User authentication (Login/Register/OTP reset)
- ⚡ Fast UI with Vite + React

## 🎥 Demo Video

Click the thumbnail below to watch the full project demo:

[![AgriShare Demo Video](https://img.youtube.com/vi/IVweF9UVLgw/maxresdefault.jpg)](https://youtu.be/IVweF9UVLgw)

## 🔗 Related Repositories

> ### ⚙️ [**AgriShare Backend Repository →**](https://github.com/DohalSri123/AgriShare.git)
> The Django backend powering crop prediction, disease detection, and AI insights for this frontend.
> **Repo:** [https://github.com/DohalSri123/AgriShare.git](https://github.com/DohalSri123/AgriShare.git)

## 🛠️ Tech Stack

- React (Vite)
- Tailwind CSS
- JavaScript (ES6+)
- Fetch API
- JWT Authentication

## 📦 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/agri-share-frontend.git
cd agri-share-frontend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Setup Tailwind CSS

Install Tailwind:

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Update `tailwind.config.js`:

```js
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Add to `src/index.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 4. Configure Environment Variables

Create a `.env` file in root:

```env
VITE_BASE_URL=http://127.0.0.1:8000/
```

### 5. Run the development server

```bash
npm run dev
```

App will run at:

```
http://localhost:5173/
```

## 🔌 API Integration

All backend API calls are handled in:

```
src/api/api.js
```

Example:

```js
export const getPredictionInfo = async (predictionData) => {
  const response = await fetch(`${BASE_URL}prediction-diseasae/get_info_ds/`, {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
    },
    body: JSON.stringify(predictionData),
  });

  return await response.json();
};
```

## 📂 Project Structure

```
src/
│
├── components/
├── pages/
├── api/
│   └── api.js
│
├── App.jsx
├── main.jsx
└── index.css
```

## ⚠️ Important Notes

- Make sure backend is running on:

```
http://127.0.0.1:8000/
```

- Enable CORS in Django backend
- Do NOT hardcode API URLs — use `.env`

## 🚀 Build for Production

```bash
npm run build
```

Preview build:

```bash
npm run preview
```

## 🎯 Future Improvements

- 🌍 Multi-language support
- 📱 Mobile optimization
- 📊 Data visualization
- 🌐 Deployment (Vercel / Netlify)

## 👨‍💻 Author

Dohalsri Vemulapalli

## 📜 License

This project is for educational purposes.

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

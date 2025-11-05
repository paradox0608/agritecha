# 🌱 AgriTech - Gamified Sustainable Farming Platform

A comprehensive, multilingual web application designed to promote sustainable agriculture among Indian farmers and globally through gamification, AI-powered insights, and community engagement.

## 🎯 Features

### ✨ Core Features

- **🎮 Gamified Learning System**
  - Earn XP points and level up
  - Complete daily and weekly challenges
  - Unlock badges and achievements
  - Compete on global leaderboards
  - Track learning streaks

- **🗣️ Multi-Language Support**
  - 15+ languages including:
    - Indian: Hindi, Bhojpuri, Maithili, Tamil, Telugu, Bengali, Marathi, Gujarati, Kannada, Malayalam, Punjabi
    - International: English, Spanish, French
  - Real-time language switching
  - Voice-enabled in all languages

- **🎙️ Voice Integration**
  - Speech-to-text search
  - Text-to-speech responses
  - Voice commands throughout the app
  - Accessibility-first design

- **🤖 AI-Powered Advisory**
  - AI chatbot for farming queries
  - Personalized recommendations
  - Soil health analysis
  - Crop-specific advice
  - Weather-based suggestions

- **📚 Educational Content**
  - Interactive lessons on sustainable farming
  - Quizzes and mini-games
  - Video tutorials
  - Step-by-step guides
  - Certificate courses

- **🌾 Practical Tools**
  - Soil health tracker
  - Real-time market rates
  - Government schemes database
  - Crop rotation planner
  - Water management calculator

- **👥 Community Features**
  - Discussion forums
  - Experience sharing
  - Expert Q&A
  - Regional groups
  - Success stories

## 🏗️ Tech Stack

- **Frontend**: React.js 18+
- **Routing**: React Router DOM 6
- **State Management**: Context API
- **Styling**: CSS3 with CSS Variables
- **Charts**: Recharts
- **Icons**: React Icons
- **Notifications**: React Toastify
- **Backend**: Firebase (Authentication & Firestore)
- **AI Integration**: OpenAI API / Gemini (configurable)
- **Voice**: Web Speech API
- **Localization**: Custom i18n implementation

## 📁 Project Structure

```
agritech-platform/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── Layout.js
│   │   ├── Navbar.js
│   │   ├── Sidebar.js
│   │   ├── VoiceSearch.js
│   │   └── *.css
│   ├── contexts/
│   │   ├── AuthContext.js
│   │   └── LanguageContext.js
│   ├── pages/
│   │   ├── LandingPage.js
│   │   ├── Login.js
│   │   ├── Signup.js
│   │   ├── Dashboard.js
│   │   ├── Profile.js
│   │   ├── Challenges.js
│   │   ├── Lessons.js
│   │   ├── Schemes.js
│   │   ├── Community.js
│   │   ├── SoilHealth.js
│   │   ├── MarketRates.js
│   │   ├── Leaderboard.js
│   │   ├── Advisory.js
│   │   └── *.css
│   ├── config/
│   │   └── firebase.js
│   ├── utils/
│   │   └── translations.js
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   └── index.css
├── package.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Node.js 16+ and npm/yarn
- Firebase account (for authentication and database)
- OpenAI API key (optional, for AI features)

### Installation

1. **Clone or navigate to the project directory**
   ```powershell
   cd C:\Users\anjal\agritech-platform
   ```

2. **Install dependencies**
   ```powershell
   npm install
   ```

3. **Configure Firebase**
   - Go to [Firebase Console](https://console.firebase.google.com/)
   - Create a new project
   - Enable Authentication (Email/Password)
   - Enable Firestore Database
   - Copy your Firebase configuration
   - Update `src/config/firebase.js` with your credentials

4. **Configure Environment Variables (Optional)**
   Create a `.env` file in the root directory:
   ```env
   REACT_APP_OPENAI_API_KEY=your_openai_api_key
   REACT_APP_GEMINI_API_KEY=your_gemini_api_key
   ```

5. **Start the development server**
   ```powershell
   npm start
   ```

6. **Open your browser**
   Navigate to `http://localhost:3000`

## 🎨 Design Theme

The platform uses a nature-inspired color scheme:
- **Primary Green**: `#4CAF50`
- **Dark Green**: `#2E7D32`
- **Light Green**: `#81C784`
- **Sky Blue**: `#87CEEB`
- **Beige**: `#F5F5DC`
- **Earth Brown**: `#8B7355`

## 🌟 Key Pages

### 1. Landing Page (`/`)
- Hero section with animated logo
- Feature showcase
- Statistics
- Call-to-action

### 2. Authentication (`/login`, `/signup`)
- Email/password authentication
- User profile creation
- Region and crop selection

### 3. Dashboard (`/dashboard`)
- User statistics overview
- Weekly progress chart
- Quick actions
- Recent achievements

### 4. Challenges (`/challenges`)
- Daily and weekly challenges
- Difficulty levels (Easy, Medium, Hard)
- XP rewards
- Completion tracking

### 5. Lessons (`/lessons`)
- Categorized learning modules
- Progress tracking
- Interactive content
- Certificates

### 6. Leaderboard (`/leaderboard`)
- Global rankings
- Regional leaderboards
- User highlighting
- Points system

### 7. AI Advisory (`/advisory`)
- Real-time chat interface
- Voice input support
- Contextual responses
- Multi-language support

## 🔧 Configuration

### Adding New Languages

Edit `src/utils/translations.js`:
```javascript
export const translations = {
  // ... existing languages
  newLang: {
    dashboard: 'Translation',
    challenges: 'Translation',
    // ... add all keys
  }
};
```

Update `src/contexts/LanguageContext.js`:
```javascript
availableLanguages: [
  // ... existing languages
  { code: 'newLang', name: 'Language Name' }
]
```

### Customizing Gamification

Edit `src/contexts/AuthContext.js`:
```javascript
const addPoints = (points) => {
  const newPoints = user.points + points;
  const newLevel = Math.floor(newPoints / 1000) + 1; // Adjust level formula
  updateUser({ points: newPoints, level: newLevel });
};
```

## 📱 Responsive Design

The platform is fully responsive and works seamlessly on:
- 📱 Mobile devices (320px+)
- 📱 Tablets (768px+)
- 💻 Laptops (1024px+)
- 🖥️ Desktops (1440px+)

## 🔐 Security

- Firebase Authentication
- Protected routes
- Secure localStorage usage
- Input validation
- XSS protection

## 🌐 Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📊 Performance Optimization

- Code splitting with React.lazy
- Optimized images
- Minimal dependencies
- Efficient state management
- Lazy loading for routes

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is open-source and available under the MIT License.

## 👥 Team

Built with ❤️ for sustainable agriculture

## 🔮 Future Enhancements

- [ ] Mobile app (React Native)
- [ ] Offline mode with PWA
- [ ] Advanced AI models integration
- [ ] Blockchain-based rewards
- [ ] IoT sensor integration
- [ ] Weather API integration
- [ ] Government scheme API integration
- [ ] Payment gateway for premium features
- [ ] Advanced analytics dashboard
- [ ] Social media sharing
- [ ] Email notifications
- [ ] Push notifications
- [ ] Video calling for expert consultation
- [ ] Marketplace for organic products
- [ ] Farm management tools

## 📞 Support

For issues, questions, or suggestions:
- Create an issue on GitHub
- Email: support@agritech.com
- Community Forum: forum.agritech.com

## 🙏 Acknowledgments

- React team for the amazing framework
- Firebase for backend services
- OpenAI for AI capabilities
- All contributors and supporters

---

**Made with 🌱 for a greener future**

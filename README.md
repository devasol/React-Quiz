# React Quiz App 🧠⚛️

A modern, interactive React quiz application that tests your knowledge of React concepts and best practices. Built with React 18, featuring advanced state management using useReducer and Context API.

## 🌟 Features

- **Interactive Quiz Experience**: 15 carefully crafted questions covering React fundamentals to advanced concepts
- **Real-time Timer**: 30 seconds per question with automatic progression
- **Progress Tracking**: Visual progress bar showing current question and completion status
- **Score System**: Points-based scoring with different weights for question difficulty
- **High Score Persistence**: Your best score is saved locally and persists across sessions
- **Responsive Design**: Clean, modern UI that works on all devices
- **State Management**: Advanced state management using useReducer and Context API
- **Error Handling**: Graceful error handling for data loading failures

## 🚀 Live Demo

[View Live Demo](https://react-quiz-dawit.netlify.app/)

## 🛠️ Technologies Used

- **React 18.2.0** - Modern React with hooks and functional components
- **Context API** - Global state management without prop drilling
- **useReducer** - Complex state logic management
- **Local Storage** - High score persistence
- **CSS3** - Custom styling with modern CSS features
- **Create React App** - Development environment and build tools

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (version 14.0 or higher)
- npm or yarn package manager

## ⚡ Quick Start

1. **Clone the repository**

   ```bash
   git clone https://github.com/devasol/React-Quiz.git
   cd React-Quiz
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Start the development server**

   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📜 Available Scripts

### `npm start`

Runs the app in development mode at [http://localhost:3000](http://localhost:3000).
The page will reload when you make changes.

### `npm test`

Launches the test runner in interactive watch mode.

### `npm run build`

Builds the app for production to the `build` folder.
The build is minified and optimized for best performance.

### `npm run server`

Starts a JSON server on port 9000 for local development with the questions data.

## 🏗️ Project Structure

```
React-Quiz/
├── public/
│   ├── questions.json          # Quiz questions data
│   └── index.html             # HTML template
├── src/
│   ├── components/            # React components
│   │   ├── App.js            # Main app component
│   │   ├── Header.js         # App header
│   │   ├── StartScreen.js    # Quiz start screen
│   │   ├── Question.js       # Question display
│   │   ├── Options.js        # Answer options
│   │   ├── Progress.js       # Progress bar
│   │   ├── Timer.js          # Countdown timer
│   │   ├── NextButton.js     # Navigation button
│   │   ├── FinishScreen.js   # Results screen
│   │   ├── Loader.js         # Loading component
│   │   └── Error.js          # Error component
│   ├── contexts/
│   │   └── QuizContext.js    # Global state management
│   ├── index.js              # App entry point
│   └── index.css             # Global styles
├── src-no-context/           # Original version without Context API
└── data/
    └── questions.json        # Questions data source
```

## 🎯 How It Works

### State Management Architecture

The app uses a sophisticated state management system built with React's useReducer and Context API:

- **QuizContext**: Provides global state to all components
- **useReducer**: Manages complex state transitions with actions like:
  - `dataReceived`: Load quiz questions
  - `start`: Begin the quiz
  - `newAnswer`: Handle answer selection
  - `nextQuestion`: Progress to next question
  - `finish`: Complete the quiz
  - `restart`: Reset for a new attempt
  - `tick`: Handle timer countdown

### Key Features Implementation

- **Timer System**: Each question has a 30-second countdown that automatically progresses
- **Scoring**: Questions have different point values (10, 20, or 30 points) based on difficulty
- **High Score**: Uses localStorage to persist the best score across browser sessions
- **Error Handling**: Graceful fallbacks for network issues when loading questions

## 🎮 Quiz Content

The quiz includes 15 questions covering:

- **React Fundamentals**: Components, JSX, props, and data flow
- **State Management**: useState, useReducer, derived state
- **Effects**: useEffect, dependency arrays, cleanup
- **Advanced Concepts**: Performance optimization, best practices

**Total Possible Score**: 280 points

## 🚀 Deployment

### GitHub Pages Deployment

1. **Build the project**

   ```bash
   npm run build
   ```

2. **Deploy to GitHub Pages**

   ```bash
   # Install gh-pages if you haven't already
   npm install --save-dev gh-pages

   # Add to package.json scripts:
   # "predeploy": "npm run build",
   # "deploy": "gh-pages -d build"

   npm run deploy
   ```

### Other Deployment Options

- **Netlify**: Drag and drop the `build` folder
- **Vercel**: Connect your GitHub repository
- **Heroku**: Use the Node.js buildpack

## 🔧 Customization

### Adding New Questions

Edit `public/questions.json` or `data/questions.json`:

```json
{
  "question": "Your question here?",
  "options": ["Option 1", "Option 2", "Option 3", "Option 4"],
  "correctOption": 0,
  "points": 10
}
```

### Modifying Timer

Change the `SECS_PER_QUESTION` constant in `src/contexts/QuizContext.js`:

```javascript
const SECS_PER_QUESTION = 30; // Change this value
```

### Styling

The app uses CSS modules. Main styles are in:

- `src/index.css` - Global styles
- Component-specific styles are inline or in the main CSS file

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built as part of a React learning journey
- Inspired by modern quiz applications
- Uses Create React App for development setup
- Questions designed to test practical React knowledge

## 📞 Contact

- **GitHub**: [@your-username](https://github.com/devasol)
- **Email**: dawit8908@gmail.com
- **LinkedIn**: [Your Name](https://www.linkedin.com/in/dawit-solomon-0450602a0/)

---

⭐ **Star this repository if you found it helpful!**

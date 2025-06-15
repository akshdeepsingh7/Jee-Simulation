# JEE Simulation 📚

A comprehensive, interactive mock test application designed specifically for JEE Main preparation. Features a modern, responsive interface with real-time timer, question palette, and detailed scoring system.

## ✨ Features

### 🎯 Core Functionality
- **Multi-section Support**: Organize questions by subjects (Physics, Chemistry, Mathematics)
- **Real-time Timer**: 10-minute countdown with visual alerts
- **Question Navigation**: Easy movement between questions with status tracking
- **Answer Management**: Save, mark for review, and clear responses
- **Automatic Submission**: Test auto-submits when time expires

### 📊 Question Status Tracking
- **Not Visited** (Grey): Questions not yet opened
- **Not Answered** (Red): Visited but no answer selected
- **Answered** (Green): Questions with selected answers
- **Marked for Review** (Violet): Flagged for later review
- **Answered & Marked** (Violet with ✓): Answered but flagged for review

### 🎨 User Experience
- **Modern UI**: Gradient backgrounds and smooth animations
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Visual Feedback**: Hover effects and status indicators
- **Accessibility**: Proper contrast ratios and semantic markup

### 📈 Scoring System
- **+4 points** for correct answers
- **-1 point** for incorrect answers
- **0 points** for unanswered questions
- Detailed result breakdown with performance metrics

## 🚀 Quick Start

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A local web server (optional, but recommended for JSON loading)

### Installation

1. **Download the files**
   ```bash
   # Clone the repository
   git clone https://github.com/akshdeepsingh7/Jee-Simulation.git
   cd Jee-Simulation
   
   # Or download as ZIP from GitHub
   ```

2. **Create your question bank**
   - Use the provided `questions.json` format (see structure below)
   - Organize questions by sections

3. **Run the application**
   ```bash
   # Option 1: Simple file opening (may have CORS issues)
   # Just open index.html in your browser
   
   # Option 2: Local server (recommended)
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using Live Server (VS Code extension)
   # Right-click on index.html → "Open with Live Server"
   ```

4. **Access the test**
   - Open your browser and navigate to `http://localhost:8000`
   - Click "Start Test" to begin

## 📁 File Structure

```
jee-simulation/
├── index.html          # Main application file
├── questions.json      # Question database
└── README.md          # This file
```

## 📝 Question Format

The `questions.json` file should follow this structure:

```json
{
  "Physics": [
    {
      "text": "What is the SI unit of force?",
      "options": ["Newton", "Joule", "Watt", "Pascal"],
      "correct": 0
    },
    {
      "text": "Which law states F = ma?",
      "options": ["First Law", "Second Law", "Third Law", "Universal Law"],
      "correct": 1
    }
  ],
  "Chemistry": [
    {
      "text": "What is the atomic number of Carbon?",
      "options": ["4", "6", "8", "12"],
      "correct": 1
    }
  ],
  "Mathematics": [
    {
      "text": "What is the derivative of x²?",
      "options": ["x", "2x", "x²", "2x²"],
      "correct": 1
    }
  ]
}
```

### Question Object Properties
- `text`: The question statement (string)
- `options`: Array of 4 answer choices (array of strings)
- `correct`: Index of the correct answer (0-3) (number)

## 🛠️ Customization

### Changing Test Duration
Edit the JavaScript variable in `index.html`:
```javascript
let timeLeft = 10 * 60; // Change 10 to desired minutes
```

### Modifying Scoring
Update the scoring logic in the `calculateResults()` function:
```javascript
score += 4; // Points for correct answer
score -= 1; // Points deducted for wrong answer
```

## 🐛 Troubleshooting

### Common Issues

**Questions not loading**
- Ensure `questions.json` is in the same directory as `index.html`
- Check browser console for CORS errors
- Use a local server instead of opening the file directly

**Timer not working**
- Check JavaScript console for errors
- Ensure the browser supports modern JavaScript features

**Responsive issues**
- Clear browser cache
- Check viewport meta tag is present
- Test on different screen sizes

### Error Messages

- **"Could not load questions"**: JSON file missing or malformed
- **Timer shows "NaN"**: JavaScript execution error
- **Buttons not responding**: Event listeners not attached properly

## 🤝 Contributing

Want to improve this mock test? Here are ways to contribute:

1. **Report Bugs**: Open an issue describing the problem
2. **Suggest Features**: Propose new functionality
3. **Submit Questions**: Add more practice questions
4. **Improve UI/UX**: Enhance the user interface

### Development Setup
```bash
# Fork the repository on GitHub
# Clone your fork
git clone https://github.com/your-username/Jee-Simulation.git
cd Jee-Simulation

# Make your changes
# Test thoroughly
# Submit a pull request to akshdeepsingh7/Jee-Simulation
```

## 📊 Performance Tips

- **Question Loading**: For large question banks, consider implementing lazy loading
- **Mobile Optimization**: Test on various devices for optimal experience
- **Accessibility**: Use screen readers to verify accessibility compliance

## 🆘 Support

Need help? Here are your options:

1. **Documentation**: Check this README thoroughly
2. **Issues**: Open a [GitHub issue](https://github.com/akshdeepsingh7/Jee-Simulation/issues) for bugs
3. **Discussions**: Use [GitHub Discussions](https://github.com/akshdeepsingh7/Jee-Simulation/discussions) for questions
4. **Contact**: Reach out to [@akshdeepsingh7](https://github.com/akshdeepsingh7) for urgent issues

## 🏆 Acknowledgments

- Inspired by the official JEE Main exam interface
- Built with modern web technologies
- Designed for optimal learning experience

---

**Developed by [@akshdeepsingh7](https://github.com/akshdeepsingh7) | Made with ❤️ for JEE aspirants**

*Good luck with your preparation! 🎓*

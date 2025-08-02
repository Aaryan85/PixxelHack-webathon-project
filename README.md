PixxelHack-webathon-project
🧠 Responsive Quiz App

A fully responsive, interactive **Quiz Web Application** built using **HTML**, **CSS**, and **vanilla JavaScript**. This app dynamically loads questions, tracks the user’s score, and updates the UI in real time, providing an engaging and user-friendly quiz experience on both desktop and mobile devices.

---

 👥 Team Information

#Team Name: ByteBros
  Team Members:

  * Aaryan Yadav
  * Sumit Yadav
* **GitHub Handle:** [@aaryan85](https://github.com/aaryan85)
* **Live Deployment:** [View Project](https://aaryan85.github.io/PixxelHack-webathon-project/index.html)

---

## 🌟 Features

* ✅ Multiple-choice questions with single-answer selection
* ✅ Live score tracking
* ✅ Question number indicator (e.g., “3 of 10”)
* ✅ Responsive design: works well on mobile, tablet, and desktop
* ✅ Clickable options for better UX
* ✅ Simple and clean UI design
* ✅ Final result screen showing the total score

---

## 📂 Project Structure

```
quiz-app/
├── index.html       # HTML markup (structure of the quiz)
├── style.css        # Styling and responsive design
├── script.js        # JavaScript logic (quiz flow, question loading, scoring)
└── README.md        # Documentation
```

---

## 🚀 Getting Started

Follow the steps below to set up and run the project locally on your computer:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/quiz-app.git
```

### 2. Navigate into the Project Directory

```bash
cd quiz-app
```

### 3. Open in Browser

You can open `index.html` directly in your browser:

* On Windows:

  * Right-click → Open With → Your browser
* Or drag and drop `index.html` into your browser window

---

## 💡 How the App Works

* The app starts by loading the first question from a JavaScript array (`quizDB`)
* Each option is displayed as a radio input
* When a user selects an answer and clicks **Submit**:

  * It checks if the selected answer matches the correct one
  * If correct, the score is incremented
  * Moves to the next question
* After the last question:

  * The app displays the final score inside the `.quiz-container`

---

## 🔧 Customizing the Quiz

To **add or edit questions**, open `script.js` and modify the `quizDB` array like this:

```js
const quizDB = [
  {
    question: "Your custom question?",
    options: ["Option 1", "Option 2", "Option 3", "Option 4"],
    answer: "Correct Answer"
  },
  ...
];
```

✔ Make sure the `answer` field exactly matches one of the `options`.

---

## 🔧 Responsive Design Tips

Your app is already responsive, but ensure the following for better mobile performance:

* Use:

  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```
* CSS should include media queries or flexible units (%, em, rem)
* Example CSS tip for mobile options:

  ```css
  li {
    width: 100%;
    padding: 12px;
    font-size: 1rem;
  }
  ```

---

## ✍️ Example Code Snippets

### HTML (index.html)

```html
<div class="quiz-container">
  <div id="QuestionNo"></div>
  <h2 id="question">Loading...</h2>
  <ul id="options"></ul>
  <button id="submit">Submit</button>
  <div id="result-box">
    <p id="result"></p>
  </div>
</div>
```

### JavaScript (script.js)

```javascript
submitBtn.addEventListener("click", () => {
  const selected = getSelected();
  if (!selected) {
    alert("Please select an answer!");
    return;
  }

  if (selected === quizDB[currentQuestion].answer) {
    score++;
  }

  currentQuestion++;
  if (currentQuestion < quizDB.length) {
    loadQuestion();
  } else {
    document.querySelector(".quiz-container").innerHTML =
      `<h1>You scored ${score} out of ${quizDB.length}</h1>`;
  }
});
```

---

## 👨‍💻 Author

**Aaryan Yadav**
📧 Connect on GitHub: [@aaryan85](https://github.com/aaryan85)
🌐 Project made with ❤️ using HTML, CSS, JavaScript

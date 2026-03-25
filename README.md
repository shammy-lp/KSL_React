# Title: Learning React Framework by Creating a Kenya Sign Language Tool.

## 1.Objectives
By the end of me building and learning the React framework, I want to learn and accomplish:
  1. A strong understanding of core React concepts like components, state and hooks.
  2. Hands-on experience in creating interactive and dynamic front-end features.
  3. The ability to efficiently manage data and UI updates in a React app.
  4. Improved skills in styling, responsive design and building user-friendly interfaces.
  5. Practical application of React knowledge through building this Kenya Sign Language Tool to reinforce learning.

### Why React?
By learning React, I am able to create front-end systems for my machine learning workflows and pipelines. This allows me to intergrate my already built machine learning models and pipelines with design interfaces where users can interact with them.

### End Goal: 
My end goal is to have a minimum viable tool that lets users view and practice Kenya Sign Language signs for letters, with a simple, interactive and responsive interface built using React, while demonstrating my understanding of core React concepts.

## 2.Quick Summmary of the React Framework
  1. **Component** – This is a reusable piece of the UI. Think of it as a building block, like a button or a sign display.
  2. **JSX**– This is a syntax that looks like HTML but works in JavaScript. Used to define what your UI looks like.
  3. **Props** – Short for properties. They let you pass data from one component to another.
  4. **State** – This is a way for a component to remember data that can change over time, like the letter a user selects.
  5. **Event Handling** –This lets your app respond to user actions, like clicks or selections.
  6. **Conditional Rendering** – This shows or hides parts of the UI depending on the state, like showing a sign only after a letter is picked.
  7. **Lists & Keys** – Used to display multiple items (like all letters) dynamically and efficiently.

## 3.System Requirements
### 1. Operating System (OS)
Windows, macOS or Linux

### 2. Tools & Editors
VS Code (or any code editor)

Web Browser (Chrome, Edge)

Vercel - for deployment

Claude - for development assistance

### 3. Packages & Setup
Node.js & npm

Vite or Create React App

React

## 4.Installation & SetUp Instructions
### Option 1: Run Locally (Optional)
If you want to run and test the project on your own machine:
  1. Clone the repository
     
``git clone <your-repo-link>``

``cd <your-project-folder>``

  2. Install dependencies
``npm install``

  3. Start the development server
``npm run dev``

  4. Open the app in your browser
By default, the app will run at:
http://localhost:5173/

If the port is in use, Vite will suggest another port like 5174

### Option 2: Deploy and Run on Vercel (Recommended)
  1. Push your project to GitHub
  2. Go to Vercel and log in
  3. Import your GitHub repository
  4. Click Deploy

Vercel will automatically:

Install dependencies ``npm install``

Build the project ``npm run build``

Host the project on a live URL

Access your live app

After deployment, Vercel provides a URL like:
https://your-app-name.vercel.app

## 5.Minimal Working Examples
This project demonstrates a simple version of the KSL Alphabet Learner built with Next.js (React).

It includes:

  1. A Learning Page displaying the 26 letters of the aphabet with emoji - like animated hand signs.
  2. A Quiz Page where learners can gauge their understanding.
  3. Basic progress tracking (accuracy, score) stored in local state.
  4. A simple Kenyan-themed UI using colors inspired by the Kenyan national flag.

### Project Structure
```
/app
  /learn
    page.js
  /quiz
    page.js
/components
  AlphabetCard.js
  QuizCard.js
  ProgressTracker.js
/lib
  data.js
```
### Part 1: /components/AlphabetCard.js
It displays a single card showing a letter and its hand sign.It is used on the Learning Page to visually present each alphabet letter with subtle animation.

```
"use client";
import { motion } from "framer-motion";

export default function AlphabetCard({ letter, sign }) {
  return (
    <motion.div
      whileHover={{ scale: 1.1 }}
      className="p-4 bg-black text-white rounded-xl text-center shadow-md"
    >
      <div className="text-4xl">{sign}</div>
      <div className="mt-2 text-lg font-bold">{letter}</div>
    </motion.div>
  );
}
```
### Part 2: /lib/data.js
It stores the alphabet data (letter + hand sign) for Learning and Quiz page
```
// Stores the KSL alphabet letters and signs
export const alphabet = [
  { letter: "A", sign: "✊🏿" },
  { letter: "B", sign: "🖐🏿" },
  { letter: "C", sign: "🤏🏿" },
];
```

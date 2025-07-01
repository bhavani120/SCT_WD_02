<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Quiz Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 30px;
    }

    h1 {
      color: #333;
    }

    .quiz-container {
      background: white;
      padding: 20px 30px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      width: 350px;
    }

    .question {
      font-size: 1.2em;
      margin-bottom: 15px;
    }

    .answers button {
      display: block;
      width: 100%;
      margin: 8px 0;
      padding: 10px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      background-color: #e0e0e0;
    }

    .answers button:hover {
      background-color: #d0d0d0;
    }

    #next-btn {
      margin-top: 20px;
      padding: 10px 20px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      display: none;
    }
  </style>
</head>
<body>

  <h1>Quiz Game</h1>
  <div class="quiz-container">
    <div class="question" id="question">Question text</div>
    <div class="answers" id="answer-buttons"></div>
    <button id="next-btn" onclick="nextQuestion()">Next</button>
  </div>

  <script>
    const questions = [
      {
        question: "What is the capital of France?",
        answers: [
          { text: "Paris", correct: true },
          { text: "London", correct: false },
          { text: "Rome", correct: false },
          { text: "Berlin", correct: false }
        ]
      },
      {
        question: "Which planet is known as the Red Planet?",
        answers: [
          { text: "Mars", correct: true },
          { text: "Jupiter", correct: false },
          { text: "Saturn", correct: false },
          { text: "Venus", correct: false }
        ]
      },
      {
        question:
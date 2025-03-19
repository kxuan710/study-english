# Study English  
Dự án hỗ trợ học tiếng Anh

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flashcards</title>
    <style>
        .card {
            width: 200px;
            height: 300px;
            border: 1px solid #000;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            text-align: center;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="card" onclick="flipCard()">Click to flip</div>

<script>
    const card = document.querySelector('.card');
    let isFlipped = false;

    const words = [
        { term: 'Apple', definition: 'A fruit that is red or green.' },
        { term: 'Cat', definition: 'A small domesticated carnivorous mammal.' },
    ];

    function flipCard() {
        if (isFlipped) {
            card.textContent = words[0].term;
        } else {
            card.textContent = words[0].definition;
        }
        isFlipped = !isFlipped;
    }

    card.textContent = words[0].term;
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>English Grammar Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }
        .question {
            margin: 10px 0;
        }
        .answer {
            padding: 5px;
            margin-right: 10px;
        }
    </style>
</head>
<body>

    <h1>English Grammar Quiz</h1>
    <div id="quiz-container">
        <div class="question">
            <p>1. Choose the correct form of the verb: "She ____ a doctor."</p>
            <input type="radio" id="q1a1" name="q1" class="answer" value="is"> is<br>
            <input type="radio" id="q1a2" name="q1" class="answer" value="are"> are<br>
            <input type="radio" id="q1a3" name="q1" class="answer" value="am"> am<br>
        </div>
        <div class="question">
            <p>2. What is the past tense of "run"?</p>
            <input type="radio" id="q2a1" name="q2" class="answer" value="ran"> ran<br>
            <input type="radio" id="q2a2" name="q2" class="answer" value="runned"> runned<br>
            <input type="radio" id="q2a3" name="q2" class="answer" value="runs"> runs<br>
        </div>
        <button onclick="checkAnswers()">Submit</button>
        <p id="result"></p>
    </div>

    <script>
        function checkAnswers() {
            let score = 0;
            if (document.getElementById('q1a1').checked) {
                score++;
            }
            if (document.getElementById('q2a1').checked) {
                score++;
            }
            document.getElementById('result').innerHTML = "Your score: " + score + "/2";
        }
    </script>

</body>
</html>

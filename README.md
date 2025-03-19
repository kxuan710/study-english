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

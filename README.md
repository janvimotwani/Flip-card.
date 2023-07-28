//html structure

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flip Card Project</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="flip-card">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <!-- Front content goes here -->
                <h2>Front Side</h2>
            </div>
            <div class="flip-card-back">
                <!-- Back content goes here -->
                <h2>Back Side</h2>
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
# Flip-card.

//CSS
body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f0f0f0;
}

.flip-card {
    width: 200px;
    height: 200px;
    perspective: 1000px; 
}

.flip-card-inner {
    width: 100%;
    height: 100%;
    transition: transform 0.6s;
    transform-style: preserve-3d;
    position: relative;
}


.flip-card-front, .flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #ccc;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}


.flip-card-front {
    background-color: #fff;
    z-index: 2;
}


.flip-card-back {
    background-color: #f9c;
    transform: rotateY(180deg);
}


.flipped {
    transform: rotateY(180deg);
}


//script.js
const flipCard = document.querySelector('.flip-card');

flipCard.addEventListener('click', () => {
    flipCard.classList.toggle('flipped');
});

<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz Überraschung</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; padding: 50px; }
        .quiz { margin: 20px auto; width: 300px; }
        .hidden { display: none; }
    </style>
</head>
<body>

    <h2>Beantworte diese Fragen!</h2>
    <div class="quiz">
        <p>Was ist die Hauptstadt von Frankreich?</p>
        <button onclick="nextQuestion(1)">Paris</button>
        <button onclick="nextQuestion(0)">London</button>
    </div>

    <div class="quiz hidden" id="q2">
        <p>Welcher Park hat ein berühmtes Schloss?</p>
        <button onclick="nextQuestion(1)">Disneyland</button>
        <button onclick="nextQuestion(0)">Europa-Park</button>
    </div>

    <div class="quiz hidden" id="q3">
        <h2>🎉 Überraschung! 🎉</h2>
        <p>Mir flüget nach Disneyland Paris! 🏰✨</p>
    </div>

    <script>
        let currentQuestion = 1;
        function nextQuestion(correct) {
            if (correct) {
                document.querySelector(".quiz").classList.add("hidden");
                if (currentQuestion < 3) {
                    document.getElementById("q" + currentQuestion).classList.remove("hidden");
                    currentQuestion++;
                }
            }
        }
    </script>

</body>
</html>

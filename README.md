# xk4zuma.github.io.

<!DOCTYPE html>
<html>
<head>
    <title>aki ganda</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <h1>sorry na :< </h1>
    <img id="responseImage" src="https://media.giphy.com/media/KI5JqBqOKCPjG/giphy.gif" width="75%">
    <p id="question">tatampo ka parin ba sakin? <br>
    dahil sa nagawa ko kahapon sorry na plss?</p>
    <button id="yesButton">Oo</button>
    <button id="noButton">Hindi</button>

    <p class="hidden" id="message1">Sorry na patawarin mo na ko di na mauulit paghe-headglitch ko. I'll play fair na next time hehe. Sorry na, okay?</p>
    <button class="hidden" id="okayButton1">Okay</button>
    <button class="hidden" id="notOkayButton" onclick="notOkayResponse()">Di okay</button>

    <p class="hidden" id="message2">Yiee.. so it means pinapatawad mo na ako hehe.</p>
    <button class="hidden" id="okayButton2">Yeah</button>

    <p class="hidden" id="message3">Tara, play ba ulit tayo 1v1?</p>
    <button class="hidden" id="yesButton2">Yes</button>
    <button class="hidden" id="noButton2">No</button>

    <p class="hidden" id="finalMessage">Okay, chat mo na ako sa IG if mag oopen kana hehe.</p>
    <p class="hidden" id="finalMessage2">Whyy?? Chat mo ako sa IG bakit no huhu.</p>

    <script>
        // Function to show an element
        function showElement(elementId) {
            document.getElementById(elementId).classList.remove('hidden');
        }

        // Function to hide an element
        function hideElement(elementId) {
            document.getElementById(elementId).classList.add('hidden');
        }

        // Event handling for "Yes" button
        document.getElementById('yesButton').addEventListener('click', function () {
            hideElement('question');
            hideElement('yesButton');
            hideElement('noButton');

            showElement('message1');
            showElement('okayButton1');
            showElement('notOkayButton');
            document.getElementById('responseImage').src = 'https://tenor.com/view/cat-sad-gif-26415220.gif'; // Update the image source to empty
        });

        // Event handling for "No" button
        document.getElementById('noButton').addEventListener('click', function () {
            hideElement('question');
            hideElement('yesButton');
            hideElement('noButton');

            showElement('message2');
            showElement('okayButton2');
            document.getElementById('responseImage').src = 'https://tenor.com/view/cat-cat-jumping-cat-excited-excited-dance-gif-19354605.gif'; // Update the image source to empty
        });

        // Event handling for "Okay" button (after first message)
        document.getElementById('okayButton1').addEventListener('click', function () {
            hideElement('message1');
            hideElement('okayButton1');
            hideElement('notOkayButton');

            showElement('message2');
            showElement('okayButton2');
            document.getElementById('responseImage').src = 'https://tenor.com/view/cat-cat-jumping-cat-excited-excited-dance-gif-19354605.gif';
        });

        // Event handling for "Okay" button (after the second message)
        document.getElementById('okayButton2').addEventListener('click', function () {
            hideElement('message2');
            hideElement('okayButton2');

            showElement('message3');
            showElement('yesButton2');
            showElement('noButton2');
        });

        // Event handling for "Yes" button (final message)
        document.getElementById('yesButton2').addEventListener('click', function () {
            hideElement('message3');
            hideElement('yesButton2');
            hideElement('noButton2');

            showElement('finalMessage');
        });

        // Event handling for "No" button (final message)
        document.getElementById('noButton2').addEventListener('click', function () {
            hideElement('message3');
            hideElement('yesButton2');
            hideElement('noButton2');

            showElement('finalMessage2');
            document.getElementById('responseImage').src = 'https://tenor.com/view/cat-sad-gif-26415220.gif';
        });

        // Function for handling "Di okay" button response
        function notOkayResponse() {
            alert('why not naman? explain mo sakin sa ig :<< ill make it up to you to not hate me :< ');
        }
    </script>
</body>
</html>

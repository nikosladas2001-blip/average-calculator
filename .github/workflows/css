function addGrade() {
    let container = document.getElementById('grades-container');
    let count = container.getElementsByClassName('grade').length + 1;

    let input = document.createElement('input');
    input.type = 'number';
    input.className = 'grade';
    input.placeholder = 'Βαθμός ' + count;
    input.step = '0.1';

    container.appendChild(input);
}

function removeGrade() {
    let container = document.getElementById('grades-container');
    let grades = container.getElementsByClassName('grade');
    if (grades.length > 1) { // πάντα αφήνουμε τουλάχιστον 1 πεδίο
        container.removeChild(grades[grades.length - 1]);
    }
}

function calculateAverage() {
    let gradesInputs = document.getElementsByClassName('grade');
    let gradesArray = [];

    for (let input of gradesInputs) {
        let value = parseFloat(input.value);
        if (isNaN(value)) {
            document.getElementById('result').innerText = "Συμπλήρωσε όλους τους βαθμούς!";
            document.getElementById('result').style.color = "black";
            document.getElementById('message').innerText = "";
            return;
        }
        gradesArray.push(value);
    }

    let sum = gradesArray.reduce((a, b) => a + b, 0);
    let average = sum / gradesArray.length;

    let schoolAverage = 13;
    let resultElement = document.getElementById('result');
    let messageElement = document.getElementById('message');

    resultElement.innerText = "Μέσος Όρος: " + average.toFixed(2);

    if (average > schoolAverage) {
        resultElement.style.color = "green";
        messageElement.style.color = "green";
        messageElement.innerText = "Πέρασες το μάθημα!";
    } else {
        resultElement.style.color = "red";
        messageElement.style.color = "red";
        messageElement.innerText = "Δεν πέρασες το μάθημα.";
    }
}

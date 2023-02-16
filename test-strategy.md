///El rango de numeros aleatorios estaba erroneo////
    var randomNumber = Math.floor(Math.random() * 100) + 1;

///Cambiamos la declaracion de variables a tipo VAR////
    var guesses = document.querySelector('.guesses');
    var lastResult = document.querySelector('.lastResult');
    var lowOrHi = document.querySelector('.lowOrHi');
    var guessSubmit = document.querySelector('.guessSubmit');
    var guessField = document.querySelector('.guessField');
    var guessCount = 1;
    var resetButton;

///Colocamos Number para representar valores numericos
      var userGuess = Number(guessField.value);

///Los Mensajes estaban al revez
        lastResult.textContent = '¡Felicidades! ¡Ganaste!';
        lastResult.style.backgroundColor = 'green';
        lowOrHi.textContent = '';
        setGameOver();

///Igualamos el guessCount a 10 y eliminamos la Variable ATTEMPS
      } else if (guessCount === 10) {
        lastResult.textContent = '¡¡¡Fin del Juego, Intentar de Nuevo!!!';
        lowOrHi.textContent = '';
        setGameOver();


 ///Los signos de mayor y menor estaban cruzados
        if(userGuess < randomNumber) {
          lowOrHi.textContent='¡El numero es muy bajo!' ;
          lowOrHi.style.color = 'green';
        } else if(userGuess > randomNumber) {
          lowOrHi.textContent = 'El numero es muy alto!';
          lowOrHi.style.color = 'red';
        }


//El addEventListener estaba mal escrito 
    guessSubmit.addEventListener('click', checkGuess);



 resetButton.parentNode.removeChild(resetButton);
      guessField.disabled = false;
      guessSubmit.disabled = false;
      guessField.value = '';
      guessField.focus();
      lastResult.style.backgroundColor = 'white';
      //Faltaba hacer referencia a la cantidad de numeros aleatorios
      randomNumber=Math.floor(Math.random() * 100) + 1;

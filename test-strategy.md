1. Linea 44.  let randomNumber = Math.random() * 10; 1.no establece el rango de numeros 2. expresion incompleta no establece le punto flotante 3. se cambia de let a var para bridnar seguridad
|| Correcion a: var randomNumber = Math.floor(Math.random() * 100) + 1;
2. Linea 46. const ATTEMPS = 5; *el numero de intentos es menor al solicitado
||Correccion a: const ATTEMPS = 10;
3. Linea 53 let guessCount = 10;
  Linea 54 let resetButton;
  Liena 58  let userGuess = guessField.value;
  Cambio de let a var para manejar mejor la seguridad
  ||Correccion a 
  Linea 53 var guessCount = 10;
  Linea 54 var resetButton;
  Liena 58  var userGuess = guessField.value;
4. Linea 64.   if(userGuess === randomNumber) {
   Linea 65   lastResult.textContent = '!!!Pérdistes!!!';
   Linea 66   lastResult.style.backgroundColor = 'black';
   Linea 67   lowOrHi.textContent = '';
   Liena 68   setGameOver();
   Fragmento de cogido donde se observa que en la linea 65 el texto esta mal, ya que si se cumple la funcion esta deveria de ser verdadera, no falsa.
   Linea 66 el color se cambia a verde
 || Correccion a: Linea 64.   if(userGuess === randomNumber) {
                 Linea 65   lastResult.textContent = '!!!Felicitaciones! adivinaste el número!!!';
                 Linea 66   lastResult.style.backgroundColor = 'green';
                 Linea 67   lowOrHi.textContent = '';
                 Liena 68   setGameOver();
5. Linea 69 else if(guessCount === ATTEMPS) {
   linea 70  lastResult.textContent = 'Felicitaciones! adivinaste el número!';
   linea 71  lastResult.style.backgroundColor = 'red';
   linea 72  setGameOver();
   Las instrucciones indican que si el usuario llega 10 intentos y no gano, pero en el codigo se muestra lo contrario
  ||Correccion a: Linea 69 else if(guessCount === ATTEMPS) {
                 linea 70  lastResult.textContent = '¡¡Pérdiste!!';
                 linea 71  lastResult.style.backgroundColor = 'red';
                 linea 72  setGameOver();
  6.  Linea 75      lastResult.style.backgroundColor = 'green';
      Linea 76  if(userGuess < randomNumber) {
     Linea 77  lowOrHi.textContent = 'El número es mayor!';
    La condicion if nos indica que si userGuess es menor a random numer debe mostrar es menor, en el codigo indica lo contrari, cambio de color  
    ||Correccion a:  Linea 75      lastResult.style.backgroundColor = 'red';
                     Linea 76  if(userGuess < randomNumber) {
                     Linea 77  lowOrHi.textContent = 'El número es menor!';
 7. Linea 78 } else if(userGuess > randomNumber) {
   linea 79  lowOrHi.textContent = 'El número es menor!';
   La condicion nos expresa que si userGuess es mayor que randomNumber debe mostrar mayor, el codigo nos indica lo contrario
   ||Correccion a: Linea 78 } else if(userGuess > randomNumber) {
                   linea 79  lowOrHi.textContent = 'El número es mayor!'; 
 8. Linea 102 for(let i = 0; i < resetParas.length; i++) { || cambio de let a var para brindar mas seguridad	for( var i = 0; i < resetParas.length; i++) {
9. Linea 114. randomNumber = Math.floor(Math.random()) + 1;
    1.no establece el rango de numeros 2. expresion incompleta no establece le punto flotante 
  ||Correccion: Linea 114.  randomNumber = Math.floor(Math.random()* 100) + 1;

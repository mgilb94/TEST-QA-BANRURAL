	<label for="guessField">Ingresa el número a adivinar: </label><input type="text" id="guessField" class="guessField">
En este label acepta letras y simbolos. Las instrucciones indican que solo numeros enteros.
	
	const ATTEMPS = 5; En este ejercicio solicitaban que fueran 10 intentos y dentro del codigo del programa hay solo 5 intentos
Correcion: Modificar que haga los 10 intentos en el valor de la constante para .


Si el usuario gano muestra el mensaje !!!Pérdiste!!! 
		Si el jugador perdio muestra Felicitaciones! adivinaste el número!
Correcciones: invertir los textos en los resultados.


    if(userGuess < randomNumber) {
        lowOrHi.textContent = 'El número es mayor!';
      } else if(userGuess > randomNumber) {
        lowOrHi.textContent = 'El número es menor!';
      }
    }
    Al ejecutar la sentencia if el resultado esperado es el contrario
Correcciones: invertir la condicionales o cambiar las descripcion del texto



	const lowOrHi = document.querySelector('lowOrHi');  referencia no definida
Correcciones: .lowOrHi escribir la referencia correctamente


	guessSubmit.addeventListener('click', checkGuess); resetButton.addeventListener('click', resetGame); metodos mal escritos
Correcciones: Escribir bien los metodos.


	const resetParas = document.querySelectorAll('.resultParas p'); referencia mal escrita
Correcciones: Colocar referencia correctamente.

	let randomNumber = Math.random() * 100-10; el numero random el número a adivinar puede que pertenezca y puede que no pertenezca al conjunto de los enteros (e.g. 1, 2, 3...)
Correcciones: agregar un rango de 1 al 100 en la funcion random y que sean enteros


	if(guessCount === 1), if(userGuess === randomNumber), else if(guessCount === ATTEMPS) dentro de las sentencias esta escrito 3 signos ===
Correcciones: Eliminar el igual


 Al momento de mostrar se debe mostrarse el mensaje de color rojo: "!!!Pérdistes!!!",
            Debe mostrar el mensaje de color verde: "Felicitaciones! adivinaste el número!", 
			Debe mostrar el siguiente mensaje en color negro: "Incorrecto! El número es mayor!", 
			en caso que sea menor, se debe mostrar: "Incorrecto! El número es menor!".
Correcciones: Cambiar los colores de cada mensaje asi como se solicito
	  
    if(userGuess == randomNumber) {
      lastResult.textContent = '!!!Pérdistes!!!';
      lastResult.style.backgroundColor = 'black';
      lowOrHi.textContent = '';
      setGameOver(); 
	   
	 
	  
    } else if(guessCount === ATTEMPS) {
      lastResult.textContent = 'Felicitaciones! adivinaste el número!';
      lastResult.style.backgroundColor = 'red';
      setGameOver();
    }
			

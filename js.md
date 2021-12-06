# Javascript

1.  Che differenza c'è tra `var`, `let` e `const`?
var è la vecchia keyword con la quale veniva dichiarata una variabile in javascript, viene ancora utilizzata per
il mantenimento di codice vecchio. Let identifica una variabile che può essere modificata lungo il corso dell'esecuzione dello script mentre const rappresenta una costante il cui valore non potrà essere modificato.


2.  Cos'è il DOM?
Il DOM (Document Object Model) è il modello a oggetti del documento che il browser crea quando la pagina viene caricata. In poche parole è l'interfaccia che permette di creare,cambiare o rimuovere elementi dal documento.

3.  Cosa cambia invocando la funzione `myFunction` in questi modi?

    ```
    myFunction(++i);
    myFunction(i++);
    ```

nel primo caso viene ritornato il nuovo valore incrementato di i.
nel secondo caso viene fatto l'incremento ma viene ritornato il vecchio valore di i.
assumendo che i = 1 l'output del primo esempio sarebbe 2 mentre nel secondo sarebbe 1.

4. Esistono modificatori di accesso alle proprietà di un oggetto in javascript? Si possono creare proprietà private in un oggetto javascript?
per accedere alle proprietà di un oggetto javascript possiamo utilizzare la dot notation (var rooms = hotel.rooms) oppure possiamo specificare la proprietà di un oggetto scrivendo il suo nome in forma di stringa fra quadre (var rooms = hotel["rooms"]). Javascript non supporta ancora le proprietà private (anche se sono in via di implementazione), tuttavia ci sono modi in cui simularle utilizzando closures e prefissi.


5. Cos'è una closure? Sai fare un esempio?
(argomento che non conosco bene)
una closure è una funzione che ha accesso allo scope del genitore, anche dopo che la funzione genitore viene chiusa.


6. A cosa può servire la seguente funzione?

    ```
    var myfunc = function (fn, context) {
      return function () {
          return fn.apply(context, arguments);
      }
    }
    ```

il valore di this viene modificato in context.

7. Cos'è una `Promise`? Quali problemi permette di risolvere? Quali altri modi mette a disposizione javascript per risolvere problemi analoghi?
(argomento che non conosco bene)
Una Promise è un oggetto che potrebbe produrre un valore in futuro. Le Promise vengono utilizzate per gestire le operazioni asincrone. Un altro metodo prevede l'utilizzo delle callback functions che però, in caso ci sia l'esigenza di gestire molteplici operazioni asincrone, potrebbero rendere il codice poco leggibile. 


8. Scrivi una funzione che si comporti in modo da rispettare gli output seguenti:

    ```
    console.log(multiply(2,3));	// Outputs 6
    console.log(multiply(2)(3));	// Outputs 6
    ```

function multiply(a,b){
  return a * b;
}

function multiply (a) {
  return function (b) {
    return a * b;
  }
}

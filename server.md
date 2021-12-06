# Utilizza il tuo linguaggio di programmazione preferito

1. Conosci dei pattern di programmazione ad oggetti? Sapresti fare qualche esempio?
Ho gia programmato ad oggetti ma non ho mai utilizzato pattern specifici.

2. Cosa sono i metodi `getter` e `setter` e perché sono importanti?
getter e setter sono metodi per ottenere e assegnare valori delle variabili.
Oltre a velocizzare la scrittura del codice, mediante il loro utilizzo si impedisce di sovvrascrivere accidentalmente dati chiave.

3. Cosa sono e come ci si protegge da attacchi di SQL Injection?
(argomento che non conosco bene) 
la SQL injection è una tecnica che consiste nell'inserire nei campi di input una query SQL che verrà poi letta dal database.
Preverrei questo pericolo mediante un attenta convalida dei dati inseriti in input. 
 
4. Scrivi una funzione che accetti come unico argomento un numero naturale `n`, e che restituisca un array contente i numeri da 1 ad `n` sostituendo ai multipli di 3 la parola `lin`, ai multipli di 4 la parola `ux`, ai multipli di entrambi la parola `linux`. Exempio:

```
myFunction (20) // [1, 2, 'lin', 'ux', 5, 'lin', 7, 'ux', 'lin', 10, 11, 'linux', 13, 14, 'lin', 'ux', 17, 'lin', 19, 'ux']
```
<!-- dichiaro in scope globale l'arrey vuoto -->
let numbers=[];
function myFunction (n) {
    <!-- assegno ad i il valore 1 e faccio ciclare finchè i non è minore o uguale a n -->
    for (i=1; i <= n; i++){
        <!-- se i è multiplo di 3 o 4 pusho la stringa "linux" in numbers -->
        if (i % 3 == 0 && i % 4 == 0){
          numbers.push("linux")
        <!-- se è multiplo di tre pusho "lin"  -->
        }if(i % 3 == 0){
          numbers.push("lin");
        <!-- se è multiplo di 4 pusho "ux" -->
        } else if (i % 4 == 0){
          numbers.push("ux");
        <!-- se non è multiplo ne di 3 ne di 4 pusho i -->
        } else {
          numbers.push(i);
        }
    }
}

5. Quali metodi HTTP conosci per effettuare richieste?
GET,POST,HEAD,PUT,DELETE,PATCH

6. Quali metodi conosci per autenticare richieste ad un web service REST?
non ne conosco nessuno. 

7. Come puoi ispezionare una richiesta HTTP e la sua risposta?
la richiesta http può essere ispezionata tramite devTools sotto la finestra Network

8. Prova a risolvere il seguente esercizio:

>   Tutti quanti amiamo Scarabeo, ci piace comporre parole a partire da un bel mucchio di lettere.
>
>   Scrivi una funzione che dati due input:
>
>   - una frase da scrivere
>   - un'insieme di lettere
>
>  restituisca come output un booleano che indica se dato l'insieme di lettere è possibile scrivere il messaggio.
>
>  Assunzioni:
>
>  - messaggio e insieme contengono solo lettere minuscole dell'alfabeto inglese
>  - l'insieme contiene lettere ordinate in modo casuale (random)
>  - l'insieme di lettere potrebbe essere molto molto grande
>
>  Suggerimento: attento alla performance! Sai "misurarla"?

# Ripasso in TxT 
React e javascript in txt

## Numeri in JS
 JS è Case Sensitive e tipizzazione debole o dinamica  quando dichiaro una variabile  non ne specifici il tipo
    Ogni tipo di dato primitivo può essere convertito in un altro tipo di dato primitivo 
    Non ci sono distinzione di numeri decimali o interi --> var uno = 1.34;
    Si possono scirverei numeri in diverse basi es ottale o esadecimale --> var esadec = 0x123;
    --> ottale inizia con 0
    --> esadecimale con 0 e x 
    ogni evento che va al di fuori dell'intervallo genera due valori speciali 
    infinity e -infinity 
    NaN --> Not a Number --> valore numerico non definito 
    Null--> una varibaile non oggetto ne stringa ne numero  
    
    * - negazione 
    * ++ incremento
    * -- decremento
    * === strettamente uguale 
    * !== strettamente diverso 


## \n
 serve per andare a capo all'interno di una frase 
    posso  usarlo anche per mettere all'interno di una stringa ' senza terminare la stringa
    Es:  l\'altro ieri ho volato con l\'aereo 


## Variabili nome 

    Permesso : _ e $ 
    Non Permesso : numeri spazio . - ? !  


## Operatore

    * && --> and
        es: 5 > 2 && 3 ! 4 
    * || --> or
        true || ( 4 >= 6 )
    * !  --> not 
.        


## Array
var arraygiorni = [
    "lun",
    "mar",
];

var ArrayMisto = [123, "Ciaoo", true, null ];
##Array di Array
var ArrArr = [123, "stringa", ['a', 'b', 'c']];

## Array somma
function summ(){
    var z = arguments[2]+arguments[3];
    return z;
}

##Array Multidimensionali
array matrici esempio sottostanmte di matrice 3x3 di interi 
var matrice = [[12,34,21],[2,54,32],[37,54,6]]
Per accedere all'interno di un determinato elemnto sarà come 
var elementoPrecisoArrayPerIlDue = matrice[1][0] ## Partono da 0

## Obj 
var persona = {
    nome: "Marta",
    cognome: "Nove",
}

##, ? per assegnamenti condizionali 
 condizione ? valore : valore 2 
    se condizione è vera viene restituito valore 1 se falsa valore 2
    es:  
    x%2 == 0 ? "pari" : "dispari" 


## Operatori  di assegnamento composti

    x += 3; --> x = x + 3;
    "piano"+"forte"; --> pianoforte


## Operatori Bitwise
Trattano i valori numerici come sequenze di bit  
  * & --> and bitwise -- confronta i bit degli oerandi e restituisce 1 se entrambi i bit sono 1 altrimenti 0
  * | -->  or bitwise -- confronta a coppie i bit degli ooerandi e restituisce 1 se alemno uno dei bit è 1 altrimenti 0
  * * --> xor -- confronta a coppie i bit degli operandi e restituisce 1 se uno dei bit ma non entrambi, è 1 altrimenti e 0 
  * ~ --> not -- inverte il valore di ciascun numero
  * << --> left shift -- sposta di n valori verso sinistra la rappresentazione binaria di un numero 
  * >> --> right shift -- sposta di n valori verso destra la rappresentazione binaria di un numero 


## Forme Compatte
x += y --> x = x + y 
   x -= y --> x = x - y
   x *= y --> x = x * y
   x /= y --> x = x / y
   x %= y --> x = x % y
   var strumento = "piano";
   strumento += "forte";


##Conversioni tra tipi di variabili 

    undefined --> false
    null --> false 
    numero --> true in tutti i casi 
    stringa vuota --> false 
    stringa -->    true in tutti gli altri casi  


## Switch
var number = 1;
switch(number){
    case 1:
        console.log("uno");
    case 2:
        console.log("due");
}

## Funz
function somma(){
    var z= 11+2;
    return z;
}
var risultato = somma();

## Var Local VS Var Global
var numGlob = 4;
function functnumeroLocale(){
    var numeroLoc = 8;
    console.log(numeroLoc);
}
##Date e Orari 
var nuovaData = new Date("01/1/2012 15:30" )

##switch Data
var oggi = new Date();
var giorno;
switch (oggi.getDay()) {
    case 0:
        giorno = "Domenica";
    case 1:
        giorno = "Lunedi";
    case 3:
        giorno = "Martedì";
    case 4:
        giorno = "Mercoledì";
    case 5:
        giorno = "Giovedì";
    case 6:
        giorno = "venerdì";
    case 7:
        giorno = "Sabato";
    break;
}
console.log("Oggi è " + giorno)

##ARRAY per fars dare data attuale 
var giorno = ["lunedì", "martedì", "mercoledì", "giovedì", "venerdì", "sabato", "domenica"][new Date().getDay()];
console.log("Oggi è " + giorno);

##Per ottenere attuali giorno, mese, anno
getFullYear()	##Restituisce l'anno rappresentato con quattro cifre
getMonth()	##Restituisce il mese (da 0 a 11)
getDate()	##Restituisce il giorno del mese (da 1 a 31)
getDay()	##Restituisce il giorno della settimana (da 0 a 6)
getHours()	##Restituisce l'ora
getMinutes()	##Restituisce i minuti
getSeconds()	##Restituisce i secondi
getMilliseconds()	##Restituisce i millisecondi

##Per modificare la data 
setFullYear() ##Imposta l'anno di una data
setMonth()	##Imposta il mese di una data
setDate()	##Imposta il giorno del mese di unadata
setHours()	##Imposta l'ora di una data
setMinutes()	##Imposta i minuti di una data
setSeconds()	##Imposta i secondi di una data
setMilliseconds()	##Imposta i millisecondi di una data
setTime()	##Imposta data e ora specificandolain millisecondi rispetto al 1 Gennaio 1970

##Impostare giorno del prossimo anno
var dataAnnoProssimo = new Date();
dataAnnoProssimo.setFullYear(data.getFullYear() +1); 
console.log(data);

##Confronto tra date
var scadenza = new Date("2012, 11, 4");
var oggi = new Date();
if (oggi < scadenza) messaggio = "Non Scaduto";
if (oggi > scadenza) messaggio = "Scaduto";
console.log(messaggio);

##Convertire la data in una stringa
toDateString()	##Converte la componente data in stringa, escludendo l'ora
toISOString()	##Converte una data in stringa in formato ISO
toLocaleDateString()	##Converte la componente data in stringa, escludendo l'ora, secondo le impostazioni locali
toLocaleTimeString()	##Converte la componente ora in stringa, escludendo la data, secondo le impostazioni locali
toLocaleString()	##Converte una data in stringa secondo le impostazioni locali
toString()	##Converte una data in stringa
toTimeString()	##Converte la componente ora in stringa, escludendo la data
toUTCString()	##Converte una data UTC in stringa

## Funzioni anonime xxx riprendere
(function(x, y){
    return x + y;
}(4+8));

## parseInt 
La funzione parseInt() converte una stringa in un valore intero 
   prevede due parametri: il primo è la stringa da convertire, mentre il secondo 
   è opzionale e indica la base del sistema di rappresentazione numerica utilizzato.
 

## parseFloat 
La funzione prseFloat() 
   La funzione parseFloat() invece prevede un solo argomento e restituisce un valore numerico
   intero o decimale in base alla presenza del separatore decimale.


## typeof 
Serve per verificare il tipo della variabile 
  i tipi restituiti possono essere di diverso tipo : 
     string boolean number function object undefined xml
 
var prova = new function(){};
var numero = 1;
var carattere = "Salve";
console.log(typeof prova); ## ritorna "function"
console.log(typeof numero); ## ritorna "number"
console.log(typeof carattere); ##ritorna "string"








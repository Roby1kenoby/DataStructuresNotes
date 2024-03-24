* Concatenare Stringhe: usare il + 
* Cast dei tipi in automatico (solo da un tipo più piccolo ad uno grande, tipo da int a float, o da byte a int).
* È abbastanza furbo da cercare di fare il cast in automatico per accomodare eventuali operazioni che i dati base non permetterebbero (tipo somme di byte, che vanno da 0 a 256, che vanno oltre a 256 in un int)
```java
byte a = 40
byte b = 50
byte c = 100
int d = a * b / c
// funziona perchè sto mettendo il risultato in un int
```
* Posso anche convertire stringhe in int e viceversa
* Per convertire manualmente:
``` java
int num = (int)(10.5f)
```
* Uguaglianza indicata con == assegnazione con = 
* ATTENZIONE: Le copie degli oggetti sono copie del valore, non della reference. Quindi, se passo una variabile ad una funzione, nella funzione avrò il valore, e non la reference al valore.

```Java
int a = 10
int b = 20

reverse(a, b)

static int reverse(int a, int b){
		int temp = a;
		int b = a;
		int a = b;
```
b e a nella funzione fanno vita a se, non sono a e b al di fuori della funzione. Pertanto, al di fuori della funzione, a e b rimarranno invariati.
a e b nella funzione sono in un scope ridotto (la funzione)
* ATTENZIONE: quanto sopra, va bene per i tipi final (int, string ecc), ma per un Array invece no.
  Se passo un oggetto (per es un array) ad una funzione, sto passando il valore della reference (la reference vera e propria), e quindi se cambio qualcosa dentro la funzione, anche ciò che sta fuori verrà cambiato.
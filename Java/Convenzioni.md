Classi con prima lettera maiuscola, e in genere nominate public main

```java
public class Main{
    public static void main(String[] args){
       System.out.println("Hello World!");
	   // devo prima creare un oggeto Scanner per poter ricevere input
       Scanner input = new Scanner(System.in);
       System.out.println(input.next());
    }
}
```
Esempio di classe con funzione principale.
ATTENZIONE: è necessario nominare le classi pubbliche col nome del file.java o viceversa, altrimenti non funziona.

ATTENZIONE: ci deve essere sempre la funzione public static void main, è l'entry point del programma. Prima di quello non viene eseguito niente.
(args sono i parametri da linea di comando.)

Devo concludere ogni riga con ;

Scanner è la libreria per leggere informazioni.
System.out è per farle uscire, system.in è per farle entrare. Di default, input e output sono sul terminal, ma è possibile cambiare su qualsiasi altra fonte (file, ecc)






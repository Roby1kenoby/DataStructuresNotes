If
```java
if(true){
	System.out.println("Hello world");
}
else if{
	return
}
else{
	return
}
```
While (usare quando non so a priori quante volte dovrò eseguire l'operazione)
```java
int a = 0
while(a<10){
	System.out.println(a);
	a++;
}
/* con do - while, l'istruzione viene eseguita almeno una volta*/
int n = 1
do {
	System.out.println('Ciao');
}
while (n != 1)
```
For (usare quando invece so quante volte dovrò far girare)
```java
for(int c = 1; c != 5, c++){
	System.out.println(c);
}
```
Condizioni di uguaglianza
```Java
/* attenzione, che stiamo comparando delle reference, non direttamente i valori.*/
a == b 
```
Switch\\Case (non passa tutti i casi come l'if, ma va direttamente a quello che corrisponde)
```java
switch(variabile){
	case "Valore1":
		/*istruzioni*/
		/*il break fa uscire dal case*/)
		break;
	case "Valore2":
		/*istruzioni*/
		break;
	case "Valore3" -> /*istruzioni in formato arrow, più leggibili*/;
	case "Valore4", "Valore5", "Valore6" -> /*istruzioni valide per più case*/;
	default:
		/*ultime istruzioni, non serve il break*/
}
```
Attenzione, se dimentico un break in uno dei casi, lui va avanti ad eseguire anche quelli dopo.
Nella versione con -> non ho bisogno di metterli.

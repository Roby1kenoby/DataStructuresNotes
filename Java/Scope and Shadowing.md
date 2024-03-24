Block Scoping
```Java
int a = 10;
int b = 20;

{
	/*posso modificare il valore della reference a*/
	a = 78
	int c = 45
}
/* questo qui sotto va in errore perchè c esiste solo nello scope del blocco precednete*/
c = 123
```
Shadowing
```Java
public class Shadowing{
	// deve essere static perchè poi la uso in un metodo static
	static int x = 90; // questo valore verrà shadowed
	public static void main(String[] args){
		// qui dentro e in ogni sotto funzione posso utilizzare x
		system.out.println(x) // scriverà 90
		int x = 40
		system.out.println(x) // scriverà 40
	}	
}
```

```Java
public class Shadowing{
	// deve essere static perchè poi la uso in un metodo static
	static int x = 90; // questo valore verrà shadowed
	public static void main(String[] args){
		// qui dentro e in ogni sotto funzione posso utilizzare x
		system.out.println(x) // scriverà 90
		int x 
		system.out.println(x) // questo va in errore, perchè lo shadowing si attiva solo quando la variabile viene inizializzata con un valore. Sopra l'ho solo definita (ridefinita, rispetto alla definizione fuori da main)
		x = 40
		system.out.println(x) // scriverà 40
	}	
}
```

Variable Length Arguments (non so in anticipo quanti parametri riceverò)
```Java
public class Sum{
	public static void main(string[]args){
		fun(1,2,3,4,5,6,7,8)
	}
	static void fun(int ...v){
		// v è un array di lungheza variabile che contiene n parametri di tipo int, passati a runtime
	}
	static vodi fun2(int a, int b, String ...s){
		// così posso specificare i primi due parametri specifici int, e poi un nr variabile di stringhe
	}
}
```
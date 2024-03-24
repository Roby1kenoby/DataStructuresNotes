File .java -> compiler -> file .class (byte code) -> interpreter -> machine code

C'è una conversione intermedia che viene poi interpretata. Questo è comodo, perchè così mi basta avere l'interprete giusto per l'ambiente che mi interessa e posso usare lo stesso codice sorgente su ambiente diversi (linux, mac, windows, ecc), ottenendo l'indipendenza dalla piattaforma.

Per es, C++ salta la parte intermedia (va direttamente a machine code)
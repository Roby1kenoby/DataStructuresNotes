Come prima cosa aprire un git cmd e spostarsi nella cartella desiderata
* Git init: permette di inizializzare un repository
* Git status: elenca lo stato del repository (cosa è tracciato e cosa no)![[GitStatus.png]]
* Git add: aggiunge allo stage tutto quello che non è tracciato, se ci metto un . davanti. In alternativa se voglio mandare in stage singoli file, posso inserire i nomi dei singoli file.
* git commit: effettua il commit dei file in stage.
	* -m: parametro che contiene il messaggio di commit
	![[GitCommit.png]]
* git restore: effettua la rimozione dei file in stage.
	* --staged: posso passargli il nome file singolo, oppure . per tutti i file
* git log: fa vedere tutta la storia del repo
  ![[GitLog.png]]
* git reset: permette di riportare il repo ad uno specifico commit
	* hash: inserisco direttamente il codice univoco del commit, dopo reset: per indicare a quale commit devo tornare
	  ![[GirReset.png]]
	* --hard origine\\nomebranch: dopo aver fatto un fetch dei dati di un progetto forkato o clonato, mi permette di mettermi allo stesso livello con il repo locale 
* git stash: permette di prendere tutta una serie di cambiamenti e metterli non come commit, ma in un'area di "backstage", in modo che io possa richiamarli in qualsiasi momento, ma non influenzino il tree principale (inizio a fare delle modifiche per della roba alternativa a quello che devo fare, non le finisco, ma poi devo tornare al prog principale, che deve essere pulito).
	* devo prima fare add . comunque, per mandare in stage i file da stashare.
  ![[GitStash.png]]
	* pop: recupero la roba nel backstage e la rimette in stage
	* clear: pulisce i file che ci sono nel backstage
* gir remote: permette di collegare il repo locale con un repo online (github)
	* add origin: per indicare l'ulr del repo in cui scrivere
	* add upstream: permette di inserire un'altra origine remota che però non è la tua personale, ma è quella da cui prendi dei fork
	* -v: per visualizzare l'origin del repository locale
* git push: permette di mandare sul repo online i cambiamenti committati
	* origin: specifica l'url al quale inviare (definito prima con l'add origin)
		* master: il ramo su cui effettuare il commit. In atlernativa posso passare il nome di un altro branch che ho creato per pushare su quello
	* -f: serve per effettuare un force del repo online. In genere, se faccio un push e apro una pull request, si porta dietro tutti i commit. Se ne voglio rimuovere uno, faccio un reset al commit precedente, quindi faccio un push con -f per aggiornare la pull request allo stato corretto.
	* origin -d nomeramo: permette di rimuovere un ramo dal repo online
* git pull: permette di recuperare tutto quello che c'è di nuovo sul repo online
	* serve passare l'url del repository (se voglio recuperare tutto, se no ci sono comandi per parti specifiche)
	* è l'alternativa a fare il fetch + reset. Devo però cmq fare il push per sincronizzare il repo online
* git branch: crea un nuovo ramo per il repository (in genere non si committa mai sul main, per progetti condivisi e usati dalle pesone)
	* devo dare un nome al branch creato
* git checkout: mi permette di spostarmi su un branch
	* devo indicare il nome del branch su cui voglio spostarmi (anche il master è un branch)
* git merge: unisce un ramo al main
	* devo indicare il nome del ramo da cui fare il merge
* git clone: permette di clonare sulla tua macchina un repository
	* devo indicare come parametro l'url del repo online
* git remove: permette di cancellare dei rami locali
	* -d nomeramo: lo elimina solo se è mergiato col main
	* -D nomeramo: lo elimina anche se non è mergiato
* git fetch: permette di tirare giù da repo clonato e forkato i cambiamenti
	* --all: tutti i file
	* --prune: dopo all, anche quelli cancellati
* git rebase: permette di accorpare dei commit in un unico commit
	* -i hash versione (preso da log)
	* poi posso mettere una s davanti ai commit per accorparli
	* ![[GitSquash.png]]


Il processo è 
1) Nuove modifiche
2) Devono essere aggiunte allo stage
3) A questo punto posso effettuare il commit, per creare un hash unico delle aggiunte fatte
4) Posso poi collegare il repository locale con uno online
5) Quando voglio sincronizzare il locale con l'online, faccio un push
Ogni commit ha un suo hash, costruito sopra ai commit precedenti.

Non committare mai sul master.
==Fare sempre un branch, modificare su quello e poi richiedere un pull nel master branch.==
==Idealmente, fare un branch per ogni feature\\bug da implementare\\risolvere==


HEAD è dove sta puntando il git (dove verranno aggiunte le mie modifiche)
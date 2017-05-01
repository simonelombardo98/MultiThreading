# MultiThreading
JAVA Mutithreading per le classi 4te

Con questo progetto vorrei introdurre gli allievi delle 4te ai concetti di Programmazione Concorrente

## Cos'e' la con-correnza?
e' il verificarsi di eventi allo stesso tempo (contemporaneamente)

Pensiamo alla vita delle persone:
* piu' persone vivono nello stesso giorno
* ogni persona puo' fare piu' cose allo stesso tempo (es. studiare, ascoltare musica e giocare ad un videogioco...)
* in un bar affollato ci sono diversi baristi per smaltire la folla che vuole il caffe'
* mentre un ufficio svolge una pratica un altro ufficio ne svolge un'altra (non in Italia... dove nessun ufficio svolge qualcosa)

I sistemi informatici che sono uno strumento umano, e che si interfacciano con l'umanita' sono progettati per poter fare piu' di una cosa contemporaneamente.

In questo modo lo stesso utente puo' fare piu' cose al computer contemporaneamente (es. leggere email, ascoltare musica online, stampare documento) e piu' persone possono accedere allo stesso programma (facebook, mail, registro elettronico...)

Supponiamo che piu' utenti debbano usare il registro elettronico, se il programma fosse progettatto senza usare la programmazione concorrenziale (multithreading), solo un utente alla volta sarebbe in grado di accedervi.

Molto tempo e' usato dall'utente per inserire i dati o leggerli, e in quel tempo il programma non esegue nessun codice, non utilizzando (sprecando) la potenza di calcolo del computer in uso.

Se piu' utenti potessero accedere al registro di classe contemporaneamente, il computer, in attesa che un utente compia una certa azione, potrebbe eseguire il codice per soddisfare la richiesta di un altro utente.

In generale la Programmazione Concorrente porta ad un utilizzo piu' intelligente ed efficiente dello strumento informatico.

## Processo
e' un programma (flusso di istruzioni e dati) indipendente da un altro programma con cui non condividono nulla ...tranne la CPU

esempio: un programma di calcolo e un videogioco

uno strumento informatico che permette a piu' processi di essere in esecuzione contemporaneamete e' detto multi-processing

## Thread
e' una porzione di un programma che viene eseguito contemporaneamente ad altre porzioni dello stesso programma. 
![THREADs PIC](https://github.com/Prof-Matteo-Palitto-JCMaxwell/MultiThreading/blob/master/RopeThreds.png)

Spesso THREADs comunicano, condividono risorse, collaborano e hanno parte di codice in comune.

esempio: il registro elettronico che permette a piu' utenti di accedervi contemporaneamente

uno strumento informatico che permette a piu' processi di essere in esecuzione contemoporaneamete e' detto multi-threading


## Al fine di presentare i concetti di mutithreading in JAVA usero' due esempi

1. Multithread.java che vuole illustrare i seguenti concetti base:
 * 1. MAIN e' un thread come gli altri e quindi puo' terminare prima che gli altri
 * 2. Piu' THREADs vengono eseguiti allo stesso tempo
 * 3. THREADs possono essere interrotti e hanno la possibilita' di interrompersi in modo pulito
 * 4. THREADs possono essere definiti mediante una CLASSE che implementa un'INTERFACCIA Runnable
 * 5. THREADs possono essere avviati in modo indipendente da quando sono stati definiti
 * 6. posso passare parametri al THREADs tramite il costruttore della classe Runnable

2. FilosofiACena.java (Filosofi a cena) che vuole illustrare i seguenti concetti di comunicazione tra THREADs e condivisione di risorse:
 * 0. THREADs comunicano condividendo variabili
 * 1. MONITOR gestiscono attività di coordinamento e di accesso alle variabili tra più THREADs. 
 * 2. Le variabili dell'OGGETTO MONITOR sono le risorse da condividere tra THREADs
 * 3. Le attivita' CRITICHE che vengono fatte sulle variabili del MONITOR sono i metodi SINCRONIZZATI della classe MONITOR
 * 4. i THREADs ricevono il puntatore all'OGGETTO MONITOR e ne usano i metodi per accedere alle risorse
 * 5. la parola SYNCHRONIZED chiude l'accesso agli altri THREADs che vogliono usare la stessa risorsa (competizione)
 * 6. WAIT e' usato per mettere in attesa i THREADs che vogliono usare una risorsa OCCUPATA (collaborazione)
 * 7. NOTIFY[ALL] e' usato per comunicare ai THREADs quando la risorsa e' di nuovo disponibile (collaborazione)

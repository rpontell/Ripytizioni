# Ripytizioni
Testo ed esempi presi da https://codegrind.it/documentazione/python

## Documentazione base

### Esecuzione del Programma:
Apri un editor di testo o un ambiente di sviluppo integrato (IDE) che supporti Python e scrivi il codice
Salva il file con estensione .py (ad esempio, ciao.py).
Apri un terminale o prompt dei comandi.
Naviga nella directory in cui hai salvato il file.
Esegui il programma inserendo python ciao.py e premi Invio.

### Commenti
    #Questo è un commento in Python in singola riga
    print("Ciao, Mondo!")  # Stampa il messaggio sulla console

Commenti: In Python, i commenti sono righe che vengono ignorate dall’interprete e vengono utilizzate per fornire spiegazioni o note al codice. I commenti iniziano con il simbolo #.

I commenti multi-linea sono utili quando devi fornire spiegazioni più dettagliate su parti più estese di codice. Python non supporta commenti multi-linea tradizionali, ma puoi ottenere lo stesso effetto utilizzando triple virgolette (''' o """) all’inizio e alla fine del blocco di commento.

    '''
    Questo è un commento
    su più linee.
    Puoi scrivere qui
    spiegazioni più lunghe.
    '''

### Istruzione di Stampa
La funzione print() viene utilizzata per visualizzare testo o dati sulla console. 

### Indentazione in Python e Assenza del Punto e Virgola
In Python, a differenza di molti altri linguaggi di programmazione, l’indentazione svolge un ruolo fondamentale nella struttura del codice. L’indentazione è utilizzata per definire i blocchi di codice, come le istruzioni all’interno di cicli, funzioni e condizioni. Non vengono utilizzate parentesi graffe {} o punti e virgola ; per separare le istruzioni; invece, la struttura è determinata dall’uso corretto dell’indentazione.

    if x > 0:
        print("x è positivo")
        print("Questo è all'interno del blocco 'if'")  # Questo è allineato con il print precedente

    print("Questo è fuori dal blocco 'if'")  # Questo è allineato con la prima riga

L’indentazione definisce il blocco di codice all’interno dell’istruzione if x > 0:. Tutte le istruzioni all’interno di questo blocco devono essere allineate alla stessa distanza. Quando l’indentazione viene interrotta, il blocco di codice termina. L’ultima riga, print(“Questo è fuori dal blocco ‘if’”), non è indentata, quindi non fa parte del blocco if.

    a = 10
    b = 20
    print(a)
    print(b)

A differenza di molti linguaggi, Python non richiede l’uso del punto e virgola ; per separare le istruzioni. Ogni istruzione viene terminata automaticamente alla fine della riga.

### Creazione di Variabili
In Python, puoi creare una variabile assegnando un valore ad un nome. Non è necessario dichiarare il tipo di dato in anticipo. Le variabili devono essere inizializzate al momento della creazione 

    numero = 42
    testo = "Ciao, mondo!"

Le variabili in Python seguono alcune convenzioni per una migliore leggibilità e coerenza nel codice:

I nomi delle variabili possono contenere lettere, numeri e underscores _, ma devono iniziare con una lettera o un underscore.
I nomi delle variabili sono sensibili alle maiuscole e minuscole: nome e Nome sono considerate variabili diverse. -Usa nomi significativi che riflettano il contenuto o l’uso della variabile. Ad esempio, conto_bancario è più descrittivo di x.
Segui lo stile “snake_case” per separare le parole nei nomi delle variabili. Ad esempio, nome_completo anziché NomeCompleto.

### Assegnazione Multipla
Puoi assegnare valori a più variabili in una sola riga:

    x, y, z = 10, 20, 30

### Scambiare Valori tra Variabili:
È possibile scambiare i valori di due variabili senza una variabile temporanea:

    a = 5
    b = 10
    a, b = b, a  # Ora a è 10 e b è 5

### Costanti
Sebbene Python non abbia un tipo di dato “costante” come in altri linguaggi, puoi considerare i nomi in maiuscolo come convenzione per rappresentare costanti. Anche se i valori delle variabili possono essere cambiati, seguendo questa convenzione si indica che il valore dovrebbe rimanere immutato.
Le costanti seguono una convenzione di nomenclatura simile a quella delle variabili, ma vengono scritte in maiuscolo con underscores per separare le parole. Questo aiuta a identificare facilmente le costanti all’interno del codice.

    PI_GRECO = 3.14159265359
    LIMITE_VELOCITA = 100  # Ad esempio, il limite di velocità

    raggio = 5
    area_cerchio = PI_GRECO * (raggio ** 2)

Le costanti sono utilizzate per rappresentare valori che non cambieranno durante l’esecuzione del programma. Ad esempio, puoi utilizzare costanti per rappresentare parametri matematici, impostazioni globali o valori noti.

### Tipi di dati
Intero (int): Rappresenta numeri interi, positivi o negativi.

    numero_intero = 42

Numero in Virgola Mobile (float): Rappresenta numeri decimali.

    numero_virgola_mobile = 3.14

Stringa (str): Rappresenta sequenze di caratteri.

    testo = "Ciao, mondo!"

Booleano (bool): Rappresenta i valori di verità, True o False.

    condizione = True

Lista (list): Rappresenta una sequenza ordinata di valori.

    numeri = [1, 2, 3, 4, 5]

Tupla (tuple): Simile alle liste, ma immutabile.

    coordinate = (10, 20)

Set (set): Rappresenta una collezione non ordinata di valori unici.

    colori = {"rosso", "verde", "blu"}

Dizionario (dict): Rappresenta una mappa di chiavi e valori.

    persona = {"nome": "Alice", "età": 25}

Range (range): Rappresenta una sequenza di numeri.

    valori = range(0, 5)  # Genera una sequenza: 0, 1, 2, 3, 4

### Casting
Casting Implicito (Coercizione di Tipo):
Il casting implicito avviene automaticamente quando Python converte un tipo di dato in un altro in modo compatibile. Questo accade spesso durante le operazioni che coinvolgono tipi di dati diversi.

    numero_intero = 10
    numero_decimale = 3.14
    risultato = numero_intero + numero_decimale  # Casting implicito da intero a decimale
    print(risultato)  # Output: 13.14

Casting Esplicito (Conversione di Tipo)
Il casting esplicito, anche noto come conversione di tipo, implica la conversione manuale di un tipo di dato in un altro utilizzando funzioni integrate come int(), float(), str(), ecc.

    numero_come_stringa = "42"
    numero_intero = int(numero_come_stringa)  # Casting esplicito da stringa a intero
    print(numero_intero)  # Output: 42

Casting Comuni
int(x): Converte x in un intero.
float(x): Converte x in un decimale.
str(x): Converte x in una stringa.

### Output 
La funzione print() in Python consente di visualizzare i dati sullo schermo. Puoi passare variabili, stringhe e altri tipi di dati come argomenti

    nome = "Sara"
    età = 21

    print("Ciao,", nome, "!")
    print("Hai", età, "anni.")

Da come output: 

    Ciao, Alice!
    Hai 30 anni.

Puoi formattare l’output utilizzando le stringhe di formattazione, come ad esempio le f-string.

    nome = "Bob"
    punteggio = 85

    print(f"Il giocatore {nome} ha ottenuto un punteggio di {punteggio}.")

Da come output: 

    Il giocatore Bob ha ottenuto un punteggio di 85.

### Input 
La funzione input() ti consente di ottenere input dall’utente. L’input viene restituito come una stringa.

    nome = input("Inserisci il tuo nome: ")
    print("Ciao,", nome, "!")

Se l’utente inserisce “Riccardo”, l’output sarà:

    Inserisci il tuo nome: Riccardo
    Ciao, Riccardo!

## Esercizi documentazione base

Variabili
https://codegrind.it/esercizi/python/variabili

Costanti
https://codegrind.it/esercizi/python/costanti

Tipi di Dati
https://codegrind.it/esercizi/python/tipi-di-dati


## Operatori 

### Operatori aritmetici 
Addizione (+) usata per: 
sommare due numeri.

    a = 10
    b = 5
    somma = a + b
    print(somma)  # Output: 15

concatenare stringhe o unire liste.

    #Concatenazione di stringhe
    stringa1 = "Ciao, "
    stringa2 = "Mondo!"
    print(stringa1 + stringa2)  # Output: Ciao, Mondo!

    #Unione di liste
    lista1 = [1, 2, 3]
    lista2 = [4, 5]
    print(lista1 + lista2)  # Output: [1, 2, 3, 4, 5]

Sottrazione (-) usata per sottrarre un numero da un altro.

    a = 10
    b = 5
    sottrazione = a - b
    print(sottrazione)  # Output: 5

Moltiplicazione (*) usata per:
per moltiplicare due numeri.

    a = 10
    b = 5
    moltiplicazione = a * b
    print(moltiplicazione)  # Output: 50

ripetere stringhe o liste.

    #Ripetizione di una stringa
    stringa = "Python"
    print(stringa * 3)  # Output: PythonPythonPython

    #Ripetizione di una lista
    lista = [1, 2]
    print(lista * 3)  # Output: [1, 2, 1, 2, 1, 2]

Divisione (/)
restituisce il quoziente della divisione, sempre come numero in virgola mobile (float), anche se i numeri divisi sono interi.

    a = 10
    b = 4
    divisione = a / b
    print(divisione)  # Output: 2.5

Divisione Intera (//)
restituisce il quoziente intero della divisione, scartando la parte decimale.

    a = 10
    b = 4
    divisione_intera = a // b
    print(divisione_intera)  # Output: 2

Modulo (%)
restituisce il resto della divisione.

    a = 10
    b = 4
    resto = a % b
    print(resto)  # Output: 2

Potenza (**)
utilizzato per elevare un numero a una certa potenza.

    base = 2
    esponente = 3
    potenza = base ** esponente
    print(potenza)  # Output: 8

### Operatori di Assegnazione con Operatori Aritmetici
permettono di eseguire operazioni e assegnare il risultato in una singola espressione.
+= Somma e assegna

    x = 5
    x += 3  # Equivalente a x = x + 3
    print(x)  # Output: 8

-= Sottrai e assegna

    x = 5
    x -= 3  # Equivalente a x = x - 3
    print(x)  # Output: 2

*= Moltiplica e assegna
    x = 5
    x *= 3  # Equivalente a x = x * 3
    print(x)  # Output: 15

/= Dividi e assegna

    x = 5
    x /= 2  # Equivalente a x = x / 2
    print(x)  # Output: 2.5

//= Divisione intera e assegna

    x = 5
    x //= 2  # Equivalente a x = x // 2
    print(x)  # Output: 2

%= Modulo e assegna

    x = 5
    x %= 2  # Equivalente a x = x % 2
    print(x)  # Output: 1

**= Potenza e assegna

    x = 2
    x **= 3  # Equivalente a x = x ** 3
    print(x)  # Output: 8

### Operazioni con Numeri Complessi
I numeri complessi sono rappresentati con la notazione a + bj dove a è la parte reale e b è la parte immaginaria. Puoi usare gli stessi operatori aritmetici anche con numeri complessi.

    a = 1 + 2j
    b = 3 + 4j

    #Addizione
    somma = a + b
    print(somma)  # Output: (4+6j)

    #Moltiplicazione
    moltiplicazione = a * b
    print(moltiplicazione)  # Output: (-5+10j)

### Precedenza degli Operatori
Ecco un ordine di precedenza generale per gli operatori aritmetici (dal più alto al più basso):

** Potenza
*, /, //, % rispettivamente Moltiplicazione, divisione, divisione intera, modulo
+, - rispettivamente Addizione, sottrazione

La precedenza può essere modificata utilizzando le parentesi.

    risultato = 10 + 2 * 3
    print(risultato)  # Output: 16 (moltiplicazione prima dell'addizione)

    #Con parentesi
    risultato = (10 + 2) * 3
    print(risultato)  # Output: 36 (addizione prima della moltiplicazione)

### Operatori di Confronto
Uguaglianza (==): Verifica se due valori sono uguali.
Diversità (!=): Verifica se due valori sono diversi.
Maggiore (>): Verifica se il valore a sinistra è maggiore del valore a destra.
Minore (<): Verifica se il valore a sinistra è minore del valore a destra.
Maggiore o Uguale (>=): Verifica se il valore a sinistra è maggiore o uguale al valore a destra.
Minore o Uguale (<=): Verifica se il valore a sinistra è minore o uguale al valore a destra.

Gli operatori di confronto sono ampiamente utilizzati in condizioni, cicli e nell’elaborazione dei dati. Consentono di prendere decisioni basate su relazioni tra valori senza utilizzare dichiarazioni if.

### Operatori Logici
Operatore and 
L’operatore logico and restituisce True se entrambe le condizioni sono vere, altrimenti restituisce False.

    valore1 = 10
    valore2 = 5

    risultato = (valore1 > 5) and (valore2 < 8)  # True

Operatore or
L’operatore logico or restituisce True se almeno una delle condizioni è vera, altrimenti restituisce False.

    valore1 = 3
    valore2 = 8

    risultato = (valore1 > 5) or (valore2 < 5)  # False

Operatore not
L’operatore logico not restituisce il valore opposto di una condizione. Se la condizione è vera, restituirà False, e viceversa.

    valore = 7

    risultato = not (valore > 5)  # False

Python legge gli operatori in generale da sinistra a destra e verifica sequenzialmente le condizioni se sono Vere o False
Ciò significa che se una condizione è falsa, Python non valuterà le condizioni successive.

### Operatore di Assegnazione
L’operatore = assegna il valore a destra alla variabile a sinistra.

### Operatori di Appartenenza
permettono di verificare se un determinato valore o oggetto è presente in una sequenza, come una lista, una stringa, un dizionario o un set. 

L’Operatore in
restituisce True se l’elemento è presente nell’iterabile specificato altrimenti restituisce False.
Sintassi: elemento in iterabile

es lista

    numeri = [1, 2, 3, 4, 5]

    #Verifica se il numero 3 è presente nella lista
    if 3 in numeri:
        print("3 è nella lista.")
    else:
        print("3 non è nella lista.")
    
    #OUT: 3 è nella lista.

es stringa

    frase = "Benvenuto in Python"

    #Verifica se la parola "Python" è presente nella stringa
    if "Python" in frase:
        print("La parola 'Python' è presente.")
    else:
        print("La parola 'Python' non è presente.")

    #OUT: La parola 'Python' è presente.

L’Operatore not in
restituisce True se l’elemento non è presente nell’iterabile, altrimenti restituisce False.
Sintassi: elemento not in iterabile

es lista 

    numeri = [1, 2, 3, 4, 5]

    #Verifica se il numero 6 non è presente nella lista
    if 6 not in numeri:
        print("6 non è nella lista.")
    else:
        print("6 è nella lista.")

    #OUT: 6 non è nella lista.

es stringa

    frase = "Python è potente"

    #Verifica se la parola 'Java' non è presente nella stringa
    if "Java" not in frase:
        print("La parola 'Java' non è presente nella frase.")

    #OUT: La parola 'Java' non è presente nella frase.

## Esercizi operatori

Operatori Matematici
https://codegrind.it/esercizi/python/operatori-matematici

Metodi Stringhe
https://codegrind.it/esercizi/python/metodi-stringhe

Formattazione Stringhe
https://codegrind.it/esercizi/python/formattazione-stringhe

Liste
https://codegrind.it/esercizi/python/liste

Dizionari
https://codegrind.it/esercizi/python/dizionari

Tuple
https://codegrind.it/esercizi/python/tuple

Set
https://codegrind.it/esercizi/python/set

## Controllo del flusso

### Condizionali IF

Istruzione if

    if condizione:
        #Blocco di codice da eseguire se la condizione è vera
..............................

    età = 18

    if età >= 18:
        print("Sei maggiorenne")

Istruzione else
viene utilizzata per eseguire un blocco di codice quando la condizione dell’istruzione if è falsa.

    età = 15

    if età >= 18:
        print("Sei maggiorenne")
    else:
        print("Sei minorenne")

Istruzione elif
viene utilizzata per gestire più condizioni alternative. Puoi usarla dopo l’istruzione if o dopo un’altra istruzione elif.

    punteggio = 85

    if punteggio >= 90:
        print("Hai ottenuto un A")
    elif punteggio >= 80:
        print("Hai ottenuto un B")
    elif punteggio >= 70:
        print("Hai ottenuto un C")
    else:
        print("Hai ottenuto un voto inferiore a C")

Istruzioni if Annidate
Puoi annidare istruzioni if all’interno di altre istruzioni if, else o elif.

    età = 18
    documento = True

    if età >= 18:
        if documento:
            print("Puoi accedere al locale")
        else:
            print("Devi avere un documento")
    else:
        print("Sei minorenne, non puoi accedere")

### Operatori Logici con l’Istruzione if
Puoi utilizzare gli operatori logici and, or e not all’interno delle condizioni dell’istruzione if per creare espressioni condizionali più complesse.

    età = 17
    documento = False

    if età >= 18 and documento:
        print("Puoi accedere al locale")
    else:
        print("Non puoi accedere")

o combinazioni di operatori logici

    valore = 15

    if (valore > 10 or valore < 5) and not valore == 12:
        print("La condizione è vera")

## Esecizi controllo flusso 
https://codegrind.it/esercizi/python/condizionali-if

## Cicli e Iterazioni

### Ciclo While
consente di eseguire un blocco di codice ripetutamente fintanto che una certa condizione è vera. Questo tipo di ciclo è ideale quando il numero di iterazioni non è noto in anticipo. 

    while condizione:
        #Blocco di codice da eseguire finché la condizione è vera
...............................

    contatore = 0
    while contatore < 5:
        print("Iterazione:", contatore)
        contatore += 1
In questo esempio, il blocco di codice all’interno del ciclo while verrà eseguito finché la condizione contatore < 5 è vera. Ogni volta che il blocco viene eseguito, il valore del contatore viene incrementato di 1.

### Ciclo while Infinito
Attenzione ai cicli while infiniti, in cui la condizione non diventa mai falsa. Questo può causare l’esecuzione continua del blocco di codice, bloccando il programma.
    while True:
        print("Questo è un ciclo infinito!")

### Cicli Annidati e Cicli con Istruzioni Condizionali
Puoi annidare cicli while all’interno di altri cicli while o all’interno di strutture di controllo come le istruzioni if per gestire situazioni più complesse.
Esempio di Ciclo Annidato:

    fila = 1
    while fila <= 3:
        posto = 1
        while posto <= 5:
            print("Fila:", fila, "- Posto:", posto)
            posto += 1
        fila += 1

Esempio di Ciclo con Istruzione Condizionale:

    contatore = 0
    while contatore < 10:
        if contatore % 2 == 0:
            print(contatore, "è pari")
        else:
            print(contatore, "è dispari")
        contatore += 1

### Ciclo For
iterare su una sequenza di elementi, come una lista, una stringa o una sequenza numerica. Questa struttura di controllo consente di eseguire un blocco di codice per ogni elemento nella sequenza.

    for elemento in sequenza:
        # Blocco di codice da eseguire per ogni elemento nella sequenza
.........................
Esempio con Lista:

    numeri = [1, 2, 3, 4, 5]
    for numero in numeri:
        print(numero)

il blocco di codice all’interno del ciclo for verrà eseguito per ogni numero nella lista numeri.

Esempio con Stringa:

    parola = "Python"
    for carattere in parola:
        print(carattere)

il ciclo for itera su ogni carattere nella stringa parola e ne stampa uno alla volta.

Esempio con Range:

    for numero in range(5):
        print(numero)

il ciclo for utilizza la funzione range per generare una sequenza di numeri da 0 a 4 e li stampa.

### Iterazione con Indice
Puoi utilizzare la funzione enumerate per ottenere sia l’elemento che l’indice durante l’iterazione.

    parole = ["ciao", "mondo", "python"]
    for indice, parola in enumerate(parole):
        print("Indice:", indice, "- Parola:", parola)

### Cicli Annidati
Puoi annidare cicli for all’interno di altri cicli for o all’interno di strutture di controllo come le istruzioni if per gestire situazioni più complesse.

    for i in range(3):
        for j in range(3):
            print("i:", i, "- j:", j)

### Utilizzo di range in Cicli
La funzione range è spesso utilizzata per generare sequenze numeriche per l’iterazione nei cicli for.

    for numero in range(1, 6):
        print(numero)

### Break e Continue
Se necessiti di un Break nel tuo codice consiglio di rivederee modificarlo

## Esecizi Cicli

Ciclo For
https://codegrind.it/esercizi/python/ciclo-for

Ciclo While
https://codegrind.it/esercizi/python/ciclo-while

## Funzioni
Le funzioni sono uno strumento essenziale nella programmazione Python che ti consente di raggruppare e organizzare il codice in blocchi riutilizzabili. Una funzione è un insieme di istruzioni che può essere chiamato con un nome per eseguire un’azione specifica.

### Definizione
utilizzando la parola chiave def, seguita dal nome della funzione e le parentesi tonde (). È possibile definire parametri all’interno delle parentesi, che rappresentano i dati che la funzione accetta.

    def nome_funzione(parametro1, parametro2, ...):
        #Blocco di codice della funzione
        #Può contenere istruzioni e calcoli
        return risultato
.....................

    def saluta(nome):
        messaggio = "Ciao, " + nome
        print(messaggio)

### Chiamata 
utilizzando il suo nome seguito dalle parentesi tonde ().

    nome_funzione(argomento)
.....................

    saluta("Alice")

### Tipi di parametri
I parametri sono dati che possono essere passati alla funzione quando viene chiamata. Puoi definire quanti parametri desideri all’interno delle parentesi della definizione della funzione.

    def somma(a, b):
        risultato = a + b
        return risultato

Parametri posizionali: 
sono i parametri di una funzione il cui valore viene determinato dall’ordine in cui vengono passati.

    def somma(a, b):
        return a + b

    print(somma(5, 10))  # Output: 15

In questo caso, i valori 5 e 10 vengono associati ai parametri a e b in base all’ordine in cui sono passati.

Parametri con nome: 
vengono passati specificando esplicitamente il nome del parametro. Questo rende il codice più leggibile e permette di passare gli argomenti in un ordine diverso da quello dei parametri nella definizione della funzione.

    def informazioni_persona(nome, eta):
        print(f"Nome: {nome}, Età: {eta}")

    informazioni_persona(nome="Anna", eta=30)  # Output: Nome: Anna, Età: 30
    informazioni_persona(eta=25, nome="Luca")  # Output: Nome: Luca, Età: 25

In questo esempio, l’ordine degli argomenti non è importante, poiché specifichiamo esplicitamente il nome del parametro.

Parametri con valori predefiniti:
se un argomento non viene passato, il parametro assuma un valore predefinito.

    def informazioni_persona(nome, eta=18):
        print(f"Nome: {nome}, Età: {eta}")

    informazioni_persona("Giulia")  # Output: Nome: Giulia, Età: 18
    informazioni_persona("Marco", 25)  # Output: Nome: Marco, Età: 25

In questo caso, se non fornisci un valore per eta, verrà utilizzato il valore predefinito di 18.

Parametri Variabili: *args e **kwargs
A volte potrebbe essere necessario definire una funzione che accetta un numero variabile di argomenti. Per gestire questa situazione, Python offre i parametri speciali *args e **kwargs.

Ordine dei Parametri:
Quando definisci una funzione con diversi tipi di parametri, l’ordine è importante:

Parametri Posizionali
Parametri con Valori Predefiniti
Parametri Variabili (*args)
Parametri con Nome Variabili (**kwargs)

### Tipi di Argomenti
Argomenti Posizionali: 
Gli argomenti vengono passati in base alla posizione, nell’ordine in cui sono definiti nella firma della funzione.

Argomenti per Parola Chiave: 
Gli argomenti vengono passati utilizzando il nome del parametro corrispondente, consentendo di specificare l’ordine in modo esplicito.

Argomenti Arbitrari: 
Puoi utilizzare l’operatore * per accettare un numero arbitrario di argomenti posizionali.

    def stampa_args(*args):
        for arg in args:
            print(arg)

Argomenti per Parola Chiave Arbitrari: 
Puoi utilizzare l’operatore ** per accettare un numero arbitrario di argomenti per parola chiave.

    def stampa_kwargs(**kwargs):
        for chiave, valore in kwargs.items():
            print(chiave, valore)

Argomenti come Liste:
Puoi passare liste come argomenti alle funzioni e manipolarle all’interno della funzione stessa.

    def raddoppia_elementi(lista):
        for indice in range(len(lista)):
            lista[indice] *= 2
        return lista

### Ritorno da una Funzione
Una funzione può restituire un valore utilizzando l’istruzione return. Puoi specificare quale valore restituire quando la funzione viene chiamata.

    def somma(a, b):
        return a + b

    risultato = somma(5, 3)
    print(risultato)  # Output: 8

La funzione somma restituisce il risultato della somma di a e b utilizzando return.
Il valore di ritorno viene assegnato alla variabile risultato, che viene poi stampata.

Non tutte le funzioni devono restituire un valore. Se una funzione non include return, restituisce automaticamente None. Questo è utile per funzioni che eseguono un’azione, ma non devono restituire un risultato.

    def saluta(nome):
        print(f"Ciao, {nome}!")

    risultato = saluta("Anna")
    print(risultato)  # Output: Ciao, Anna! \n None

In questo caso, saluta non restituisce un valore esplicito, quindi risultato assume il valore predefinito None.

Puoi restituire più valori da una funzione utilizzando le tuple. Questo è particolarmente utile quando una funzione deve calcolare e restituire più risultati.

    def operazioni(a, b):
        somma = a + b
        differenza = a - b
        prodotto = a * b
        return somma, differenza, prodotto

    risultato = operazioni(10, 5)
    print(risultato)  # Output: (15, 5, 50)

In questo esempio, la funzione operazioni restituisce tre valori: la somma, la differenza e il prodotto di a e b. I valori vengono raccolti in una tupla e assegnati alla variabile risultato.

Una funzione può restituire valori diversi in base a condizioni specifiche all’interno della funzione. Questo può essere utile per gestire casi diversi senza dover scrivere più funzioni.

    def controlla_parita(numero):
        if numero % 2 == 0:
            return "Pari"
        else:
            return "Dispari"

    print(controlla_parita(10))  # Output: Pari
    print(controlla_parita(7))   # Output: Dispari

Qui, la funzione controlla_parita restituisce una stringa diversa a seconda che il numero sia pari o dispari.

### Ricorsione
La ricorsione è una tecnica in cui una funzione richiama se stessa per risolvere un problema. Questa tecnica è spesso utilizzata per problemi che possono essere suddivisi in sottoproblemi simili.
Una funzione ricorsiva è una funzione che richiama se stessa all’interno del proprio corpo. Quando si utilizza la ricorsione, è fondamentale avere una condizione di uscita (o caso base) per evitare di entrare in un ciclo infinito di chiamate ricorsive.

Una funzione ricorsiva segue solitamente questa struttura

Caso base: La condizione che termina la ricorsione.
Chiamata ricorsiva: La funzione richiama se stessa con un input modificato, avvicinandosi al caso base.

    def conta(n):
        if n <= 0:  # Caso base
            return
        else:
            conta(n - 1)  # Chiamata ricorsiva
            print(n)

    conta(5)
    #OUT:
    #1
    #2
    #3
    #4
    #5

In questo esempio la funzione conta richiama se stessa con un valore ridotto (n - 1), avvicinandosi al caso base (n <= 0).
Quando la ricorsione raggiunge il caso base, la funzione termina, e i numeri vengono stampati nell’ordine corretto.

antaggi
Semplicità: La ricorsione può semplificare la soluzione di problemi complessi che hanno una struttura naturale ricorsiva, come alberi, grafi e sequenze.
Eleganza: Spesso, le soluzioni ricorsive risultano più eleganti e più concise rispetto alle soluzioni iterative.
Svantaggi
Prestazioni: Le funzioni ricorsive possono essere meno efficienti delle soluzioni iterative, soprattutto se non sono ottimizzate con tecniche come la memorizzazione (memoization).
Stack Overflow: Le chiamate ricorsive consumano memoria nello stack di chiamate. Senza una condizione di uscita, si rischia di esaurire lo spazio dello stack, causando un errore di ricorsione infinita.

La funzione fattoriale può essere scritta ricorsivamente come segue:

    def fattoriale(n):
        if n == 0:  # Caso base
            return 1
        else:
            return n * fattoriale(n - 1)  # Chiamata ricorsiva

    print(fattoriale(5))  # Output: 120

Ecco una funzione ricorsiva per calcolare il numero di Fibonacci n-esimo:

    def fibonacci(n):
        if n == 0:  # Caso base
            return 0
        elif n == 1:  # Caso base
            return 1
        else:
            return fibonacci(n - 1) + fibonacci(n - 2)  # Chiamata ricorsiva

    print(fibonacci(6))  # Output: 8

Spesso un problema che può essere risolto con la ricorsione può anche essere risolto con un approccio iterativo, come i loop for o while.

In generale:
La ricorsione può essere più intuitiva per problemi che hanno una struttura naturale ricorsiva, come la traversata di alberi.
L’iterazione è generalmente più efficiente dal punto di vista delle prestazioni e meno soggetta a problemi di memoria.

### Scope Variaibili
In Python, le variabili possono essere definite sia nell’ambito locale che in quello globale. L’ambito di una variabile definisce dove è accessibile e modificabile.

Ambito Locale
Una variabile definita all’interno di una funzione è considerata locale a quella funzione. Questa variabile è accessibile solo all’interno della funzione stessa e non è visibile da altre parti del codice al di fuori di quella funzione.

    def mia_funzione():
        variabile_locale = "Sono locale"
        print(variabile_locale)

    mia_funzione()
    # Stampa: "Sono locale"

    # La seguente riga causerebbe un errore poiché variabile_locale non è definita qui
    # print(variabile_locale)

Ambito Globale
Una variabile definita al di fuori di qualsiasi funzione è considerata globale e può essere accessibile da qualsiasi parte del codice, comprese le funzioni. Tuttavia, se desideri modificare una variabile globale all’interno di una funzione, dovrai utilizzare la parola chiave global per indicare che stai facendo riferimento alla variabile globale.

    variabile_globale = "Sono globale"

    def mia_funzione():
        global variabile_globale
        variabile_globale = "Modificato all'interno della funzione"

    mia_funzione()
    print(variabile_globale)
    # Stampa: "Modificato all'interno della funzione"

Quando si utilizzano variabili sia locali che globali con lo stesso nome, l’ambito locale avrà la priorità all’interno della funzione. Se non esiste una variabile locale con lo stesso nome, Python cercherà la variabile nel contesto globale.

## Esercizi funzioni
https://codegrind.it/esercizi/python/funzioni

## Programmazione ad oggetti
La Programmazione Orientata agli Oggetti (OOP) è un paradigma di programmazione che consente di organizzare e strutturare il codice in modo più modulare e intuitivo. In OOP, i concetti del mondo reale sono rappresentati da “oggetti” e “classi”, che contengono attributi (proprietà) e metodi (azioni). Python è un linguaggio che supporta pienamente la programmazione orientata agli oggetti e ci offre strumenti potenti per creare, utilizzare e manipolare oggetti. Esploriamo i concetti fondamentali dell’OOP in Python.

### Oggetti e Classi
In OOP, un “oggetto” è un’istanza di una “classe”. Una “classe” è un modello o una definizione di un oggetto. Gli oggetti rappresentano elementi del mondo reale e le classi ne definiscono la struttura e il comportamento. 
Ad esempio, possiamo avere una classe “Automobile” che definisce le proprietà (marca, modello, colore) e i metodi (accelerare, frenare) di un’automobile.
Creare una Classe  

    class Automobile:
        marca = ""
        modello = ""
        colore = ""

        def accelerare(self):
            print("Sto accelerando")

        def frenare(self):
            print("Sto frenando")

Creare un Oggetto

    auto1 = Automobile()
    auto2 = Automobile()

Le “proprietà” rappresentano gli attributi di un oggetto, come colore, marca, ecc. 
I “metodi” sono le azioni che un oggetto può eseguire, come accelerare, frenare, ecc.

    auto1.marca = "Toyota"
    auto1.modello = "Corolla"
    auto1.colore = "Rosso"
    auto1.accelerare()  # Stampa: "Sto accelerando"

    auto2.marca = "Ford"
    auto2.modello = "Mustang"
    auto2.colore = "Blu"
    auto2.frenare()  # Stampa: "Sto frenando"

Un costruttore è un metodo speciale chiamato automaticamente quando si crea un nuovo oggetto dalla classe. In Python, il costruttore predefinito è \__init__. È utilizzato per inizializzare le proprietà dell’oggetto.

    class Persona:
        def __init__(self, nome, età):
            self.nome = nome
            self.età = età

    persona1 = Persona("Alice", 30)
    persona2 = Persona("Bob", 25)

Puoi modificare o eliminare le proprietà di un oggetto dopo averlo creato.
    auto1.colore = "Nero"  # Modifica la proprietà "colore" di auto1
    del auto2.colore  # Elimina la proprietà "colore" di auto2

La keyword self si riferisce all’oggetto stesso e viene utilizzata all’interno dei metodi di una classe per accedere alle proprietà e ai metodi dell’oggetto.

    class Automobile:
        # ... altre definizioni di classe ...

        def accelerare(self):
            print(f"{self.marca} {self.modello} sta accelerando")

### Modificatori di accesso
I modificatori di accesso definiscono il livello di visibilità e accessibilità degli attributi e dei metodi all’interno di una classe in Python. Sebbene Python non abbia modificatori di accesso “veri e propri” come altri linguaggi, utilizza delle convenzioni per controllare l’accesso agli attributi e ai metodi.

Public Access (Accesso Pubblico)
In Python, gli attributi e i metodi sono pubblici per impostazione predefinita, il che significa che possono essere accessibili da qualsiasi parte del codice, sia all’interno che all’esterno della classe.

    class Persona:
        nome = "Alice"

    persona = Persona()
    print(persona.nome)  # Accesso pubblico: "Alice"

Protected Access (Accesso Protetto)
Python utilizza una convenzione per segnalare che un attributo o un metodo dovrebbe essere trattato come “protetto”. Un attributo o metodo protetto inizia con un singolo underscore _.

    class Persona:
        _nome = "Alice"  # Attributo protetto

    persona = Persona()
    print(persona._nome)  # Accesso protetto: "Alice"

Anche se è possibile accedere agli attributi protetti dall’esterno della classe, è consigliato trattarli come se fossero privati.

Private Access (Accesso Privato)
Anche se Python non impedisce l’accesso agli attributi o ai metodi privati dall’esterno della classe, utilizza una convenzione per segnalare che questi dovrebbero essere trattati come “privati”. Gli attributi o metodi privati iniziano con due underscore __.

    class Persona:
        __nome = "Alice"  # Attributo privato

    persona = Persona()
    # Il seguente causerebbe un errore poiché __nome è considerato privato
    # print(persona.__nome)

Getter e Setter
Per modificare o recuperare attributi protetti o privati, è comune utilizzare metodi getter e setter.

    class Persona:
        def __init__(self, nome):
            self.__nome = nome

        def get_nome(self):
            return self.__nome

        def set_nome(self, nuovo_nome):
            self.__nome = nuovo_nome

    persona = Persona("Alice")
    print(persona.get_nome())  # Recupero attributo privato tramite metodo getter
    persona.set_nome("Bob")    # Imposto attributo privato tramite metodo setter

### Ereditarietà
L’ereditarietà è il processo attraverso il quale una classe figlia acquisisce gli attributi e i metodi della classe genitore. La classe genitore è spesso chiamata “superclasse” o “classe base”, mentre la classe figlia è chiamata “sottoclasse” o “classe derivata”.
Per creare una classe derivata da una classe base, la classe figlia deve essere definita con il nome della classe genitore tra parentesi. La classe figlia può quindi accedere agli attributi e ai metodi della classe genitore.

    class Veicolo:
        def __init__(self, marca):
            self.marca = marca

        def descrizione(self):
            return f"Questo è un veicolo di marca {self.marca}"

    class Automobile(Veicolo):
        pass

    auto = Automobile("Toyota")
    print(auto.descrizione())  # "Questo è un veicolo di marca Toyota"

L’ereditarietà consente di evitare la duplicazione del codice, poiché le classi figlie possono ereditare le funzionalità dalla classe genitore. Ciò promuove la riutilizzabilità e semplifica la manutenzione del codice.

### Polimorfismo
Il polimorfismo è un concetto fondamentale nell’ambito della programmazione orientata agli oggetti che si riferisce alla capacità di oggetti di classi diverse di rispondere a un medesimo metodo in modo diverso. Questo concetto favorisce la modularità, la flessibilità e la riutilizzabilità del codice. Esploriamo come il polimorfismo si manifesta attraverso le classi e l’ereditarietà in Python.
Nelle classi, il polimorfismo può essere realizzato mediante l’implementazione di metodi con lo stesso nome in diverse classi. Ogni classe può definire il proprio comportamento per il metodo.

    class Cane:
        def verso(self):
            return "Abbau abbau!"

    class Gatto:
        def verso(self):
            return "Miao miao!"

    animali = [Cane(), Gatto()]

    for animale in animali:
        print(animale.verso())

In questo esempio, sia la classe Cane che la classe Gatto hanno un metodo verso(). Sebbene abbiano nomi di metodo identici, producono output diversi.

Il polimorfismo viene ampliato nell’ereditarietà, dove classi derivate possono sovrascrivere i metodi della classe genitore per fornire comportamenti specifici.

    class Veicolo:
        def suona_clacson(self):
            return "Beep beep!"

    class Automobile(Veicolo):
        def suona_clacson(self):
            return "Tut tut!"

    class Camion(Veicolo):
        def suona_clacson(self):
            return "Honk honk!"

    veicoli = [Automobile(), Camion()]

    for veicolo in veicoli:
        print(veicolo.suona_clacson())

Qui, Automobile e Camion sono sottoclassi di Veicolo e sovrascrivono il metodo suona_clacson() della classe genitore.

Vantaggi del Polimorfismo
Riutilizzo del Codice: Il polimorfismo permette di utilizzare interfacce comuni e codice condiviso tra diverse classi.
Flessibilità: Le classi possono essere scambiate senza modificare il codice che le utilizza, purché rispettino le interfacce comuni.
Estensibilità: È possibile aggiungere nuove classi senza alterare il codice esistente, a condizione che rispettino le interfacce richieste.

## Esecizi OOP

Iteratori
https://codegrind.it/esercizi/python/iteratori

Classi
https://codegrind.it/esercizi/python/classi

Ereditarietà
https://codegrind.it/esercizi/python/ereditarieta

## Moduli
Un modulo in Python è un file che contiene definizioni di funzioni, classi e variabili. I moduli permettono di organizzare il codice in unità logiche e indipendenti.

Per utilizzare un modulo in un altro file, è necessario importarlo. Ciò consente di accedere a tutte le definizioni all’interno del modulo.

    import mio_modulo
    
    nome = "Alice"
    saluto = mio_modulo.saluta(nome)
    
    print(saluto)
    print(f"Pi greco è approssimativamente {mio_modulo.pi_greco}")

### Modulo Math
Il modulo math offre varie funzioni che coprono una vasta gamma di operazioni matematiche. Ecco alcune delle funzioni comuni:

math.sqrt(x): Calcola la radice quadrata di x.
math.exp(x): Calcola il valore esponenziale di x.
math.log(x, base): Calcola il logaritmo naturale di x con una base specificata opzionalmente.
math.sin(x), math.cos(x), math.tan(x): Calcola il seno, il coseno e la tangente trigonometrica di x.
math.radians(x), math.degrees(x): Converti tra gradi e radianti.
math.pi e math.e: Costanti per π (pi greco) e la base del logaritmo naturale (e).

    import math
    
    # Calcola la radice quadrata
    risultato_radice = math.sqrt(25)
    print("Radice quadrata di 25:", risultato_radice)
    
    # Calcola il valore esponenziale
    risultato_esponenziale = math.exp(2)
    print("Valore esponenziale di 2:", risultato_esponenziale)
    
    # Calcola seno e coseno
    angolo = math.radians(30)  # Converti gradi in radianti
    risultato_seno = math.sin(angolo)
    risultato_coseno = math.cos(angolo)
    print("Seno di 30 gradi:", risultato_seno)
    print("Coseno di 30 gradi:", risultato_coseno)

Il modulo math fornisce anche funzioni avanzate come funzioni trigonometriche, logaritmiche, statistiche e speciali.

    import math
    
    # Calcola il fattoriale
    risultato_fattoriale = math.factorial(5)
    print("Fattoriale di 5:", risultato_fattoriale)
    
    # Calcola il valore di π (pi greco)
    valore_pi = math.pi
    print("Valore di π:", valore_pi)
    
    # Calcola il massimo comune divisore (MCD)
    risultato_mcd = math.gcd(30, 45)
    print("MCD di 30 e 45:", risultato_mcd)

### Modulo Random
Il modulo random di Python fornisce strumenti per generare numeri casuali, mescolare sequenze, selezionare elementi casuali da una lista e molto altro.

#### Funzioni Principali del Modulo random

1. random.random(): Generare un Numero Decimale Casuale tra 0 e 1
La funzione random.random() restituisce un numero in virgola mobile casuale compreso tra 0.0 e 1.0.

        import random
        
        numero_casuale = random.random()
        print(numero_casuale)  # Output: un numero tra 0.0 e 1.0

2. random.randint(a, b): Generare un Numero Intero Casuale
La funzione random.randint(a, b) restituisce un numero intero casuale compreso tra a e b (inclusi).

        numero_intero = random.randint(1, 10)
        print(numero_intero)  # Output: un numero intero tra 1 e 10 (incluso)

3. random.choice(seq): Selezionare un Elemento Casuale da una Lista
La funzione random.choice(seq) restituisce un elemento casuale da una sequenza, come una lista o una stringa.

        lista = ['apple', 'banana', 'cherry ]
        elemento_casuale = random.choice(lista)
        print(elemento_casuale)  # Output: un elemento casuale dalla lista

4. random.choices(population, k): Selezionare Più Elementi Casuali
La funzione random.choices(population, k) seleziona una lista di k elementi casuali dalla sequenza population, con ripetizione.

        frutti = ['apple', 'banana', 'cherry', 'orange']
        scelte_casuali = random.choices(frutti, k=3)
        print(scelte_casuali)  # Output: una lista di 3 elementi casuali dalla lista originale

5. random.sample(population, k): Selezionare Più Elementi Casuali Senza Ripetizione
La funzione random.sample(population, k) restituisce una lista di k elementi casuali dalla sequenza population, senza ripetizione.

        frutti = ['apple', 'banana', 'cherry', 'orange']
        campione_casuale = random.sample(frutti, k=2)
        print(campione_casuale)  # Output: una lista di 2 elementi casuali senza ripetizione

6. random.uniform(a, b): Generare un Numero Decimale Casuale tra Due Limiti
La funzione random.uniform(a, b) restituisce un numero decimale casuale compreso tra a e b (inclusi).

        decimale_casuale = random.uniform(1.5, 5.5)
        print(decimale_casuale)  # Output: un numero decimale tra 1.5 e 5.5

7. random.shuffle(seq): Mescolare una Lista
La funzione random.shuffle(seq) mescola gli elementi di una lista in place.

        frutti = ['apple', 'banana', 'cherry', 'orange']
        random.shuffle(frutti)
        print(frutti)  # Output: una lista con gli elementi in ordine casuale

8. random.randrange(start, stop[, step]): Generare un Numero Intero con Intervallo
La funzione random.randrange(start, stop[, step]) restituisce un numero intero casuale tra start e stop, con uno step opzionale. Il numero stop non è incluso nell’intervallo.

        numero_intero = random.randrange(1, 10, 2)
        print(numero_intero)  # Output: un numero intero tra 1 e 9 con step di 2

#### Impostare un Seed con random.seed()
Puoi utilizzare random.seed() per inizializzare il generatore di numeri casuali con un seed specifico. Questo ti permette di ottenere risultati riproducibili, utili per test o debug.

Esempio di Utilizzo di random.seed()

    random.seed(42)
    print(random.random())  # Output: 0.6394267984578837
    print(random.randint(1, 10))  # Output: 2

In questo esempio, ogni volta che imposti il seed a 42, otterrai sempre gli stessi numeri casuali. Questo è utile quando desideri che l’esecuzione del programma produca lo stesso output ogni volta per scopi di testing.

#### Distribuzioni Probabilistiche
Il modulo random supporta anche la generazione di numeri casuali basati su diverse distribuzioni probabilistiche.

1. random.gauss(mu, sigma): Distribuzione Normale (Gaussiana)
La funzione random.gauss(mu, sigma) restituisce un numero casuale dalla distribuzione normale (gaussiana) con media mu e deviazione standard sigma.

        numero_normale = random.gauss(0, 1)
        print(numero_normale)  # Output: un numero casuale dalla distribuzione normale con media 0 e deviazione standard 1

2. random.expovariate(lambd): Distribuzione Esponenziale
La funzione random.expovariate(lambd) restituisce un numero casuale da una distribuzione esponenziale con parametro lambd.

        numero_esponenziale = random.expovariate(1.5)
        print(numero_esponenziale)  # Output: un numero casuale dalla distribuzione esponenziale

## Modulo Sys
Il modulo sys in Python fornisce varie funzioni e variabili per interagire direttamente con l’interprete Python e gestire il flusso di esecuzione del programma. Attraverso sys, puoi accedere agli argomenti passati da linea di comando, controllare l’input/output standard e ottenere informazioni sull’ambiente di runtime.

### 1. sys.argv: Argomenti da Linea di Comando
Una delle funzionalità principali di sys è la gestione degli argomenti passati da linea di comando. Gli argomenti vengono raccolti in una lista chiamata sys.argv.

Esempio di Utilizzo di sys.argv

    import sys
    
    # Stampa tutti gli argomenti
    print(f"Argomenti da linea di comando: {sys.argv}")
    
    # Stampa solo il nome dello script
    print(f"Nome dello script: {sys.argv[0]}")
    
    # Verifica se ci sono altri argomenti
    if len(sys.argv) > 1:
        print(f"Primo argomento: {sys.argv[1]}")
    else:
        print("Nessun argomento fornito.")

Terminal window

    $ python script.py argomento1 argomento2

Output:

    Argomenti da linea di comando: ['script.py', 'argomento1', 'argomento2']
    Nome dello script: script.py
    Primo argomento: argomento1

In questo esempio, sys.argv\[0] contiene il nome dello script, mentre sys.argv\[1] e successivi contengono gli argomenti passati dall’utente.

### 2. sys.exit(): Uscire dal Programma
Puoi terminare l’esecuzione di un programma Python in qualsiasi momento utilizzando sys.exit(). Puoi anche specificare un codice di uscita: 0 indica una terminazione con successo, mentre qualsiasi altro valore indica un’uscita con errore.

Esempio di Utilizzo di sys.exit()

    import sys
    
    if len(sys.argv) < 2:
        print("Errore: nessun argomento fornito.")
        sys.exit(1)  # Uscita con codice di errore 1
    
    print("Programma eseguito correttamente.")

Terminal window

    $ python script.py

Output:

    Errore: nessun argomento fornito.

In questo esempio, se non vengono forniti argomenti, il programma termina con un codice di errore (1).

### 3. sys.stdin, sys.stdout e sys.stderr: Input e Output Standard
Il modulo sys ti permette di accedere ai flussi di input e output standard attraverso le variabili sys.stdin, sys.stdout e sys.stderr. Puoi usarli per leggere l’input dall’utente o per scrivere messaggi su specifici canali di output.

Esempio di Utilizzo di sys.stdin e sys.stdout

    import sys
    
    # Legge l'input dall'utente utilizzando sys.stdin
    print("Inserisci il tuo nome:")
    nome = sys.stdin.readline().strip()
    
    # Scrive l'output su stdout
    sys.stdout.write(f"Ciao, {nome}!\n")

Esempio di Utilizzo di sys.stderr
sys.stderr è usato per scrivere messaggi di errore. È separato da sys.stdout per distinguere l’output normale dagli errori.

    import sys
    
    # Stampa un messaggio di errore
    sys.stderr.write("Questo è un messaggio di errore.\n")

Output:

    Questo è un messaggio di errore.

Puoi reindirizzare questi flussi su file o altre destinazioni per catturare l’output in modo personalizzato.

### 4. sys.path: Percorso di Ricerca dei Moduli
La variabile sys.path è una lista che contiene i percorsi dove Python cerca i moduli quando viene eseguito un import. Puoi modificare sys.path per aggiungere directory personalizzate e importare moduli da percorsi specifici.

Esempio di Utilizzo di sys.path

    import sys
    
    # Stampa i percorsi di ricerca dei moduli
    print("Percorsi di ricerca dei moduli:")
    for percorso in sys.path:
        print(percorso)
    
    # Aggiungi un nuovo percorso
    sys.path.append("/percorso/del/mio/modulo")

In questo modo, puoi aggiungere directory personalizzate alla lista di ricerca dei moduli e rendere disponibili moduli esterni non installati nella directory predefinita.

### 5. sys.version: Versione di Python
La variabile sys.version fornisce informazioni dettagliate sulla versione di Python in esecuzione. Questo è utile per verificare la compatibilità di uno script con diverse versioni di Python.

Esempio di Utilizzo di sys.version

    import sys
    
    print(f"Versione di Python: {sys.version}")

Output:

    Versione di Python: 3.10.4 (default, Sep  11 2024, 10:00:00)
    [GCC 9.3.0]

### 6. sys.platform: Identificare il Sistema Operativo
La variabile sys.platform contiene una stringa che identifica il sistema operativo su cui Python è in esecuzione. Questo è utile quando devi scrivere codice che si comporti in modo diverso su sistemi operativi diversi.

Esempio di Utilizzo di sys.platform

    import sys
    
    if sys.platform == "win32":
        print("Stai eseguendo Python su Windows.")
    elif sys.platform == "linux":
        print("Stai eseguendo Python su Linux.")
    elif sys.platform == "darwin":
        print("Stai eseguendo Python su macOS.")
    else:
        print("Sistema operativo non riconosciuto.")

Output su Windows:

    Stai eseguendo Python su Windows.

Output su Linux:

    Stai eseguendo Python su Linux.

### 7. sys.getsizeof(): Verificare la Dimensione di un Oggetto
La funzione sys.getsizeof() restituisce la dimensione in byte di un oggetto in Python. Questa funzione è utile per ottimizzare l’uso della memoria e comprendere meglio l’impatto delle strutture dati nel programma.

Esempio di Utilizzo di sys.getsizeof()

    import sys
    
    lista = [1, 2, 3, 4, 5]
    print(f"Dimensione della lista: {sys.getsizeof(lista)} byte")

Output:

    Dimensione della lista: 96 byte

### 8. sys.modules: Moduli Importati
La variabile sys.modules è un dizionario che contiene tutti i moduli attualmente importati nell’interprete Python. Può essere usata per verificare quali moduli sono stati importati e per ricaricare moduli in modo dinamico.

Esempio di Utilizzo di sys.modules

    import sys
    
    # Verifica se il modulo "math" è già stato importato
    if "math" in sys.modules:
        print("Il modulo math è già importato.")
    else:
        print("Il modulo math non è importato.")

Output:

    Il modulo math è già importato.

### 9. sys.maxsize: Intero Massimo
La variabile sys.maxsize rappresenta il valore massimo che un intero può assumere su una determinata piattaforma. È utile per definire limiti superiori nel codice.

Esempio di Utilizzo di sys.maxsize

    import sys
    
    print(f"Dimensione massima di un intero: {sys.maxsize}")

Output:

    Dimensione massima di un intero: 9223372036854775807

## Esercizi moduli
https://codegrind.it/esercizi/python/moduli
https://codegrind.it/esercizi/python/math

## Algoritmi 
### Complessità computazionale
### Ordinamento
### Ricerca per chiave
### Backtracking



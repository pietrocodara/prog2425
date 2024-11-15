# Introduzione alla programmazione per tutti
# (Brevi dispense del corso pomeridiano)

## Lezione 1

### Informazioni pratiche

- Docenti: Pietro Codara, Carmelo Castiglione
- Email: cognome.nome@issvigano.edu.it
- Server Discord: [link invito](https://discord.gg/asU9rqaf)
- Questo file è in formato markdown (estensione `md`); per vederlo *ben formattato* sul vostro PC potete aprirlo in VS Code (vedi di seguito), cliccare con il tasto destro sul nome del file e scegliere *Open Preview*. Se volete imparare ad usare markdown per scrivere i vostri appunti: https://www.markdownguide.org/basic-syntax/

### Configurazione ambiente di sviluppo

- Installazione Python: https://www.python.org/
- scaricate l'ultima versione di Python per il vostro OS dalla sezione downloads del sito
- installate come una normale applicazione, mantenendo le impostazioni di default
- Installazione Visual Studio Code, un noto editor utilizzato per la programmazione in diversi linguaggi: https://code.visualstudio.com/
- scaricate ed installate l'ultima versione stabile di VS Code per il vostro OS

### Scrivere ed eseguire un programma in VS code

*Visual Studio Code* (*VS Code*, in breve) è un editor di testo con funzionalità avanzate per la programmazione.  È utilizzato come ambiente di sviluppo per scrivere programmi in diversi linguaggi. Noi lo useremo per la programmazione in Python. Non è una scelta obbligata: potreste usare un qualsiasi altro editor già installato sul vostro sistema, come *Blocco Note* (scelta sconsigliata!), o l'ambiente di sviluppo *IDLE*, già compreso nel pacchetto di installazione di Python.

Per scrivere il nostro primo programma in Python, eseguiamo le seguenti operazioni.

1) Creiamo (ad esempio dallo strumento *Esplora file* di Windows) una cartella dove mettere i nostri programmi. Evitate di utilizzare sempre il Desktop ;)
2) Da VS Code, apriamo la cartella appena creata scegliendo *Open folder* nel menù *File*.
3) Nella barra *Explorer* di VS Code, che potete aprire/chiudere cliccando sul tasto in altro a destra, sotto il simbolo dell'applicazione, clicchiamo sul pulsante che si trova alla destra del nome della cartella (passandoci sopra compare la scritta *new file*) e creiamo un nuovo file con estensione `py`. Chiamiamo il file `ciao.py`. Se sbagliate a digitare il nome del file potete rinominarlo cliccandoci sopra con il tasto destro, oppure selezionandolo e premendo F2.
4) Apriamo, cliccandoci sopra, il file `ciao.py` ed *editiamolo* inserendo la seguente *linea di codice*. Dopo aver fatto le vostre modifiche ricordatevi di salvare il file!
```python
print('Hello world!')
```
5) Apriamo il *terminale*, cliccando sulla barra in basso oppure dal menù *View* scegliendo *Terminal*, e verifichiamo la presenza di Python digitando `py` (oppure `python` o `python3`). Dovrebbe aprirsi l'interfaccia a linea di comando dell'*interprete Python*. Da questa interfaccia possiamo eseguire comandi Python: provate a scrivere `2+3` e premete invio. Per uscire scriviamo `exit()` dopo il *prompt*, rappresentato dal simbolo  `>>>`.
6) Eseguiamo il file `ciao.py` dal terminale, digitando il comando `py ciao.py` (se non funziona `py`, usate `python` o `python3`, come avete fatto al punto precedente).

Nota: possiamo digitare i comandi da terminale più velocemente usando qualche trucchetto. Premendo `tab` dopo aver digitato qualche carattere viene completato automaticamente il nome del file. Premendo la freccia in alto si richiama l'ultimo comando (usando *freccia su* e *freccia giù* potete navigare lo storico dei comandi digitati).

### La funzione `print()`

Prepariamo ora una seconda versione del nostro programma, che possiamo chiamare `ciao2.py`.
```python
print('Hello world!')
print("Ciao mondo!")
```

Il programma esegue per due volte la *funzione* `print()` di Python. La funzione `print()` permette di stampare una *stringa*, ovvero una sequenza di caratteri di testo. Nel nostro programma la prima *invocazione* della funzione `print()` stamperà la stringa `Hello world!`. Una stringa in Python può essere delimitata in diversi modi: possiamo usare il simbolo `'` (apice), come in `'Hello world'` oppure il simbolo `"` (doppio apice o virgoletta), come in `"Ciao mondo!"`. 

Eseguendo il programma con il solito comando `py ciao2.py` viene visualizzato sul terminale il seguente *output*.

```
Hello world!
Ciao mondo!
```

Torniamo ora a "lavorare" sul nostro editor VS code. Premete il pulsante in basso della barra sinistra dei pulsanti (se ci passate sopra con il mouse compare la scritta *Extensions*). Viene visualizzato un elenco di *estensioni* che potete installare in VS code per aumentarne le funzionalità. Dal campo di ricerca in alto cercate *Python*. Dovreste trovare un'estensione chiamata Python, creata da Microsoft. Installatela premendo l'apposito pulsante. Dovrebbe comparirvi una schermata che conferma l'avvenuta installazione e descrive l'estensione, fornendo alcune istruzioni per configurarla e utilizzarla.

Tornate ora sul codice del programma `ciao2.py`. Cliccate sul tasto *play* (*run python file*) che si trova alla destra del nome del file che state editando. Vedrete comparire sul terminale il comando per eseguire il programma (in forma estesa e con tutti i percorsi assoluti completi) e, poco dopo, il risultato dell'esecuzione. Un terzo modo per eseguire il programma è accedere al menù *Run* e cliccare su *Run without debugging*. Un altro modo, equivalente al precedente, è premere `CTRL+F5`.


### Variabile

Una *variabile* è un riferimento a un *dato* che è salvato in memoria. Il nome dato a una variabile dal programmatore ricorda spesso (ma non sempre, dipende dalla scelta del programmatore) il significato del valore memorizzato: per esempio, si può usare il termine *nome* o il termine *name* per una variabile in cui è memorizzato il nome di una persona; si può usare il termine *eta* (meglio se senza accenti: non ci piace usare caratteri così strani come le lettere accentate nei nostri programmi) o il termine *age*, ad esempio, per una variabile dove è salvata l'età di una persona, e così via. La *variabile* è lo strumento più semplice e comodo che possiamo usare nei nostri programmi per memorizzare dati, recuperare valori memorizzati e manipolarli. Per introdurre una nuova variabile in Python e *assegnare* alla variabile un nuovo valore si usa l'istruzione:

```python
cognome = "Codara"
```

Questa istruzione *assegna* alla variabile `cognome` il valore `"Codara"`. 
Il simbolo `=` esegue un *assegnamento* (o *assegnazione*) di un valore a una variabile.

Nota: per dare un nome a una variabile potete usare tutti i caratteri dell'alfabeto ed eventualmente anche numero e il carattere `_` (underscore). Non usate un numero all'inizio del nome. Ad esempio, il nome `citta_1` è valido, ma il nome `76_forever` non lo è.

Possiamo riassegnare il valore a una variabile in un nostro programma. Apriamo nel nostro editor un nuovo file, chiamato `variabile.py` e scriviamo:

```python
stringa = "Pietro"
print(stringa)
stringa = "Casa"
print(stringa)
```

Analizziamo il programma scritto. La prima *riga* assegna il valore `"Pietro"` alla variabile chiamata `stringa`. La seconda riga stampa il valore della variabile. Notate che il testo dentro le parentesi della funzione `print()`, che si chiama *parametro* della funzione ed è un valore *passato* alla funzione in modo che questa possa utilizzarlo, non è racchiuso tra apici. Non si tratta infatti di una stringa, ma è piuttosto il nome di una variabile. Non commettete l'errore di scrivere `print('stringa')`: verrebbe stampato in output `stringa` e non, come desiderato, `Pietro`. Anzi, provate a commettere questo errore, eseguite il programma e osservate cosa succede!

Alla terza riga viene assegnato alla variabile un nuovo valore: la stringa `"Casa"`. Il valore memorizzato in precedenza, la stringa `"Pietro"` non sarà da questo momento più accessibile, perchè il nuovo valore contenuto nella variabile `stringa` è la stringa `"Casa"`. 

Nell'ultima riga del programma viene salvato il nuovo valore di `stringa`, mostrando così ciò che è successo con l'assegnamento della riga 3.

Domanda: è possibile fare in modo che la funzione `print()` non vada a capo dopo aver stampato la stringa? Risposta: si, anche se di norma (di *default*) la funzione `print()` stampa *un carattere di a capo* dopo il testo ricevuto come parametro, è possibile modificare questo comportamento.
Per farlo, dobbiamo *passare* alla funzione `print()` un altro parametro, anche se "in un modo abbastanza strano", che capiremo più avanti:

```python
stringa = "Pietro"
print(stringa,end=" --- ")
stringa = "Casa"
print(stringa)
```

Eseguendo questo programma, immediatamente dopo la stringa `Pietro` viene stampato il testo ` --- ` (spazi iniziale e finale inclusi) e poi la stringa `Casa`. Come risultato, vedremo sul terminale la stampa: `Pietro --- Casa`.

Osservazione: spesso, quando si cita il nome di una *funzione* si mette in coda al nome una coppia di parentesi tonde, senza parametri all'interno, ad indicare che si tratta di una funzione e non di altro, ad esempio non di una variabile. Per esempio, abbiamo parlato nelle righe precedenti della funzione `print()`. 

Proviamo a modificare il programma  `variabile.py` che abbiamo scritto poco fa, scrivendo questa volta:

```python
stringa = "Pietro"
print(Stringa)
stringa = "Casa"
print(stringa)
```

Eseguiamo il programma dopo questa modifica. Dovremmo ottenere un output simile a questo:
```
Traceback (most recent call last):
  File "Z:\python\variabile.py", line 2, in <module>
    print(Stringa)
          ^^^^^^^
NameError: name 'Stringa' is not defined. Did you mean: 'stringa'?
```

L'interprete Python ci sta segnalando che la seconda riga (`"Z:\python\variabile.py", line 2`) contiene un errore. In particolare, si tratta di un `NameError` ed è dovuto al fatto che l'interprete non conosce il nome `Stringa` (`name 'Stringa' is not defined`). In effetti, il simbolo `Stringa` che chiediamo alla `print()` di stampare non esiste: l'unica variabile nel nostro programma è `stringa`, con l'iniziale minuscola, e per Python le lettere maiuscole e le lettere minuscole sono *diverse* (si dice che il linguaggio è *case sensitive*).

Questo messaggio dell'interprete è molto importante, perché ci permette di correggere il nostro programma. Commetterete molti errori nel programmare e molti di questi verranno segnalati in questo modo dall'interprete: leggete sempre il messaggio che viene stampato con attenzione! Non sarà sempre facile capire cosa vuole dirci, ma con l'esercizio imparerete a capire al volo ciò che sta dietro a tutti i messaggi d'errore più comuni.


> #### Esercizio 1.1
>
> Aprite il file `ciao.py`. Modificate qualcosa nel codice, ad esempio eliminate un apice all'inizio o alla fine della stringa `Hello world!`. Eseguite il programma e leggete con attenzione il messaggio che viene visualizzato sul terminale. Correggete l'errore e introducetene un altro. Eseguite nuovamente il messaggio e, di nuovo, leggete attentamente ciò che vi viene segnalato. Riportate infine il programma nel suo stato originale ed eseguite.

> #### Esercizio 1.2
> Assegnate a una variabile il titolo della vostra canzone preferita. Fate poi in modo che il vostro programma stampi su terminale, mediante l'esecuzione di funzioni `print()`, il testo `La mia canzone preferita è: titolo`, dove titolo è il contenuto della variabile. Ad esempio, se avete memorizzato nella variabile il valore `Love Will Tear Us Apart` ed eseguite il vostro programma, otterrete sul terminale la stampa `La mia canzone preferita è: Love Will Tear Us Apart`.

> #### Esercizio 1.3
> Scrivete un programma contenente come unica istruzione `import this`. Eseguite il programma e leggete ciò che viene visualizzato sul terminale.
>

## Lezione 2

Ecco il risultato dell'esecuzione del comando `import this`, citato nell'ultimo esercizio.

```
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

La maggior parte di queste considerazioni vale per ogni linguaggio di programmazione: tenetelo a mente, quando programmata! ;)

### Metodi per le stringhe

Giochiamo un po' con le stringhe.

```py
nome = 'Alan'
print("Ciao " + nome + " Turing " + "!")
print("Ciao", nome, "Turing", "!")

nome_completo = nome + " Turing"
print(nome_completo)

saluto = "Ciao " + nome_completo
print(saluto)
```

Eseguendo il programma qui sopra otteniamo quanto segue.

```
Ciao Alan Turing !
Ciao Alan Turing !
Alan Turing
Ciao Alan Turing
```

Osserviamo che con la funzione `print()` è possibile stampare più valori, separando gli *argomenti* (le stringhe da stampare) che passiamo alla funzione con il carattere `,`. Nella stampa, le varie stringhe passate come argomento vengono separate da uno spazio. È questo il caso della seconda istruzione `print()` eseguita nel codice. Nella prima *chiamata* alla `print()`, invece, si passa un solo argomento alla funzione, una unica stringa ottenuta per concatenazione (utilizzando l'operatore `+`). Il risultato, come si può osservare, è in questo caso lo stesso.


Aggiungendo in coda al precedente programma la riga di codice `print(saluto*3)` otteniamo oltre al vecchio output il testo `Ciao Alan TuringCiao Alan TuringCiao Alan Turing`.

Eseguiamo ora il seguente programma:

```py
nome_cognome = "grace hopper"
print(nome_cognome.upper())
print(nome_cognome.lower())
print(nome_cognome.title())
print(nome_cognome)
```

otteniamo:
```
GRACE HOPPER
grace hopper
Grace Hopper
grace hopper
```

Le *funzioni* `upper()`, `lower()` e `title()` restituiscono la stringa `nome_cognome` modificata: nel primo caso tutti i caratteri diventano maiuscoli, nel secondo minuscoli, nel terzo diventa maiuscola ogni iniziale di parola e minuscolo il resto. Queste funzioni sono un po' "speciali" e lo vediamo perché si *invocano* in maniera diversa rispetto alle funzioni "tradizionali", come `print()`: scriviamo infatti il nome di un *oggetto*, nel nostro caso la stringa `nome_cognome`, poi un carattere `.`, infine il nome della funzioni (con tra parentesi eventuali argomenti). Funzioni di questo tipo si chiamano *metodi*. I metodi eseguono un'azione su un oggetto specifico, nel nostro caso la stringa `nome_cognome`.
Osservate che i metodi `upper()`, `lower()` e `title()` non modificano la stringa `nome_cognome` (è chiaro guardando l'ultima stampa!), ma ne restituiscono una copia modificata.

Esistono molti altri metodi per le stringhe. Ecco un esempio di codice che utilizza `removeprefix()` e `removesuffix()`. Entrambi i metodi ricevono un parametro tra parentesi: il prefisso (o il suffisso) da rimuovere.

```py
url = 'https://www.python.org/'
print(url)
url_senza_prefisso = (url.removeprefix("https://"))
print("Senza prefisso:",url_senza_prefisso)
url_senza_suffisso = (url_senza_prefisso.removesuffix("/"))
print("Senza suffisso:",url_senza_suffisso)
print()
print("Url originale:",url)
```

L'output sarà:
```
https://www.python.org/
Senza prefisso: www.python.org/
Senza suffisso: www.python.org

Url originale: https://www.python.org/
```

Notate che, anche in questo caso, i metodi non hanno modificato la stringa a cui sono stati applicati.

### Stringhe formattate

Le stringhe formattate, o f-stringhe (*f-string* in inglese), possono essere utilizzate, tra l'altro, per inserire all'interno di stringhe *espressioni* che devono essere valutate, come ad esempio variabili, o funzioni e calcoli di cui ci serve il risultato.
Una f-stringa è denotata da una `f` che precede la stringa. Le espressioni da valutare in una f-stringa sono racchiuse tra `{}`.

```py
nome = "ada"
cognome = "lovelace"
stringa = f"{nome.title()} {cognome.title()} è ricordata come la prima programmatrice al mondo!"
print(stringa)
```

Il precedente programma stampa il contenuto della variabile `stringa`, ovvero:
```
Ada Lovelace è ricordata come la prima programmatrice al mondo!
```

### Caratteri speciali

L'istruzione
```
print("Languages:\n\tPython\n\tC\n\tJavaScript")
```

stampa
```
Languages:
  Python
  C
  JavaScript
```

La sequenza `\n` rappresenta un unico carattere: il carattere di *invio* (a capo). La sequenza `\t` rappresenta un unico carattere: il carattere di tabulazione (*tab*).


I caratteri di *spaziatura* (*whitespace*) all'inizio e alle fine di una stringa possono essere eliminati con i metodi `lstrip()`, `rstrip` e `strip`. Ad esempio, se `stringa = ' pippo '`, l'esecuzione di `stringa.lstrip()` restituisce la stringa `'pippo '`, eliminando lo spazio a sinistra (*left* strip).


### I numeri

Eseguiamo sulla console di Python alcuni comandi che coinvolgono numeri piuttosto che stringhe, come invece era stato fatto sinora.

```py
>>> num = 5
>>> num
5
>>> num + 4
9
>>> 18 + 5
23
>>> 18 - 5
13
>>> 18 * 5
90
>>> 5/2
2.5
>>> 5//2
2
>>> 5%2
1
>>> 5**2
25
```

I risultati restituiti dovrebbero essere abbastanza chiari. Osserviamo che `/` rappresenta la divisione, mentre `//` rappresenta una divisione intera (che produce quindi un quoziente intero). Il resto di una divisione intera è calcolato grazie all'operatore `%`. Infine, l'operatore `**` permette l'elevamento a potenza.

Il seguente esempio mostra il comportamento dell'interprete Python in alcuni casi particolari.

```py
>>> "Mario" + 2
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
>>> "2" + "2"
'22'
>>> 5.5 + 2
7.5
>>> 5.5 + 2.09
7.59
>>> "5.5" + "2"
'5.52'
>>> num_grande = 1000000000
>>> num_grande
1000000000
>>> num_grande = 1_000_000_000
>>> num_grande
1000000000
>>> x = 4
>>> y = 4
>>> area = x*y
>>> area
16
>>> x, y = 4,4
>>> x
4
>>> y
4
>>> x,y,z = 1,2,3
>>> x
1
>>> y
2
>>> z
3
>>> x,y = y,x
>>> x
2
>>> y
1
```

Osserviamo che istruzioni come `x,y,z = 1,2,3` permettono l'assegnamento contemporaneo di più valori a diverse variabili. L'esecuzione di `x,y=y,x`, in particolare, provoca lo scambio di valori tra le due variabili `x` e `y`.

## Tipi di dato

La funzione `type()` di Python restituisce il tipo di dato di un oggetto.

```py
>>> type(2)
<class 'int'>
>>> type(4.67)
<class 'float'>
>>> type('Ada Lovelace')
<class 'str'>
>>> type(f'Il dado ha {3+3} facce')
<class 'str'>
```

Gli `int` sono numeri interi, i `float` sono numeri decimali (in *virgola mobile*), mentre il tipo `str` rappresenta le stringhe.


## Commenti

Potete aggiungere commenti al codice o commentare istruzioni perché non siano eseguite inserendo a inizio riga il simbolo `#`.

Ad esempio:
```py
# Questo è un commento
print('Questo no')
# print('Io non verrò stampata, perché l'istruzione è commentata')
```

In VS Code potete selezionare una o più righe da commentare e premere **ctrl+ù** per commentare tutto il blocco selezionato. Eseguendo la stessa operazione su un blocco di codice già commentato, le righe vengano decommentate.

## Lezione 3

Una lista è una semplice *struttura dati* che contiene un elenco di elementi.
Una lista è delimitata da parentesi quadre. La lista `[]` è una lista vuota, prima di elementi. La lista `['Pietro']` contiene un solo elemento: la stringa `'Pietro'`. Ecco un esempio che crea una lista di più elementi ed esegue alcune operazioni su di essa.

```py
studenti = ['Andrea','Giovanni','Marco','Giacomo','Maria']

# Gli elementi in una lista sono accessibili tramite indice. Il primo elemento di una lista ha indice 0, il secondo 1, e così via
print(studenti[0]) #stampa il primo elemento
print(f'Il secondo elemento della lista, scritto in maiuscolo, è {studenti[1].upper()}')

studenti[0] = 'Andreina' # modifica il primo elemento in Andreina

studenti.append('Lucia') # aggiunge l'elemento Lucia in fondo alla lista

print(studenti) # stampa: ['Andreina', 'Giovanni', 'Marco', 'Giacomo', 'Maria', 'Lucia']

presenti = [] # crea una nuova lista, vuota
presenti.append(studenti[0])
presenti.append(studenti[1])
presenti.append(studenti[3])
print(presenti) # stampa: ['Andreina', 'Giovanni', 'Giacomo']

print(len(studenti)) # stampa 6, la lunghezza, ovvero il numero di elementi, della lista studenti
print(f'Ci sono {len(studenti)-len(presenti)} assenti')

del studenti[0] # cancella l'elemento in posizione 0 dalla lista
print(studenti) # stampa: ['Giovanni', 'Marco', 'Giacomo', 'Maria', 'Lucia']

studenti.pop() # rimuove l'ultimo elemento della lista (e ne restituisce il valore)
print(studenti) # stampa: ['Giovanni', 'Marco', 'Giacomo', 'Maria']

print(studenti.pop(2)) # il metodo pop() rimuove l'elemento in posizione 2, la print riceve il valore rimosso e lo stampa
print(studenti) # stampa: ['Giovanni', 'Marco', 'Maria']

studenti.remove('Marco')
print(studenti) # stampa: ['Giovanni', 'Maria']

nome_da_rimuovere = 'Giovanni'
studenti.remove(nome_da_rimuovere)
print(studenti) # stampa: ['Maria']
```

Testiamo nella console di Python alcuni uso particolari degli indici. Notate la possibilità di *contare dalla fine* della lista (usando indici negativi) e gli errori che vengono segnalati.

```py
>>> lista = ['Ada','Ava','Eva']
>>> lista[-1]
'Eva'
>>> lista[3]  
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>> lista[-3] 
'Ada'
>>> lista[-4] 
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```


## Lezione 4

Eseguiamo alcune operazioni sulle liste, tra cui gli ordinamenti.

```py
pizze=["margherita","diavola","4 stagioni","romana","kebab"]

print(pizze) # stampa: ['margherita', 'diavola', '4 stagioni', 'romana', 'kebab']
print(pizze[0])

pizze.reverse()
print("menù invertito (rispetto all'ordine attuale) ", pizze) # stampa: ['kebab', 'romana', '4 stagioni', 'diavola', 'margherita']

pizze.sort()
print("menù ordinato: ", pizze)  # stampa: ['4 stagioni', 'diavola', 'kebab', 'margherita', 'romana']

pizze.sort(reverse=True)
print("menù in ordine inverso: ", pizze) # stampa: ['romana', 'margherita', 'kebab', 'diavola', '4 stagioni']

pizze.append("marinara")
pizze.remove("kebab")
print("menù aggiornato", pizze) # stampa: ['romana', 'margherita', 'diavola', '4 stagioni', 'marinara']
```

Scorriamo le liste con il ciclo `for`. Occorre prestare molta attenzione nell'uso del costrutto `for`: dopo l'istruzione `for` tutte le istruzioni che vanno ripetute devono rientrare (essere indentate)
L'istruzione `for pizza in pizze:` prende a uno a uno tutti gli elementi della lista `pizze` e li mette nella variabile `pizza`. Al primo *passo* del ciclo in `pizza` finisce l'elemento `pizze[0]` e vengono eseguite tutte le righe indentate che seguono il `for`. Si torna poi all'inizio del ciclo, `pizza` prende valore `pizze[1]` e si rieseguono le stesse istruzioni, con il nuovo valore di `pizza`. L'esecuzione prosegue così fino a quando `pizze` non ha più elementi.

```py
pizze=["margherita","diavola","4 stagioni","romana","kebab"]
n=0
# Il ciclo seguente visualizza la lista delle pizze in formato:
# 1 -  margherita
# 2 -  diavola
# 3 -  4 stagioni
# 4 -  romana
# 5 -  kebab
for pizza in pizze:
    n+=1
    print(n, "- ", pizza)

# Il ciclo seguente invece mantiene la visualizzazione su una riga (con un "piccolo" difetto nella stampa dell'ultima pizza)
print("Nel nostro ristorante potrete trovare: ",end="")
for pizza in pizze:
    print(pizza, end=", ")

print()

# Il ciclo seguente compone la scritta da stampare pezzo per pezzo, grazie al ciclo. Poi stampa l'intera scritta, dopo averla ripulita dalla virgola finale:
#
    
scritta = "Nel nostro ristorante potrete trovare: "
for pizza in pizze:
    scritta += pizza + ', '

scritta = scritta.removesuffix(', ')
print(scritta)
```

Lavoriamo, infine, su liste di numeri, introducendo anche l'uso di `range()`, che genera un intervallo di numeri da un minimo a un massimo (eventualmente con una certa distanza, o passo, tra loro).

```py
n=10
# range(n) genera l'intervallo di numeri da 0 a n-1(fino cioè a n escluso!)
for x in range(n):
  print(x,end=' ') # stampa: 0 1 2 3 4 5 6 7 8 9 

print()
# range(m,n) genera l'intervallo di numeri da m a n-1 (fino cioè a n escluso!)
m=3
for x in range(m,n):
  print(x,end=' ') # stampa: 3 4 5 6 7 8 9 

print()
# range(m,n,p) genera l'intervallo di numeri da m a n-1 con incremento di p (e non più di 1)
m=3
for x in range(m,n,2):
  print(x,end=' ') # stampa: 3 5 7 9 

print()

for x in range(4):
   print('Ciao mondo!') # stampa: 'Ciao mondo!' 4 volte 

print()
n = 100
# Calcoliamo la somma dei primi n numeri interi
somma=0
for x in range(1,n+1):
    somma += x 
print(somma) # stampa 5050

print(n*(n+1)//2) # stampa la stessa somma calcolata con la formula di Gauss

lista_numeri=list(range(n+1)) #crea una lista di numeri tra 1 e 100
print(sum(lista_numeri)) # stampa la solita somma calcolata mediante la funzione sum() di Python
print(sum(range(1,n+1))) # come sopra, ma usando sum direttamente sul range()

lista=[10, 20, 30, 40]
somma = 0
# somma tutti i valori in lista maggiorati del 10% se l'elemento ha indice dispari, del 20% se l'elemento ha indice pari
for indice in range(0,len(lista),2):
    print(indice)
    somma += lista[indice] * 1.2 # stiamo scorrendo le posizioni pari: somma maggiorato del 20%
for indice in range(1,len(lista),2):
    print(indice)
    somma += lista[indice] * 1.1 # stiamo scorrendo le posizioni pari: somma maggiorato del 10%

print(somma) # stampa 114 = (10+30)*1,2 + (20+40)*1,1
```

## Lezione 5

### La funzione `input()`

La funzione `input()` di Python ci permette di leggere un valore dall'input, solitamente inserito dall'utente. Il valore letto viene restituito da `input()` come una stringa, anche se si tratta di un numero o di un dato di altro tipo. È possibile passare alla funzione `input()` un parametro: la stringa da visualizzare per richiedere all'utente di inserire l'input.

Nel seguente esempio la prima riga di codice visualizza il messaggio `Come ti chiami? `. Il programma resta poi in attesa dell'input dell'utente. Quando l'utente avrà finito di digitare il testo e premuto invio, il testo digitato verrà restituito dalla funzione `input()` e assegnato alla variabile `nome`. La riga successiva stampa il messaggio `Ciao {nome}`, dove `nome` è il testo inserito dall'utente.

```py
nome = input("Come ti chiami? ")
print(f'Ciao {nome}')
```

### Conversione di tipo

Chiediamo ora all'utente di inserire un numero invece che del testo, mediante l'istruzione:

```py
num = input("Pensa a un numero. Che numero hai pensato? ")
```

Eseguendo ora `print(type(num))` otteniamo in risposta `<class 'str'>`. Il valore letto è quindi memorizzato in `num` come stringa. Ipotizziamo che `num` contenga il valore `'23'` proviamo ad eseguire dei calcoli con `num`. Eseguendo `doppio = num * 2` e stampando il valore di `doppio` otteniamo un risultato indesiderato: `2323`, cioè il "doppio" di una stringa. Eseguendo invece `somma = num + 2` ci viene segnalato un errore, perché con l'operatore `+` possiamo solo sommare *due* numeri o concatenare *due* stringhe. Per sistemare questo problema, e visto che nel nostro programma quando leggiamo un numero vogliamo utilizzarlo come tale, convertiamo la stringa in numero mediante la funzione `int()`, come segue:

```py
num = int(input("Pensa a un numero. Che numero hai pensato? "))
```

Dopo l'esecuzione di questa istruzione, la variabile num conterrà effettivamente un numero intero, se il valore letto in input può essere effettivamente convertito in intero (altrimenti, ad esempio se viene inserito `ciao`, viene segnalato un errore). Esistono numerose altre funzione di conversione, ad esempio `str()`, `float()`, `bool()`. Tutte queste funzioni provano a convertire il parametro ricevuto nel tipo desiderato.


Costruiamo ora un programma in grado di indovinare il numero pensato dall'utente.

```py
num = int(input("Pensa a un numero. Che numero hai pensato? "))
print(f'Il numero che hai pensato è più grande di {num-1} e più piccolo di {num+1}')
print(f'Indovino... hai pensato {num}')
```

### Il costrutto di selezione `if`

Il programma che abbiamo scritto è effettivamente piuttosto stupido: chiediamo all'utente cosa ne pensa.

```py
giudizio = int(input('Che voto dai a questo programma indovino (da 0 a 10)?'))
print(giudizio)
```


Salutiamo infine l'utente, ma facciamo in modo che il saluto sia diverso a seconda del voto ricevuto. Per eseguire codice differente a seconda del verificarsi di opportune condizioni utilizziamo il costrutto `if` del linguaggio. Ecco la sintassi del costrutto `if` nel linguaggio python:

```py
if condizione:
    istruzioni
```

`condizione` deve essere una espressione valutabile come vera o falsa. Se `condizione` è vera, allora vengono eseguire le `istruzioni` interne all'`if`, ovvero quelle che seguono l'`if` e sono indentate.
In caso contrario, se `condizione` è falsa, l'esecuzione continua con le eventuali istruzioni che seguono l'if. È anche possibile specificare istruzioni da eseguire solo quando `condizione` è falsa. Per farlo, si utilizza la clausola `else`, come segue:

```py
if condizione:
    istruzioni_1
else:
    istruzioni_2
```

In questo caso le `istruzioni_1` vengono eseguite *solo* quando `condizione` è vera, mentre le `istruzioni_2` vengono eseguite *solo* quando `condizione` è falsa. Nella sua versione più completa, il costrutto `if` di Python` si presenta così:

```py
if condizione_1:
    istruzioni_1
elif condizione_2:
    istruzioni_2
...
else:
    istruzioni_n
```

Questo `if` si comporta così: se `condizione_1` è vera viene eseguito il blocco di istruzioni `istruzioni_1`, altrimenti, se `condizione_2` è vera viene eseguito il blocco `istruzioni_2`, altrimenti, ...; altrimenti (dunque se nessuna delle precedenti condizioni risulta vera viene eseguito il blocco `istruzioni_n`. Possono essere presenti anche più clausole `elif`.

Per costruire le condizioni da verificare facciamo uso di operatori di confronto come `<`, `<=` (minore o uguale), `>`, `>=` (maggiore o uguale), `==` (uguale a), `!=` (diverso da). Possiamo combinare più espressioni con gli operatori logici `and`, `or` e `not`: 
- la condizione `C1 and C2` è vera solo se sia `C1` che `C2` sono vere; 
- la condizione `C1 or C2` risulta vera quando almeno una tra `C1` e `C2` è vera;
- la condizione `not C` (la negazione di `C`) è vera se `C` è falsa ed è falsa se `C` è vera.

(Precisazione: diciamo che un'espressione è vera quando viene valutata a `True`; diciamo che è falsa se prende valore `False`)

Alcuni esempio:
- per testare se il valore di `x` è compreso tra `0` e `10` possiamo usare la condizione `x>=0 and x<=10`;
- per testare se `x` è minore di `0` o maggiore di `10` possiamo usare la condizione precedente negata, `not(x>=0 and x<=10)`, oppure scrivere `x<0 or x>10`;
- per testare se il valore di `x` è compreso tra `0` e `10` e quello di `y` è compreso tra `0` e `10`, possiamo scrivere `(x>=0 and x<=10) and (y>=0 and y<=10)`; in questo caso potremmo anche non usare le parentesi (anche se talvolta alcune parentesi inutili rendono più leggibile la condizione).


Grazie all'uso dell'`if` possiamo concludere il nostro programma come segue:

```py
if giudizio < 0 or giudizio > 10:
    print("Hai sbagliato a votare!")
elif giudizio >= 8:
    print("Grazie per il tuo giudizio positivo")
elif giudizio >= 6:
    print("si, vabbeh...")
else:
    print("Non tornare più a trovarci!")
```

> #### Esercizio
> Scrivete un programma che legga da tastiera:
>- numero di biglietti da acquistare
>- costo del singolo biglietto
>
>Dopo aver letto i due valori, stampate il costo totale dell'acquisto tenendo conto dei seguenti sconti/supplementi:
>- fino a 2 biglietti: 2€ di supplemento
>- oltre i 5 biglietti: sconto 5%
>- oltre i 10 biglietti: un biglietto omaggio
>- oltre i 20 biglietti: 10% di sconto

Ecco una possibile soluzione dell'esercizio assegnato.

```py
num = int(input("Quanti biglietti? "))
costo = int(input("Quanto costa un biglietto? "))

if (num<1):
    print('Compra più biglietti!')
elif num < 3:
    print(f'Costo: {num}x{costo}+2 = {num*costo+2}€')
elif num < 11:
    print(f'Costo: ({num}x{costo})-5% = {num*costo*0.95}€')
elif num < 21:
    print(f'Costo: ({num}-1)x{costo} = {(num-1)*costo}€')
else:
    print(f'Costo: ({num}x{costo})-10% = {num*costo*0.9}€')
```

### Lettura di dati da file mediante redirezione dello standard input

Considerate il seguente programma, che legge da tastiera un nome e un cognome per poi stampare una messaggio di saluto.

```py
nome = input()
cognome = input()
print(f'Ciao {nome} {cognome}')
```

Immaginiamo che i dati relativi alla persona da salutare siano presenti su un file e non debbano quindi essere digitati da tastiera. Ad esempio, potremmo aver preparato sul nostro computer un file di testo, diciamo `anagrafica.txt` formato dalle seguenti due linee:

```txt
Pietro
Codara
```
Il nostro programma dovrebbe quindi prendere il nome e il cognome direttamente da file, senza chiedere l'input all'utente. Ci sono vari modi per leggere i dati da file in Python. Noi non ne useremo nessuno e faremo leggere il file di testo al nostro sistema operativo. 

Preparate quindi in una stessa directory i due file `saluto.py`, contenente il programma Python, e `anagrafica.txt`, contenente due righe di testo, con il nome sulla prima riga e il cognome sulla secondo.

Se il vostro sistema è Windows, digitate sulla linea di comando:
```cmd
Get-Content anagrafica.txt | py saluto.py
```

Il comando che avete appena digitato esegue il programma prendendo l'input da file piuttosto che da tastiera. Più in dettaglio, `Get-Content anagrafica.txt` restituisce in output il contenuto del file `anagrafica.txt` (provate a eseguire solo questo comando), mentre il simbolo `|` indica che l'output del comando non deve essere inviato allo *standard output* usuale (dunque visualizzato sullo schermo), ma deve essere utilizzato come input per il comando successivo. Visto che il comando successivo esegue il nostro programma, le due `input()` non resteranno in attesa di valori digitati dall'utente, perché ricevono già i valori restituiti dal comando `Get-Content` (cioè le due righe contenute nel file di testo). 

Lo stesso effetto può essere ottenuto in Linux digitando sul terminale il comando:

```shell
py somecode.py < anagrafica.txt 
```

In questo caso quello che avviene è leggermente diverso: viene infatti eseguito un solo comando (`py somecode.py`), ma l'input, grazie all'utilizzo del simbolo `<`, viene preso dal file `anagrafica.txt`.

### Generazione di numeri casuali

In Python è possibile generare numeri casuali grazie ad alcune funzione presenti in un modulo aggiuntivo che si chiama `random`. Per poter utilizzare queste funzioni nei nostri programmi occurre *importare* il modulo, inserendo nel nostro programma il comando `import random`. Le funzioni presenti nel modulo `random` potranno poi essere eseguite nel programma scrivendo `random.nomefunzione()`, per specificare che la funzione `nomefunzione()` fa parte del modulo importato.

Potete trovare all'indirizzo https://docs.python.org/3/library/random.html una descrizione delle numerose funzioni presente nel modulo. Noi useremo la funzione `randint()` che riceve in ingresso due numeri e restituisce un numero intero pseudo-casuale incluso tra i due. Ad esempio, il programma

```py
import random
casuale = random.randint(0,10)
print(casuale)
```

stampa un numero casuale compreso tra 0 e 10 (inclusi). Provate a scriverlo e ad eseguirlo più volte.


### Scrittura di dati su file mediante redirezione dello standard output

Costruiamo un ultimo esempio, in cui immaginiamo di avere un file di testo contenente dati sulle precipitazioni in ogni giorno dell'anno (365 righe con un numero su ogni riga che indica i millimetri di pioggia caduti nel giorno) e di volere un programma in grado di trovare la massima quantità di pioggia caduta in un giorno dell'anno (quindi il massimo valore nel file).

Visto che in realtà il file in questione non l'abbiamo, ne creiamo uno come campione: ci servirà per testare il nostro programma. Il seguente codice fa quasi tutto ciò che ci serve, perché è in grado di stampare 365 valori casuali tra 0 e 100, uno per riga.

```py
import random

for x in range(365):
    print(random.randint(0,100))
```

Quello che ci resta da fare è stampare i valori su file piuttosto che sullo schermo. Come nel caso della lettura dati da file, anche in questa occasione Python offre diverse funzioni per l'apertura e la scrittura di file, ma noi lasceremo fare al sistema operativo. In Windows e in Linux per *redirigere* l'output di un comando vi basta scrivere `comando > nomefile`. Ad esempio, se il vostro programma si chiama `creafile.py`, il comando `py creafile.py > pioggia.txt` crea il file `pioggia.txt` e lo riempie con 365 valori casuali tra 0 e 100, senza stampare nulla a video.

Ci serve a questo punto il programma in grado di trovare il massimo tra i 365 valori presenti nel file. Pensiamo a un programma in grado di trovare il massimo tra 365 valori letti in input, per poi usare la tecnica vista in precedenza per fare in modo che l'input sia preso dal file `pioggia.txt`. Possiamo per esempio leggere 365 valori e inserirli in una lista. Utilizzeremo la funzione `max()` di Python per trovare il valore massimo nella lista. Ecco il programma completo, che chiamiamo `pioggia.py`. Ricordatevi di eseguirlo in Windows con il comando `Get-Content pioggia.txt | py pioggia.py`, altrimenti vi toccherà inserire a mano 365 valori!

```py
lista = []
for _ in range(365):
    num = int(input())
    lista.append(num)

massimo = max(lista)
print(f'Il massimo valore nella lista è {massimo}')
```

Nel codice il simbolo `_` sostituisce qualunque altro simbolo (`x`, `i`, ...) che potremmo usare per la variabile che contiene il valore preso dal `range`. Notate che, in effetti, il valore non ci serve a nulla (ci basta ripetere le due istruzioni seguenti per 365 volte).

### Esercizi

#### Esercizio 1

Scrivete un programma che legga un valore intero `n` e successivamente chieda all'utente di inserire `n` numeri interi.
Memorizzate gli `n` interi letti in una lista e:
- calcolate e visualizzate il massimo dei numeri presenti nella lista;
- calcolate e visualizzate il minimo dei numeri presenti nella lista;
- costruite una nuova lista ottenuta da quella che avete eliminando tutti i numeri negativi e prendendo dunque solo i numeri positivi o nulli;
- calcolate e visualizzate la media dei numeri non negativi, ovvero dei numeri che avete inserito nella lista costruita al punto precedente.

#### Esercizio 2

Abbiamo costruito un programma in grado di trovate il massimo tra 365 valori indicanti i millimetri di pioggia caduti nei giorni di un anno, memorizzati in un file `pioggia.txt`.

Modificatalo in modo che il programma stampi a video il giorno in cui ha piovuto di più (e non i mm di pioggia caduti) e il giorno in cui ha piovuto di meno. Nel caso (piuttosto frequente, in effetti) in cui più giorni abbiano gli stessi valori, stampate il primo di questi giorni. Potete esprimere il giorno come un numero tra 1 e 365  e stampare quindi messaggi come "Il giorno 133 dell'anno è stato il più piovoso", "Il giorno 23 dell'anno è stato il meno piovoso".

#### Esercizio 3

(da mapio@github)
Scrivere un programma che, dato un intero `n` > 1 letto da tastiera, stampi `n` "denti di sega" alti 4 righe. Ad esempio, dato `3` come parametro, il programma deve stampare

       ^     ^     ^  
      / \   / \   / \
     /   \ /   \ /   \
    /     V     V     \


Inserendo invece il valore `5` il programma stamperà

       ^     ^     ^     ^     ^  
      / \   / \   / \   / \   / \
     /   \ /   \ /   \ /   \ /   \
    /     V     V     V     V     \
  
#### Esercizio 4 (Distanza tra pari)

(da mapio@github)
Data una sequenza di numeri interi diremo che due numeri pari sono a *distanza* `N` se tra di loro si trovano esattamente `N` numeri dispari e nessun numero pari.

Ad esempio, data la sequenza

```
    1 2 3 4 9 5 6 7 11 3 5 8 13
```

la distanza tra `2` e `4` è `1`, tra `4` e `6` è `2` e tra `6` e `8` è `4`.

Scrivere un programma che dopo aver letto un valore `n`, legga una sequenza di `n` numeri interi e stampi la massima distanza tra i numeri pari in essa contenuti, o `-1` se nella sequenza non ci sono almeno due numeri pari.

Ad esempio, leggendo la sequenza
```
    4 1 3 2 3 4 22 4 5 6 7 8 10 6 12 9
```
il programma deve stampare il valore `2`.

#### Esercizio 5 (Caratteri unici)

(da mapio@github)
Scrivete un programma che, letta una parola composta dai caratteri `a`, ..., `z`, stampi ciascun carattere che la compone una unica volta, nell'ordine in cui vi appare (per la prima volta); altrimenti detto, il programma deve stampare la parola che si otterrebbe da quella data cancellando, a partire dalla sua seconda occorrenza, ogni carattere che vi occorre più di una volta.

Ad esempio, data la parola `mamma` verrà stampato `ma`, e data la parola `pizza` verrà stampato `piza`.

Nota: data una stringa `parola` l'espressione `"a" in parola` vale `True` se la stringa `parola` contiene il carattere `a` e `False` altrimenti; è possibile usare `not in` per testare se un carattere *non* compare in una parola.

## Lezione 6

### Ciclo `while`

Il costrutto `while` è un'alternativa al `for`, che abbiamo già visto, per realizzare un ciclo. La sintassi del `while` è la seguente:
```py
while condizione:
    blocco_istruzioni
```

Quando si incontra un costrutto `while` viene testata la `condizione`: se risulta vera allora si entra nel ciclo, si esegue `blocco_istruzioni`, e si torna a testare la `condizione` per decidere se ripetere nuovamente l'esecuzione di `blocco_istruzioni`. Quando `condizione` è falsa si *esce dal ciclo*, proseguendo con l'istruzione successiva al `while` (in Python, la prima non indentata dopo il ciclo).

Ad esempio, il seguente ciclo stampa tutti i numeri da `1` a `5`, dopodiché stampa la scritta `fine`.

```py
numero = 1
while numero <= 5 and numero > 0:
    print(numero)
    numero += 1

print('fine')
```

Qui, la variabile `numero` vale inizialmente `1`. Si testa poi la condizione `numero <= 5 and numero > 0`, che risulta vera (perché `numero` è minore di 5 e anche maggiore di 0). Si entra allora nel ciclo dove si stampa `numero` (cioè il valore `1`) e poi si incrementa `numero`, che diventa `2`. Poiché la condizione risulta ancora vera si ripete il ciclo, e poi ancora e ancora, finché dopo qualche iterazione `numero` viene incrementato a `6` e il test della condizione da esito negativo (perché `6>5`). A quel punto si esce dal ciclo e viene stampata la stringa `fine`.

Il ciclo appena visto è in effetti più semplice da realizzare con un `for`. Ecco un altro esempio di ciclo `while` dove invece sembra più naturale l'utilizzo del `while` piuttosto che del `for`.

```py
print('Inserisci i nomi dei presenti. Termina con "quit"')
presenti = []
test = True
nome = input()
while nome != 'quit':
    presenti.append(nome)
    nome = input()

print(presenti)
```

Questo ciclo legge una lista di nomi e li inserisce in un array. La lista non ha una dimensione fissata: l'inserimento termina quando viene letta la stringa `quit`. 

Quando si utilizza un ciclo `while` occorre in generale che le istruzioni del ciclo modifichino i valori che vengono testati nella condizione, altrimenti si rischia un ciclo (o *loop*) infinito. Se, ad esempio, nel primo `while` che abbiamo scritto non modifichiamo il valore di `numero`, la condizione resta sempre vera e il programma non esce mai dal ciclo (continua a stampare lo stesso valore). 

Ci sarebbe in realtà un altro modo per forzare l'uscita da un ciclo: l'uso dell'istruzione `break`. Quando il programma incontra questa istruzione esce dal ciclo in esecuzione, indipendentemente dal valore della condizione. L'istruzione `break` può essere usata, ad esempio, dentro un `if`, per dire che quando si verifica una cerca condizione, allora bisogna terminare il ciclo.

Una tecnica talvolta utilizzata per l'implementazione dei cicli è l'uso di una variabile booleana di controllo. Inizialmente si pone questa variabile a `true` per segnalare che si deve entrare nel ciclo. Come condizione del `while` si usa la stessa variabile: mentre questa resta vera si resta nel ciclo. All'interno del ciclo, quando si verificano le condizioni desiderate, si assegna semplicemente alla variabile valore `false`, in modo da provocare l'uscita al successivo controllo della condizione del ciclo.

# Funzioni

Abbiamo già usato diverse funzioni, come, ad esempio:
- `print()`, che riceve in ingresso una stringa, passata tra le parentesi quando la funzione viene *invocata* (un altro termine utilizzato al posto di *invocata* è *chiamata*) e la stampa;
- `max()`, che riceve in ingresso una lista di numeri (o anche un po' di numeri che non fanno parte di una lista) e ne restituisce il valore più grande, senza stampare nulla - il valore *restituito* può essere poi assegnato ad una variabile, stampato o altro, a scelta del programmatore;
- `int()`, che riceve un valore e ne restituisce l'"equivalente" intero.

Abbiamo anche utilizzato funzioni che non sono tra quelle già disponibili in Python, ma sono definite in moduli esterni, che importiamo nel nostro programma. Un esempio è la funzione `random.randint(0,10)` del modulo `random`.

E' anche possibile definire nuove funzioni, da utilizzare poi liberamente nel nostro programma. Per definire una nuova funzione usiamo la parola chiave `def`. Ecco un esempio.

```py
def stampa_menu():
    print("1. Spaghetti al pomodoro")
    print("2. Spinaci della nonna")
    print("3. Frutta di stagione")
    print("4. Patate lesse")

stampa_menu()

print("Vuoi visualizzare di nuovo il menu (s/n)?")
risposta = input()

if risposta.lower() == "s":
    stampa_menu()
else:
    print("arrivederci!")
```

In questo esempio definiamo la funzione `stampa_menu` che non fa altro che eseguire  4 `print()`. Ogni volta che vogliamo visualizzare il menù possiamo invocare la nostra funzione, senza bisogno di riscrivere tutte le `print()`. Questo *riuso* del codice è uno dei motivi per cui si scrivono nuove funzioni.

La funzione che abbiamo appena definito non ha parametri: viene invocata senza passarle alcun valore. Inoltre, non restituisce nulla, ma stampa semplicemente a video delle stringhe. Nell'esempio che segue definiamo una funzione con parametri che restituisce un valore.

```py
def close_test(n1, n2, c):
    if abs(n1 - c) <= abs(n2 - c):
        res = n1
    else:
        res = n2
    return res
n1 = int(input("Inserisci il primo numero: "))
n2 = int(input("Inserisci il secondo numero: "))
c = int(input("Inserisci il numero \"centro\": "))
res = close_test(n1, n2, c)
print(res)
input()
```

La funzione `close_test` riceve 3 numeri `n1`, `n2` e `c`, calcola quale tra `n1` e `n2` è più vicino a `c` e restituisce questo valore. Il nostro programma legge i 3 valori da passare alla funzione, invoca la funzione e salva il valore restituito nella variabile `res`. La variabile `res` viene poi stampata.

Analizziamo meglio cosa succede. Le prime 6 righe di codice non fanno altro che *definire* la funzione. Il programma "non fa nulla" per ora, ma da questo momento in poi è possibile utilizzare (invocare) la funzione `close_test()`. 
Qualche riga più sotto, l'istruzione `res = close_test(n1, n2, c)` invoca effettivamente la funzione. Alla funzione vengono passati i valori `n1`, `n2` e `c`, letti dalle input delle righe precedenti. Inizia quindi l'esecuzione delle istruzioni della funzione. I valori che la funzione riceve vengono copiati in 3 variabili locali alla funzione e non visibili all'esterno della stessa. Queste variabili si chiamano `n1`, `n2` e `c`: i nomi che abbiamo specificato tra parentesi alla prima riga, quando cioè abbiamo definito la funzione. In questo caso particolare, queste variabili hanno esattamente gli stessi nomi delle variabili utilizzate qualche riga più sotto, al di fuori della funzione, ma sono di fatto entità distinte: se modificassimo `n1`, `n2` e `c` all'interno della funzione, questa modifica non avrebbe effetto al di fuori della funzione. 
La funzione si chiude con un'istruzione nuova: `return res`. Questa istruzione *restituisce* il valore contenuto nella variabile `res`.
Riassumendo, quando il programma esegue `res = close_test(n1, n2, c)` viene eseguita la funzione `close_test`, la quale restituisce un valore che viene assegnato alla variabile `res`.

Se avete capito quanto appena scritto, vi sarà chiaro che se sostituiamo interamente la definizione della funzione con quella che segue non cambia nulla: la funzione, e dunque l'intero programma, fa esattamente la stessa cosa.

```py
def close_test(valore_a, valore_b, centro):
    if abs(valore_a - centro) <= abs(valore_b - centro):
        res = valore_a
    else:
        res = valore_b
    return res
```
 
### Operazioni sulle liste

#### List comprehension

In chiusura, vediamo un po' di istruzioni che velocizzano e semplificano le operazioni sulle liste.

Costruiamo una lista di numeri tra 0 e 10 (in un programma, o come qui di seguito, nella console di Python).

```py
>>> lista = list(range(11))
>>> lista
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

Per costruire la lista dei quadrati dei nostri numeri potremmo implementare un ciclo (e lo sapremmo fare molto facilmente). In Python, esiste un modo più rapido ed efficace per costruire liste in queste occasioni: le *list comprehension*:

```py
>>> quadrati = [num**2 for num in lista]
>>> quadrati
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

Ecco altri esempi di *comprensioni di liste*:
```py
>>> succ = [num**2+1 for num in lista]
>>> succ
[1, 2, 5, 10, 17, 26, 37, 50, 65, 82, 101]
>>> succ = [num**2+1 for num in range(100)]
>>> succ
[1, 2, 5, 10, 17, 26, 37, 50, 65, 82, 101, 122, 145, 170, 197, 226, 257, 290, 325, 362, 401, 442, 485, 530, 577, 626, 677, 730, 785, 842, 901, 962, 1025, 1090, 1157, 1226, 1297, 1370, 1445, 1522, 1601, 1682, 1765, 1850, 1937, 2026, 2117, 2210, 2305, 2402, 2501, 2602, 2705, 2810, 2917, 3026, 3137, 3250, 3365, 3482, 3601, 3722, 3845, 3970, 4097, 4226, 4357, 4490, 4625, 4762, 4901, 5042, 5185, 5330, 5477, 5626, 5777, 5930, 6085, 6242, 6401, 6562, 6725, 6890, 7057, 7226, 7397, 7570, 7745, 7922, 8101, 8282, 8465, 8650, 8837, 9026, 9217, 9410, 9605, 9802]  
```

#### Slicing

Le seguenti istruzioni accedono ai primi due elementi della lista `quadrati`.

```py
>>> quadrati[0]
0
>>> quadrati[1]
1
```

Tramite lo *slicing* possiamo ottenere intere porzioni di una lista. Ad esempio, per avere la sottolista composta da tutti gli elementi dalla posizione `1` alla posizione `5` (quest'ultima **esclusa**) di quadrati scriviamo:

```py
>>> quadrati[1:5]
[1, 4, 9, 16]
```

Per ottenere tutti gli elementi dall'inizio e fino alla posizione `5` (esclusa) scriviamo:

```py
>>> quadrati[:5]  
[0, 1, 4, 9, 16]
```

Per ottenere tutti gli elementi dalla posizione `3` alla fine scriviamo:

```py
>>> quadrati[3:]
[9, 16, 25, 36, 49, 64, 81, 100]
```

Per ottenere tutti gli elementi dalla posizione `3` al penultimo (escluso) scriviamo:

```py
>>> quadrati[3:-2]
[9, 16, 25, 36, 49, 64]
```

Possiamo anche ottenere tramite *slicing* tutti gli elementi della lista:

```py
>>> quadrati[:]    
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

Questa operazione apparentemente inutile (perché non usare direttamente la lista `quadrati` piuttosto?) ci può servire quando vogliamo *clonare* un'intera lista per lavorare in maniera distinta su due copie.

Se scriviamo infatti:

```py
>>> l = quadrati
>>> l
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

la variabile `l` diventa un riferimento alla stessa lista `quadrati`. Il problema è che non ne è una copia, ma appunto un riferimento alla stessa lista di elementi in memoria. Ce ne accorgiamo se modifichiamo `l`, perché la modifica si ripercuote su `quadrati`.

```py
>>> l[0] = 1000
>>> l
[1000, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> quadrati
[1000, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```
Assegnando invece a `l` uno *slicing* riusciamo effettivamente a clonare `quadrati` e a lavorare sulle due liste `quadrati` e `l` in maniera indipendente.

```py
>>> l = quadrati[:]
>>> l
[1000, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> l[0]= 0
>>> l
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>> quadrati
[1000, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
>>>
```

### Conclusioni

Sono terminate le 12 ore di introduzione a Python. Se il ritmo è stato per voi troppo alto, potete approfittare di queste dispense per rivedere con calma quanto fatto. 

Se, al contrario, avreste voluto fare di più (ma anche se il vostro giudizio è positivo o neutro!), potete segnalarlo nel questionario di soddisfazione che trovate qui:

> https://www.issvigano.edu.it/servizio/questionari-di-soddisfazione/

cercando "Giochi di Informatica - Introduzione a Python". Siete invitati a compilarlo tutti esprimendo il vostro giudizio e aggiungendo eventuali osservazioni personali. 

Mi raccomando: continuate a programmare! ;)

Se non ne avete, potete chiedere a me o al vostro docente di informatica qualche esercizio o qualche riferimento per studiare argomenti più avanzati. Potete soprattutto (e siete caldamente invitati a farlo!!!) iscrivervi al portale di allenamento delle Olimpiadi di Informatica:

> https://training.olinfo.it/

Qui troverete un percorso di apprendimento con documenti, video ed esercizi (*algobadge*) e numerosi esercizi delle passate edizioni delle competizioni. Attenzione: negli esercizi più datati non sono ammesse soluzioni in Python :(

Qui trovate, inoltre, tutti i link di riferimento per questa competizione (la principale gara di programmazione):

> https://olinfo.it/

Infine, qui

> https://www.vigainsider.it/giochi/

Trovate informazioni utili su molte iniziative (giochi, competizioni, corsi) di informatica a cui la nostra scuola ha aderito negli ultimi anni.

Se vi servono informazioni scrivete. 

Io aspetto le vostre iscrizioni ;)

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

*Visual Studio Code* (*VS Code*, in breve) è un editor di testo con funzionalità avanzate per la programmazione.  È utilizzato come ambiente di sviluppo per scrivere programmi in diversi linguaggi. Noi lo useremo per questo primo esercizio di programmazione in Python. Non è una scelta obbligata: potreste usare un qualsiasi altro editor già installato sul vostro sistema, come *Blocco Note* (scelta sconsigliata!), o l'ambiente di sviluppo *IDLE*, già compreso nel pacchetto di installazione di Python.

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

### Utilizzare l'ambiente Idle

Proviamo a eseguire lo stesso programma nell'ambiente *Idle*, incluso nell'installazione standard di Python. Cerchiamo e apriamo *Idle* sul nostro computer. Si aprirà una finestra con la *shell* che ci permette di inviare comandi direttamente all'interprete Python. Andiamo ora sul menù *file*, scegliamo *open* e apriamo il file *ciao.py* che abbiamo editato prima in VS Code. Si aprirà la finestra dell'editor, dove possiamo vedere e modificare il nostro programma. Accediamo da questa finestra al menù *Run* e selezioniamo *Run module*. Il programma verrà eseguito e l'output visualizzato sulla shell.


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

Alla terza riga viene assegnato alla variabile un nuovo valore: la stringa `"Casa"`. Il valore memorizzato in precedenza, la stringa `"Pietro"` non sarà da questo momento più accessibile, perché il nuovo valore contenuto nella variabile `stringa` è la stringa `"Casa"`. 

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

La maggior parte di queste considerazioni vale per ogni linguaggio di programmazione: tenetelo a mente, quando programmate! ;)



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

### Liste

Una lista è una semplice *struttura dati* che contiene un elenco di elementi.
Una lista è delimitata da parentesi quadre. La lista `[]` è una lista vuota, prima di elementi. La lista `['Pietro']` contiene un solo elemento: la stringa `'Pietro'`. Ecco un esempio che crea una lista di più elementi ed esegue alcune operazioni su di essa.

```py
studenti = ['Andrea','Giovanni','Marco','Giacomo','Maria']

# Gli elementi in una lista sono accessibili tramite indice. Il primo elemento di una lista ha indice 0, il secondo 1, e così via
print(studenti[0]) #stampa il primo elemento
print(f'Il secondo elemento della lista, scritto in maiuscolo, è {studenti[1].upper()}')

studenti[0] = 'Andreina' # modifica il primo elemento in Andreina
```

## Lezione 3

```py
# Prepariamo una lista con i nomi di alcuni studenti
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

Eseguiamo ora alcune operazioni sulle liste, tra cui gli ordinamenti. Come esempio, inseriamo in una lista alcune pizze disponibili in una pizzeria.

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

Scorriamo le liste con il *ciclo* `for`.
Occorre prestare molta attenzione nell'uso del costrutto `for`: dopo l'istruzione `for` tutte le istruzioni che ne fanno parte devono rientrare (si dice: devono essere *indentate*)
L'istruzione `for pizza in pizze:` prende a uno a uno tutti gli elementi della lista `pizze` e li mette nella variabile `pizza`. Al primo *passo* del ciclo nella variabile `pizza` finisce l'elemento `pizze[0]` e vengono eseguite tutte le righe indentate che seguono il `for`. Si torna poi all'inizio del ciclo, `pizza` prende valore `pizze[1]` e si rieseguono le stesse istruzioni, con il nuovo valore di `pizza`. L'esecuzione prosegue così fino a quando `pizze` non ha più elementi.

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

Vi propongo in chiusura alcuni esercizi, parzialmente già risolti in classe.

> #### Esercizio 3.1
>
> Preparate una lista contenente tutti i voti che avete preso in Matematica dall'inizio dell'anno (inserite nella lista almeno 3 voti: se non ne avete 3, inventatene voi qualcuno). Calcolate e stampate il voto massimo, il voto minimo e la media dei voti.
> Se volete, potete utilizzare le funzioni `max`, `min` e `sum` di Python che calcolano, rispettivamente, il valore massimo, il minimo e la somma dei valori di una lista.
>
> Fate la stessa cosa con i voti di Italiano.


> #### Esercizio 3.2
>
> Usando le due liste costruite per l'esempio precedente, provate a calcolare e visualizzare il voto massimo e il voto minimo tra tutti i voti che avete preso, indipendentemente dalla materia.
> Calcolate poi la media complessiva di tutti i voti.
>

> #### Esercizio 3.3
>
> Usando ancora le due liste costruite per l'esempio precedente, calcolate la materia in cui andate meglio. Visualizzate poi sullo schermo un messaggio come questo (utilizzando i vostri dati):
> *La materia in cui vai meglio è matematica. In matematica hai preso finora i seguenti voti: 7, 8, 9, 10*
>

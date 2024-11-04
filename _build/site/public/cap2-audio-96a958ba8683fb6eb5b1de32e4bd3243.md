Audio Digitale
====

## Segnale (audio) digitale

Come abbiamo discusso in precedenza, il fenomeno del suono può riferirsi sia a una sensazione uditiva nell’aria sia alla perturbazione in un mezzo che causa tale sensazione. Una domanda interessante è come si passi da tali fenomeni a numeri all’interno di un computer, memorizzati in un array di interi, ad esempio, che possiamo manipolare a piacimento. E poi, se (e in caso affermativo, come) sia possibile ricostruire un segnale acustico partendo da questi numeri.

Come fenomeno fisico, il suono può essere inteso come una vibrazione, come il movimento di molecole che causa variazioni nella pressione di un mezzo, come l’aria che ci circonda. Queste vibrazioni nell’aria possono quindi essere misurate con un microfono, nel quale la variazione di pressione fa muovere un diaframma (supponendo che si tratti di un microfono dinamico). Questo movimento viene poi tradotto in un segnale di tensione tramite una bobina mobile e un magnete. Abbiamo quindi un’idea di come un segnale passi dall'essere movimento di molecole in un gas a un segnale elettrico. Il segnale di tensione prodotto da un microfono è un segnale continuo, cioè può assumere un valore in qualsiasi momento, come accade per la pressione in un punto nello spazio. Inoltre, anche in un istante di tempo specifico, può assumere un numero infinito di valori diversi, anche se l’intervallo è limitato.

Il segnale audio digitale è una rappresentazione discreta di un segnale audio continuo, ottenuta attraverso processi di campionamento e quantizzazione. A differenza del segnale analogico, che varia in modo continuo nel tempo e nell’ampiezza, il segnale digitale è caratterizzato da valori discreti in intervalli di tempo definiti. L’audio digitale sfrutta principi matematici e tecnici per rappresentare segnali continui in forma discreta e comprensibile per le tecnologie digitali. La frequenza di campionamento e la profondità di bit determinano la fedeltà della rappresentazione, mentre il processo di quantizzazione introduce una piccola distorsione inevitabile. Il risultato finale è un segnale che, pur essendo discreto, conserva gran parte delle caratteristiche del segnale analogico originale, consentendo una riproduzione precisa e flessibile.

Un computer può memorizzare solo un numero finito di valori numerici, e tali valori possono assumere solo un numero finito di possibili valori. Quindi, dobbiamo passare dalla misurazione di infiniti valori temporali, che possono assumere un numero infinito di valori diversi, a una rappresentazione finita. In altre parole, dobbiamo passare da segnali analogici a segnali digitali. In relazione a ciò, si pone anche la questione di come possiamo ricostruire i segnali analogici. I processi coinvolti in tutto ciò si chiamano campionamento, quantizzazione e ricostruzione, rispettivamente.

In termini hardware, un convertitore analogico-digitale (ADC) è un dispositivo, o chip, che converte segnali da analogici a digitali tramite campionamento e quantizzazione, mentre un convertitore digitale-analogico (DAC) converte i segnali digitali in analogici tramite ricostruzione. Nella Figura è mostrato un esempio di sistema di elaborazione audio.

```{image} images/sistema.png
:alt: long
:class: bg-primary mb-1
:width: 700px
:align: center
```
Le vibrazioni nell’aria, rappresentate dal segnale analogico, vengono convertite da un segnale di pressione a uno elettrico dal microfono. Il segnale analogico dal microfono viene poi trasformato in uno digitale tramite l’ADC, dopodiché il segnale digitale può essere elaborato da un computer. Il segnale digitale elaborato può quindi essere convertito in uno analogico tramite il DAC e, infine, riconvertito in un segnale di pressione da inviare, per esempio, ad un altoparlante attivo.

Per quanto riguarda il motivo per cui preferiamo elaborare segnali digitali piuttosto che analogici, ci sono molte ragioni tecniche; le più importanti sono che i computer sono flessibili, possono fare cose che potremmo solo sognare con l’hardware analogico e sono generalmente molto più economici rispetto alla corrispondente soluzione analogica. È interessante notare, a margine, che mentre la maggior parte del mondo ha da tempo compreso i vantaggi dell’elettronica digitale, molti appassionati di apparecchiature musicali sono ancora riluttanti a utilizzare strumenti digitali.

In questo capitolo, spiegheremo cosa sono il campionamento e la quantizzazione, come funzionano e anche come possiamo ricostruire segnali analogici partendo da quelli digitali.

##### Campionamento

Il processo di campionamento trasforma un segnale analogico in un segnale discreto, raccogliendo valori a intervalli di tempo regolari. In linea di principio, il teorema di campionamento di Nyquist-Shannon afferma che, affinché un segnale possa essere rappresentato senza ambiguità, la frequenza di campionamento ￼deve essere almeno il doppio della frequenza massima del segnale originale. 

Supponiamo di avere un segnale nel tempo continuo, $x(t)$, definito per ogni valore reale di $t$ e che vogliamo elaborare con un DSP. Il processo di campionamento comporta la misurazione del valore di questa funzione in istanti di tempo specifici, $t_n$, indicizzati da \( n = 0,1,2,\dots \), per ottenere il segnale $x_n(t)=x(t_n)$, che chiamiamo segnale a tempo discreto. Il modo più semplice e comune di campionare è il campionamento uniforme, che significa campionare a punti equidistanti, cioè,
\[
t_n = T_s n, \qquad n = 0,1,2,\dots
\]

dove $T_s$ è il tempo (in secondi) tra due campioni consecutivi ed è chiamato `periodo di campionamento`. Possiamo osservare che un segnale campionato, o digitale, è in realtà solo una sequenza ordinata di numeri. Più piccolo è ￼, più finemente campioniamo il segnale continuo originale, ￼. Possiamo rappresentare il numero di campioni ottenuti per secondo utilizzando la frequenza di campionamento, definita come

Ecco la traduzione del testo:

La frequenza di campionamento è misurata in Hertz. L’audio viene solitamente campionato a 44,1 kHz e oltre, mentre la voce può essere campionata fino a 8 kHz, il che risulta in segnali comprensibili ma certamente non di alta qualità. Nella Fig. 3.2, il processo di campionamento è esemplificato da un segnale continuo, ￼, che viene campionato per ottenere il segnale a tempo discreto, ￼.

Per esplorare ulteriormente il campionamento, consideriamo un esempio. Supponiamo che ￼ sia una singola sinusoide di frequenza ￼ in Hertz, cioè,
￼. (3.4)
Se campioniamo questo a intervalli regolari, cioè con campionamento uniforme, con un periodo di campionamento di ￼, allora il segnale campionato, che ora è una funzione dell’indice di campionamento ￼, è dato da

Se hai bisogno di ulteriori traduzioni o chiarimenti, fammi sapere!




##### Quantizzazione

Il secondo passo nella digitalizzazione di un segnale è la quantizzazione, che mappa l’ampiezza continua dei campioni del segnale in valori discreti. Questo processo introduce un errore di quantizzazione che può essere definito come la differenza tra il valore reale del segnale e il valore quantizzato.

Se utilizziamo una profondità di ￼ bit per rappresentare ogni campione, il numero di livelli di quantizzazione disponibili sarà pari a ￼. L’intervallo di ampiezza ￼ del segnale sarà suddiviso in questi ￼ livelli, con una risoluzione di quantizzazione (ovvero la distanza tra due livelli di quantizzazione consecutivi) data da:

￼

L’errore di quantizzazione ￼ è generalmente modellato come un rumore uniforme compreso tra ￼ e ￼.

3. Rappresentazione in Frequenza del Segnale Digitale

Una volta che il segnale è campionato e quantizzato, possiamo analizzarlo anche in frequenza. Considerando un segnale discreto ￼ nel dominio del tempo, la sua trasformata di Fourier discreta (DFT) è data da:

￼

dove \( k = 0, 1, \dots, N-1 \) rappresenta le frequenze discrete. La DFT è fondamentale per l’analisi e la manipolazione dei segnali digitali, poiché permette di rappresentare e processare il segnale nel dominio delle frequenze.

4. Codifica e Bitrate

Il bitrate di un segnale digitale audio è la quantità di dati trasmessi per secondo ed è dato da:

￼

dove ￼ è la frequenza di campionamento e ￼ è la profondità di bit. Ad esempio, per un segnale audio a 44.1 kHz e 16 bit di profondità, il bitrate sarà:

￼

In presenza di due canali (stereo), il bitrate raddoppia.

5. Conclusione



## Conversione analogico-digitale (ADC)

## Il processo di campionamento
## Prefiltro passa-basso antialiasing
## Il processo di quantizzazione



## Mean Square Errors (MSE) e Signal to Noise Ratio (SNR)
## Conversione Digitale-Analogica (DAC)

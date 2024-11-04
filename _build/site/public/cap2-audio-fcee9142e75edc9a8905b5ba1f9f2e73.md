Audio Digitale
====
---
##### Introduzione

Il suono, definito come effetto uditivo, è il risultato della percezione delle vibrazioni sonore da parte di un sistema sensoriale dedicato, come l’orecchio umano o microfoni artificiali. Queste vibrazioni sono generate da sorgenti sonore e si propagano attraverso diversi mezzi, con l’aria che è il più comune, ma anche l’acqua e i solidi come le rocce possono trasmettere suoni in modo simile. In sostanza, il suono nasce in natura come vibrazioni meccaniche, si propaga nella stessa forma e viene percepito come tali.

Sin dai tempi antichi, scienziati e inventori hanno cercato di migliorare la propagazione naturale del suono, sviluppando dispositivi artificiali per aumentarne l’efficienza di trasmissione. L’obiettivo era quello di permettere al suono di viaggiare su distanze più lunghe senza subire significativi disturbi, comunemente noti come “rumore”. Inoltre, si è cercato di memorizzare il suono su supporti che permettessero il trasporto nel tempo e nello spazio, consentendo una conservazione permanente delle informazioni sonore.

La svolta decisiva in questo campo si è avuta con l’invenzione del telefono, attribuita a Antonio Meucci, ma brevettata per primo da Alexander Graham Bell. Questo dispositivo ha rivoluzionato la comunicazione, trasformando i segnali sonori in segnali elettrici, in grado di mantenere gran parte delle informazioni originali del suono. I segnali elettrici possono essere trasmessi più facilmente e rapidamente, inizialmente attraverso cavi elettrici e, successivamente, tramite onde elettromagnetiche con l’avvento della radio, sviluppata da Guglielmo Marconi.

Per garantire che il suono potesse essere nuovamente ricostruito all’arrivo, si è stabilita una relazione rigorosa tra il suono originale e le grandezze fisiche associate. Questo processo, noto come trasduzione, consiste nella trasformazione del suono in corrente elettrica, permettendo così di trasmettere informazioni sonore in forma di segnali elettrici. Al ricevitore, questi segnali vengono convertiti nuovamente in suono tramite un altoparlante.

La registrazione dei suoni ha seguito principi simili. Utilizzando variazioni di campo magnetico nei registratori a bobina o i parametri fisici dei solchi nei dischi in vinile, i segnali sonori venivano trascritti su supporti fisici. Con l’avvento delle tecnologie informatiche, la digitalizzazione ha introdotto un nuovo modo di codificare i suoni. In questo caso, i parametri acustici delle onde sonore vengono rappresentati come lunghe sequenze numeriche, dette “digit”, che consentono una rappresentazione precisa dei suoni originali e una riconversione di alta qualità.

Il processo di digitalizzazione implica la conversione delle grandezze fisiche continue (analogiche) in serie numeriche di cifre digitali. Queste sequenze numeriche possono essere memorizzate in vari tipi di supporti, come pen drive, hard disk o memorie ottiche (CD, DVD, Blu-Ray), rendendo così possibile il trasporto e la conservazione delle informazioni sonore nel tempo.

È importante notare che i segnali digitali differiscono qualitativamente e quantitativamente da quelli analogici. Tuttavia, con una frequenza di campionamento adeguata e una buona connessione durante la trasmissione, le differenze possono risultare impercettibili ai sensi umani, sia nell’udito che nella vista.

Attualmente, la conversione del suono in segnali elettrici avviene attraverso l’uso di microfoni, che producono un segnale elettrico ininterrotto quando colpiti da onde sonore. Questo segnale, rappresentato in un certo range di tensione, è considerato un segnale analogico. La conversione in digitale avviene attraverso la lettura ripetuta dei valori di tensione, con l’obiettivo di mantenere una rappresentazione accurata della forma d’onda originale. Il teorema del campionamento stabilisce che, se la frequenza di campionamento è sufficientemente alta, non si perdono informazioni significative.

Le frequenze di campionamento per i segnali audio possono variare da 8000 campioni al secondo per la voce telefonica a 44100 campioni al secondo per audio di qualità musicale. Ogni singolo campione può assumere valori compresi tra un minimo e un massimo, offrendo potenzialmente infiniti valori di lettura.

Per completare la conversione analogico-digitale, è necessario suddividere l’intero range dinamico del segnale in intervalli finiti e codificare ciascun intervallo con un valore digitale. Questo processo si compone di due fasi: quantizzazione e codifica. La quantizzazione suddivide il range in intervalli che sono potenze di due, permettendo che ogni campione venga catalogato in uno di questi intervalli e codificato con n bit. Le applicazioni comuni della digitalizzazione utilizzano un minimo di 8 bit per campione per la telefonia e fino a 20 bit o più per la musica, consentendo una rappresentazione fedele del suono originale.

L’aumento dei bit per campione migliora la qualità del segnale e riduce l’impatto del rumore di quantizzazione, ma già 8 bit sono sufficienti per soddisfare gli standard di alta fedeltà (HiFi). La sequenza numerica risultante, nota come segnale audio digitale, contiene tutte le informazioni necessarie per riprodurre fedelmente la forma d’onda elettrica originale, che a sua volta è un’immagine quasi perfetta del suono originale.

Infine, il segnale audio digitale può essere convertito nuovamente in analogico mediante convertitori D/A, permettendo di ottenere la forma elettrica originaria, che, se inviata a un altoparlante, riproduce il suono originale. Sebbene questo processo introduca rumore, le tecnologie moderne consentono di mantenere il rumore a livelli accettabili. Un ulteriore passo consiste nella codifica del segnale audio digitale, che prevede la compressione delle informazioni per ridurre lo spazio occupato. Tecniche di codifica moderne, come gli standard MP3 e Vorbis, sono ampiamente utilizzate per la diffusione efficace di musica e suoni in generale.

## Segnale audio digitale

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

Supponiamo di avere un segnale nel tempo continuo, $x(t)$, definito per ogni valore reale di $t$ e che vogliamo elaborare con un DSP. Il processo di campionamento comporta la misurazione del valore di questa funzione in istanti di tempo specifici, $t_n$, indicizzati da \(n= 0,1,2,\dots\), per ottenere il segnale $x_n=x(t_n)$, che chiamiamo `segnale a tempo discreto`. Il modo più semplice e comune di campionare è il campionamento uniforme, che significa campionare a punti equidistanti, cioè,
\[
t_n = T_s n, \qquad n = 0,1,2,\dots
\]

dove $T_s$ è il tempo (in secondi) tra due campioni consecutivi ed è chiamato `periodo di campionamento`. Possiamo osservare che un segnale campionato, o digitale, è in realtà solo una sequenza ordinata di numeri. Più piccolo è $T_s$, più finemente campioniamo il segnale continuo originale, $x(t)$. Possiamo rappresentare il numero di campioni ottenuti per secondo utilizzando la `frequenza di campionamento`, definita come
$$f_s=\frac{1}{T_s}.$$

La frequenza di campionamento è misurata in Hertz (Hz). L’audio viene solitamente campionato a $44.1$ kHz e oltre, mentre la voce può essere campionata fino a $8$ kHz, il che risulta in segnali comprensibili ma certamente non di alta qualità. Nella figura 3.2, il processo di campionamento è esemplificato da un segnale continuo, $x(t)$, che viene campionato per ottenere il segnale a tempo discreto $x_n$.

```{image} images/sampling.png
:alt: long
:class: bg-primary mb-1
:width: 400px
:align: center
```

Per esplorare ulteriormente il campionamento, consideriamo un esempio. Supponiamo che $x(t)$ sia una singola sinusoide di frequenza $f$ in Hertz, cioè,

$$x(t)=\sin\left( 2\pi ft \right)$$.

Usando la definizione di frequenza di campionamento, otteniamo 

$$x_n=\sin\left( 2\pi \frac{f}{f_s}n \right)$$.

da cui possiamo definire la seguente quantità

$$\omega=2\pi \frac{f}{f_s}$$

che chiamiamo `frequenza digitale`. Essa esprime il numero di radianti per campione. Da una tale frequenza digitale da sola, quindi, non possiamo determinare quale sarebbe la frequenza in Hertz, a meno che non conosciamo la frequenza di campionamento. Una frequenza digitale di $\omega=2\pi$ corrisponde alla frequenza di campionamento, indipendentemente dal valore che essa assume. Questo spiega intuitivo nel fatto che un segnale digitale è semplicemente una sequenza di numeri; quindi, senza ulteriori conoscenze, non avremmo modo di dedurre nulla riguardo alla frequenza di campionamento.

Ora, la domanda fondamentale che dovremmo porci è questa: quale frequenza di campionamento dobbiamo scegliere per campionare il seno nell’equazione (3.4)? Parlando tecnicamente, ciò di cui ci preoccupiamo quando campioniamo è se lo spettro, ossia i contenuti in frequenza, del segnale campionato è lo stesso di quello del segnale continuo originale. Se lo è, significa che abbiamo una rappresentazione digitale perfetta del segnale analogico. Si può dimostrare che se campioniamo il segnale con una frequenza di campionamento che è più del doppio della frequenza del seno, il segnale campionato avrà lo stesso spettro dell’originale. Ora, sorgono un paio di domande. In primo luogo, come generalizziamo questo risultato a qualsiasi segnale, non solo ai seni? La risposta a questa domanda è che, come abbiamo già accennato, (quasi) qualsiasi segnale può essere considerato composto da un numero di seni, e possiamo utilizzare il principio di prima, secondo cui la frequenza di campionamento deve essere più del doppio delle frequenze dei seni. Quindi, se la frequenza più alta di un seno in un segnale è ￼, allora la frequenza di campionamento dovrebbe rispettare

Se hai bisogno di ulteriori traduzioni o assistenza, non esitare a chiedere!

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


# LSTM-Music-Generation
Generazione di composizioni musicali utilizzando una rete neurale LSTM (Long Short-Term Memory). La rete si addestrerà con file MIDI

## Requirements
- Python 3.x
- Keras
- music21
- Google Colab o una buona GPU

## Librerie utilizzate e dati
Invece di utilizzare interamente i file MIDI, li elaboreremo per ottenere solo le informazioni utili allo scopo e scartare il resto. 

Per questo lavoro verra' usata la libreria [**music21**](http://web.mit.edu/music21/). Questa liberia consente di lavorare facilmente coi MIDI. 
Crea una sua rappresentazione dei MIDI, con oggetti **Note** di **Chord** che rappresentano la musica nei MIDI. E' una rappresentazione piu' facile da leggere rispetto ai MIDI e aiutera' la nostra rete a *capire* la musica e riuscire a creare nuove composizioni.

### Dataset MIDI
Per una maggior accuratezza verranno utilizzate composizioni dello stesso artista. 

Ho compresso in un unico  [file zip](https://github.com/kinycx/LSTM-Music-Generation/blob/main/midi_files.zip) 90 composizioni di musica classica dalla saga videoludica **Final Fantasy** presi da [thefinalfantasy.net](https://thefinalfantasy.net/site/midi-collection.html)

 
Se non si utilizza colab inserire **midi_files.zip** nella directory.

## Diagramma del Modello

![model](https://github.com/kinycx/LSTM-Music-Generation/blob/main/model.png)

## Addestrare il Modello
1. Caricare un file col nome **midi_files.zip** contenente i file .mid con i quali si vuole addestrare la rete
2. Addestrare il modello fino a raggiungere un valore di **loss** inferiore a 0.7
3. Nella sezione *Generazione Musica* del Notebook modificare il percorso della variabile **weights** in base a quale modello si voglia utilizzare per generare una composizione
4. Avviare la generazione della composizione

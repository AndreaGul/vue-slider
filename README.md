# Slider

Descrizione:
Partendo dal markup della versione svolta in js plain, rifare lo slider ma questa volta usando Vue.

lo slider è conposto il 4 parti
dato che vue sia stato collegato correttamente.

Nel data ci definiamo un array che al suo interno contiene tutte le immagini, titoli e paragrafi che andranno inserite nel dom

1 immagine principale

per inserire un immagine usando il tag img
e v-bind sull'atributo src ci andiamo a chiamare la proprieta che al suo interno ha l'immagine

2 titolo e descrizione della serie

per inserire il titolo in data ci andiamo a definire una proprietà title e al suo interno ci andiamo ad inserire il nome della serie
A sua volta anche per il testo

all'interno del div con classe id app e,
all'interno dell'h3 ci andiamo con la sintassi baffo baffo e vado ad inserire il nome della proprieta' che contiene il titolo

3 banner con tutte le immagini
Per inserire più immagini useremo il ciclo v-for quindi per slide in slides nel src dell'immagine vado a inserire sempre con il v-bind davanti al src l'img presa dal for.

3.1 l'immagine principale nel banner, ha una classe active che rappresenta appunto l'immagine principale, per renderla dinamica anche per futuri passaggi, utilizzando v:bind e if dato dall'operatore ternario, posso inserire in una sola riga che: la classe da aggiungere dipende dal fatto che se dato index = 0 se ? si mi restitusce "active" se : no mi restituisce un stringa vuota

4 lo slider presenta la funzionalità che al click sulle freccetta le immagini vadano avanti o indietro

4.1 nell'html affianco al tag contenente la freccia andiamo ad inserire l'event handler v-on:click="handler" che avra come handler la funzione che dobbiamo crearci nei methods di vue nel js

la funzione next al suo interno dovra contenere un incremento di varibile in modo tale da cambiare indice dell'immagine principale
nei data quindi ci andiamo a definire una proprietà position che avra un valore di partenza di 0 e all'interno di next incrementeremo il suo valore di 1.
Quindi ogni volta che si clicchera sulla freccia next l'indice cambiare
Al momento cambia solo il valore della prprieta position senza variare il dom quindi c'è bisogno di collegarli.
Nell'al posto degli indici che indicano che immagine sto prendendo dall'array vado and inserire il nome della proprietà position

nella funzione prev vado ad inserire una decrementazione del lavore di position

4.2 all'interno di prev e next devo andare ad inserire una condizione per quando lindice supera o è inferiore agli elementi presenti nell'array

nella funzione next dovrò andar ad inserire una condizione nella quale se position è maggiore della lunghezza dell'array slides -1 allora position sarà= a 0

nella funzione prev se position è minore di 0 allora position sarà uguale alla lunghezza dell'array -1

Bonus:
1- al click su una thumb, visualizzare in grande l'immagine corrispondente
2- applicare l'autoplay allo slider: ogni 3 secondi, cambia immagine automaticamente
3- quando il mouse va in hover sullo slider, bloccare l'autoplay e farlo riprendere quando esce

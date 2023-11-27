# Slider

Descrizione:
Partendo dal markup della versione svolta in js plain, rifare lo slider ma questa volta usando Vue.

lo slider è conposto il 4 parti
dato che vue sia stato collegato correttamente

1 titolo della serie

per inserire il titolo in data ci andiamo a definire una proprietà titolo e al suo interno ci andiamo ad inserire il nome della serie

all'interno del div con clsse id app
all'interno dell'h1 ci andiamo a con la sintassi baffo baffo ci vado ad inserire il nome della proptrieta ch contiene il titolo

2 immagine principale
nel data ci definiamo un array che al suo interno contiene tutte le immagini che andranno inserite nel dom

per inserire un immagine usando il tag img
e v-bind sull'atributo src ci andiamo a chiamare la proprieta che al suo interno ha l'immagine

3 banner con tutte le immagini
per inserire più immagini useremo il ciclo v-for quindi per img in imgs nel src dell'immagine vado a inserire sempre con il v-bind davanti al src l'img presa dal for

3.1 l'immagine principale nel banner ha una classe active che rappresenta appunto che è la principale, per renderla dinamica anche per futuri passaggi, utilizzando v:bind e if dato dal quoziente ternario io posso inserire in una sola riga che la classe da aggiungere dipende dal fatto che se dato position = 0 se ? si mi restitusce "active" se : no mi restituisce un stringa vuota

4 descrizione dell'immagine mostra
vado a definire in data tutte le proprietà che contengono i dati da inserire nella descrizione, con il markup html e la sintassi baffo baffo inserisco i dati interessati

5 lo slider presenta la funzionalità che al click sulle freccetta le immagini vadano avanti o indietro

5.1 nell'html affianco al tag contenente la freccia andiamo ad inserire l'event handler v-on:click="handler" che avra come handler la funzione che dobbiamo crearci nei methods di vue nel js

la funzione next al suo interno dovra contenere un incremento di varibile in modo tale da cambiare indice dell'immagine principale
nei data quindi ci andiamo a definire una proprietà position che avra un valore di partenza di 0 e all'interno di next incrementeremo il suo valore di 1.
Quindi ogni volta che si clicchera sulla freccia next l'indice cambiare
Al momento cambia solo il valore della prprieta position senza variare il dom quindi c'è bisogno di collegarli.
Nell'al posto degli inici che indicano che immagine sto prendendo dallarray vado and inserire il nome della proprietà position

nella funzione prev vado ad inserire un decrementazione del lavore di position

5.2 all'interno di prev e next devo andare ad inserire una condizione per quando lindice supera o è inferiore agli elementi presenti nell'array

nella funzione next dovrò andar ad inserire una condizione nella quale se position è maggiore della lunghezza dellarray imgs -1 allora position sarà= a 0

nella funzione prev se position è minore di 0 allora position sarà uguale alla lunghezza dell'array -1

Bonus:
1- al click su una thumb, visualizzare in grande l'immagine corrispondente
2- applicare l'autoplay allo slider: ogni 3 secondi, cambia immagine automaticamente
3- quando il mouse va in hover sullo slider, bloccare l'autoplay e farlo riprendere quando esce

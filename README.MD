#  DS_SUN.BAS - Earth-Sun Distance & Solar Diameter

**DS_SUN** è un calcolatore astronomico ad alta precisione scritto in **QuickBASIC 4.5**. Il programma determina la distanza istantanea tra la Terra e il Sole (Distanza Eliocentrica) e il conseguente diametro angolare apparente del disco solare visto dal nostro pianeta.

La precisione raggiunta dai modelli implementati (in particolare il metodo di Keplero e quello di Meeus) presenta scarti minimi (circa 1000 km) rispetto alle effemeridi professionali moderne.

##  Metodi di Calcolo Implementati

Il software confronta tre approcci matematici per la risoluzione dell'orbita terrestre:

1.  **Metodo Classico (DS0):** Una soluzione analitica basata sull'anomalia media con termini correttivi di secondo ordine.
2.  **Metodo di Keplero (Newton-Raphson):** Risolve l'equazione trascendente di Keplero $M = E - e \sin(E)$ utilizzando il metodo iterativo di Newton-Raphson (6 iterazioni). Questo permette di ricavare l'Anomalia Eccentrica con estrema precisione.
3.  **Metodo di Jean Meeus (Equazione del Centro):** Implementa l'equazione del centro e considera l'eccentricità dell'orbita terrestre come una variabile che muta nel tempo, garantendo un'accuratezza superiore sul lungo periodo.

##  Output del Programma
Per ogni metodo, il programma fornisce:
* **Distanza istantanea** espressa in chilometri (km).
* **Diametro Angolare** del Sole, formattato in Primi (') e Secondi ('') d'arco.



[Image of Earth's orbit around the sun showing perihelion and aphelion]


##  Dettagli Tecnici
* **Costanti Astronomiche:** Utilizza l'Unità Astronomica (AU) definita come $149.597.870$ km e il diametro solare reale di $1.392.700$ km.
* **Precisione:** Calcolo interamente in doppia precisione a 64-bit (`DEFDBL`).
* **Epoca:** Calcolo basato sui giorni trascorsi dal **J2000.0**.

---
*Sviluppato da Marco da Venezia (1990 - rev. Gennaio 2026)*

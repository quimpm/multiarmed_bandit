# Restless bandit

Aquest document es per a fer el guió del video.

### Restless

*Video amb cara*

El problema de multiarmed bandits pot ser convertit amb un problema més
difícil afegint una evolució en les màquines. Per aixo s'utilitza el
que s'anomenen les cadenes de Markov.

*Segueix amb un video de l'explicació on es dibuixa un graf estil markov
i s'explica el càlcul amb matrius i vectors.*

Amb aquestes màquines es poden descriure de la següent forma: **exemple amb
pluja i sol, probabilitats amb tal tal.**

*Subratllant la matriu i posant en diferents perspectives*

Tornant al nostre problema, podem expressar dues cadenes de Markov, la
primera amb la que canviarà la màquina que hem triat, i la segona amb
la que canviarà les màquines que no hem triat.

*Video amb cara* 

Aquesta simplificació és interessant, ja que seguint amb l'exemple del
restaurant, que un restaurant canvies o no de cuiner podria modificar
la nostra percepció de "Guanyar-Perdre", però aquest canvi no necessita
que nosaltres anem a aquest restaurant en específic.

## PSPACE

La primera vegada que vam veure aquest problema vam trobar la informació
erronia que aquest pertanyia a NP. A l'any 1999, **nom dels autors** van
demostrar que pertanyia a PSPACE-hard, una categoria més complexa que NP.

Però, per explicar com ho van demostrar, primer hem de saber la diferencia
entre una complexitat hard i una complexitat completa. 

*Seguint amb un paper, es dibuixa les complexitats hard i completa*

Quan ens referim a que un problema és, per exemple, NP-complet, ens referim
a que aquest problema es pot transformar en qualsevol dels altres problemes
NP-complet i que qualsevol problema NP-complet es pot transformar en aquest.

Quan ens referim a que un problema és hard, significa que tots els problemes
complets es poden transformar en aquest problema però no es sap com fer-ho
en el sentit contrari.

*Amb un altre paper s'explica on està PSPACE*

Algunes de les complexitats dels problemes poden quedar així. Dins d'aquestes
complexitats, que NP sigui subconjunt de PSPACE ens va soptar. Però, la demostració
es senzilla. Una de les definicions de NP és donada una instància del problema
podem aconseguir la solució d'aquesta en temps polinomial. En l'exemple del SAT,
seria comprovar que una Interpretació és soluble en la Formula. La definició de
PSPACE és que la memòria que ocupa en la MT és polinomial. Llavors podem arribar
a l'absurd que una màquina de turing pertanyent a NP tingués més memòria que 
polinomial, significaria que com a mínim ha gastat un cicle en llegir-escriure-ho
i per tant no té un temps polinomial.

*Video amb cara*

Llavors, tornant a la demostració de PSPACE-hard, els autors estaven treballant
amb un problema de Xarxes demostrant que la solució òptima no es podia donar en
un temps menor a l'EXP, i per a fer-ho demostren que un dels problemes relaxats 
és PSPACE-complet. Finalment, a l'ultima secció fent un resum de les conclusions,
es diu com reduir aquest problema al problema de restless bandit, deixant el nostre
problema com a PSPACE.

## Upper Confidence Bound

*Video amb cara*

Que el problema sigui PSPACE-hard ens dona a pensar que una solució optima amb un
temps raonable és, al menys, dificil. Llavors, com podem afrontar un problema que
troba el seu òptim és poc raonable. La primera pregunta que ens hem de fer és si
la diferència entre un suboptim i un optim ens interessa. Llavors un mecanisme
que es sol a fer és la relaxació del problema. Per exemple, un problema de restless
bandit relaxat és un problema de multiarmed bandit. Una solució d'aquest problema 
està demostrat que és una bona heurística pel problema de restless. Dins dels algorismes
que es solen a utilitzar per aquests problemes és el de **Upper Confidence Bound**.



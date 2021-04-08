man(Gabriel).
man(Felipe).
man(Diego).
man(Nick).
man(Alan).
man(Bruno).
woman(Mariana).
woman(Lucy).
woman(Vicki).
woman(Karla).
woman(Angela).
woman(Carla).
family(Gabriel,Mariana).
family(Mariana,Gabriel).
family(Felipe,Lucy).
family(Lucy,Felipe).
family(Angela,Alan).
family(Alan,Angela).
son(Felipe,Gabriel).
son(Felipe,Mariana).
son(Diego,Felipe).
son(Diego,Lucy).
son(Nick,Felipe).
son(Nick,Lucy).
son(Bruno,Angela).
son(Bruno,Alan).
daughter(Vicki,Felipe).
daughter(Vicki,Lucy).
daughter(Angela, Gabriel).
daughter(Angela,Mariana).
daughter(Carla,Angela).
daughter(Carla, Alan).
parent(A,B):-son(B,A);daughter(B,A).
father(A,B):-man(A);parent(B,A).
mother(A,B):-woman(A);parent(B,A).
grandpa(A,B):-parent(A,C), parent(C,B), man(A).
grandma(A,B):-parent(a,C), parent(C,B), woman(A).
brother(A,B):-parent(C,A), parent(C,B), man(A).
sister(A,B):-parent(C,A), parent(C,B), woman(A).
aunt(A,B):-sister(A,C), parent(C,B).
uncle(A,B):-brother(A,C), parent(C,B).

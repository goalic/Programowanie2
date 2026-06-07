Programowanie 2: Projekt

Wybrany zbiór danych: Video_Game_Sales_as_of_Jan_2017.csv


Zbiór danych zawiera 17415 wierszy (gry) i 15 kolumn, opisujących różne właściwości gier:
Name (potem usunięty do dalszej analizy) - Platform (Nintendo/PC/PS itp.) - Year_of_Release (1991 - 2009) - NA/EU/JP/Other/Global_Sales (w milionach) - Critic/User_Count - Critic/User_Score


Celem analizy jest przewidywanie zmiennej Global_Sales - stała się ona zmienną przewidywaną (fred_Y), oddzieloną od zmiennych przewidujących (fred_X).


Po One Hot Encodingu i podziale na zbiory testowe i treningowe, dane wyglądają następująco:

X_train: (13932, 687)

X_test: (3484, 687)

Y_train: (13932,)

Y_test: (3484,)


Z uwagi na to, że Global_Sales jest zmienną numeryczną, ciągłą - a więc liniową - zastosowałam modele: Regresja Liniowa (model 1) oraz Random Forest Regressor (model 2)


MODEL 1: REGRESJA LINIOWA

a) na zbiorze treningowym,
- RMSE = 0.003 [na skalowanych danych]
- RMSE = 0.005 [po odwróceniu skalowania]

b) na zbiorze testowym:
- RMSE = 0.003 [na skalowanych danych]
- RMSE = 0.005 [po odwróceniu skalowania]


MODEL 2: RANDOM FOREST REGRESSOR

a) na zbiorze treningowym
- RMSE = 0.197 [na skalowanych danych]
- RMSE = 0.218 [na odwróceniu skalowania]

b) na zbiorze testowym
- RMSE = 0.127 [na skalowanych danych]
- RMSE = 0.194 [na odwróceniu skalowania]

RMSE MODELU 1 < RMSE MODEL 2 ==> REGRESJA LINIOWA RADZI SOBIE LEPIEJ, dlatego próbuję jeszcze dobrania hiperparametrów do Random Forest


Nawet po zastosowaniu hiperparametrów, RMSE Random Forest = 0.526.

Zatem modelem, który sprawdził się lepiej jest Regresja Liniowa z RMSE wynoszącym: 0.005

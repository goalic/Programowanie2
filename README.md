Programowanie 2: Projekt

Wybrany zbiór danych: Video_Game_Sales_as_of_Jan_2017.csv


Zbiór danych zawiera 17415 wierszy (gry) i 15 kolumn, opisujących różne właściwości gier:
Name (potem usunięty do dalszej analizy) - Platform (Nintendo/PC/PS itp.) - Year_of_Release (1991 - 2009) - NA/EU/JP/Other/Global_Sales (w milionach) - Critic/User_Count - Critic/User_Score

Baza danych została podzielona na zbiór treningowy (80%) i testowy (20%)

Celem analizy jest przewidywanie zmiennej Global_Sales - stała się ona zmienną przewidywaną, oddzieloną od zmiennych przewidujących.


Kształt zbiorów zaaplikowanych do modeli wyglądają następująco:

X_train: (13932, 634)
Y_train: (13932,)

X_test: (3484, 634)
Y_test: (3484,)


Z uwagi na to, że Global_Sales jest zmienną o postaci ciągu liczb, zastosowano modele liniowe: Regresję Liniową (model 1) oraz Random Forest Regressor (model 2).


MODEL 1: REGRESJA LINIOWA

a) na zbiorze treningowym,
- RMSE = 1.206

b) na zbiorze testowym:
- RMSE = 1.836


MODEL 2: RANDOM FOREST REGRESSOR

a) na zbiorze treningowym
- RMSE = 1.099

b) na zbiorze testowym
- RMSE = 1.704

PO GRID SEARCH:
- RMSE = 1.682

WYNIKI:

RMSE dla Random Forest z hiperparametrami: 1.6830
RMSE dla regresji liniowej: 1.8364

Zatem skuteczniejszym modelem jest Random Forest.

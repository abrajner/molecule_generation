#Projekt zaliczeniowy - Studio projektowe 2 
skład zespołu: Alicja Brajner, Krzysztof Pala 

źródło kodu: https://github.com/awslabs/dgl-lifesci/tree/master/examples/generative_models/dgmg

##Przygotowanie środowiska
Do uruchomienia projektu konieczne są cztery biblioteki: rdkit, dgllife, dgl, torch.

Powinny zostać zaainstalowane w wirtualnym środowisku za pomocą następujących komend: 
```
conda install rdkit

pip install dgllife

pip install dgl

pip install torch
```

##Uruchomienie projektu 
Następnie z terminala należy uruchomić komendy: 

```
python train.py -d ChEMBL -o canonical -w 1
```

Obecnie ilośc epok ustawiona jest na 3, w przypadku kiedy trening zajmowałby zbyt dużo czasu
liczbę tę można zmienić w pliku utils.py w linii 129. 

Po zakończonym treningu należy wykonać evaluację przy użyciu następującej komendy

```
python eval.py -d ChEMBL -o canonical -p ./training_results/
```
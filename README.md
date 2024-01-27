Le projet consiste à implémenter en Python, d’entraîner et d’évaluer
un modèle de plongement de mots statique semblable au célèbre algorithme
word2vec. Le modèle de base que nous avons implémenté ici est alors le modèle skip gram with negative sampling. Nous démarrons par une implémentation basique de la méthode susmentionnée, puis nous proposons une implémentation des améliorations de ce modèle comme proposé dans le papier de Mikolov. 

## Contenu :

Dans ce projet vous trouverez les dossiers et fichiers suivants: 

- `/data`: dossier des données d'entraînement tokénisés et données d'évaluation basés sur Le Comte de Monte Cristo d'Alexandre Dumas,
    - `/Le_comte_de_Monte_Cristo.100`: jeu de données pour l'évaluation des modèles
    - `/Le_comte_de_Monte_Cristo.train`: texte tokenisé d'entraînement des modèles 
- `/embeddings`: dossier des embeddings créés à l'issu de l'apprentissage. Il manque le fichier d'embeddings pour w2v.py 
en raison d'un oubli de sauvegarde dans le code, mais il n'a pas été regénéré en raison du coût en temps de l'entraînement
    - `/embeddings_amelioration_train.txt`: embeddings sous format txt du modèle w2v_amelioration.py
- `/eval_w2v.py`: code d'évaluation d'un modèle word2vec. Il peut s'executer de la même manière que les modèles, à condition d'y avoir
indiquer dans le code dans les paramètres le chemin du fichier d'embeddings issu du modèle évalué.
- `/requirements.txt`: liste les librairies à installer pour le projet
- `/tp_w2v.pdf`: sujet du projet
- `/w2v_amelioration.py`: implémentation du modèle w2v amélioré selon la méthode présentée par Mikolov (cf. piste à creuser)
- `/w2v.py`: implémentation du modèle initial w2v.

## Execution du code
Installez les librairies nécessaires: 
```sh
pip install -r requirements.txt
```

Les fichiers .py sont équipés du test 
```python
if __name__ == '__main__':
```
Pour exécuter l'entraînement d'un des deux modèles, il suffit d'executer dans le terminal:
```sh
python <nom du fichier>
```
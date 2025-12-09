# Project-09-M1-biochimie-
# for Biology Master tlemcen ...13/12/2025
#Marsi Chaimae, master 1 biochimie  13/12/2025
#Les membres de groupe 
#Guermat fatima zohra 
#Maasri nihel
#Tikhemarine sihem
#Benhamida manel
import pandas as pd
# Données : séquences ADN, longeur, pourcentage de GC data = {
"séquence":["ATGCGTACGTA","GCTAGCTAGGCC","ATGCGCGTAAGT","TACGATCGTA","ATGAAAGGCTT","CGTACGTAGC","TTAACCGGAT"]
"Longueur"[12,12,12,10,11,10,10],
"Pourcentage GC":[50,66.67,58.33,40,45.45,60,50]
}
# Création d'un DataFrame(tableau Pandas)
df=pd.DaraFrame(data)
print("**************Créaction et affichage**************")
# affichage du tableau
print("tableau des Séquences ADN :")
print(df)


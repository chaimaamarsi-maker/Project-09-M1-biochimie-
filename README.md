#Projecrt-09-M1-biochimie-
# for Biology Master tlemcen ...13/12/2025
#Marsi Chaimae, master 1 biochimie  13/12/2025
#Les membres de groupe 
#Guermat fatima zohra 
#Maasri nihel
#Tikhemarine sihem
#Benhamida manel
import pandas as pd
# Données : séquences ADN, longeur, pourcentage de GC 
data = {
"séquence":["ATGCGTACGTA","GCTAGCTAGGCC","ATGCGCGTAAGT","TACGATCGTA","ATGAAAGGCTT","CGTACGTAGC","TTAACCGGAT"],
"Longueur":[12,12,12,10,11,10,10],
"Pourcentage GC":[50,66.67,58.33,40,45.45,60,50]
}
# Création d'un DataFrame(tableau Pandas)
df = pd.DataFrame(data)
print("**************Créaction et affichage**************")

# affichage du tableau
print("tableau des Séquences ADN :")
print(df,"\n\n")

# Opération sur les tableaux:
print("************** Opération**************")
#1) sélectionner la colonne “Longueur”
Longueur = df["Longueur"]
print(Longueur)
#3)Filtrer les séquences avec un Longueur supérieur à 10
print("************** Filtrage avec Longueur **************")
# Filtrer les séquences avec un Longueur supérieur à 10
filtered_df = df[df["Longueur"] > 10]
print(filtered_df)
#4) Calculer la moyenne du pourcentage de GC
print("************* Calcul de la moyenne*************")
# Calculer la moyenne du pourcentage de GC
average_gc = df["Pourcentage GC"] .mean()
print(f"Pourcentage moyen de GC : {average_gc:.3f}%") 
#5) Ajouter une nouvelle colonne avec des calculs
print("************* Ajouter une nouvelle colonne *************") 
# Ajouter une nouvelle colonne "Catégorie GC" 
df["Catégorie GC"] = df["Pourcentage GC"].apply(lambda x: "Riche" if x > 55 else ("Moyen" if 45 <= x <= 55 else "Faible"))
print(df)
# 6)Ajouter une colonne comptant les 'G'
df["Nombre de G"] = df["séquence"].str.count("G")

print("=====6) Nombre de G ajoutés =====")
print(df, "\n")
# 7) Calculer l'écart type de Pourcentage GC et de longueur
écart_type_gc = df["Pourcentage GC"].std()
écart_type_long = df["Longueur"].std()
print("===== Écart type =====")
print("Écart type de pourcentage GC:", écart_type_gc)
print("Écart type de longueur:", écart_type_long)
print(df,"\n\n")
#7) Sauvegarde et chargement des données avec pandas
#Sauvegarder le DataFrame dans un fichier csv
df.to_csv("tableau_séquence.csv", index=Flase)

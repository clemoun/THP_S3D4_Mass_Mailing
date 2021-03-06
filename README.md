# Introduction
Bienvenue sur ce repo d'envoi d'emails et de follow en maaaaaaaasse. 

### Equipe
Projet THP mené par le __groupe 3 de Montpellier__ :
* Herve Lee
* Arthur Vouloir
* Thierry Delongueville
* Clement Baldy

### Les grandes lignes du programme
Ce programme a pour objectif d'interpeler les mairies de 3 départements: __Pyrénées-Atlantiques__ , __Hérault__ et __Gard__.
Pour cela il va
* Scrapper les emails de toutes les mairies de ces 3 départements
* Les stocker dans un CSV bien rangé
* Envoyer un email à chaque mairie
* Trouver les mairies sur Twitter et les follow pour pouvoir les interpeller un peu


### Lancer le programme
1. Clonez ou downloadez le repo Github
2. Taper les lignes suivantes:
```$ bundle install```
```$ ruby app.rb```
3. Ensuite lancez des scrapping (choix 1 à 3)
4. Faites un dump des résultats dans un .csv (choix 4)
5. A partir du CSV vous pouvez lancer un mailing (choix 5)
6. Trouvez les comptes Twitter (choix 6) des villes pour les follow (choix 7)

# Arborescence des programmes
1. Un programme `townhalls_scrapper` va scrapper les emails de toutes les mairies de ces départements
2. Un programme `townhalls_adder_to_db` va passer ces emails dans une base de données (townhalls.csv)
3. Un programme `townhalls_mailer.rb` va envoyer un email à chacune de ces mairies
4. Un programme `townhalls_follower.rb` va compléter `townhalls.csv` avec les handles Twitter des mairies et les follow sur Twitter


# Mode d'emploi
Lancez la commande `$ ruby app.rb`
Utilisez ensuite l'interface du terminal pour lancer les différents programmes.

### Important !

La fonction "inscrire dans un csv" ne sera réalisée que si au moins un département est scrappé.
Les fonctions "mails" et "twitter" ne seront réalisée que si le CSV contient au moins un département.


### gem utilisées :
* Gmail
* twitter
* pry
* csv
* dotenv
* nokogiri
* bundler


# Travail réalisé

### Texte de l'email envoyé:  

Bonjour,
        Je m'appelle Arthur, je suis élève à The Hacking Project, une formation au code gratuite, sans locaux, sans sélection, sans restriction géographique. La pédagogie de notre école est celle du peer-learning, où nous travaillons par petits groupes sur des projets concrets qui font apprendre le code. Le projet du jour est d'envoyer (avec du codage) des emails aux mairies pour qu'ils nous aident à faire de The Hacking Project un nouveau format d'éducation pour tous.
        Déjà 500 personnes sont passées par The Hacking Project. Est-ce que la mairie de xxxx veut changer le monde avec nous ?
        Charles, co-fondateur de The Hacking Project pourra répondre à toutes vos questions : 06.95.46.60.80

### Nombre de mairies contactées:  

Le programme a contacté en tout 1243 mairies dans les 3 departements.

### Nom du compte Twitter utilisé pour le bot:  
@ArthurVouloir

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
COMMENT ÇA FONCTIONNE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1 SEUL FICHIER index.html pour TOUS (profs + élèves)

Les niveaux sont chargés dynamiquement via l'URL :
   https://lejardindesoiseaux.com/jeumotif/index.html?prof=nomprof


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
POUR LE PROFESSEUR
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. Aller sur : https://lejardindesoiseaux.com/jeumotif/
2. Mode professeur (mot de passe : prof123)
3. Créer vos niveaux
4. Cliquer "☁️ Sauvegarder en ligne"
5. Entrer votre nom (ex: dupont)
6. Copier le code généré automatiquement
7. Sauvegarder

➜ Vous obtenez une URL comme :
   https://lejardindesoiseaux.com/jeumotif/index.html?prof=dupont


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
POUR LES ÉLÈVES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

L'élève ouvre l'URL fournie par le prof :
   https://lejardindesoiseaux.com/jeumotif/index.html?prof=dupont

➜ L'application :
   ✅ Charge automatiquement les niveaux du prof
   ✅ Force le mode élève
   ✅ Masque le bouton "Mode Professeur"
   ✅ Affiche "Niveaux de dupont" discrètement


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
FICHIERS CRÉÉS SUR LE SERVEUR
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

data/
├── dupont.json          (5-10 Ko)
├── martin.json          (5-10 Ko)
└── .rate_limits.json    (1 Ko)



━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
SÉCURITÉ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📍 Élèves : Chargement PUBLIC (sans mot de passe)
   → Action : load_public
   → Lecture seule des niveaux

📍 Professeur : Modification PROTÉGÉE (avec mot de passe)
   → Action : load (avec authentification)
   → Peut modifier et re-sauvegarder


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
INSTALLATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. Upload via FTP dans /www/jeumotif/ :
   - index.html
   - api.php
   - .htaccess
   - data/ (dossier vide)


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
EXEMPLE D'UTILISATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Prof Martin sauvegarde ses niveaux :
➜ Fichier créé : data/martin.json 
➜ URL élèves : https://lejardindesoiseaux.com/jeumotif/index.html?prof=martin

Prof Dupont sauvegarde ses niveaux :
➜ Fichier créé : data/dupont.json
➜ URL élèves : https://lejardindesoiseaux.com/jeumotif/index.html?prof=dupont



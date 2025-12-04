╔═══════════════════════════════════════════════════════════════╗
║              VERSION OPTIMISÉE - Plus de fichiers HTML !      ║
╚═══════════════════════════════════════════════════════════════╝

✨ NOUVEAUTÉ : ÉCONOMIE D'ESPACE

Avant : 450 Ko par professeur (index.html dupliqué)
Après : 5-10 Ko par professeur (seulement le JSON)

🎯 GAIN : ~440 Ko par professeur !


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
├── dupont.json          (5-10 Ko) ✅ Petit !
├── martin.json          (5-10 Ko)
└── .rate_limits.json    (1 Ko)

PLUS de fichiers .html de 450 Ko !


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
TEST LOCAL (XAMPP)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. Copier le dossier dans C:\xampp\htdocs\jeumotif_optimise\
2. Démarrer Apache
3. Tester en tant que prof :
   http://localhost/jeumotif_optimise/index.html
4. Sauvegarder (nom: test)
5. Tester en tant qu'élève :
   http://localhost/jeumotif_optimise/index.html?prof=test


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
AVANTAGES
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✅ Économie d'espace : ~440 Ko par prof
✅ 1 seul fichier à maintenir (index.html)
✅ Mises à jour facilitées
✅ URL propre et simple
✅ Sécurité : les élèves ne peuvent pas modifier
✅ Le JSON reste protégé (avec mot de passe pour le prof)


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

2. Permissions :
   chmod 755 data/
   chmod 644 index.html api.php .htaccess

3. Tester :
   https://lejardindesoiseaux.com/jeumotif/

Vous pouvez supprimer template-eleve.html si présent (plus utilisé).


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
EXEMPLE D'UTILISATION
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Prof Martin sauvegarde ses niveaux :
➜ Fichier créé : data/martin.json (8 Ko)
➜ URL élèves : https://lejardindesoiseaux.com/jeumotif/index.html?prof=martin

Prof Dupont sauvegarde ses niveaux :
➜ Fichier créé : data/dupont.json (7 Ko)
➜ URL élèves : https://lejardindesoiseaux.com/jeumotif/index.html?prof=dupont

Total serveur : 456 Ko (index.html) + 15 Ko (2 JSON) = 471 Ko
Au lieu de : 456 Ko + 456 Ko + 456 Ko = 1.3 Mo


━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CAPACITÉ
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Avec 100 Mo disponibles sur OVH :

Version ANCIENNE : ~220 profs max (450 Ko chacun)
Version OPTIMISÉE : ~12 000 profs max (8 Ko chacun)

En pratique, vous aurez largement assez d'espace ! 🎉

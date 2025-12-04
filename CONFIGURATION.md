# Configuration de Programmation Motifs

## Modifier la limite maximale de niveaux

Par défaut, l'application autorise la création de **100 niveaux maximum** (tous cursus confondus).

### Pour changer cette limite :

#### 1. Dans `index.html`

Modifiez la ligne **1860** :

```javascript
const MAX_TOTAL_LEVELS = 100; // ← Changez cette valeur
```

Exemple pour autoriser 500 niveaux :
```javascript
const MAX_TOTAL_LEVELS = 500;
```

#### 2. Dans `api.php`

Modifiez la ligne **16** pour qu'elle corresponde :

```php
define('MAX_TOTAL_LEVELS', 100); // ← Changez cette valeur
```

Exemple pour autoriser 500 niveaux :
```php
define('MAX_TOTAL_LEVELS', 500);
```

**IMPORTANT :** Les deux valeurs doivent être identiques !

### Ajustements automatiques

Lorsque vous modifiez `MAX_TOTAL_LEVELS`, tout le reste s'adapte automatiquement :

✅ Validation dans la popup "Création automatisée des niveaux"
✅ Blocage des compteurs quand la limite est atteinte
✅ Messages d'erreur avec la bonne limite
✅ Validation lors de l'ajout manuel de niveaux
✅ Vérification côté serveur (api.php)

### Limite pour cursus "Tous"

La constante `MAX_LEVELS_PER_INPUT_ALL` (ligne 1861) définit la limite pour le cursus "Tous" :

```javascript
const MAX_LEVELS_PER_INPUT_ALL = 33; // Cursus "Tous" (× 3 cursus)
```

Cette valeur est fixée à 33 car le cursus "Tous" génère des niveaux pour 3 cursus (5ème, 4ème, 3ème).
- 33 mondes × 1 niveau × 3 cursus = 99 niveaux au total (≤ 100)

Si vous changez `MAX_TOTAL_LEVELS`, vous devrez peut-être ajuster cette valeur :
```javascript
const MAX_LEVELS_PER_INPUT_ALL = Math.floor(MAX_TOTAL_LEVELS / 3);
```

## Autres paramètres de configuration

### Nombre de sauvegardes par heure

Dans `api.php`, ligne 14 :
```php
define('MAX_REQUESTS_PER_HOUR', 10); // Nombre de sauvegardes autorisées par heure et par professeur
```

### Mot de passe professeur (mode local)

Dans `index.html`, ligne 1858 :
```javascript
const TEACHER_PASSWORD = 'prof123'; // Mot de passe pour accéder au mode professeur
```

### Nettoyage automatique des fichiers

Dans `api.php`, ligne 15 :
```php
define('CLEANUP_DAYS', 365); // Nombre de jours avant suppression automatique des fichiers inactifs (1 an)
```

**Comment ça fonctionne :**
- L'application supprime automatiquement les niveaux qui n'ont **pas été ouverts depuis plus d'un an**
- Le nettoyage s'effectue automatiquement **à chaque ouverture du mode professeur**
- Cela garantit que la liste des niveaux sauvegardés est toujours à jour
- Suppression silencieuse en arrière-plan (pas de message visible)

**Critères de suppression :**
- Un fichier est supprimé si `last_access` > 365 jours
- `last_access` est mis à jour quand :
  - Un professeur sauvegarde ses niveaux
  - Un professeur charge ses niveaux
  - Un élève accède aux niveaux (via l'URL publique)

**Pour changer la durée :**
```php
define('CLEANUP_DAYS', 730); // 2 ans au lieu d'1 an
```


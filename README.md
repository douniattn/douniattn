![Snake animation](https://raw.githubusercontent.com/douniattn/douniattn/output/github-contribution-grid-snake.svg)

## Barcelone à deux

Carnet de voyage en français du 12 au 16 novembre 2026. Site statique en HTML,
CSS et JavaScript, sans dépendance de compilation.

### Lancer localement

Depuis la racine du dépôt :

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Ouvrir <http://localhost:8000>. Le mode hors ligne nécessite localhost ou HTTPS,
et une première ouverture connectée. Le pied de page confirme la mise en mémoire.
Les polices distantes sont facultatives, avec des polices système en remplacement.
Les itinéraires Google Maps et les billetteries nécessitent une connexion.
Tous les liens cartographiques utilisent les URL officielles Google Maps,
avec un itinéraire piéton ou voiture selon le trajet.

### Contenu et confidentialité

`data.js` est la source commune du programme, des visites, des prix en centimes,
des lieux, de l’histoire, des sources et des phrases. Les prévisions sont celles
fournies pour la planification, consultées le 10 novembre 2026, pas un flux météo.
Les modifications météo, les étapes et les accès vérifiés
sont conservés uniquement dans le stockage local du navigateur.

Les horaires et numéros de vol sont visibles directement dans la journée du lundi,
dans la vue d’ensemble comme dans le détail du jour, sans rubrique à déplier,
avec l’accord explicite de l’utilisateur pour leur présence sur une version
publique. Ils ne sont pas inclus dans les métadonnées de partage.
Une rubrique repliée ne protège pas les données.

Les quatre vues partagent les mêmes données. Le fuseau est `Europe/Madrid`.
En dehors du séjour, l’accueil ouvre la vue d’ensemble. Pendant le séjour,
il ouvre le jour courant. Les étapes ne sont jamais validées automatiquement.
Le sélecteur permet de consulter n’importe quelle journée.

L’impression depuis le navigateur prépare la vue active sur papier et développe
ses rubriques pour inclure les anecdotes. Les rubriques retrouvent ensuite
leur état initial. Il n’y a pas de bouton d’impression dans le site.

Après une modification des fichiers, incrémenter le nom du cache dans `sw.js`
pour distribuer la nouvelle version aux appareils ayant déjà ouvert le carnet.

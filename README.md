# gwaleen-docs

### Commandes

| version minimum | émetteur | trame                     | description                                                                         |
| --------------- | -------- | ------------------------- | ----------------------------------------------------------------------------------- |
| initial         | tablette | `a#`                      | requête de ping a la règle                                                          |
| initial         | règle    | `%a:e#`                   | réponse du ping de la règle                                                         |
| initial         | tablette | `b#`                      | requête des information de la règle                                                 |
| initial         | règle    | `%b:[NAME],[VERSION],#`   | réponse du nom et de la version de la règle                                         |
| initial         | tablette | `&q#`                     | requête sur le pourcentage de batterie                                              |
| initial         | règle    | `%q:[PERCENT_OF_BATT],0#` | réponse du pourcentage de batterie                                                  |
| initial         | tablette | `&t#`                     | requête pour l'humidité et la température du boitier                                |
| initial         | règle    | `$t,[TEMP] °C,[HUM] %#`   | réponse pour l'humidité et la température du boitier                                |
| initial         | règle    | `%l,[VAL]#`               | prise de mesure de la règle en millimètre                                           |
| initial         | règle    | `%t:0#`                   | envoyé quand l'aimant est déposé sur la règle (avant prise de mesure)               |
| initial         | règle    | `%t:1#`                   | envoyé quand l'aimant est enlevé de la règle (après prise de mesure)                |
| v1.4.0          | tablette | `%cal:start#`             | Lancement de la procédure de calibration par le code                                |
| v1.4.0          | règle    | `%cal:put,[POS]#`         | La règle demande à poser le pointeur sur la position `[POS]` souvent `0` puis `375` |
| v1.4.0          | règle    | `%cal:remove#`            | La règle demande à enlever le pointeur de la position                               |
| v1.4.0          | règle    | `%cal:done#`              | La règle indique que la calibration est terminé                                     |

- *version minimum indique que les commandes ne sont pas disponible pour les règles avant cette version.*
- *Toutes les commandes sont optionnel*
- *Toutes les commandes sont des Strings.*
- *Les commandes envoyées par la règle ne contienne pas de retours a la ligne.

### Usage Bluetooth

1. Activer le bluetooth sur la règle
2. Connectez-vous à la règle en Serial
3. Enjoy!

### Usage Filaire

Pré-requis Windows: https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers

1. Branchez la règle au PC
2. Il devrait il y avoir un port en plus de rajouté dans les périphériques
3. connectez vous en Serial RS-232
4. Enjoy!

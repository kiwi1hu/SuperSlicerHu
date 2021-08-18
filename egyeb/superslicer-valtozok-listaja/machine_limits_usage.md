# machine\_limits\_usage

* Technológia : FDM & SLA
* Csoport : [Nyomtató beállítások](../../beallitasok/printer_settings.md)
* Alcsoport : [Limites de la machine](../../beallitasok/printer_settings.md#limites-de-la-machine)
* Mód : Haladó

## Comment appliquer les limites

### Leírás

Option qui permet de définir comment appliquer les limites de la machine.

Attention même si vous utilisez un profil d'impression qui définit une accélération de 5000, si pour votre machine la limite d'accélération est de 4000, le G-Code sorti utilisera la limite de 4000.

* Vous pouvez également l'utiliser comme sauvegarde et pour avoir une meilleure estimation du temps d'impression, option _**Utiliser pour l'estimation du temps**_.
* Option _**Émettre également les limites dans le G-Code**_. Les valeurs seront sauvegardées dans le G-Code, elles permettront une meilleure estimation du temps d'impression et seront écrites en début de fichier G-Code, avec M201, M202 M203, M204 et M205.
* Si vous voulez seulement sauvegarder les valeurs, choisissez l'option _**Utiliser aussi pour l'estimation du temps**_ et écrivez vous-même les limites dans la section G-Code personnalisé.
* L’option _**Utiliser uniquement pour sauvegarde**_ ne fera d’écrire les données dans les paramètres sauvegardés du G-Code.
  * Also emit limits to G-code
  * Use also for time estimate
  * Use only as safeguards
  * Disable

[Vissza a változók listájához](../../variable_list)


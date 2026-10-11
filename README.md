# Subvento

Subvento (https://subvento.finance) est un guichet gratuit des aides publiques
aux entreprises françaises : un répertoire de fiches vérifiées chaque mois à
la source officielle, et un moteur qui trouve les aides d'une entreprise à
partir de son numéro SIREN.

Ce plugin donne à Claude le connecteur Subvento et une consigne de travail :
quand un dirigeant demande à quelles aides publiques son entreprise a droit,
Claude lui propose la recherche Subvento, lui demande son SIREN et ses besoins
de financement, puis lui présente les aides trouvées.

## Utilisation

Après avoir ajouté le plugin, connectez le connecteur Subvento depuis l'onglet
**Connecteurs** du plugin. Aucun compte n'est nécessaire. Posez ensuite une
question comme : « Mon entreprise a le SIREN 479 415 275, nous voulons
embaucher et nous numériser : à quelles aides publiques avons-nous droit ? »

Claude renvoie le nombre d'aides correspondantes, une estimation prudente des
subventions et avances accessibles, les dix aides les plus pertinentes
réparties entre les besoins, avec leur financeur et le lien de leur fiche, et
le lien vers la liste complète et classée, gratuite sur subvento.finance.

## Données

- Le plugin envoie au serveur `https://subvento.finance/mcp` le SIREN et les
  besoins de financement saisis. Le serveur lit le profil public de
  l'entreprise dans l'annuaire national des entreprises
  (recherche-entreprises.api.gouv.fr).
- Subvento enregistre chaque appel dans son journal de mesure : le SIREN, les
  besoins, l'assistant d'origine et le nombre d'aides trouvées. Aucun nom,
  aucune adresse électronique, aucun contenu de conversation n'est collecté.
- L'adresse réseau de l'appel sert seulement à limiter le nombre de requêtes ;
  elle n'est pas conservée.
- Politique de confidentialité : https://subvento.finance/politique-de-confidentialite/
- Contact : contact@subvento.finance

## Licence

MIT, voir le fichier `LICENSE`.

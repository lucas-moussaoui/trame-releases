# Trame — Règles de confidentialité

*Dernière mise à jour : 31 août 2026*

Trame est une application de prise de notes personnelle. Aucune donnée n'est vendue,
louée ou partagée avec des tiers, et l'application n'affiche aucune publicité.

## Données collectées

- **Compte** : adresse e-mail et mot de passe (haché), pour l'authentification.
- **Contenu** : les notes, pages, événements et fichiers créés par l'utilisateur.

Ces données sont hébergées sur [Supabase](https://supabase.com) (Union européenne) et
répliquées localement sur les appareils pour le fonctionnement hors ligne. Chaque compte
est isolé au niveau de la base par des politiques de sécurité par ligne (RLS).

## Utilisation des données Google

Lorsque l'utilisateur relie son compte Google, Trame demande la seule autorisation
`https://www.googleapis.com/auth/drive.file`, volontairement la plus restreinte possible :

- Trame n'accède **qu'aux fichiers qu'elle a elle-même créés** dans Google Drive.
- Elle ne peut ni lire, ni lister, ni modifier les autres fichiers du Drive.
- Ces fichiers sont rangés dans un dossier `Trame`, visible et contrôlable par
  l'utilisateur depuis son Drive.

Ils servent uniquement à afficher les pièces jointes dans l'application. Ils ne sont ni
analysés, ni transmis à un tiers, ni utilisés pour entraîner un modèle.

L'utilisation des informations reçues des API Google par Trame respecte la
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
y compris ses exigences d'utilisation limitée (*Limited Use*).

## Fonctionnalités d'intelligence artificielle

Certaines fonctions envoient le contenu concerné à un fournisseur de modèle de langage
(Google Gemini par défaut), avec la clé API personnelle de l'utilisateur, et uniquement à
sa demande explicite.

## Conservation et suppression

- Les données sont conservées tant que le compte existe.
- La suppression du compte efface en cascade l'ensemble des données associées.
- L'accès Google peut être révoqué à tout moment depuis
  [myaccount.google.com/permissions](https://myaccount.google.com/permissions) ; les
  fichiers déjà présents dans le Drive restent la propriété de l'utilisateur.

## Contact

moussaouilucas@gmail.com

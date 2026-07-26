# Rôles et permissions

FeroceWork repose sur **4 rôles**. Chaque compte en possède exactement un, attribué par un administrateur. Le rôle détermine à la fois ce qui apparaît dans la navigation et ce que le serveur accepte réellement : contourner l'interface ne donne aucun accès supplémentaire.

## Les 4 rôles

| Rôle | Pour qui ? |
|---|---|
| **Utilisateur** | Toute personne de l'équipe qui a seulement besoin de gérer ses horaires et ses congés. |
| **Logistique** | Les opérateurs terrain : réception, scan, comptage, préparation de commandes. |
| **Manager** | Les responsables d'équipe : tout ce que fait la logistique, plus la supervision RH. |
| **Administrateur** | Les gestionnaires de l'application : tout, y compris les comptes et l'audit. |

## Matrice des permissions

| Fonctionnalité | Utilisateur | Logistique | Manager | Admin |
|---|:---:|:---:|:---:|:---:|
| Tableau de bord | ✅ | ✅ | ✅ | ✅ |
| Ses propres horaires et congés | ✅ | ✅ | ✅ | ✅ |
| Livraisons, arrivages, réceptions, recherche SSCC | ❌ | ✅ | ✅ | ✅ |
| Incomplets | ❌ | ✅ | ✅ | ✅ |
| Préparation de commandes | ❌ | ✅ | ✅ | ✅ |
| Solder une caisse d'arrivage | ❌ | ❌ | ✅ | ✅ |
| Valider un re-scan exceptionnel | ❌ | ❌ | ✅ | ✅ |
| Horaires de toute l'équipe | ❌ | ❌ | ✅ | ✅ |
| Valider les demandes de congé, gérer les absences | ❌ | ❌ | ✅ | ✅ |
| Reporter les heures supplémentaires | ❌ | ❌ | ✅ | ✅ |
| Base contractuelle hebdo des salariés | ❌ | ❌ | ❌ | ✅ |
| Gestion des utilisateurs et des rôles | ❌ | ❌ | ❌ | ✅ |
| Journal d'activité | ❌ | ❌ | ❌ | ✅ |

## Garde-fous

- Un administrateur **ne peut pas se rétrograder lui-même** ni désactiver son propre compte : impossible de se retirer accidentellement l'accès admin.
- Les vérifications de permissions sont faites **côté serveur** à chaque action, pas seulement dans l'affichage.
- Une page accédée sans le rôle requis redirige simplement vers le tableau de bord.

## Changer de rôle

Seul un administrateur peut modifier le rôle d'un compte, depuis la page de gestion des utilisateurs (voir [Administration](Administration)). Le changement prend effet immédiatement.

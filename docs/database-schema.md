# Schéma des données Supabase

Ce workflow attend des tables spécifiques dans Supabase. Voici la structure requise.

## Table `profil`
| Colonne | Type | Description |
|---|---|---|
| `business` | text | Nom / Identité (ex: Expert Tech) |
| `style` | text | Style de rédaction |
| `ton` | text | Ton global |
| `sujets` | text | Sujets principaux |
| `categories` | text | |
| `public_cible` | text | |

## Table `idees_posts`
| Colonne | Type | Description |
|---|---|---|
| `id` | int | Clé primaire |
| `sujet_detaille` | text | Le sujet que l'IA doit aborder |
| `statut` | text | `nouveau` ou `publie` |

## Table `historique_posts`
| Colonne | Type | Description |
|---|---|---|
| `contenu` | text | Le post généré |
| `action` | text | Toujours `post_now` |

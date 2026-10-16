# Architecture et Flux

Ce workflow s'exécute de manière séquentielle, déclenché automatiquement selon un intervalle de temps.

## Diagramme Détaillé

```mermaid
graph TD
    subgraph Déclencheur
        A[Schedule Trigger]
    end

    subgraph Récupération Contexte
        B[Supabase: Idée] --> C[Supabase: Profil]
        C --> D[Supabase: Historique]
    end

    subgraph Traitement IA
        D --> E[Code: Prompt Engineering]
        E --> F((API Gemini))
        F --> G[Code: Clean JSON]
    end

    subgraph Publication & Notification
        G --> H((Webhook Make))
        H --> I[Supabase: Archiver]
        I --> J[Supabase: Maj Statut]
        J --> K((Telegram))
    end

    A --> B

# Schéma de l'Architecture Cible

## 🔄 Workflow DevSecOps pour le Patch Management

```mermaid
graph TD
    A[Développeur] --> 1. Push Code| B[GitLab Repository]
    B -->|2. Déclenche Pipeline| C[GitLab CI/CD]
    C -->|3. Scan des Dépendances| D[Trivy]
    D -->|4. Détecte Vulnérabilités| E[Rapport]
    E -->|5. Affiche dans| F[GitLab Security Dashboard]
    E -->|6. Bloque si critique| G[Merge Request]
    G -->|7. Correction| A

# Description de l'Architecture Cible

## 🎯 Objectifs
- Intégrer la sécurité dès le développement (Shift Left).
- Automatiser la détection et la correction des vulnérabilités.
- Centraliser les rapports pour une visibilité globale.

## 🏗️ Workflow Détaillé
1. **Développement** : Le développeur push son code avec des dépendances (`package.json`, `requirements.txt`).
2. **Pipeline CI/CD** : GitLab déclenche automatiquement un pipeline à chaque push.
3. **Scan des dépendances** : **Trivy** scanne les fichiers pour détecter les vulnérabilités.
4. **Rapport** : Les résultats sont affichés dans le **Security Dashboard** de GitLab.
5. **Blocage** : Si une vulnérabilité **critique** est détectée, la Merge Request est bloquée.
6. **Correction** : Le développeur corrige les dépendances (ex: `npm update lodash`).
7. **Re-scan** : Le pipeline relance un scan après correction.
8. **Déploiement** : Si tout est OK, le code est déployé.

# Preuves de Concept (POC) - Patch Management

## 🎯 Objectif
Démontrer l'efficacité des outils de **patch management** (Trivy, npm audit) sur un **projet Node.js fictif**.

## 📁 Structure
## 🚀 Étapes Réalisées
1. **Création du projet pilote** :
   - Projet Node.js avec des dépendances vulnérables (`lodash@4.17.20`, `axios@1.6.1`).

2. **Scan initial** :
   - Exécution de `trivy fs` et `npm audit` via le pipeline GitLab → **3 vulnérabilités détectées**.

3. **Correction** :
   - Mise à jour de `lodash` et `axios` → **1 vulnérabilité restante** (`express`).

4. **Automatisation** :
   - Intégration de **Trivy dans un pipeline GitLab CI/CD**.

## 📊 Résultats
| Outil | Vulnérabilités Détectées | Temps d'Exécution | Facilité d'Intégration |
|-------|---------------------------|-------------------|-------------------------|
| Trivy | 3 | 12s | ⭐⭐⭐⭐ |
| npm audit | 3 | 5s | ⭐⭐⭐⭐⭐ |

## ✅ Conclusion
Ce POC montre que :
1. Les outils de **patch management** détectent efficacement les vulnérabilités.
2. L’**automatisation dans GitLab CI/CD** permet de bloquer les MR avec des dépendances non sécurisées.
3. **Trivy + npm audit** est une combinaison **gratuite et efficace** pour RapidSoft.

# Rapport de Scan - Projet Pilote Node.js

## 📅 Date du Scan
29/05/2026

## 🔍 Outils Utilisés
- **Trivy** (via le pipeline GitLab)
- **npm audit** (intégré à npm)

## 📊 Résultats
   Vulnérabilité | Sévérité | Package | Version Actuelle | Version Sécurisée | CVE | Status |
 |---------------|----------|---------|----------------------|------------------------|---------|------------|
 | Prototype Pollution | HIGH | lodash | 4.17.20 | 4.17.21 | [CVE-2023-29650](https://nvd.nist.gov/vuln/detail/CVE-2023-29650) | ✅ Corrigé |
 | Regular Expression DoS | MEDIUM | axios | 1.6.1 | 1.6.2 | [CVE-2023-45857](https://nvd.nist.gov/vuln/detail/CVE-2023-45857) | ✅ Corrigé |
 | Memory Leak | LOW | express | 4.18.1 | 4.18.2 | [CVE-2023-23607](https://nvd.nist.gov/vuln/detail/CVE-2023-23607) | ⚠️ À corriger |

## 📈 Statistiques
- **Total des vulnérabilités** : 3
- **Critiques** : 0
- **Hautes** : 1
- **Moyennes** : 1
- **Faibles** : 1

## 🔧 Actions Réalisées
1. Mise à jour de `lodash` en version **4.17.21** :
   ```bash
   npm install lodash@4.17.21

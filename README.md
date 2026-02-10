# GLPI Helm Chart 🚀🔐

`#helm` `#kubernetes` `#glpi` `#devsecops` `#argocd`

Chart Helm pour déployer GLPI avec PVC, Service et Ingress. Le mot de passe DB est géré via un `Secret` Kubernetes. ✅

## Contenu 📦
- Deployment
- Service
- PVC (optionnel)
- Ingress (optionnel)
- Secret DB

## Valeurs clés ⚙️
- `image.repository`, `image.tag`
- `service.type`, `service.port`
- `ingress.enabled`, `ingress.host`
- `persistence.enabled`, `persistence.storageClass`, `persistence.size`
- `glpi.dbHost`, `glpi.dbName`, `glpi.dbUser`, `glpi.dbPassword`

## Sécurité 🔒
- Le mot de passe DB est injecté depuis un `Secret` (`templates/secret.yaml`).
- Pour un vrai contexte DevSecOps, privilégie une gestion externe des secrets (ex: Sealed Secrets, External Secrets, Vault).

## Arborescence 📁
- `Chart.yaml`
- `values.yaml`
- `templates/`
  - `_helpers.tpl`
  - `deployment.yaml`
  - `service.yaml`
  - `pvc.yaml`
  - `ingress.yaml`
  - `secret.yaml`

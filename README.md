# Infrastructure AWS avec Terraform

Infrastructure cloud complète provisionnée avec Terraform et testée avec LocalStack.

## Architecture

- **VPC** — Réseau privé isolé (10.0.0.0/16)
- **Subnet public** — Zone accessible depuis internet
- **Internet Gateway** — Connexion vers internet
- **Security Group** — Contrôle du trafic (port 80)
- **EC2** — Serveur applicatif (Amazon Linux 2023)

## Technologies utilisées

- Terraform
- AWS (LocalStack)
- Docker

## Lancer le projet

```bash
# Démarrer LocalStack
docker run --rm -it -p 4566:4566 localstack/localstack

# Initialiser Terraform
tflocal init

# Créer l'infrastructure
tflocal apply

# Détruire l'infrastructure
tflocal destroy
```

## Auteur

[mounib-md](https://github.com/mounib-md)
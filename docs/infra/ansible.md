# Infrastructure — Ansible

Configuration et déploiement de l'environnement via Ansible.

## Structure

```
ansible/
├── inventory/hosts
└── roles/
    └── cece_env/
        ├── files/          # starship.toml, config fish…
        └── tasks/main.yml
```

## Lancer le playbook

```bash
cd ansible
ansible-playbook -i inventory/hosts roles/cece_env/tasks/main.yml
```

# linux-admin-lab

Laboratório de administração Linux: dois servidores (Debian e Rocky Linux) montados e operados como se fossem de produção. Projeto em andamento, com entrega prevista até 25/10/2026.

## Objetivo

Praticar e documentar o que um administrador de servidores Linux precisa dominar: configuração segura, usuários e permissões, disco, serviços, automação e backup com restore testado.

## Ambiente

| Servidor | Sistema | Recursos |
| --- | --- | --- |
| srv01 | Debian 13 | 2 GB de RAM, 20 GB de disco |
| srv02 | Rocky Linux 9 ou 10 | 2 GB de RAM, 20 GB de disco |

Virtualização: KVM/QEMU com virt-manager.

## Checklist do laboratório

| Etapa | Status |
| --- | --- |
| Base: hostname, fuso America/Sao_Paulo, IP estático e atualizações automáticas de segurança | A fazer |
| Usuários: grupos infra e suporte, sudo restrito e pasta compartilhada com setgid e ACL | A fazer |
| SSH: somente chave, root e senha desativados, fail2ban ativo | A fazer |
| Firewall: ufw no Debian e firewalld no Rocky | A fazer |
| Disco: LVM em segundo disco, montagem por UUID e extensão do volume com o servidor ligado | A fazer |
| Serviços: nginx com página de status e unit systemd própria | A fazer |
| healthcheck.sh: CPU, memória, disco, serviços com falha e uptime | A fazer |
| backup.sh: rsync via SSH com retenção de 7 diários e 4 semanais e restore testado | A fazer |
| usuarios.sh: cria e desativa usuários a partir de um CSV | A fazer |
| Agendamento com systemd timers | A fazer |
| Logs: journald persistente e logrotate | A fazer |
| Scripts sem avisos no shellcheck | A fazer |

## Estrutura planejada

Pastas: docs (arquitetura, troubleshooting e prints), scripts (healthcheck.sh, backup.sh e usuarios.sh), systemd (arquivos .service e .timer) e config (exemplos de sshd_config.d e sudoers.d).

## Aviso

Nenhum IP, hostname, senha ou dado real de empresa é publicado neste repositório.

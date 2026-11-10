# Comandos essenciais de Git

Referência rápida dos comandos praticados no curso, organizada por etapa do fluxo.

## 1. Ciclo de vida local

| Comando | O que faz |
|:--|:--|
| `git init` | Cria um repositório na pasta atual |
| `git status` | Mostra o estado dos arquivos (não rastreado, modificado, staged) |
| `git add <arquivo>` | Prepara a mudança para o próximo commit (`git add .` prepara tudo) |
| `git commit -m "feat: mensagem"` | Grava um snapshot com mensagem no padrão Conventional Commits |
| `git diff` | Mostra mudanças ainda não preparadas |
| `git diff --staged` | Mostra mudanças já preparadas para o commit |
| `git log --oneline --graph` | Mostra o histórico resumido, em formato de grafo |

Arquivos que não devem ser versionados (logs, pastas de editor) são listados no `.gitignore`.

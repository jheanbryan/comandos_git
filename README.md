# Comandos Git e Login no GitHub

## Comandos Básicos do Git

| **Comando**                                   | **Descrição**                                       |
|-----------------------------------------------|-----------------------------------------------------|
| `git init`                                    | Inicializa um repositório.                          |
| `git clone <URL-do-repositório>`             | Clona um repositório existente.                     |
| `git status`                                  | Verifica o status do repositório.                   |
| `git add <nome-do-arquivo>`                  | Adiciona arquivos ao índice (staging).              |
| `git add .`                                   | Adiciona todos os arquivos ao índice.               |
| `git commit -m "Mensagem do commit"`         | Faz um commit das alterações.                        |
| `git log`                                     | Exibe o histórico de commits.                       |
| `git checkout -- <nome-do-arquivo>`          | Reverte alterações em um arquivo.                   |
| `git branch <nome-da-branch>`                 | Cria uma nova branch.                               |
| `git checkout <nome-da-branch>`               | Muda para uma branch existente.                      |
| `git merge <nome-da-branch>`                  | Mescla uma branch na branch atual.                  |
| `git branch -d <nome-da-branch>`              | Deleta uma branch.                                  |
| `git push origin <nome-da-branch>`            | Envia alterações para o repositório remoto.         |
| `git pull origin <nome-da-branch>`            | Faz pull das alterações do repositório remoto.      |
| `git diff`                                    | Verifica as diferenças entre commits.                |
| `git revert <ID-do-commit>`                   | Reverte um commit específico.                        |
| `git reset --hard <ID-do-commit>`             | Resetar o repositório para um estado anterior.      |
| `git remote -v`                               | Verifica a configuração remota.                     |
| `git remote add origin <URL-do-repositório>`  | Adiciona um repositório remoto.                     |

## Comandos de Login e Gerenciamento de Credenciais

| **Comando**                                    | **Descrição**                                         |
|------------------------------------------------|-------------------------------------------------------|
| `git config --global user.name "Seu Nome"`     | Define seu nome de usuário para commits.              |
| `git config --global user.email "seu@email.com"` | Define seu e-mail para commits.                     |
| `git config --global --unset user.name` | Remove o name do usuário.                     |
| `git config --global --unset user.email` | Remove o email do usuário.                     |
| `git credential-cache exit`                     | Remove as credenciais armazenadas em cache.           |
| `git config --global credential.helper store`   | Armazena as credenciais em um arquivo de texto.       |
| `git config --global credential.helper cache`   | Armazena as credenciais em memória temporariamente.   |
| `ssh-keygen -t rsa -b 4096 -C "seu@email.com"` | Gera uma nova chave SSH.                              |
| `ssh-add ~/.ssh/id_rsa`                         | Adiciona a chave SSH ao agente de autenticação.       |
| `ssh -T git@github.com`                         | Testa a conexão SSH com o GitHub.                     |
| `git remote set-url origin <nova-URL>`         | Altera a URL do repositório remoto (se necessário).   |
| `git config --global --unset credential.helper` | Remove o helper de credenciais configurado.           |
| **Para Token de Acesso Pessoal:**              |                                                       |
| `gh auth login`                                 | Inicia o processo de login usando a CLI do GitHub.    |
| `gh auth logout`                                | Faz logout da CLI do GitHub.                          |
| **Para Configurar um Token de Acesso Pessoal:** |                                                     |
| Acesse **GitHub > Settings > Developer settings > Personal access tokens** | Crie e gerencie tokens de acesso.  |


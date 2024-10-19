# Comandos Git e Login no GitHub

## Comandos Básicos do Git

| **Comando**                                   | **Descrição**                                       |
|-----------------------------------------------|-----------------------------------------------------|
| `git init`                                    | Inicializa um repositório.                          |
| `git clone <URL-do-repositório>`             | Clona um repositório existente.                   
  |
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


# Commits Semânticos

## Estrutura de uma Mensagem de Commit Semântico

| **Parte**          | **Descrição**                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------|
| **Tipo**           | Descreve a natureza da mudança (ex: `feat`, `fix`, `docs`, etc.).                                            |
| **Escopo**         | Um substantivo que descreve uma seção do código afetada (opcional).                                           |
| **Descrição**      | Um resumo breve das mudanças feitas, escrita no modo imperativo.                                            |
| **Corpo**          | Explicações adicionais sobre a mudança, como a razão por trás dela (opcional).                               |
| **Rodapé**         | Informações sobre mudanças importantes ou referências a issues (opcional).                                   |

## Tipos Comuns de Commits

| **Tipo**   | **Descrição**                                              |
|------------|-----------------------------------------------------------|
| `feat`     | Uma nova funcionalidade para o usuário.                   |
| `fix`      | Uma correção de bug para o usuário.                       |
| `docs`     | Alterações na documentação.                                |
| `style`    | Mudanças que não afetam o significado do código.          |
| `refactor` | Mudança de código que não corrige um bug nem adiciona uma funcionalidade. |
| `perf`     | Mudança de código que melhora o desempenho.               |
| `test`     | Adicionando testes que estavam faltando ou corrigindo testes existentes. |
| `chore`    | Alterações no processo de build ou ferramentas auxiliares. |

## Exemplos de Mensagens de Commit Semântico

| **Mensagem de Commit**                               | **Descrição**                                         |
|-----------------------------------------------------|-------------------------------------------------------|
| `feat(auth): add login functionality`               | Adiciona funcionalidade de login.                     |
| `fix(ui): resolve popup not opening`                | Corrige um problema com o popup que não abria.       |
| `docs(README): update installation instructions`    | Atualiza as instruções de instalação.                 |
| `refactor(api): restructure user service`           | Reestrutura o serviço de usuário para melhor legibilidade. |
| `perf(performance): optimize image loading speed`   | Otimiza a velocidade de carregamento de imagens.      |

# Criar Token no GitHub (classico)

1. Acesse o GitHub e faça login na sua conta.
2. No canto superior direito, clique na sua foto de perfil e selecione "Settings" (Configurações).
3. No menu lateral esquerdo, clique em "Developer settings" (Configurações de desenvolvedor).
4. Em seguida, clique em "Personal access tokens" (Tokens de acesso pessoal) e depois em "Tokens (classic)".
5. Clique no botão "Generate new token (classic)" (Gerar novo token clássico).
6. Dê um nome para o token, por exemplo, "Disciplina de Web Design".
7. Selecione as permissões necessárias para o token clássico, como "repo" para acesso a repositórios, "read:org" para ler informações da organização, etc.
8. Após selecionar as permissões, clique no botão "Generate token" (Gerar token).
9. O token clássico gerado será exibido na tela. Copie o token e guarde-o em um local seguro, pois ele não será mostrado novamente.
10. Use o token clássico para autenticar suas operações no GitHub, como clonar repositórios e fazer push. Lembre-se de usar o token como senha ao autenticar via HTTPS.

# Clonar um repositório usando o token clássico

1. Abra o terminal ou prompt de comando.
2. Navegue até a pasta onde deseja clonar o repositório.
3. Use o comando `git clone` seguido da URL do repositório, substituindo `USERNAME` pelo seu nome de usuário e `TOKEN` pelo token clássico que você gerou. O comando deve ser semelhante a este: `git clone https://USERNAME:TOKEN@github.com/USERNAME/REPO.git nome-da-pasta`.
4. Pressione Enter e o repositório será clonado para a pasta especificada.

> [!NOTE]
> `nome-da-pasta` é o nome da pasta onde o repositório será clonado. Você pode escolher qualquer nome para essa pasta ou omitir essa parte para clonar em uma pasta com o mesmo nome do repositório.

> [!NOTE]
> No windows para abrir o terminal já na pasta correta, abra o explorador de arquivos, navegue até a pasta onde deseja clonar o repositório, clique na barra de endereço, digite `cmd` e pressione Enter. O terminal será aberto na pasta atual.

> [!NOTE]
> Nos sistemas operacionais baseados em Unix (Linux e macOS), abra o terminal e use o comando `cd` para navegar até a pasta onde deseja clonar o repositório. Por exemplo: `cd /caminho/para/pasta`.
> Na maioria dos casos, é possível abrir o terminal diretamente na pasta desejada clicando com o botão direito do mouse na pasta e selecionando a opção "Open Terminal Here" (Abrir terminal aqui) ou similar, dependendo do sistema operacional e do gerenciador de arquivos utilizado.

# Abrir um projeto no Visual Studio Code com configurações separadas

1. Abra o terminal ou prompt de comando na pasta superior do projeto.
2. Use o comando `code --user-data-dir=data-vscode --extensions-dir=data-vscode/extensions nome-da-pasta` para abrir o Visual Studio Code com configurações separadas para o projeto. Substitua `nome-da-pasta` pelo nome da pasta do projeto que você deseja abrir.
3. O Visual Studio Code será aberto com as configurações e extensões específicas para o projeto, permitindo que você trabalhe de forma isolada sem afetar as configurações globais do editor.

> [!NOTE]
> O comando `code` é utilizado para abrir o Visual Studio Code a partir do terminal. Certifique-se de que o Visual Studio Code esteja instalado e que o comando `code` esteja disponível no seu PATH para que o comando funcione corretamente. Se o comando `code` não estiver funcionando, você pode precisar adicionar o Visual Studio Code ao PATH ou usar o caminho completo para o executável do Visual Studio Code.

# Git - Configurações globais

1. Abra o terminal ou prompt de comando.
2. Use o comando `git config --global user.name "Seu Nome"` para configurar seu nome de usuário global para o Git. Substitua "Seu Nome" pelo seu nome real ou nome de usuário que deseja usar para suas contribuições no GitHub.
3. Use o comando `git config --global user.email "seu@email.com"` para configurar seu email global para o Git. Substitua "seu@email.com" pelo seu email real que deseja usar para suas contribuições no GitHub.

> [!NOTE]
> As configurações globais do Git são aplicadas a todos os repositórios no seu sistema. Se você quiser configurar um nome de usuário ou email diferente para um repositório específico, você pode usar os mesmos comandos sem a opção `--global` dentro do diretório do repositório para configurar as informações localmente para aquele repositório específico.

# Git - Configurações locais

1. Navegue até o diretório do repositório onde deseja configurar as informações locais usando o terminal ou prompt de comando.
2. Use o comando `git config user.name "Seu Nome"` para configurar seu nome de usuário local para o Git. Substitua "Seu Nome" pelo nome que deseja usar para suas contribuições nesse repositório específico.
3. Use o comando `git config user.email "seu@email.com"` para configurar seu email local para o Git. Substitua "seu@email.com" pelo seu email real que deseja usar para suas contribuições nesse repositório específico.

> [!NOTE]
> As configurações locais do Git são aplicadas apenas ao repositório onde foram configuradas. Elas sobrescrevem as configurações globais para aquele repositório específico, permitindo que você use informações diferentes para diferentes projetos, se necessário.

# Git - Add, commit e push

1. Após fazer alterações nos arquivos do seu projeto, use o comando `git add .` para adicionar todas as alterações ao stage do Git. Você também pode usar `git add nome-do-arquivo` para adicionar apenas um arquivo específico.
2. Use o comando `git commit -m "Mensagem do commit"` para criar um commit com as alterações adicionadas. Substitua "Mensagem do commit" por uma descrição clara e concisa das alterações que você fez.
3. Use o comando `git push`

```bash
git add .
git commit -m "Mensagem do commit"
git push
```

# Git - Pull

1. Para atualizar seu repositório local com as últimas alterações do repositório remoto, use o comando `git pull`. Isso irá buscar as alterações do repositório remoto e mesclá-las com seu repositório local.

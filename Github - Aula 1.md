# Aula 1 - Básico do Git/GitHub

## o que é git e github?

É fundamental entender que **Git** e **GitHub** são ferramentas distintas que trabalham em conjunto. O **Git** é um **sistema de controle de versão distribuído**. Sua principal função é rastrear e gerenciar as mudanças nos arquivos de um projeto ao longo do tempo, permitindo manter um histórico, voltar a versões anteriores e facilitar o trabalho colaborativo. O Git funciona localmente no seu computador, armazenando informações em uma pasta oculta `.git` dentro do seu projeto.

O **GitHub**, por sua vez, é uma **plataforma online** para **hospedar repositórios Git**. Ele funciona como uma "rede social para desenvolvedores", facilitando o armazenamento, compartilhamento e colaboração em projetos de código.


1. **Criar uma conta no GitHub:**
    
    - O primeiro passo para usar o GitHub é criar uma conta na plataforma.
    - Acesse o site `https://github.com/`.
    - Clique na opção "Sign Up" (ou "Cadastrar-se") no canto superior direito.
    - Preencha seu e-mail e clique em "Continue".
    - Defina uma senha para sua conta e clique em "Continue".
    - Escolha um nome de usuário (que será seu "nick") e clique em "Continue".
    - Responda se deseja receber notificações e resolva o enigma para verificar.
    - Clique em "Create account".
    - Um código de verificação será enviado para o e-mail informado, que você precisará digitar para confirmar a conta.
2. **Criar um Repositório Remoto no GitHub:**
    
    - Após criar sua conta, você pode criar um repositório no GitHub para hospedar seu projeto.
    - Volte para a tela inicial do GitHub e selecione a opção "Create repository" (ou "Criar repositório").
    - Defina um **nome para o seu repositório**. É comum usar o mesmo nome da pasta do seu projeto local.
    - Especifique se o repositório será **público** (visível para qualquer pessoa) ou **privado** (acessível apenas para pessoas autorizadas). Escolha a opção que preferir.
    - Clique no botão "Create repository".
    - Ao criar o repositório, o GitHub exibirá comandos que você pode usar para conectar um repositório local existente a este repositório remoto.
3. **Instalar o Git Localmente:**
    
    - Para usar o Git na sua máquina, você precisa instalá-lo.
    - Acesse o site oficial do Git (mencionado como git-scm.com nos materiais) e faça o download da versão para o seu sistema operacional.
    - Execute o instalador. As opções padrão (`Next`, `Next`) geralmente funcionam.
    - Você pode usar o "Git Bash" (um terminal para comandos Git no Windows) ou o terminal integrado do seu editor de código.
    - Para verificar se a instalação foi bem-sucedida, abra o terminal e digite `git --version`. Ele deve mostrar a versão instalada.
	  
	Também é necessário configurar no git bash as seguintes coisas:
    
	 - `$ git config --global user.name "[nome]"`: Configura o **nome** que você deseja que seja ligado às suas transações de commit.
	- `$ git config --global user.email "[endereco-de-email]"`: Configura o **e-mail** que você deseja que seja ligado às suas transações de commit.
    
    
    
4. **Criar um Diretório de Projeto Local e Inicializar um Repositório Git:**
    
    - Crie uma pasta no seu computador para o seu projeto (por exemplo, na área de trabalho).
    - Abra o terminal (Git Bash ou terminal integrado) dentro dessa pasta.
    - Para transformar essa pasta em um repositório Git local, digite o comando `git init`.
    - Este comando inicializa um **repositório Git vazio** e cria uma pasta oculta `.git` onde o Git armazenará todas as configurações e o histórico de versionamento.
    - Após `git init`, você verá que o terminal indica que você está na branch `master` ou `main` (a branch principal padrão). A nomenclatura padrão tem mudado de `master` para `main`.
5. **Adicionar Arquivos e Fazer o Primeiro Commit (Localmente):**
    
    - Crie ou adicione arquivos ao seu diretório de projeto. Por exemplo, crie um arquivo `README.md`. O `.md` indica que é um arquivo Markdown, comum para descrições de projeto.
    - Use o comando `git status` para ver o estado atual dos seus arquivos – quais foram modificados ou criados e ainda não foram adicionados ao versionamento.
    - Use o comando `git add [arquivo]` para adicionar um arquivo específico à **área de "staging"**. A área de staging é onde você prepara as mudanças que quer incluir no próximo "commit".
    - Alternativamente, `git add .` adiciona todas as mudanças na pasta atual (arquivos criados, modificados, etc.) à área de staging.
    - Use `git status` novamente para ver que os arquivos na área de staging aparecem em verde.
    - Use o comando `git commit -m "[mensagem descritiva]"` para gravar permanentemente as mudanças que estão na área de staging no histórico do projeto. O `-m` permite adicionar uma mensagem que descreve as mudanças feitas neste commit. O commit é um "snapshot", uma versão específica do seu projeto naquele momento.
6. **Conectar o Repositório Local ao Repositório Remoto (GitHub):**
    
    - Para enviar seus commits locais para o GitHub, você precisa vincular os dois repositórios.
    - No seu terminal local, use o comando `git remote add origin [link_do_repositório_github]`.
    - `remote` refere-se ao repositório remoto.
    - `add` é para adicionar um novo remote.
    - `origin` é um nome ("apelido") comum dado ao repositório remoto principal, mas você pode escolher outro nome.
    - `[link_do_repositório_github]` é o URL do repositório que você criou no GitHub. O GitHub exibe este link na página do repositório.
7. **Enviar os Commits Locais para o GitHub (`git push`):**
    
    - Com os repositórios conectados, você pode enviar seus commits locais para o GitHub usando o comando `git push`.
    - Use `git push origin main` (ou `master`, dependendo da sua branch principal).
    - `origin` é o apelido do repositório remoto para onde você está enviando.
    - `main` (ou `master`) é a branch local que você está enviando para a branch correspondente no remoto.
    - Na primeira vez que você executa `git push`, o Git pode solicitar seu nome de usuário e o token de acesso pessoal para autenticação. Digite seu usuário, pressione Enter, e depois copie e cole o token (ele não aparecerá no terminal) e pressione Enter novamente.
    - Após o push, suas alterações (os commits) estarão disponíveis no repositório do GitHub. Você pode verificar atualizando a página do repositório no navegador. Para pushes futuros, o comando `git push` simplificado pode ser suficiente.

[[github-git-cheat-sheet.pdf]][[github-git-cheat-sheet.pdf]]
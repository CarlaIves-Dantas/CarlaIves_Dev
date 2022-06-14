# 1. Navegação Básica no Terminal :desktop_computer: 

##### GUI(Interface gráfica) x CLI(Comandos por linhas)

######  1. 1 *Sistema Windows                                                         Sistema Linux*

Criar pastas/arquivos: **mkdir**                                       **mkdir**
Mudar de pastas: **cd**                                                      **cd**
Listar as pastas: **dir**                                                        **ls**
Deletar arquivos: **del**                                                     **rm** 
Deletar pasta: **rmdir nome do diretório /s /q**         **rf**

## 2. Criar Perfil no GitHub

https://github.com

## 3. Criar Chave SSH

https://github.com/settings/keys

##### 3.1 Clicar no ícone :computer_mouse: 

#####  <u>Nova Chave SSH</u>

##### 3.2 Retorna ao GIT BASH e executa os comandos listados a baixo:

ssh-keygen -t ed25519 -C emailcadastrado@noperfildogithub (enter)

*Digita uma senha aleatória 2x*

cd/c/users/nome/.ssh/  (comando para acessar a pasta oculta .ssh)

*digita: ls (para listar as chaves)*

cat id_ed25519.pub (Essa chave pública que sempre será exposta lá no GitHub) 
cópia o código e insere no site da GitHub no campo armazenamento da chave.

##### 3.3 Gerar o agent pid

$eval $(ssh-agent -s)
agent pid 0x0x

##### 3.4 Adicionar o agent pind:

ssh-add id-ed25519 (enter)
insere a mesma senha criada para chave ssh
Identidade Adicionada

## 4. Primeiros Comandos no Git

### 4.1 Iniciar Git 

​       git init

##### 4.1.1 Criando o primeiro repositório

Acessar a pasta do diretório C / com o botão direito acessar Git Here/ com o Git Bash aberto no diretorio C / Criar a Parta de Trabalho Workspace

Digite o comando: **mkdir** Workspace (enter)
acessar a pasta: **cd** workspace
Criar a pasta: **mkdir** Nome do repositório (enter)
Acessar pasta: **cd** Nome do repositório (apertar TAB para preencher o nome mais rápido)
Inicializar o Git dentro da Pasta para que possa ser versionada: **git init**
Para visualizar a pasta oculta de gerenciamento do git: **ls -a**

**cd ..** (retorna a pasta repositório)

##### 4.1.2 Criando o autor dos commits

verificando identidade configurada para assinatura dos commits:

git config --list (aparece todas as configurações listadas, atentar para user.email e user.name)

Caso sejam diferentes do email e usuário do GitHub, deletar esses dados e configurar com os dados do Github conforme comandos:

git config --global --unset user.email "email@registrado.com"

git config --global --unset user name "nome registrado"

Se você der git config --list você irá observar que esses dois dados foram apagados das configurações.

Para inserir os dados corretos:

git config --global user.email "email@email.com"
git config --global user.name "nome"



### 4.2 Iniciar o versionamento

​       git add

##### 4.2.1 Adicionar um arquivo

git add* (enter)

git commit -m "commit inicial" (enter)

##### 4.2.2 Verificando o status do arquivo

git status (enter)

Nesse ponto criamos nova pasta e movemos o arquivo criado, gerando nova atualização no Stage. Onde devemos enviar as atualizações para o stage através do git add (nome do arquivo) (nome da pasta criada) (enter)

##### 4.2.3 Retornar os arquivos para Untracked 

git restore --stage



### 4.3 Criar um Commit

​       git commit

##### 4.3.1 Criar um commit

git commit -m "cria pasta Livro-de-anotacoes, move arquivo para Livro-de-anotacoes"

Caso exista alterações no arquivo Anotacoes.md usar o código git add * (salva todas as alterações realizadas nos arquivos)

##### 4.3.1 Adicionar novo arquivo

echo > README.md








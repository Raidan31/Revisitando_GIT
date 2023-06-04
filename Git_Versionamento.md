# 1. O que é GIT?

## GIT é sistema de versionamento de código, que guarda os registros de versão como snapshots(fotos) do estado do projeto, além da referência/caminho pra essa foto.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 2. GIT e suas operações locais:

## As maiorias das operações feitas pelo GIT são locais e por isso boa parte das operações são praticamente instantâneas devido à facilidade de acessar arquivos em seu próprio computador.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 3. GIT vs GIT Hub

## GIT Hub é a plataforma utilizada para armazenar os repositórios e o GIT é um sistema de controle de versão distribuído amplamente utilizado para o rastreamento de alterações em arquivos e o gerenciamento de projetos de desenvolvimento de software. 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 4. Comandos Terminal GitBash

## **clear**: Limpa a tela

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **cd**: Altera o diretório de trabalho atual das sessões do terminal para o argumento de diretório passado

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git clone**: Basicamente, faz uma cópia idêntica da versão mais recente de um projeto em um repositório e a salva em seu computador.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git init**: Inicia um repositório git, assim uma ramificação inicial sem nenhum commit será criada

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **git branch**: Esse comando criará uma branch em seu local de trabalho. Para fazer o push (algo como enviar) da nova branch para o repositório remoto, você precisa usar o comando a seguir

    como ver as branchs?: git branch --list

    como excluir a branch?: git branch -d <nome-da-branch>
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **git diff**: Mostra exatamente as linhas que foram modificadas/acrescentadas

    git diff --staged: verifica os arquivos modificados que estão na área de STAGED.

    git diff origin/nome da branch: mostra quais alterações serão feitas ao buscar as atualizações com o git fetch
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git log**: Mostra o histórico dos commits feitos e os autores responsaveis pelo commit e as datas do commit.

    git log --origin --decorate: Ele indica onde o head está
    head = é a uma referência especial que representa a ponta atual de um ramo ou branch em um repositório Git. É um ponteiro para a última confirmação (commit) feita no ramo em que você está trabalhando.
    Ele também é usado para determinar o que será incluído em novos commits e quais alterações serão refletidas ao realizar operações como checkout, merge e rebase.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git restore nome do arquivo**: remove a modificação feita no arquivo não commitado (Uma vez executado não é possivel desfazer).

    git restore --staged: Remove o arquivo da Staging Area, mas deixa suas modificações reais intocadas, quando ocorre a desistência de passar para o commit superior.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git remote**: é utilizado para visualizar os repositórios remotos configurados em um repositório Git local. Ele exibe uma lista dos nomes dos repositórios remotos configurados e as URLs associadas a eles.

    git remote -v: exibe a lista dos repositórios remotos configurados, juntamente com as URLs associadas a eles. Isso pode ser útil para verificar as URLs dos repositórios remotos.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **git checkout nome da branch**: É usado para trocar de uma branch para outra. Também podemos usar o comando para fazer o checkout de arquivos e commits.
 
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

##  **git merge**: Quando você concluir o desenvolvimento em sua branch e quando tudo funcionar bem, a etapa final é fazer o merge (mesclar ou unir, em português) da branch com a branch pai (dev ou master/main, em geral). Isso é feito com o comando git merge.

## Git merge, basicamente, integra sua branch com o recurso e todos os seus commits na branch de desenvolvimento (dev) ou na branch principal (master ou main). É importante lembrar que, primeiro, você precisa estar na branch específica na qual você quer fazer o merge de sua branch com o recurso.

## Por exemplo, ao querer fazer o merge de sua branch do recurso na branch dev:

## Primeiro, troque para a branch dev:

    git checkout dev

## Antes do merge, atualize sua branch dev local:

    git fetch

## Por fim, faça o merge da sua branch do recurso em dev:

    git merge <nome-da-branch-com-o-recurso>

**Dica: certifique-se de que sua branch dev tem a versão mais recente antes de fazer o merge de suas branches de recurso. Do contrário, você pode ter que lidar com conflitos e outros problemas indesejados.**

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **git rebase**: Reaplica commits em cima de outro commit base.

    git rebase <branch>: Move os commits da branch atual para a ponta da <branch>.

    git rebase --continue: Continua o processo de rebase após resolver conflitos.

    git rebase --abort: Cancela o processo de rebase e retorna ao estado anterior.

## O comando "git rebase" é útil para reorganizar e integrar as alterações de uma branch em outra, permitindo uma história linear e mais limpa do projeto. No entanto, é importante usá-lo com cuidado, pois pode alterar o histórico de commits existente.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **tecla TAB**: Completar caso tenha uma pasta com as iniciais que tenha sido digitadas

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **MKDIR**: Cria Pastas

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **Echo**: Printa no terminal algo que tenha sido escrito

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **del**: Deleta apenas os arquivos presentes na pasta. Não deleta a pasta.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **RMDIR**: Deleta a pasta
ex: rmdir "nome da pasta" /s /q

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **sha1**: Serve pra encriptar a pasta, gerando uma string com 40 caracteres.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **ls**: Gera uma lista de programas aparentes na pasta.
    ls -a: Mostra as pastas ocultas(Git init)

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **git add nome do arquivo**: Adiciona um arquivo específico local (untracked) ou (modified) a fase STAGED. 


    * git add*: Adiciona todos os arquivos locais a fase STAGED.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git commit -m "mensagem explicando o que ocorreu"** : Pega todos os arquivos que estejam na fase STAGED e Commita, os envelopando em uma mensagem, é aconselhavel a fazer os commits de forma incremental a cada passo do projeto para deixar claro para o time de trabalho.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git status**: Informa os status dos arquivos(Untracked, Tracked, Unmodified, Modified e Staged).

* Untracked é o estado onde o arquivo ainda não foi 'rastreado'.

* Unmodified é o estado onde o arquivo não sofreu alterações em relação a sua referência.

* Modified é o estado onde o arquivo sofreu alterações em relação a sua referência.

* Staged é o estado onde o arquivo já foi endereçado e aguarda ser transferido ao repositório.

// O reposotório local será composto por commits.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git move**: Comando para mover o arquivo.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **giti config**: Permite visualizar e configurar as opções do Git.

    git config --list: Serve para verificar as configurações presentes no seu GitHub.

    git config --global --unset user.email //escrever o e-mail: Remove o e-mail registrado.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git push origin main**: Manda os arquivos adicionados no local para o github.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git pull**: é usado para obter as atualizações de um repositório remoto. Esse comando é uma combinação de git fetch e git merge, o que significa que, quando usamos git pull, ele recebe as atualizações do repositório remoto (git fetch) e aplica imediatamente as alterações mais recentes em seu espaço de trabalho local (git merge).

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **git fetch**: Pega todas as atualizações feitas no repositório remoto, porém não aplicam imediatamente no repositório local, é possivel verificar quais serão as atualizações utilizando o comando git diff origin/nome da branch, uma vez que concorde com as atualizações é possivel utilizar o git pull


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 5. Objetos do Git

a)Blobs

Os arquivos são guardados nos blob, é guardado a encriptação do arquivo, não é guardado os nomes do autor.

b) Tree

Armazena os blobs, as encriptações e os nomes dos arquivos. Dentro das trees é possivel armazenar outras trees. As trees
tem uma encriptação própria.

c) Commit

É aquilo que da significado as operações, engloba tudo, as Tree, outros commits, o nome do autor, a mensagem e a data e
hora registradas. Os commits tem seu próprio SHA1

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 6. Chaves SSH e Tokens

Chave SSH

Estabelece conexão entre duas partes.

Comandos para a criação de chaves: 

    ssh-keygen: Gera um novo par de chaves SSH (pública e privada).

    ssh-add: Adiciona uma chave privada ao agente de autenticação SSH.
    
    ssh-agent: Gerencia as chaves privadas e fornece autenticação SSH para conexões seguras.
    
    pbcopy (no macOS) / clip (no Windows): Copia a chave pública para a área de transferência.
    
    cat ~/.ssh/id_rsa.pub: Exibe o conteúdo da chave pública no terminal.
    
    ssh-keygen -t ed25519 -C email: Gera um novo par de chaves SSH (tipo ed25519) com um comentário de e-mail.
    
    eval $(ssh-agent -s): Inicia o agente SSH e configura as variáveis de ambiente.
    
    ssh-add id-ed25519: Adiciona a chave privada "id-ed25519" ao agente de autenticação SSH.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 7. Comandos para a Configuração do GitHub

    git config --global user.email // coloca o e-mail que vai ser registrado aqui
    git config --global user.name // coloca o nome aqui

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 8. Arquivo.gitignore 

O arquivo .gitignore é um arquivo de configuração utilizado no Git para especificar quais arquivos e diretórios devem ser ignorados e não rastreados pelo sistema de controle de versão.

Quando você adiciona um arquivo ou diretório ao .gitignore, o Git irá ignorá-los, o que significa que eles não serão incluídos nas operações de commit, merge ou push. Isso é útil para evitar que arquivos desnecessários sejam adicionados ao repositório, como arquivos temporários, arquivos de configuração local ou arquivos gerados automaticamente.

    Sintaxe: Cada linha no arquivo .gitignore representa um padrão de arquivo ou diretório a ser ignorado. Você pode usar curingas (wildcards) e padrões específicos para definir quais arquivos ou diretórios devem ser excluídos. Por exemplo, *.txt irá ignorar todos os arquivos com a extensão .txt.

    Localização: O arquivo .gitignore é geralmente colocado na raiz do repositório Git. Ele será aplicado a todos os diretórios e subdiretórios abaixo dessa localização, a menos que outro arquivo .gitignore seja encontrado em um diretório específico.

    Comentários: Você pode adicionar comentários em linhas começando com # para documentar o propósito ou explicação de um padrão de exclusão.

    Regras de negação: É possível negar um padrão usando o prefixo !. Isso permite incluir arquivos específicos que correspondam a um padrão de exclusão mais amplo.

    Gitignore global: Além do .gitignore local, você também pode ter um arquivo .gitignore global que se aplica a todos os repositórios em sua máquina. Ele é geralmente localizado em ~/.gitignore_global ou ~/.config/git/ignore.

**É importante observar que o .gitignore não tem efeito retroativo.** Isso significa que se um arquivo já tiver sido rastreado pelo Git antes de ser adicionado ao .gitignore, ele continuará sendo rastreado, mesmo que seja posteriormente adicionado ao .gitignore. Nesse caso, você precisa remover explicitamente o arquivo do repositório usando o comando git rm --cached <arquivo> para parar de rastreá-lo.

O arquivo .gitignore é uma ferramenta poderosa para controlar quais arquivos são incluídos ou excluídos do repositório Git. É altamente recomendável utilizá-lo para evitar a inclusão de arquivos desnecessários ou sensíveis no histórico de commits.


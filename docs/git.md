# Estudos sobre o Git

## Introdução

No mundo do versionamento de projetos, duas ferramentas se destacam como indispensáveis: Git e Github. E não, ambos não são a mesma
coisa, mas andam de mãos bem dadas.

## O que é Git?

Em poucas palavras, Git se trata de um software gerenciador de versões de projetos (Version Control System). E quando me refiro a
projetos não precisa ser necessariamente os códigos de algum software, podem ser também livros, projetos de TCC etc.

## Quando usar Git?

Usamos o Git sempre que sentirmos a necessidade de não perder tudo que desenvolvemos até determinado ponto, e assim a cada etapa em que adicionamos algo novo ao nosso projeto o dividimos em versões. O Git irá garantir que não iremos perder o que fizemos em versões anteriores. De maneira rápida, organizada, já que não precisaremos criar diversas pastas para salvar as versões antigas.

## E onde entra o Github?

O Github seria a plataforma onde hospedariamos os nossos repositórios com projetos versionados com o Git. Com a ajuda do Git, podemos hospedar nosso projeto atualizado com poucos comandos, de maneira centralizada e também permitir que o mesmo seja compartilhado a outras pessoas. E é aqui que está a base do mundo open source e projetos colaborativos, que irei aprofundar posteriormente.

# Começando a versionar o projeto com o Git

## Passo 1 - git init

Primeiramente na pasta do projeto, devemos usar o comando **git init**. Isso fará com que o Git instale uma pasta .git e deixa sinalizado
que todos os arquivos que estiverem dentro da pasta poderão ser versionados.

## Passo 2 - controlar o acesso

### **Níveis do sistema**

A configuração será para todo mundo do computador: --system

A configuração será a mesma para todos os projetos do Git, para X usuário: --global

Apenas este projeto: --local

### Comandos

    git config --global user.name -> define o nome de usuário, que será o mesmo para outros projetos.

    git config --global user.email -> define o email.

    git config --global -l -> lista as configuração padrão, mais as que foram adicionadas.

    git config --global core.editor visualstudiocode  -> define um editor de texto que o Git irá abrir caso seja necessário.

# Entendendo o Git Workflow

Para que nosso arquivo seja versionado pelo Git, é necessário que passe por determinadas fases.

A primeira delas é quando damos o comando git init em uma pasta. Neste momento, como dito acima, você dará ao git a permissão de gerenciar todos os arquivos nela.
Os arquivos nesta pasta entrarão então em um estado chamado de **Untracked**, que significa não rastreado. Ou seja, ainda não estaremos salvando o histórico destes arquivos.

Próxima etapa portanto, é dizer ao git que queremos rastrear as alterações feitas no arquivo. O comando git add irá fazer este trabalho, que após usarmos faremos com que o arquivo entre na área de **Stage** (o arquivo está no estado staged).

Por último, faremos com que o Git grave os históricos deste arquivo no estado de staged. Guardando o arquivo da mesma maneira que foi passado ao stage. E quando quisermos acessar alguma versão passada, utilizamos o comando ... + a hashcode dada pelo git.

### Termos importantes

Commit - quando salvamos um espelho do arquivo.

Modified - arquivo que sofreu alterações e que já está sendo rastreado, mas ainda não foi salvo pelo commit.

Tracked - arquivo quando está no estado de rastreável.

### Comandos

git status -> para visualizar em que estágio está o projeto.

git add nomedoarquivo.tipo ou git add . -> adiciona um arquivo ou vários na stage.

git commit -m 'mensagem do que alteramos' ou git commit -am 'mensagem'(para arquivos já rastreados) -> aqui é quando salvamos uma versão do arquivo.  Ou com o -am já mandamos a alteração para o stage e fazemos um commit.

**DICA! Não faça commits para cada nova linha do arquivo, apenas quando fizer um conjunto de alterações que faça sentido entre si.**

git log -> visualizar as versões, bem como quem criou, data e mensagem aviso. Para sair do prompt do git log, digite **q**.

E como faço para visualizar o estado do projeto no momento de determinado commit?
Basta que digite o comando: **git checkout + código copiado da versão do commit desejado**, visto no git log.

Para que vejamos as outras versões do projeto, primeiro precisamos retornar ao estado atual dele.
Com o comando: **git checkout master**. E então repetir os passos anteriores para visualizar outras versões.

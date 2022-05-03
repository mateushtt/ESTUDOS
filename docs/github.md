# Aprendendo a mexer no GitHub

# Sincronizando projeto com o comando clone

O foco aqui é utilizar as plataformas Git no nosso computador e o GitHub de maneira integrada. Assim a melhor maneira é clonar o repositório criado no GitHub, assim sempre que fizemos um commit no projeto em nosso computador, ele será carregado e atualizado no repositório do GitHub.

### Passos

1 - Clique em **Code** dentro do repositório desejado.

2 - Copie o caminho do projeto.

3 - No terminal do VSCode digite **git clone** + o caminho.

4 - Em seguida envie o/os arquivos alterados para o estado de stage. Com o comando **git add + nomearquivo.tipo**.

    Importante: como clonamos um projeto do GitHub, automaticamente ele cria o arquivo **.git** (do comando git init)
    na pasta do repositório.

5 - Em seguida faça o commit.

6 - E então para enviar o arquivo alterado, ou novo, rode o comando **git push**.

    Importante: caso de errado de permissão, informe os dados de username e email.

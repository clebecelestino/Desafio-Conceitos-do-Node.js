<h1 align="center">
    <img alt="GoStack" src="https://rocketseat-cdn.s3-sa-east-1.amazonaws.com/bootcamp-header.png" width="200px" />
</h1>

<h3 align="center">
  Desafio 2: Conceitos do NodeJS
</h3>

<p align="center">�Sua �nica limita��o � voc� mesmo�!</blockquote>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
   <a href="#memo-licen�a">Licen�a</a>
</p>

## :rocket: Sobre o desafio

Nesse desafio, voc� deve criar uma aplica��o para treinar o que voc� aprendeu at� agora no Node.js!
Essa ser� uma aplica��o para armazenar reposit�rios do seu portf�lio, que ir� permitir a cria��o, listagem, atualiza��o e remo��o dos reposit�rios, e al�m disso permitir que os reposit�rios possam receber "likes".

### Rotas

- **`POST /repositories`**: A rota deve receber `title`, `url` e `techs` dentro do corpo da requisi��o, sendo a URL o link para o github desse reposit�rio. Ao cadastrar um novo projeto, ele deve ser armazenado dentro de um objeto no seguinte formato: `{ id: "uuid", title: 'Desafio Node.js', techs: ["Node.js", "..."], likes: 0 }`; Certifique-se que o ID seja um UUID, e de sempre iniciar os likes como 0.

- **`GET /repositories`**: Rota que lista todos os reposit�rios;

- **`PUT /repositories/:id`**: A rota deve alterar apenas o `t�tulo`, a `url` e as `techs` do reposit�rio que possua o `id` igual ao `id` presente nos par�metros da rota;

- **`DELETE /repositories/:id`**: A rota deve deletar o reposit�rio com o `id` presente nos par�metros da rota;

- **`POST /repositories/:id/like`**: A rota deve aumentar o n�mero de likes do reposit�rio espec�fico escolhido atrav�s do `id` presente nos par�metros da rota, a cada chamada dessa rota, o n�mero de likes deve ser aumentado em 1;

### Espec�fica��o dos testes

Em cada teste, tem uma breve descri��o no que sua aplica��o deve cumprir para que o teste passe.

Para esse desafio temos os seguintes testes:

- **`should be able to create a new repository`**: Para que esse teste passe, sua aplica��o deve permitir que um reposit�rio seja criado, e retorne um json com o projeto criado.

- **`should be able to list the repositories`**: Para que esse teste passe, sua aplica��o deve permitir que seja retornado um array com todos os reposit�rios que foram criados at� o momento.

- **`should be able to update repository`**: Para que esse teste passe, sua aplica��o deve permitir que sejam alterados apenas os campos `url`, `title` e `techs`.

- **`should not be able to update a repository that does not exist`**: Para que esse teste passe, voc� deve validar na sua rota de update se o id do reposit�rio enviado pela url existe ou n�o. Caso n�o exista, retornar um erro com status `400`.

- **`should not be able to update repository likes manually`**: Para que esse teste passe, voc� n�o deve permitir que sua rota de update altere diretamente os likes desse reposit�rio, mantendo o mesmo n�mero de likes que o reposit�rio j� possuia antes da atualiza��o. Isso porque o �nico lugar que deve atualizar essa informa��o � a rota de respons�vel por aumentar o n�mero de likes.

- **`should be able to delete the repository`**: Para que esse teste passe, voc� deve perimtir que a sua rota de delete excluia um projeto, e ao fazer a exclus�o, ele retorne uma resposta vazia, com status `204`.

- **`should not be able to delete a repository that does not exist`**: Para que esse teste passe, voc� deve validar na sua rota de delete se o id do reposit�rio enviado pela url existe ou n�o. Caso n�o exista, retornar um erro com status `400`.

- **`should be able to give a like to the repository`**: Para que esse teste passe, sua aplica��o deve permitir que um reposit�rio com o id informado possa receber likes. O valor de likes deve ser incrementado em 1 a cada requisi��o.

- **`should not be able to like a repository that does not exist`**: Para que esse teste passe, voc� deve validar na sua rota de like se o id do reposit�rio enviado pela url existe ou n�o. Caso n�o exista, retornar um erro com status `400`.

## :memo: Licen�a

Esse projeto est� sob a licen�a MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

---

Feito com ?? by Jaime Barbosa :wave: [Linkedin](https://www.linkedin.com/in/jaimebs/)
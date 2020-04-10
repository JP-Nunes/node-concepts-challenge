<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Challenge: Node.js concepts
</h3>

<p align="center">
  <a href="#rocket-sobre-o-desafio">About the challenge</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</p>

## :rocket: About the challenge

At this challenge, the goal is to create an application to practice the knowledge on Node.js I got from the bootcamp so far!

This app should be able to register repositories, and allow to create, list, update and remove the repositories, besides that it allows the repositories to receive "likes".


### Rotas da aplicação

- **`POST /repositories`**: The route should receive `title`, `url` and `techs` inside request body. The new project should be registered inside an object: `{ id: "uuid", title: 'Node.js challenge', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }`; Make sure that the ID is a UUID, and likes allways start as 0.

- **`GET /repositories`**: list all repositories;

- **`PUT /repositories/:id`**: The route should only update fields `title`, `url` and `techs` from the repository with the `id` given by the route params;

- **`DELETE /repositories/:id`**: The route should delete the repository with the `id` given by the route params;

- **`POST /repositories/:id/like`**: The route should raise the number of likes of a repository by 1;

### Específicação dos testes

Tests to be approved:

- **`should be able to create a new repository`**: To be approved, your app should allow the creation of a repository, and return a json with the created project.

- **`should be able to list the repositories`**: To be approved, your app should allow an array to be returned with all registered repositories.

- **`should be able to update repository`**: To be approved, your app should allow the fields `url`, `title` e `techs` to be changed. 

- **`should not be able to update a repository that does not exist`**: To be approved, you should validate on your update route, if the repository id sended by the url exists. If it doesn't, return status `400`.

- **`should not be able to update repository likes manually`**: To be approved, you shoul not allow your update route to directly change likes from that repository, keeping the same number of likes that it already had.

- **`should be able to delete the repository`**: To be approved, your app should allow a repository with an informed id to be deleted, and by doing so, return status `204`.

- **`should not be able to delete a repository that does not exist`**: To be approved, you should validate on your delete route, if the repository id sended by the url exists. If it doesn't, return status `400`.

- **`should be able to give a like to the repository`**: To be approved, your app should allow a repository with an informed id to receive likes. The likes value should be incremented by 1 each request, and as result, return a json with the repository and its likes updated.

- **`should not be able to like a repository that does not exist`**: To be approved, you have to validate on your like route if the repository id sended by the url exists. If it doesn't, return status `400`.

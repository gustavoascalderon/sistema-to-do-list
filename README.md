<h1 align="center">
  <br />
  <img
      alt="Sistema de Gerenciamento de Tarefas"
    width="150"
  />
  <br />
  <b>Sistema de Gerenciamento de Tarefas</b>
  <br />
  <sub
    ><sup><b>(TO-DO-LIST)</b></sup></sub
  >
  <br />
  <a
    href="https://github.com/gustavoascalderon/sistema-to-do-list/blob/main/.github/workflows/dotnet.yml"
  >
    <img
      src="https://github.com/gustavoascalderon/sistema-to-do-list/blob/main/.github/workflows/dotnet.yml/badge.svg"
      alt="Build Status"
    />
  </a>
  <a href="https://github.com/gustavoascalderon/sistema-to-do-list/releases/latest">
    <img
      src="https://img.shields.io/github/v/release/gustavoascalderon/sistema-to-do-list"
      alt="Latest Release"
    />
  </a>
</h1>

<p align="center">
  Esta API .NET Core é projetada para gerenciar tarefas em um sistema de To-Do List. Ela fornece endpoints para criar, editar, excluir e visualizar tarefas, além de permitir marcar tarefas como concluídas.
  <br />
</p>

<p align="center">
  Desenvolvida com Entity Framework Core e outras tecnologias modernas do .NET, este projeto visa oferecer uma API robusta para gerenciamento de tarefas.
  <br />
</p>

<p align="center">
  <br />
  <img src="./_docs/assets/carbon.png" />
</p>

## Endpoints da API

<table align="center">
  <tr>
    <th>Método</th>
    <th>Endpoint</th>
    <th>Descrição</th>
  </tr>
  <tr>
    <td>GET</td>
    <td>/api/v1/tasks</td>
    <td>Retorna uma lista de todas as tarefas</td>
  </tr>
  <tr>
    <td>GET</td>
    <td>/api/v1/tasks/{id}</td>
    <td>Retorna os detalhes de uma tarefa específica pelo ID</td>
  </tr>
  <tr>
    <td>POST</td>
    <td>/api/v1/tasks</td>
    <td>Cria uma nova tarefa</td>
  </tr>
  <tr>
    <td>PUT</td>
    <td>/api/v1/tasks/{id}</td>
    <td>Atualiza uma tarefa existente</td>
  </tr>
  <tr>
    <td>DELETE</td>
    <td>/api/v1/tasks/{id}</td>
    <td>Exclui uma tarefa</td>
  </tr>
  <tr>
    <td>PATCH</td>
    <td>/api/v1/tasks/{id}/complete</td>
    <td>Marca uma tarefa como concluída</td>
  </tr>
</table>

## Técnicas Utilizadas

<p align="center">
  - <b>Entity Framework Core:</b> ORM para gerenciamento de dados.<br />
  - <b>Design de API RESTful:</b> Garante endpoints claros e eficientes.<br />
  - <b>Injeção de Dependência:</b> Utilizada para promover baixo acoplamento e maior testabilidade.<br />
</p>

## Dependências

<table align="center">
  <tr>
    <th>Pacote</th>
    <th>Versão</th>
    <th>Link</th>
  </tr>
  <tr>
    <td>Microsoft.EntityFrameworkCore</td>
    <td>6.0.0</td>
    <td>
      <a
        href="https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/6.0.0"
        >NuGet</a
      >
    </td>
  </tr>
  <tr>
    <td>Microsoft.EntityFrameworkCore.Design</td>
    <td>6.0.0</td>
    <td>
      <a
        href="https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/6.0.0"
        >NuGet</a
      >
    </td>
  </tr>
  <tr>
    <td>Microsoft.EntityFrameworkCore.SqlServer</td>
    <td>6.0.0</td>
    <td>
      <a
        href="https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/6.0.0"
        >NuGet</a
      >
    </td>
  </tr>
  <tr>
    <td>Newtonsoft.Json</td>
    <td>13.0.1</td>
    <td>
      <a href="https://www.nuget.org/packages/Newtonsoft.Json/13.0.1">NuGet</a>
    </td>
  </tr>
</table>

## :gear: Arquitetura

```🌐
src
├── 📂 Controllers      [Rotas para os endpoints]
├── 📂 Models           [Modelos de banco de dados]
├── 📂 Services         [Regras de negócio]
├── 📂 Middlewares      [Funções intermediárias entre a requisição HTTP e a resposta final]
├── 📂 Database         [Estruturas relacionadas ao banco de dados]
│   ├── 📂 DTOs             [Modelos de entrada e View Models (Objetos de Transferência de Dados)]
│   ├── 📂 EntityFramework  [Arquivos relacionados ao ORM Entity Framework]
│   │     ├── 📂 Context         [Configurações do contexto do Entity]
│   │     ├── 📂 Migrations      [Migrações para atualizações do banco de dados]
│   ├── 📂 Repositories     [Padrão de repositório]

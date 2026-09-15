# Sistema de Gestão Escolar

## Sistema para gerenciar funcionários, alunos, cursos e matrículas

1. Quem utilizará o sistema (usuários)?
  - Funcionários

2. Quais os tipos de usuários e o que cada tipo consegue fazer?
  - Colaboradores: Cadastrar alunos, cadastrar cursos, editar dados dos alunos, editar dados dos cursos, excluir alunos, excluir cursos, listar alunos, listar cursos, matricular alunos nos cursos, desmatricular alunos dos cursos e atualizar os próprios dados
  - Admin: Todas as funções acima, mais: cadastrar outros funcionários, listar outros funcionários, editar dados dos outros funcionários e excluir outros funcionários

3. Quais informações iremos armazenar?
  - Funcionários: Nome, email, cargo, data de nascimento, cpf, senha, telefone, endereço
  - Alunos: Matrícula, CPF, Nome, data de nascimento, email, telefone, endereço
  - Cursos: Descrição, carga horária, nome
  - Matrículas: Quais alunos estão cadastrados em quais cursos

4. Quais regras ou restrições são necessárias?
  - Apenas funcionários admin podem criar/deletar outros funcionários
  - Funcionários colaboradores não podem editar dados de outros funcionários
  - CPF não pode repetir, email não pode repetir
  - Nome, email, cargo, cpf, senha, carga horária, matrícula são dados obrigatórios
  - Um aluno não pode ser matriculado duas ou mais vezes no mesmo curso
  - O sistema deve validar as informações

## PROBLEMA:
  - Esses sistema é direcionado a funcionários de escolas
  - Permite cadastrar, editar, listar e deletar alunos, cursos, matrículas e funcionários
  
## MODELO DE NEGÓCIO:
  ![Business Model Canvas](images/business-model-canvas.png)

## REQUISITOS:
1. Requisitos Funcionais:
  - Cadastrar alunos
  - Cadastrar funcionários
  - Cadastrar cursos
  - Listar alunos
  - Listar cursos
  - Listar funcionários
  - Mostrar os dados do aluno
  - Mostrar os dados do funcionário
  - Mostrar os dados do curso
  - Realizar as matrículas
  - Editar os dados do aluno
  - Editar os dados do funcionário
  - Editar os dados do curso
  - Excluir os alunos
  - Excluir os funcionários
  - Excluir os cursos
  - Excluir as matrículas
  - Login de usuários
  - Buscar aluno pelo nome
  - Buscar aluno pelo CPF
  - Buscar funcionário pelo nome
  - Buscar funcionário pelo CPF
  - Mostrar os cursos em que cada aluno está matriculado
  - Mostrar os alunos que estão matriculados em cada curso
2. Requisitos Não Funcionais:
  - Autenticação
  - Interface com navegação padronizada e consistente entre as telas
  - Interface responsiva e adaptativa a diversas resoluções de tela e dispositivos diferentes, como computador, celular e tablet
  - Interface deve ser compatível com os principais navegadores web
  - Criptografar as senhas antes de salvá-las no banco de dados
  - Disponível durante todo o horário de funcionamento da instituição
  - Restringir acesso pelo tipo de usuário
  
## REGRAS DE NEGÓCIO:
- CPF de cada aluno deve ser único
- CPF de cada funcionário deve ser único
- Email de cada funcionário deve ser único
- A matrícula de cada aluno deve ser única
- Nome de cada curso deve ser único
- Impedir exclusão de cursos que tenham alunos matriculados
- Impedir exclusão de alunos que estejam matriculados em 1 ou mais cursos

## CASOS DE USO:
  ![Casos de uso](images/diagrama-casos-de-uso.png)

## Classes:
  ![Classes](images/diagrama-classes.png)

## Sequências:
- Login:
  
  ![Login](images/DiagramasSequencias/Login.png)

- Cadastro funcionário:
  
  ![Cadastro funcionário](images/DiagramasSequencias/CadastrarFuncionario.png)

- Cadastro aluno:
  
  ![Cadastro aluno](images/DiagramasSequencias/CadastrarAluno.png)

- Cadastro curso:
  
  ![Cadastro curso](images/DiagramasSequencias/CadastrarCurso.png)

- Lista de funcionários:
  
  ![Lista funcionários](images/DiagramasSequencias/ListarFuncionarios.png)

- Lista de alunos:
  
  ![Lista alunos](images/DiagramasSequencias/ListarAlunos.png)

- Lista de cursos:
  
  ![Lista cursos](images/DiagramasSequencias/ListarCursos.png)
### Login

![Diagrama de sequência do login](images/DiagramasSequencias/Login.png)

Descreve o fluxo de autenticação do funcionário no sistema, desde o envio das credenciais até a validação do acesso.

### Cadastro de aluno

![Diagrama de sequência do cadastro de aluno](images/DiagramasSequencias/CadastrarAluno.png)

Apresenta o processo de cadastro de um novo aluno e a validação dos dados informados.

### Cadastro de funcionário

![Diagrama de sequência do cadastro de funcionário](images/DiagramasSequencias/CadastrarFuncionario.png)

Mostra o fluxo para cadastrar um funcionário, incluindo o registro das informações e a validação dos dados obrigatórios.

### Cadastro de curso

![Diagrama de sequência do cadastro de curso](images/DiagramasSequencias/CadastrarCurso.png)

Representa o cadastro de um curso e a verificação das informações antes de salvá-lo no sistema.

### Listagem de alunos

![Diagrama de sequência da listagem de alunos](images/DiagramasSequencias/ListarAlunos.png)

Descreve a solicitação e a exibição da lista de alunos cadastrados.

### Listagem de funcionários

![Diagrama de sequência da listagem de funcionários](images/DiagramasSequencias/ListarFuncionarios.png)

Apresenta o fluxo de consulta e exibição dos funcionários cadastrados.

### Listagem de cursos

![Diagrama de sequência da listagem de cursos](images/DiagramasSequencias/ListarCursos.png)

Mostra como o sistema consulta e exibe os cursos disponíveis.

### Busca de aluno pelo nome

![Diagrama de sequência da busca de aluno pelo nome](images/DiagramasSequencias/BuscarAlunoPeloNome.png)

Representa a busca de um aluno utilizando seu nome como critério.

### Busca de aluno pelo CPF

![Diagrama de sequência da busca de aluno pelo CPF](images/DiagramasSequencias/BuscarAlunoPeloCPF.png)

Representa a busca de um aluno utilizando o CPF como critério único de identificação.

### Busca de funcionário pelo nome

![Diagrama de sequência da busca de funcionário pelo nome](images/DiagramasSequencias/BuscarFuncionarioPeloNome.png)

Descreve a consulta de um funcionário a partir do nome informado.

### Busca de funcionário pelo CPF

![Diagrama de sequência da busca de funcionário pelo CPF](images/DiagramasSequencias/BuscarFuncionarioPeloCPF.png)

Descreve a consulta de um funcionário utilizando o CPF como critério de identificação.

### Dados do aluno

![Diagrama de sequência dos dados do aluno](images/DiagramasSequencias/MostrarDadosDoAluno.png)

Mostra o fluxo para consultar e exibir os dados completos de um aluno.

### Dados do funcionário

![Diagrama de sequência dos dados do funcionário](images/DiagramasSequencias/MostrarDadosDoFuncionario.png)

Mostra o fluxo para consultar e exibir os dados completos de um funcionário.

### Dados do curso

![Diagrama de sequência dos dados do curso](images/DiagramasSequencias/MostrarDadosDoCurso.png)

Apresenta a consulta e a exibição das informações detalhadas de um curso.

### Edição de aluno

![Diagrama de sequência da edição de aluno](images/DiagramasSequencias/EditarDadosDoAluno.png)

Descreve a atualização dos dados cadastrais de um aluno.

### Edição de funcionário

![Diagrama de sequência da edição de funcionário](images/DiagramasSequencias/EditarDadosDoFuncionario.png)

Descreve a atualização dos dados cadastrais de um funcionário, respeitando as permissões do usuário.

### Edição de curso

![Diagrama de sequência da edição de curso](images/DiagramasSequencias/EditarDadosDoCurso.png)

Representa a alteração das informações de um curso já cadastrado.

### Exclusão de aluno

![Diagrama de sequência da exclusão de aluno](images/DiagramasSequencias/ExcluirAluno.png)

Mostra o processo de exclusão de um aluno, incluindo a verificação de matrículas ativas.

### Exclusão de funcionário

![Diagrama de sequência da exclusão de funcionário](images/DiagramasSequencias/ExcluirFuncionario.png)

Apresenta o fluxo de exclusão de um funcionário conforme as permissões administrativas.

### Exclusão de curso

![Diagrama de sequência da exclusão de curso](images/DiagramasSequencias/ExcluirCursos.png)

Descreve a exclusão de um curso após verificar se não existem alunos matriculados nele.

### Exclusão de matrícula

![Diagrama de sequência da exclusão de matrícula](images/DiagramasSequencias/ExcluirMatriculas.png)

Mostra o fluxo para remover a matrícula de um aluno em um curso.

### Realização de matrícula

![Diagrama de sequência da realização de matrícula](images/DiagramasSequencias/RealizarMatriculaDoAlunoEmCursos.png)

Representa o processo de matricular um aluno em um curso, validando a existência da matrícula para evitar duplicidade.
@startuml

' hide the spot
' hide circle

' avoid problems with angled crows feet
skinparam linetype ortho

entity "Aluno" as e01 {
  *idAluno : number <<generated>>
  --
  *matricula : text
  *nome : text
  *email : text
  *idade : integer
}

entity "Professor" as e02 {
  *idProfessor : number <<generated>>
  --
  *nome : text
  *idade : integer
  *email : text
  *salario : integer
}

entity "Curso" as e03 {
  *idCurso : number <<generated>>
  --
  *nome : text
  *departamento : text
  *semestre : integer
}

entity "Disciplina" as e04 {
  *idDisciplina : number <<generated>>
  --
  *nome : text
  *departamento : text
  *semestre : integer
}


e01 }|..|| e02
e01 }|..|| e03

e02 }|..|| e04
e03 }|..|| e04


@enduml


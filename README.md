Controle de Gastos com Spring Boot e HTMX

Projeto Controle de Gastos. Criei essa aplicação como um projeto de estudos aqui do 2º ano de ADS para colocar em prática o que a gente vê em aula.

A ideia era construir algo útil, um sistema pra lançar as despesas e receitas, mas fugindo do JavaScript pesado como React ou Angular. Foi aí que eu descobri o HTMX, que é uma biblioteca muito massa que deixa o HTML super poderoso. O resultado é uma página que atualiza rapidinho, sem precisar recarregar tudo.

O que o sistema faz? CRUD completo de Lançamentos: Você pode Cadastrar, Listar, Editar e Deletar suas contas (o famoso CRUD que a gente não aguenta mais ouvir falar, mas precisa saber kkk).

Interface Reativa: Graças ao HTMX, quando você adiciona ou deleta um item, só a lista atualiza, não a página inteira. Fica bem mais rápido!

Tema Claro e Escuro: Pra não forçar a vista na hora de programar.

Backend com Spring Boot: A parte "de trás" foi toda feita com Java e Spring, seguindo o padrão MVC que os professores ensinam.

🛠️ Tecnologias que eu usei Aqui tá a lista do que eu usei pra construir tudo:

Backend:

☕ Java 21 e Spring Boot: O feijão com arroz do mundo Java pra criar a API e toda a lógica do sistema.

📦 Maven: Pra gerenciar as dependências e não precisar baixar JAR na mão.

🗃️ Spring Data JPA: Pra facilitar a conversa com o banco de dados.

Frontend:

🍃 Thymeleaf: Para "turbinar" o HTML e conseguir mostrar os dados que vêm do Java.

🚀 HTMX: A estrela do projeto! É ele que faz as chamadas pro backend e atualiza os pedaços da tela sem precisar de uma linha de JavaScript complexo.

Banco de Dados:

💾 H2 (para desenvolver): Um banco de dados em memória, super leve. Facilita muito pra testar as coisas rapidinho na minha máquina.

🐘 PostgreSQL (para produção): Quando o projeto vai pro ar de verdade, aí precisa de um banco mais parrudo como o Postgre.

Deploy:

🐳 Docker: Usei pra "empacotar" a aplicação inteira. Com isso, ela roda em qualquer lugar, igualzinho roda no meu PC. Salvou minha vida na hora de subir pro servidor!

🚀 Bora rodar o projeto? Pra testar aí na sua máquina é bem tranquilo.

O que você precisa ter instalado: Git

Java JDK 21

Maven

Docker (se quiser testar do jeito "profissa")

Passo a passo: Primeiro, clona o repositório pra sua máquina:

Bash

git clone https://github.com/seu-usuario/controle-de-gastos.git cd controle-de-gastos Modo 1: Rodando localmente (o jeito fácil) Isso vai usar o banco H2, que roda em memória e zera toda vez que você para a aplicação. Ótimo pra desenvolver.

Bash

O projetinho já vem com o Maven Wrapper, então nem precisa instalar nada
./mvnw spring-boot:run Depois que carregar tudo, abre o navegador em http://localhost:8080.

Modo 2: Rodando com Docker (simulando o servidor) Aqui a gente cria uma "caixinha" (container) com a aplicação dentro. É assim que ela vai rodar na nuvem.

Bash

1. Cria a imagem da aplicação
docker build -t controle-de-gastos .

2. Sobe o container
docker run -p 8080:8080 controle-de-gastos Aí é só acessar o mesmo endereço: http://localhost:8080.

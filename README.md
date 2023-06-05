# Projeto Integrador - Daarii

Projeto Integrador do Curso de Técnico em Desenvolvimento de Sistemas para a Internet Integrado ao Ensino Médio do IFC - Campus Araquari.

Alunos: [Davi Gabriel Tomaz](https://github.com/davigtomaz) e [Ariane Tainara Junkes](https://github.com/ArianeJunkes).

Links do projeto:

-   [Documentação (esse documento)](github.com/marcoandre/pi-modelo)
-   [Backend](github.com/marcoandre/pi-backend)
-   [Frontend](github.com/marcoandre/pi-frontend)

# Situação Problema

A empresa [Skoob](http://www.skoob.com.br/), existente desde 2009, criada pelo brasileiro Lindenberg Moreira, associado com Viviane Lordello, profissional de Marketing, conta com mais de 8.2 milhões de usuários cadastrados no site. 

Através de cadastro, é possível listar o que você está lendo, o que já leu, o que pretende ler, o que está relendo e quais leituras foram abandonadas, formando assim uma "estante" virtual. O sistema tem um "paginômetro", que soma as páginas dos livros marcados como já lidos, além de uma média de páginas. Títulos ainda ausentes no banco de dados podem ser adicionados pelos próprios usuários, que podem compartilhar suas opiniões sobre as obras através de avaliações com estrelas, de uma a cinco, e resenhas. 

O usuário possui ainda a opção de participar de grupos com temas diversos, desde Livros Viajantes (um usuário se dispõe a emprestar um livro de acordo com a lista de participantes definida) a Colecionadores de Marcadores de Texto. Atualmente o Skoob disponibiliza gratuitamente App para iOS e Android.


## Problemas Observados 

* **Falta de localização de onde esses livros estão fisicamente;**
* **A estilização do site é muito antiga;**

Como os empréstimos são feitos apenas em grupos, não há localização de onde se encontram meus livros emprestados e não emprestados.

A estilização do site é muito antiga, não chamando atenção para novos usuários. 


# Descrição da proposta

O nosso projeto é um sistema de biblioteca pessoal que permite aos usuários registrarem os livros que possuem e acompanhar um controle detalhado de sua coleção. Com essa aplicação, os usuários poderão organizar e gerenciar facilmente os livros que possuem, incluindo informações como título, autor, cateoria, e uma descrição detalhada. Os livros poderão ser localizados de maneira em que quando registrados o usuário irá detalhar onde esses livros estão, um exemplo seria em que um usuário tem uma biblioteca em casa e outra no trabalho, ele poderá registrar o livro falando que ele está na biblioteca do trabalho. Além disso, a aplicação poderá oferecer recursos adicionais, como a geração de relatórios e estatísticas sobre a coleção de livros.


Além disso, o sistema oferece um recurso de empréstimos, permitindo que os usuários registrem empréstimos de livros para outras pessoas. Ao registrar um empréstimo, o usuário poderá inserir os detalhes da pessoa para quem o livro foi emprestado, como nome, contato, data do empréstimo e uma data prevista de devolução. Isso ajuda a manter um registro claro dos livros emprestados e facilita o acompanhamento de quem está com cada livro.


A nosso projeto será desenvolvido utilizando o framework Vue.js para Web, que oferece um ambiente de desenvolvimento rápido e eficiente para a criação de interfaces interativas e responsivas e para aplicativo móvel utilizaremos React Native. Faremos uso de componentes reutilizáveis, rotas para navegação entre as páginas e integração com uma API para persistência dos dados.



# Regras de Negócio

- **RN001- Cadastro de livros:** Um usuário pode registrar seus livros.
- **RN002- Autorização:** Os usuários deve solicitar autorização para acesso das bibliotecas.
- **RN003- Status do livro:** Os livros terão descrição se estão disponíveis ou não disponíveis para empréstimos, ou se são livros privados sem possibilidade de solicitar o empréstimo.
- **RN004- Registro de empréstimos:** Ao registrar um empréstimo, é necessário fornecer as informações do livro emprestado e da pessoa para quem foi emprestado.
- **RN005- Cadastro de categoria:** Os usuários podem adicionar tags ou categorias personalizadas para organizar sua coleção de livros.
- **RN006- Favoritar:** É possível marcar livros como favoritos para facilitar o acesso rápido. 
- **RN007- Cadastro de feedback:** O usuário pode registrar um feedback sobre os livros que ele emprestou.
- **RN008- Registro de relatório:** O administrador deve possuir acesso ao regristo de relatório.

# Requisitos Funcionais 

Entradas

- **R.F.01- Cadastro de usuário:** Para cadastro de usuário precisa de dados como email e a criação de uma senha. Usuário: todos os níveis de usuário.
- **R.F.02- Cadastro de livros:** Para cadastro de livros precisa de dados como categoria, editora, autor e localização. Usuário: todos os níveis de usuário. 
- **R.F.03- Cadastro de feedback:** Para cadastro de feedback precisa de dados como nome do livros, nome do usuário e comentário sobre o livro. Usuário: todos os níveis de usuário.
- **R.F.04- Registro de empréstimos:** Para registrar um empréstimo de livro é necessário nome do usuário, nome do livro e data de pedido. Usuário: todos os níveis de usuário.
- **R.F.05- Devolução de empréstimo:** Para registro de devolução de empréstimo é necessário nome de usuário, nome do livro e data da devolução. Usuário: todos os níveis de usuário.


Processos

- **R.F.06- Gerenciamento de usuário:** Auteticação de login e senha, criação de perfis e permissões de acesso.
- **R.F.07 - Listagem de empréstimos:** Tem como propósito informar quantos livros o usuário tem emprestado. Usuário: todos os níveis de usuário. Usuário: todos os níveis de usuário.


Saídas


- **R.F.08 - Registro de relatório:** Para registro de relatório precisa de dados como sobre o que será o relatório exemplo: livros mais lidos, livros mais emprestados, etc... Usuário: apenas vizualização.

# Requisitos Não Funcionais

- **R.N.F. 01- Forma de uso do software:** O sistema por fazer parte de um ambiente interno, provavelmente será utilizado de acordo com as horas de trabalho da empresa, mas estará ativo 24 horas por dia em 7 dias por semana.
- **R.N.F. 02- Usabilidade:** Responsavidade para se adaptar a diferentes tamanhos de tela.
- **R.N.03- Desempenho:** Carregamento rápido das informações dos livros e empréstimos. Eficiência no processamento das operações de adiçaõ, edição e exclusão de dados.
- **R.N.F. 04- Autenticação:** Para realizar o acesso ao sistema é necessário ter um usuário de autenticação criado pelo administrador, além da possibilidade de solicitar um envio de redefinição de senha.
- **R.N.F. 06- Tecnologia Front-end:** Para a exibição em front-end, o software utilizará o CSS3 e o HTML5, além das bibliotecas de Vue.
- **R.N.F. 07- Tecnologia Back-end:** O software será desenvolvido pela linguagem de programação Django.
- **R.N.F. 08- Segurança:** Proteção de dados do usuário por meio de autenticação e autorização adequadas. Criptografia dos dados sensíveis armazenados.
- **R.N.F 09- Confiabilidade:** Backup e recuperação de dados da aplicação. Detecção e tratamento de erros e exceções.
- **R.N.F 10-Escalabilidade:** Capacidade de lidar com um grande número de livros e usuários. Dimensionamento da infraestrutura de acordo com o crescimento da aplicação.

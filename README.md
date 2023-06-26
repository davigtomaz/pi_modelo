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

O nosso projeto é um sistema de biblioteca pessoal que permite aos usuários registrar seus livros e acompanhar um controle detalhado de sua coleção. Com essa aplicação, os usuários poderão organizar e gerenciar facilmente os livros que possuem, incluindo informações como título, autor, categoria, localização e uma descrição detalhada. Com a localização, o usuário poderia especificar, por exemplo, que um livro está em sua biblioteca em casa e ou no trabalho. Além disso, a aplicação poderá oferecer recursos adicionais, como a geração de relatórios e estatísticas sobre a coleção de livros.

O sistema oferece ainda um recurso de empréstimos, permitindo que os usuários registrem empréstimos de livros para outras pessoas. Ao registrar um empréstimo, o usuário poderá inserir os detalhes da pessoa para quem o livro foi emprestado, como nome, contato, data do empréstimo e uma data prevista de devolução. Isso ajuda a manter um registro claro dos livros emprestados e facilita o acompanhamento de quem está com cada livro.

# Regras de Negócio

- **RN001- Cadastro de livros:** Para registrar seus livros, o usuário deve estar cadastrado no sistema.
- **RN002- Autorização:** Os usuários devem solicitar autorização para acesso das bibliotecas.
- **RN003- Status do livro:** Os livros terão status: se estão ou não disponíveis para empréstimos, ou se são livros privados, isto é, que não aparecem para visualização por outros usuários.
- **RN004- Registro de empréstimos:** Ao registrar um empréstimo, é necessário fornecer as informações do livro emprestado e da pessoa para quem foi emprestado.
- **RN005- Cadastro de categoria:** Os usuários podem adicionar tags ou categorias personalizadas para organizar sua coleção de livros.
- **RN006- Favoritar:** É possível marcar livros como favoritos para facilitar o acesso rápido. 
- **RN007- Cadastro de feedback:** O usuário pode registrar um feedback sobre os livros que ele emprestou.
- **RN008- Relatórios:** O administrador deve possuir acesso aos relatórios.

# Requisitos Funcionais 

**Entradas**

- **R.F.01- Cadastro de usuário:** Tem como propósito a criação de usuários no sistema, direcionando para a página de criação. Dados necessários: nome, email e senha, criação de perfis e permissões de acesso. Usuário: todos os níveis de usuário.
- **R.F.02- Cadastro de livros:** Tem como propósito adicionar livros ao sistema,verificando se o usuário pode acessá-lo e, caso possa, o direcionando para a página cadastro. Dados necessários: categoria, editora, autor e localização. Usuário: todos os níveis de usuário. 
- **R.F.03- Cadastro de feedback:** Tem como proṕosito informar os usuários de quais são os livros mais lidos e emprestados. Dados necessários: nome do livros, nome do usuário e comentário sobre o livro. Usuário: todos os níveis de usuário.
- 

**Processos**

- **R.F.04- Registro de empréstimos:** Tem como propósito autenticar o acesso ao livro, verificando se o usuário pode acessá-lo e, caso possa, o direcionando para a página de solicitação. Dados necessários: nome do usuário, nome do livro e data de empréstimo e devolução. Usuário: todos os níveis de usuário.
- **R.F.05- Devolução de empréstimo:** Tem como propósito autenticar o acesso ao livro, verificando se o usuário pode acessá-lo e, caso possa, o direcionando para a página devolução. Dados necessários: nome de usuário, nome do livro e data da devolução. Usuário: todos os níveis de usuário.
- **R.F.06- Autenticação de usuário:** Tem como propósito autenticar o acesso ao sistema, verificando se o usuário pode acessá-lo e, caso possa, o direcionando para a página principal de confirmação. Dados necessários: login e senha. Usuário: todos os níveis de usuário.

**Saídas**

- **R.F.07 - Relatório de livros emprestados:** Tem como propósito informar quais são os livros mais emprestados, os que estão emprestados no momento e os que estão vencidos. Dados necessários: nome do livro, data de empréstimo e data de devoluçaõ, categoria, editora e autor. Usuário: todos os níveis de usuário.

# Requisitos Não Funcionais

- **R.N.F. 01 - Forma de uso do software:** O sistema estará ativo 24 horas por dia em 7 dias por semana.
- **R.N.F. 02 - Usabilidade:** Responsavidade, para se adaptar a diferentes tamanhos de tela.
- **R.N.03 - Desempenho:** Carregamento rápido das informações dos livros e empréstimos. Eficiência no processamento das operações de adição, edição e exclusão de dados.
- **R.N.F. 04 - Autenticação:** será feita por senha, que será criptografada para armazenamento no banco.
- **R.N.F. 06 - Tecnologia Front-end:** Para a exibição em front-end, o software utilizará o CSS3 e o HTML5, além do framework VueJS para a interface Web.
- **R.N.F. 07 - Tecnologia Back-end:** O software será desenvolvido utilizando o framework Django com DRF.
- **R.N.F. 08 - Segurança:** Proteção de dados do usuário por meio de autenticação e autorização adequadas. Criptografia dos dados sensíveis armazenados.
- **R.N.F 09 - Confiabilidade:** Backup e recuperação de dados da aplicação. Detecção e tratamento de erros e exceções.
- **R.N.F 10 - Escalabilidade:** Capacidade de lidar com um grande número de livros e usuários. Dimensionamento da infraestrutura de acordo com o crescimento da aplicação.
- **R.N.F 11 - Tecnologia Mobile:** Para a criação de interfaces interativas e responsivas e para aplicativo móvel, utilizaremos React Native. Faremos uso de componentes reutilizáveis, rotas para navegação entre as páginas e integração com uma API para persistência dos dados.


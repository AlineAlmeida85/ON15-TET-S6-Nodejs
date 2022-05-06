# Respostas

1) qual nivel de maturidade corresponde ao CRUD (Create, Read, Update, Delete)?
#### Resposta: Maturidade 2
##### Na criação de uma tela de cadastro, é de extrema importância que as operações simples como, criar recurso, atualizar recurso, buscar recurso e deletar recurso sejam implementadas. Nesse nível de maturidade a mesma ideia deve ser utilizada com os verbos HTTP, eles devem ser suficientes para um CRUD (Crate, Read, Update, Delete). Para cada ação de um recurso da API são aplicados verbos diferentes. Dentre as opções disponíveis, baseado na arquitetura REST, as mais conhecidas são as seguintes:– POST: criação de um novo recurso, quando pensamos no recurso cliente, a ação realizada seria de criar um cliente;– GET: buscar dados de um ou vários recursos;– PUT: atualizar um recurso, por inteiro. Se um recurso cliente tem como informações os atributos nome, e-mail, data de nascimento e CPF, ao efetuar uma atualização passando o verbo PUT na requisição a API, todos os atributos do cliente devem ser enviados no corpo da requisição, mesmo aqueles que não serão atualizados;– PATCH: atualizar um recurso, parcialmente. Seguindo o mesmo exemplo da ação PUT, um cliente com seus atributos, nesse tipo de requisição apenas o atributo desejado será enviado no corpo da requisição. Geralmente para atualização é a ação mais utilizada, pois utiliza menos dados para navegação no tráfego de informação;– DELETE: remover um recurso. É importante ter-se o conhecimento de que cada recurso tem um identificador único e é esse identificador que deve ser enviado para API como um parâmetro, para que assim a API saiba qual é o recurso exato a ser deletado;– HEAD: verificar se um recurso existe, evitando o mínimo de tráfego entre a requisição a recomendação do nível de maturidade 2 é a utilização do HEAD. Se o recurso existir apenas no código 200, será retornado informado a sua existência, se não o código 404 será enviado, informando a não existência do recurso;– OPTIONS: verificar todos os tipos de operações disponíveis para um determinado recurso. Se um recurso tem operações de criação, busca, atualização é nessa requisição que devem-se ser disponibilizadas a informação dessas possibilidades. É importante que o consumidor da API saiba exatamente todas as operações disponíveis para aquele recurso. Assim caso a ação desejada não esteja disponível o desenvolvedor poderá entrar em contato com o criador da API e solicitar que essa operação seja implementada.Para Ian Robinson nesse nível temos: “Introdução de verbos padrões para lidar com situações similares da mesma forma, removendo variações desnecessárias.” (Fowler MARTIN, 2010, Tradução nossa)Dessa forma a API fica muito mais legível para manutenções, reduzindo seu custo e passando ser mais fácil de ser consumida. Já se sabe por exemplo que ao fazer um GET é esperado o retorno de dados, e isso ajuda inclusive na performance na transferência de dados.

2) qual a relação entre os metodos HTTP e o CRUD?
#### Resposta: Os Métodos HTTP são os verbos que compõem a estrutura do CRUD.

3) o que é HATEOAS? Ele é obrigatório para que uma API seja considerada RESTfull?
#### Resposta: É um componente que faz parte da arquitetura REST, cujo objetivo é ajudar os clientes a consumirem uma API sem a necessidade de conhecimento prévio. Não é obrigatório.

4) O que quer dizer quando dizemos que uma API é indepotente?
### Resposta: Uma API é considerada idempotente se o resultado de uma requisição realizada com sucesso é independente do número de vezes que é executada.

5) Qual a diferença entre os métodos PUT e PATCH?
### Resposta: O PUT, é usado para alteração de um dado completo, O PATCH é usado para atualização parcial.









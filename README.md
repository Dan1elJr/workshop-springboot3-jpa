Este projeto implementa uma API REST utilizando o framework Spring Boot para gerenciar recursos relacionados a categorias, pedidos, produtos e usuários. Cada recurso tem seu próprio controlador, conforme detalhado abaixo.

## CategoryResource

### Endpoints
- **GET /categories:** Recupera uma lista de todas as categorias.
  ```java
  @GetMapping
  public ResponseEntity<List<Category>> findAll() {...}
  ```

- **GET /categories/{id}:** Recupera uma categoria específica por ID.
  ```java
  @GetMapping(value = "/{id}")
  public ResponseEntity<Category> findById(@PathVariable Long id) {...}
  ```

### Dependências
- **Serviço Autowired:** Utiliza um serviço `CategoryService` autowired para lidar com a lógica de negócios relacionada a categorias.

## OrderResource

### Endpoints
- **GET /orders:** Recupera uma lista de todos os pedidos.
  ```java
  @GetMapping
  public ResponseEntity<List<Order>> findAll() {...}
  ```

- **GET /orders/{id}:** Recupera um pedido específico por ID.
  ```java
  @GetMapping(value = "/{id}")
  public ResponseEntity<Order> findById(@PathVariable Long id) {...}
  ```

### Dependências
- **Serviço Autowired:** Utiliza um serviço `OrderService` autowired para lidar com a lógica de negócios relacionada a pedidos.

## ProductResource

### Endpoints
- **GET /products:** Recupera uma lista de todos os produtos.
  ```java
  @GetMapping
  public ResponseEntity<List<Product>> findAll() {...}
  ```

- **GET /products/{id}:** Recupera um produto específico por ID.
  ```java
  @GetMapping(value = "/{id}")
  public ResponseEntity<Product> findById(@PathVariable Long id) {...}
  ```

### Dependências
- **Serviço Autowired:** Utiliza um serviço `ProductService` autowired para lidar com a lógica de negócios relacionada a produtos.

## UserResource

### Endpoints
- **GET /users:** Recupera uma lista de todos os usuários.
  ```java
  @GetMapping
  public ResponseEntity<List<User>> findAll() {...}
  ```

- **GET /users/{id}:** Recupera um usuário específico por ID.
  ```java
  @GetMapping(value = "/{id}")
  public ResponseEntity<User> findById(@PathVariable Long id) {...}
  ```

- **POST /users:** Cria um novo usuário.
  ```java
  @PostMapping
  public ResponseEntity<User> insert(@RequestBody User obj) {...}
  ```

- **DELETE /users/{id}:** Exclui um usuário por ID.
  ```java
  @DeleteMapping(value = "/{id}")
  public ResponseEntity<Void> delete(@PathVariable Long id) {...}
  ```

- **PUT /users/{id}:** Atualiza um usuário por ID.
  ```java
  @PutMapping(value = "/{id}")
  public ResponseEntity<User> update(@PathVariable Long id, @RequestBody User obj) {...}
  ```

### Dependências
- **Serviço Autowired:** Utiliza um serviço `UserService` autowired para lidar com a lógica de negócios relacionada a usuários.

## Observação
Certifique-se de configurar as dependências e configurações apropriadas em sua aplicação Spring Boot para uma execução adequada.

**Boa codificação!**

# ProvaArquiteturawebAV2
# Projeto de Autenticação com JWT
Este repositório contém um projeto que demonstra como implementar autenticação de login e senha utilizando JWT (Json Web Token). A autenticação JWT é uma forma segura e eficiente de gerenciar sessões de usuário em aplicações web.
![image](https://github.com/PetronioFaleixo/ProvaArquiteturawebAV2/assets/79844325/557395be-b0fa-4b3e-948c-92f11e6d19cd)

![image](https://github.com/PetronioFaleixo/ProvaArquiteturawebAV2/assets/79844325/9d27e997-b294-4b98-b43f-33d97f14b99b)

## Projeto de Autenticação com JWT

Este repositório contém um projeto que demonstra como implementar autenticação de login e senha utilizando JWT (Json Web Token). A autenticação JWT é uma forma segura e eficiente de gerenciar sessões de usuário em aplicações web.

### Funcionalidades Principais

- **AuthController**: Controlador REST para gerenciamento de autenticação.
  - `/login`: Endpoint para autenticar usuários e obter um token JWT.
  - `/novoUsuario`: Endpoint para registrar um novo usuário.
  - `/verificarCadastro/{uuid}`: Endpoint para verificar o cadastro de um usuário com base em um UUID.

- **AuthService**: Serviço responsável pela lógica de autenticação utilizando JWT.

- **UsuarioService**: Serviço responsável pelo gerenciamento de usuários, incluindo inserção de novos usuários e verificação de cadastro.

### Configuração e Execução

Para executar o projeto localmente, siga os passos abaixo:

1. Clone este repositório:

2. Importe o projeto em sua IDE preferida (por exemplo, IntelliJ IDEA, Eclipse).

3. Certifique-se de ter o Java JDK e o Maven instalados.

4. Configure as propriedades de banco de dados no arquivo `application.properties` em `src/main/resources`.

5. Execute a aplicação utilizando sua IDE ou via linha de comando: mvn spring-boot

6. Acesse a API através da URL base `http://localhost:8080`.

### Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir um pull request com melhorias, correções ou novas funcionalidades.

### Licença

Este projeto está licenciado sob a [MIT License](https://opensource.org/licenses/MIT).

---

Este repositório é uma excelente base para aprender e implementar autenticação segura em aplicações Java utilizando JWT.


# Diagrama de Componentes

+-------------------------------------------+
![image](https://github.com/PetronioFaleixo/ProvaArquiteturawebAV2/assets/79844325/6edc0ab0-5c7d-4495-b4bf-7d8fa4476ea3)


# Diagrama de Componentes e Funcionamento Geral

Web Client: Representa qualquer cliente que interage com a API, como um navegador web ou um aplicativo.

### AuthController
O `AuthController` é um controlador REST responsável por gerenciar as operações de autenticação no sistema. Ele disponibiliza os seguintes endpoints:

- **/login**: Endpoint utilizado para autenticar usuários. Quando um usuário fornece suas credenciais corretas (como nome de usuário e senha), este endpoint gera um token JWT (JSON Web Token) que pode ser utilizado para autenticação subsequente.
  
- **/novoUsuario**: Endpoint para registrar um novo usuário no sistema. Este endpoint recebe os dados necessários para criar um novo usuário, como nome, e-mail e senha.
  
- **/verificarCadastro/{uuid}**: Endpoint utilizado para verificar o cadastro de um usuário com base em um UUID específico. Esse UUID pode ser gerado durante o processo de registro e usado para confirmar o cadastro do usuário.

### AuthService
O `AuthService` é responsável pela lógica de autenticação utilizando JWT. Suas principais funções incluem:

- **Geração de Tokens JWT**: Quando um usuário é autenticado com sucesso através do `/login`, o `AuthService` gera um token JWT contendo informações específicas do usuário e um período de validade.
  
- **Validação de Tokens Recebidos**: Quando um usuário tenta acessar recursos protegidos, o `AuthService` valida o token JWT recebido para garantir que seja autêntico e que não tenha expirado.

### UsuarioService
O `UsuarioService` gerencia as operações relacionadas aos usuários no sistema. Suas responsabilidades incluem:

- **Inserção de Novos Usuários**: Recebe os dados de novos usuários vindos do endpoint `/novoUsuario` e os insere no banco de dados para que possam ser autenticados posteriormente.
  
- **Consultas de Usuários**: Fornece métodos para consultar informações de usuários armazenadas no banco de dados, essenciais para operações como verificação de cadastro (`/verificarCadastro/{uuid}`).

### Banco de Dados
O Banco de Dados armazena os dados dos usuários e outras informações necessárias para o funcionamento do sistema. As propriedades de conexão são configuradas no arquivo `application.properties`, que contém informações como URL de conexão, credenciais de acesso e outras configurações específicas do banco de dados utilizado.

### Funcionamento Geral
O sistema opera da seguinte maneira:

- **Interacão Cliente-Servidor**: O cliente (front-end ou outra aplicação) interage com o sistema exclusivamente através dos endpoints fornecidos pelo `AuthController`.
  
- **Utilização de Serviços**: O `AuthController` utiliza serviços como `AuthService` e `UsuarioService` para executar operações relacionadas à autenticação de usuários e gerenciamento de dados de usuários.
  
- **Persistência de Dados**: Todas as operações relacionadas a usuários, como autenticação, registro de novos usuários e verificação de cadastro, são persistidas e consultadas no banco de dados configurado, garantindo a integridade e segurança dos dados do sistema.

Esse diagrama simplificado fornece uma visão geral das principais partes do sistema e como elas se inter-relacionam para implementar um sistema de autenticação seguro utilizando JWT em aplicações Java.


Fim

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

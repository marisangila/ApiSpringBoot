# API com Spring Boot

## Requisitos

Antes de iniciar o desenvolvimento, é necessário configurar o ambiente de desenvolvimento. Siga as etapas abaixo:

### 1. Instalar JDK

- Baixe e instale o [Java Development Kit (JDK)](https://www.microsoft.com/openjdk).

### 2. Instalar Extensões no VS Code

Para facilitar o desenvolvimento de aplicativos Spring Boot, instale as seguintes extensões no Visual Studio Code:

- **Extension Pack for Java**: [Instalar no VS Code](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)
- **Spring Boot Extension Pack**: [Instalar no VS Code](https://marketplace.visualstudio.com/items?itemName=vmware.vscode-boot-dev-pack)

### 3. Documentação Oficial

Leia a documentação oficial para entender como configurar e trabalhar com Spring Boot no VS Code:

- [Documentação de Spring Boot no VS Code](https://code.visualstudio.com/docs/java/java-spring-boot)

### 4. Criar um Projeto Spring Boot

Acesse o site [Spring Initializr](https://start.spring.io/) para gerar um projeto Spring Boot com as dependências necessárias.

**Dependências recomendadas:**

- **Spring Web**
- **Spring Boot DevTools**
- **Lombok**

Depois de gerar o projeto, extraia o arquivo compactado e abra-o no Visual Studio Code.

### 5. Atualizar Dependências

Para garantir que todas as dependências estejam corretas, atualize o projeto usando o Maven. Certifique-se de que o arquivo `pom.xml` não contenha conflitos de dependências (nenhuma em vermelho).

## Executando o Projeto

Para executar o projeto, siga as etapas abaixo:

1. Abra o terminal no VS Code.
2. Execute o comando para rodar a aplicação:

   ```bash
      mvn spring-boot:run
   ```

## Testando a API

Para testar faça uma requição para a seguinte URI:


    ```bash
      http://localhost:8080/api/cats
    ```

# Gerando documentação de API usando Swagger:

1. Incluar as seguintes dependências no arquivo pom.xml:

 ```xml
      <dependency>
         <groupId>org.springdoc</groupId>
         <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
         <version>2.6.0</version>
      </dependency>
      <dependency>
         <groupId>org.springframework.boot</groupId>
         <artifactId>spring-boot-starter-security</artifactId>
      </dependency>
      <dependency>
         <groupId>org.springframework.boot</groupId>
         <artifactId>spring-boot-starter-web</artifactId>
      </dependency>
   ```
   
2. Edite o arquivo application.properties

   ```properties
      spring.security.user.name=admin
      spring.security.user.password=admin
   ```
3. Se o arquivo não existir criar no diretório resources

## Visualizando a documentação

1. Para visualizar a documentação gerada automaticamente acesse a seguinte URL no navegador:

   ```bash
      http://localhost:8080/swagger-ui/index.html
   ```


## Testando Requisições para API

1. Para testar API no VScode instale a seguinte extensão:

- Rest Client

2. Crie um arquivo .HTTP e insira as requisições.
    ```bash
      GET http://localhost:8080/api/cats
   ```




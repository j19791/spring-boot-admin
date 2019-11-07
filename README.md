# Projeto do curso Spring Boot Parte 2: Spring Boot Admin

### Implantação
* Criar novo projeto Spring Boot com [Spring Initializr](https://start.spring.io/)
* Incluir módulo Web
* Versão compatível com Spring Boot Admin
* Incluir no pom.xml a dependência do Spring-boot-admin:

`<dependency>`
    `<groupId>de.codecentric</groupId>`  
    `<artifactId>spring-boot-admin-starter-server</artifactId>`  
    `<version>2.1.4</version>`  
`</dependency>`  

* no application.properties, alterar a porta, para não gerar conflito com a aplicação monitorada:  
`server.port=8081`
* para acessar a aplicação de monitoramento [localhost:8081](http://localhost:8081)
* Não esquecer de colocar na classe SpringBootAdminApplication as anotações:

@EnableAdminServer  
@Configuration  
@EnableAutoConfiguration  

* no aplication.properties da api, incluir:  
`spring.boot.admin.client.url=http://localhost:8081`

* e a dependência:

`<dependency>
		    <groupId>de.codecentric</groupId>
		    <artifactId>spring-boot-admin-starter-client</artifactId>
		    <version>2.1.4</version>
</dependency>`





# Sales Report
Este é um projeto que consiste em seu backend o padrão WebService utilizando o framework Spring boot e no frontend alguns conceitos de ReactJS, abaixo o link do projeto:

Link do frontend hospedado no netlify:
- https://ajsalesreport.netlify.app/

Obs: Como eu não tenho a versão premium do Heroku, a aplicação "Adormece" após 30 minutos caso não tenha nenhum acesso, e quando o link é acessado novamente, o Heroku tem um delay de mais ou menos 45 segundos para carregar as informações do backend. Peço um pouco de paciência e compreensão.

# Telas do projeto

A ideia principal é carregar a lista de vendedores, trazendo as informações de id, data da possivel venda, nome do vendedor, quantidade de visitas, quantidade de vendas, quantidade total vendida em R$ e um botão de notificação que quando é acionado envia um SMS para pessoa com as informações parametrizadas no backend.

![image](https://user-images.githubusercontent.com/100853329/179548911-7c0108f9-48e5-43a2-a62e-e5e5931a8072.png)

Afim de ter um relatorio mais completo, foi adicionado um DE/PARA para obter informações mais detalhadas.

![image](https://user-images.githubusercontent.com/100853329/179549653-b32d5926-5dec-4778-8b76-ad54bc831ea3.png)

## Dados utilizados no projeto
Seed utilizado no projeto

```
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',121,67,18196.0,'2022-06-16');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',26,14,4255.0,'2022-06-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',55,42,13249.0,'2022-06-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',73,65,20751.0,'2022-06-10');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',47,25,7318.0,'2022-06-04');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',72,60,15608.0,'2022-06-03');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',97,68,8901.0,'2022-06-03');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',68,26,13231.0,'2022-06-02');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',73,53,19476.0,'2022-05-22');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',28,23,20530.0,'2022-05-18');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',83,44,4864.0,'2022-05-13');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',82,43,21753.0,'2022-05-06');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',43,26,7362.0,'2022-05-03');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',54,23,10549.0,'2022-04-28');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',125,84,13333.0,'2022-04-25');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',44,26,7431.0,'2022-04-23');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',46,25,21099.0,'2022-04-19');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',42,28,7217.0,'2022-04-19');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',52,21,10107.0,'2022-04-18');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',121,90,18174.0,'2022-04-17');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',65,14,8095.0,'2022-04-12');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',107,74,11507.0,'2022-04-12');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',140,74,11709.0,'2022-04-09');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',95,91,8288.0,'2022-04-08');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',68,43,17016.0,'2022-04-07');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',21,20,17126.0,'2022-04-03');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',38,15,7957.0,'2022-03-31');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',53,29,20903.0,'2022-03-29');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',19,10,3987.0,'2022-03-28');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',78,34,20795.0,'2022-03-27');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',83,44,4938.0,'2022-03-26');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',32,12,6926.0,'2022-03-13');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',64,33,8193.0,'2022-03-13');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',39,39,10557.0,'2022-03-05');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',158,84,21601.0,'2022-03-02');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',12,6,7625.0,'2022-02-28');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',82,82,22465.0,'2022-02-27');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',68,56,12595.0,'2022-02-17');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',27,13,4636.0,'2022-02-16');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',52,33,10155.0,'2022-02-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',142,81,13610.0,'2022-02-13');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',81,45,15306.0,'2022-02-08');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',64,35,17460.0,'2022-02-07');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',48,24,21413.0,'2022-02-03');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',150,82,6505.0,'2022-01-26');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',138,95,7983.0,'2022-01-18');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',70,48,9564.0,'2022-01-16');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',162,84,7302.0,'2022-01-15');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',57,54,9126.0,'2022-01-12');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',78,60,5253.0,'2022-01-06');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',81,53,11553.0,'2022-01-04');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',168,92,6299.0,'2021-12-28');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',48,13,22411.0,'2021-12-26');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',107,67,9788.0,'2021-12-24');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',106,62,18942.0,'2021-12-20');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',40,26,11731.0,'2021-12-18');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',101,68,19882.0,'2021-12-18');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',185,100,14618.0,'2021-12-17');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',82,47,7951.0,'2021-12-15');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',86,45,4147.0,'2021-12-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',95,88,12943.0,'2021-12-09');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',75,58,18747.0,'2021-12-02');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',96,50,12624.0,'2021-12-01');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',79,40,14770.0,'2021-11-21');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',73,46,14124.0,'2021-11-20');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',92,58,20953.0,'2021-11-20');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',43,30,9690.0,'2021-11-18');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',58,30,11396.0,'2021-11-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',49,14,5119.0,'2021-11-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',53,23,8206.0,'2021-11-12');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',49,25,8269.0,'2021-11-10');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',53,29,17984.0,'2021-11-09');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',43,26,3056.0,'2021-11-08');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',51,21,8624.0,'2021-11-06');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',64,41,10959.0,'2021-11-03');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',75,23,15883.0,'2021-10-30');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',51,44,14038.0,'2021-10-27');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',141,81,13535.0,'2021-10-26');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',135,98,17241.0,'2021-10-25');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',116,66,16415.0,'2021-10-19');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',60,44,5329.0,'2021-10-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',63,32,16618.0,'2021-10-07');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',176,100,5062.0,'2021-10-01');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',118,45,22235.0,'2021-09-29');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',150,97,14484.0,'2021-09-26');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',115,63,18081.0,'2021-09-24');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',159,88,16101.0,'2021-09-23');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',76,45,11150.0,'2021-09-22');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',65,63,17982.0,'2021-09-09');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',90,68,15927.0,'2021-09-08');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',22,12,9793.0,'2021-09-06');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',19,11,4185.0,'2021-09-05');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',68,21,15541.0,'2021-09-04');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',64,47,7287.0,'2021-09-04');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',153,92,17913.0,'2021-09-04');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',93,53,12648.0,'2021-09-02');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',78,32,12021.0,'2021-08-30');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',94,49,18787.0,'2021-08-29');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',54,28,3974.0,'2021-08-28');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',45,25,5681.0,'2021-08-26');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',11,1,4008.0,'2021-08-14');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',118,80,5218.0,'2021-08-13');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',52,21,21220.0,'2021-08-09');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',127,23,8831.0,'2021-08-06');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',78,23,13900.0,'2021-08-04');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',102,52,22086.0,'2021-08-03');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',54,53,15731.0,'2021-07-31');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Barry Allen',173,93,10816.0,'2021-07-22');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',60,45,17633.0,'2021-07-20');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',138,72,14528.0,'2021-07-19');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',147,96,21582.0,'2021-07-17');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Logan',32,12,9751.0,'2021-07-13');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',83,59,8496.0,'2021-07-08');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',58,48,5283.0,'2021-07-07');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Kal-El',55,35,20474.0,'2021-07-05');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Anakin',84,34,5787.0,'2021-07-01');
INSERT INTO tb_sales(seller_name,visited,deals,amount,date) VALUES ('Padme',79,68,11976.0,'2021-06-27');
```
## application-test.properties
Configuração do banco H2 e variaveis de ambiente para configuração do envio do SMS via twilio
```
twilio.sid=${TWILIO_SID}
twilio.key=${TWILIO_KEY}
twilio.phone.from=${TWILIO_PHONE_FROM}
twilio.phone.to=${TWILIO_PHONE_TO}

spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=

spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

spring.jpa.show-sql=false
spring.jpa.properties.hibernate.format_sql=true
```
## Considerações finais
Como foi um projeto simples de demonstração de aplicação, o maior foco foi aplicar os conceitos de envio de SMS via Twilio, com isso, não houve necessidade de criar a camada DTO, segue imagem abaixo:

![image](https://user-images.githubusercontent.com/100853329/179554539-763a4855-10f5-4647-ba6f-0ceb324e3a2e.png)

## Dependências utilizadas
Abaixo, as dependências utilizadas:
```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.7.1</version>
		<relativePath /> <!-- lookup parent from repository -->
	</parent>
	<groupId>com.ajunior</groupId>
	<artifactId>ajsalesreport</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>ajsalesreport</name>
	<description>This a sales report made by AJunior98</description>
	<properties>
		<java.version>17</java.version>
	</properties>
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-security</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<scope>runtime</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.springframework.security</groupId>
			<artifactId>spring-security-test</artifactId>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>com.twilio.sdk</groupId>
			<artifactId>twilio</artifactId>
			<version>8.31.1</version>
		</dependency>
		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-core</artifactId>
			<version>6.1.1.Final</version>
			<type>pom</type>
		</dependency>

	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-resources-plugin</artifactId>
				<version>3.1.0</version><!--$NO-MVN-MAN-VER$ -->
			</plugin>
		</plugins>
	</build>
</project>
```

## Postman
Abaixo a collection utilizada no Postman caso deseje testar as funcionalidades:
https://www.getpostman.com/collections/0c2c71755a0a7d107e9f

# Sistema de Agência de Viagens ✈️

Sistema desktop em **Java (Swing)** para **cadastro de clientes, destinos e pacotes turísticos**,  
com **gerenciamento de reservas**. Projeto acadêmico com foco em **POO**, **DAO/DTO** e integração **JDBC**.

<p align="left">
  <img alt="Java" src="https://img.shields.io/badge/Java-8%2B-orange">
  <img alt="Build" src="https://img.shields.io/badge/build-Ant%20%7C%20Maven-blue">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-success">
</p>

---

## ✨ Funcionalidades
- Cadastro de **clientes**
- Cadastro de **destinos** turísticos
- Cadastro de **pacotes** de viagem
- **Reservas** (associando cliente, destino e pacote)
- Interface gráfica **Swing**

---

## 🧰 Tecnologias
- Java 8+ (POO, Swing)
- MySQL (JDBC) — se aplicável
- NetBeans/Ant (ou Maven, se houver `pom.xml`)
- Padrões: DAO/DTO

---

## ⚙️ Como executar

> **Dica:** publique quaisquer **.zip/.jar** em **Releases**; mantenha o **código-fonte descompactado** no repositório para melhor visualização no GitHub.

### 1) Pré-requisitos
- **Java 8+**
- (Opcional) **MySQL** em execução (`localhost`), se o projeto usar banco
- IDE (recomendado: **NetBeans**)

### 2) Banco de dados (se aplicável)
- Execute o script SQL do projeto (ex.: `sql/agencia.sql`) para criar as tabelas.

### 3) Configuração JDBC (se aplicável)
Ajuste a conexão (ex.: `src/persistencia/Conexao.java`):
```java
String url = "jdbc:mysql://localhost:3306/agencia_db";
String user = "root";
String password = "sua_senha";
```

### 4) Executar
- **NetBeans/Ant**: abra o projeto e rode a classe principal (ex.: `AgenciaViagens.java`).  
- **Maven** (se houver `pom.xml`):
  ```bash
  mvn clean package
  java -jar target/<artefato>.jar
  ```

---

## 📁 Estrutura sugerida
```
/README.md
/LICENSE
/.gitignore
/.github/workflows/build.yml
/src/agencia/
  Cliente.java
  Destino.java
  Pacote.java
  Reserva.java
  AgenciaViagens.java
/sql/agencia.sql
nbproject/            # se NetBeans/Ant
pom.xml               # se Maven
```
> Mantenha apenas **código-fonte e configs** no versionamento. Binários e zips devem ir nas **Releases**.

---

## 🧪 CI (GitHub Actions)
Workflow de exemplo para compilar com **Ant** (se `build.xml` existir) ou **Maven** (se `pom.xml` existir) e validar o build em **Java 8** e **17**.

---

## 📝 Licença
Distribuído sob a licença **MIT**. Veja `LICENSE` para detalhes.

# 📦 Sistema de Locação de Aparelhos para Festas

Este projeto implementa um sistema distribuído cliente-servidor em Java, onde clientes podem consultar, alugar e visualizar aparelhos de festa remotamente. A comunicação entre processos é feita via **Sockets TCP**, com dados trafegando no formato **JSON** usando a biblioteca **Gson**.

---

## ✅ Funcionalidades

- 👤 Cadastro de clientes e solicitação de locação
- 📦 Controle de estoque automático após cada locação
- 🔍 Consulta de aparelhos disponíveis
- 📝 Histórico de empréstimos
- 📡 Comunicação TCP entre cliente e servidor
- 🧠 Representação externa de dados com JSON (via Gson)

---

## 🧠 Estrutura do Projeto

```LOCA-O_DE_APARELHOS/
├── bin/                         # Arquivos .class compilados
├── lib/                         # Biblioteca Gson
├── src/
│   ├── network/                 # Comunicação TCP cliente-servidor
│   │   ├── ClienteConsole.java
│   │   ├── ClienteTCP.java
│   │   └── ServidorTCP.java
│   ├── pojo/                    # Classes POJO (dados e modelos)
│   │   ├── Aparelho.java
│   │   ├── Cliente.java
│   │   ├── Gerador.java
│   │   ├── Mesa.java
│   │   ├── Palco.java
│   │   ├── Talher.java
│   │   ├── RequisicaoLocacao.java
│   │   └── RespostaLocacao.java
│   ├── service/                 # Lógica de negócio da locação
│   │   ├── Locacao.java
│   │   └── LocacaoImpl.java
│   ├── stream/                  # Streams personalizados (Input/Output)
│   │   ├── GeradorInputStream.java
│   │   └── GeradorOutputStream.java
│   └── teste/                   # Testes do projeto
│       ├── TesteArquivo.java
│       └── TesteSaidaPadrao.java
├── geradores.dat                # Arquivo gerado no teste de stream
├── Trabalho_1_Comunicação entre processos.pdf
---

---

## 🔧 Como compilar e executar

### 1. Compile os arquivos:

```bash
javac -d bin -cp lib/gson-2.8.9.jar src/**/*.java
```

### 2. Inicie o servidor:

```bash
java -cp bin:lib/gson-2.8.9.jar src.network.ServidorTCP
```

### 3. Inicie o cliente em outro terminal:

```bash
java -cp bin:lib/gson-2.8.9.jar src.network.ClienteConsole
```

---

## 📘 Etapas do trabalho implementadas

| Etapa | Descrição | Status |
|-------|-----------|--------|
| 1     | POJOs e modelo de serviço | ✅ Concluído |
| 2     | OutputStream personalizado | ✅ Concluído |
| 3     | InputStream personalizado | ✅ Concluído |
| 4     | Comunicação cliente-servidor com JSON (TCP) | ✅ Concluído |

---

## ✍️ Autor

Arthur Snow – Engenharia de Computação – UFC Quixadá

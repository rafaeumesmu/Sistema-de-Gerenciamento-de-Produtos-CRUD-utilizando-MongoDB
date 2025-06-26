# Projeto Final - Big Data e NoSQL

## Autor: Rafael Severo

Este projeto foi desenvolvido como avaliação final para a disciplina de **Big Data e NoSQL**, ministrada pelo Prof. Klayton R. Castro, no âmbito do curso de pós-graduação do IDP.

---

### 1. Propósito da Solução

O propósito deste trabalho é desenvolver o protótipo de uma solução de Big Data e NoSQL, aplicando de forma prática os fundamentos teóricos e as ferramentas exploradas em laboratório. A solução implementada é um sistema de gerenciamento de produtos (CRUD - Criar, Ler, Atualizar, Deletar), que utiliza um banco de dados NoSQL para persistência de dados e uma interface gráfica para interação do usuário. 
Este projeto atende à sugestão do **Tema 4: Aplicações com Bases de Dados Não Relacionais**.

### 2. Arquitetura da Solução

A solução foi projetada com uma arquitetura de duas camadas, visando critérios de portabilidade e escalabilidade, com uma clara separação de responsabilidades: 

* **Backend (Camada de Dados):**
    * Desenvolvido em Python, utiliza a biblioteca `pymongo` como driver para se comunicar com o banco de dados **MongoDB**.
    *  módulo `crud.py` centraliza toda a lógica de negócio e as operações de persistência de dados, incluindo as operações de criação, leitura, atualização e deleção de produtos.
* **Frontend (Camada de Apresentação):**
    * Uma interface gráfica web interativa desenvolvida com a biblioteca **Streamlit**. 
    * O arquivo `app.py` constrói a interface visual, que inclui formulários para entrada de dados e tabelas para exibição.
    * Permite que o usuário realize todas as operações CRUD de forma intuitiva, sem a necessidade de conhecimento técnico sobre o banco de dados.

### 3. Tecnologias Utilizadas

* **Linguagem de Programação:** Python
* **Banco de Dados:** MongoDB (Banco de Dados NoSQL orientado a documentos)
* **Interface Gráfica:** Streamlit
* **Driver do Banco de Dados:** Pymongo
* **Manipulação de Dados:** Pandas

### 4. Instruções de Instalação e Execução

Para testar a aplicação, siga os passos abaixo.

**Pré-requisitos:**

* Python 3.8 ou superior
* MongoDB Community Server instalado e configurado.

**Passo a Passo:**

1.  Faça o download dos arquivos `app.py` e `crud.py` para uma mesma pasta no seu computador.

2.  Abra um terminal na pasta do projeto e instale as dependências necessárias com o seguinte comando:
    ```bash
    pip install streamlit pymongo pandas
    ```

3.  **IMPORTANTE:** Certifique-se de que o serviço do MongoDB esteja em execução. Se ele não foi instalado como um serviço do Windows, será necessário iniciá-lo manualmente através do comando `mongod.exe`.

4.  Com o serviço do MongoDB ativo, execute a aplicação Streamlit com o comando:
    ```bash
    streamlit run app.py
    ```
5.  A aplicação será aberta automaticamente em seu navegador no endereço `http://localhost:8501`.



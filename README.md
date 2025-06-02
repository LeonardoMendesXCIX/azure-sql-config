# Desafio de Projeto: Configuração de Instância de Banco de Dados no Azure

## Sobre o Projeto

Este repositório foi desenvolvido como parte do desafio prático da DIO, com o objetivo de documentar o processo de configuração de uma instância de Banco de Dados no **Microsoft Azure**. 

Aqui você encontrará:

- Resumos e anotações;
- Dicas práticas;
- Capturas de tela do processo;
- Exemplos de comandos SQL para testes.

---

## Etapas Realizadas

1. Criação da conta no **Microsoft Azure**.
2. Acesso ao portal do Azure.
3. Criação da instância de Banco de Dados SQL.
4. Definição dos parâmetros:
   - Nome do banco de dados;
   - Nome do servidor;
   - Região;
   - Usuário e senha administrador.
5. Configuração das regras de firewall para permitir conexões externas.
6. Teste de conexão via **Azure Query Editor** e/ou ferramentas como **SSMS**, **DBeaver** ou **Azure Data Studio**.
7. Execução de comandos SQL para validação.
8. Documentação no GitHub.

---

## Tecnologias Utilizadas

- **Microsoft Azure**
- **Azure SQL Database / SQL Managed Instance**

---

## Anotações e Dicas Importantes

### Criação do Banco no Azure

- Na etapa de criação, opte por uma **região geográfica próxima** para melhorar a performance.
- A camada de preço pode ser ajustada posteriormente. Para fins de estudo, escolha a camada gratuita ou de menor custo.

### Configuração de Acesso (Firewall)

- É obrigatório liberar seu **IP público** para acessar o banco fora do Azure.
- Habilitar a opção **"Permitir que os serviços do Azure acessem este servidor"** ajuda em testes rápidos dentro da nuvem.

### Boas Práticas

- Guarde bem as credenciais: nome do servidor, login e senha.
- Use o **Azure Query Editor** para executar comandos SQL diretamente do navegador, sem necessidade de ferramentas externas.
- Para conexões locais, recomendo o uso de:
  - **SQL Server Management Studio (SSMS)**;
  - **DBeaver**;
  - **Azure Data Studio**.

---

## Estrutura do Repositório

```
azure-sql-config/
│
├── README.md
└── /docs
    └── comandos-sql-teste.md
```

---

## Comandos SQL de Teste

Exemplos de comandos que podem ser executados após a criação do banco para validar sua conexão:

```sql
-- Criando uma tabela simples
CREATE TABLE Clientes (
    ID INT PRIMARY KEY IDENTITY,
    Nome NVARCHAR(100),
    Email NVARCHAR(100)
);

-- Inserindo dados
INSERT INTO Clientes (Nome, Email)
VALUES ('Leonardo Mendes', 'leonardo@email.com');

-- Consultando dados
SELECT * FROM Clientes;

-- Atualizando dados
UPDATE Clientes SET Email = 'novoemail@email.com' WHERE Nome = 'Leonardo Mendes';

-- Deletando dados
DELETE FROM Clientes WHERE Nome = 'Leonardo Mendes';
```

O arquivo completo com esses comandos está na pasta [`/docs`](./docs/comandos-sql-teste.md).

---

## Conclusão

Este projeto foi uma excelente oportunidade para colocar em prática os conhecimentos adquiridos sobre serviços em nuvem e bancos de dados no **Microsoft Azure**, além de fortalecer minhas habilidades na utilização do **GitHub** para documentação técnica.

---

## 🧠 Autor

**Leonardo Mendes**  
- 💼 [LinkedIn](https://www.linkedin.com/in/leonardobelodasilvamendes/)  
- 💻 [GitHub](https://github.com/LeonardoMendesXCIX)  
- 📸 [Instagram](https://www.instagram.com/99k.04.23/)  

---
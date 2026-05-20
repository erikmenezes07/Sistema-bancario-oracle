# Sistema-bancario-oracle
Projeto Disciplina de Banco de Dados Uninassau

# Diagrama Entidade Relacionamento (DER)

```mermaid
erDiagram

    CLIENTE ||--o{ CONTA : possui
    CONTA ||--o{ MOVIMENTACAO : realiza
    CONTA ||--o{ LOG_OPERACOES : gera

    CLIENTE {
        NUMBER ID_CLIENTE PK
        VARCHAR2 NOME
        VARCHAR2 CPF
        VARCHAR2 TELEFONE
        VARCHAR2 EMAIL
    }

    CONTA {
        NUMBER ID_CONTA PK
        NUMBER ID_CLIENTE FK
        NUMBER SALDO
    }

    MOVIMENTACAO {
        NUMBER ID_MOVIMENTACAO PK
        NUMBER ID_CONTA FK
        VARCHAR2 TIPO_MOVIMENTACAO
        NUMBER VALOR
        DATE DATA_MOVIMENTACAO
    }

    LOG_OPERACOES {
        NUMBER ID_LOG PK
        VARCHAR2 USUARIO_BANCO
        VARCHAR2 OPERACAO
        NUMBER ID_CONTA
        DATE DATA_LOG
    }
``TACAO : realiza
```

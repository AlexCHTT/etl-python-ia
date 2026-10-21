# ETL com Python + IA Generativa

Pipeline ETL (Extração, Transformação e Carregamento) em Python que usa IA generativa para criar mensagens personalizadas de marketing para clientes.

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1egIeSG0gwigN4EISxoBR-v_QAZ7RR_Vs?usp=sharing)

## Fluxo

```
usuarios.csv ──► [E] Extract ──► [T] Transform (IA gera mensagem) ──► [L] Load ──► usuarios_com_mensagem.csv
(Nome, Conta, Cartão)                                                   (+ coluna Mensagem)
```

| Etapa | O que faz |
|-------|-----------|
| **Extract** | Lê um CSV de usuários (dados fictícios) com pandas |
| **Transform** | Gera, para cada cliente, uma mensagem sobre investimentos (até 100 caracteres) usando a API do Claude. Sem chave de API, usa uma mensagem-modelo |
| **Load** | Salva o resultado em `usuarios_com_mensagem.csv` |

## Como rodar

1. Clique em **Abrir no Colab** acima (ou envie o `etl.ipynb` para o Google Colab).
2. *(Opcional)* Para usar a IA, adicione o secret `ANTHROPIC_API_KEY` na barra lateral do Colab (🔑) e ative o acesso ao notebook.
3. Execute as células em ordem.

## Tecnologias

Python · pandas · Anthropic API (Claude) · Google Colab

## Observação

Todos os dados são fictícios, apenas para fins educacionais.

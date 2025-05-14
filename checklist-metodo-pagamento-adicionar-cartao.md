# Checklist e Resultados de Teste – Janelas "Método de Pagamento" e "Adicionar Cartão"

**Sprint:** 3  
**Projeto:** Urban Routes – Car Sharing  
**Ambiente testado:** Google Chrome (800x600)

---

## 📋 Método de Pagamento

| # | Descrição da Revisão | Resultado | Bug |
|--|------------------------|-----------|-----|
| 1 | Fechar a janela ao clicar no "X" | Aprovado | — |
| 2 | Fechar a janela ao clicar no botão "cancelar" | Aprovado | — |
| 3 | Campo "vazio" | Aprovado | — |
| 4 | Adicionar um cartão válido para concluir a reserva do veículo | Aprovado | — |
| 5 | Não é possível adicionar mais cartões que o permitido | Aprovado | — |
| 6 | Cartão exibido incorretamente com os quatro últimos dígitos visíveis após adição | Reprovado | [KAN-2](https://gleniofilhoo.atlassian.net/browse/KAN-2) |

---

## 📋 Campo Código

| # | Descrição da Revisão | Resultado | Bug |
|--|------------------------|-----------|-----|
| 1 | Não é permitido adicionar "00" | Reprovado | [KAN-3](https://gleniofilhoo.atlassian.net/browse/KAN-3) |
| 2 | É permitido adicionar "01" | Aprovado | — |
| 3 | É permitido adicionar "02" | Aprovado | — |
| 4 | É permitido adicionar "98" | Aprovado | — |
| 5 | É permitido adicionar "99" | Aprovado | — |
| 6 | Não é permitido adicionar "100" | Reprovado | [KAN-4](https://gleniofilhoo.atlassian.net/browse/KAN-4) |
| 7 | Formato inválido com caracteres especiais "@#%$" | Reprovado | [KAN-5](https://gleniofilhoo.atlassian.net/browse/KAN-5) |
| 8 | Inserção de letras não latinas | Reprovado | [KAN-6](https://gleniofilhoo.atlassian.net/browse/KAN-6) |
| 9 | Inserção de letras latinas | Aprovado | — |

---

## 📋 Campo Número

| # | Descrição da Revisão | Resultado | Bug |
|--|------------------------|-----------|-----|
| 1 | Campo vazio | Aprovado | — |
| 2 | Letra não latina | Reprovado | [KAN-9](https://gleniofilhoo.atlassian.net/browse/KAN-9) |
| 3 | Letras latinas | Reprovado | [KAN-8](https://gleniofilhoo.atlassian.net/browse/KAN-8) |
| 4 | Menos de 12 dígitos | Reprovado | [KAN-10](https://gleniofilhoo.atlassian.net/browse/KAN-10) |
| 5 | Impossível inserir mais de 12 dígitos | Aprovado | — |
| 6 | Caracteres especiais "@#%$" | Reprovado | [KAN-11](https://gleniofilhoo.atlassian.net/browse/KAN-11) |
| 7 | Apenas números "12 números" | Aprovado | — |
| 8 | Restrições para número: de 999 | Reprovado | [KAN-12](https://gleniofilhoo.atlassian.net/browse/KAN-12) |
| 9 | Restrições para número: até 0000 | Reprovado | [KAN-13](https://gleniofilhoo.atlassian.net/browse/KAN-13) |
| 10 | Aceita "nnnn nnnn nnnn nnnn" | Reprovado | [KAN-14](https://gleniofilhoo.atlassian.net/browse/KAN-14) |

---

## 📋 Integração dos Campos "Número" e "Código"

| # | Descrição da Revisão | Resultado | Bug |
|--|------------------------|-----------|-----|
| 1 | Inserir valores válidos em ambos os campos ativa o botão adicionar | Aprovado | — |
| 2 | Um valor inválido em "número" e válido em "código" mantém botão inativo | Aprovado | — |
| 3 | Um valor inválido em "código" e válido em "número" mantém botão inativo | Reprovado | [KAN-15](https://gleniofilhoo.atlassian.net/browse/KAN-15) |
| 4 | Ambos inválidos → botão inativo | Aprovado | — |
| 5 | Ambos vazios → botão inativo | Aprovado | — |
| 6 | Preencher com caracteres não latinos → botão inativo | Reprovado | [KAN-16](https://gleniofilhoo.atlassian.net/browse/KAN-16) |
| 7 | Preencher com letras → botão inativo | Reprovado | [KAN-17](https://gleniofilhoo.atlassian.net/browse/KAN-17) |
| 8 | Preencher com caracteres especiais → botão inativo | Reprovado | [KAN-19](https://gleniofilhoo.atlassian.net/browse/KAN-19) |
| 9 | Inserir valor numérico com caractere especial → botão inativo | Reprovado | [KAN-20](https://gleniofilhoo.atlassian.net/browse/KAN-20) |

---

**Status Geral:** A maioria das regras de validação para inserção de cartão foram testadas e vários bugs foram identificados relacionados a formatos incorretos e ativações incorretas do botão "Adicionar".

---

🧪 Criado por Glenio Filho – Sprint 3 – Urban Routes Web App

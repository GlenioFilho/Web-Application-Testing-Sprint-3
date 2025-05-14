# Casos de Teste – Lógica do Botão "Reservar"

**Sprint:** 3  
**Projeto:** Urban Routes – Car Sharing  
**Ambiente testado:** Google Chrome (800x600)

---

## 📋 Casos de Teste

| ID | Nome do Caso de Teste | Pré-condições | Etapas | Resultado Esperado | Status | Bug |
|----|------------------------|---------------|--------|---------------------|--------|-----|
| t-1 | Verificar a lógica do botão "Reservar" ao preencher todos os campos obrigatórios do formulário | 1. Inserir "East 2nd Street, 601" no campo "DE"  <br> 2. Inserir "1300 1st St" no campo "PARA"  <br> 3. Selecionar "Personal"  <br> 4. Selecionar "car sharing" | 1. Adicionar carteira  <br> 2. Adicionar cartão  <br> 3. Clicar no botão "Reservar" | O botão exibe: "Reservar". Ao clicar, a janela "O carro foi reservado" é exibida com os detalhes da reserva. | Aprovado | — |
| t-2 | Verificar a lógica do botão "Reservar" quando falta a carteira de motorista | Mesmo cenário acima, mas **não adicionar a carteira** | 1. Adicionar cartão  <br> 2. Clicar em "Reservar" | O botão exibe: "Adicionar a carteira de motorista e reservar". Botão inativo. | Aprovado | — |
| t-3 | Verificar a lógica do botão "Reservar" quando falta o método de pagamento | Mesmo cenário, mas **não adicionar cartão** | 1. Adicionar carteira  <br> 2. Clicar no botão | O botão exibe: "Adicionar o método de pagamento e reservar". Botão inativo. | Aprovado | — |
| t-4 | Verificar a lógica do botão "Reservar" com dados **errados no pagamento** | Adicionar **informações inválidas** no campo de pagamento | 1. Adicionar carteira <br> 2. Inserir dados incorretos <br> 3. Clicar em "Reservar" | Botão inativo com mensagem de erro solicitando correção dos dados. | Reprovado | [KAN-22](https://gleniofilhoo.atlassian.net/browse/KAN-22) |
| t-5 | Verificar a lógica do botão "Reservar" com dados **errados na carteira** | Adicionar **dados inválidos da carteira de motorista** | 1. Inserir carteira inválida <br> 2. Adicionar cartão <br> 3. Clicar em "Reservar" | Botão inativo com erro indicando dados inválidos da carteira. | Reprovado | [KAN-23](https://gleniofilhoo.atlassian.net/browse/KAN-23) |
| t-6 | Verificar a lógica do botão "Reservar" com todos os campos preenchidos, mas **endereços removidos** | 1. Preencher todos os campos  <br> 2. Excluir os endereços  <br> 3. Clicar em "Reservar" | O botão exibe: "Adicionar endereços e reservar". A exclusão de endereços não deveria ser permitida após reserva. | Reprovado | [KAN-24](https://gleniofilhoo.atlassian.net/browse/KAN-24) |

---

**Status Geral:** A maior parte da lógica foi validada corretamente, mas foram identificadas falhas graves em cenários com dados inválidos e ações inesperadas no formulário.

---

🧪 Criado por Glenio Filho – Sprint 3 – Urban Routes Web App

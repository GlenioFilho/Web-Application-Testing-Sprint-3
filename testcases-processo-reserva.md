# Casos de Teste – Lógica dos Recursos de Reserva

**Sprint:** 3  
**Projeto:** Urban Routes – Car Sharing  
**Ambiente testado:** Google Chrome (800x600)

---

## 📋 Casos de Teste

| ID | Nome do Caso de Teste | Pré-condições | Etapas | Resultado Esperado | Status | Bug |
|----|------------------------|----------------|--------|---------------------|--------|-----|
| t-1 | Verificar a lógica da reserva ao preencher os campos "De" e "Para" | 1. Acessar a mesa de teste <br> 2. Inserir "East 2nd Street, 601" no campo "DE" <br> 3. Inserir "1300 1st St" no campo "PARA" <br> 4. Escolher modo "Personal" <br> 5. Selecionar compartilhamento de carro | 1. Clicar no botão "Reservar" | Uma janela com o título "O carro foi reservado" deve aparecer no centro da tela, com ícone, endereço do carro, custo da corrida e cronômetro. | Aprovado | — |
| t-2 | Validar o cancelamento da reserva | Mesmo cenário do t-1, com dados válidos | 1. Adicionar carteira <br> 2. Adicionar forma de pagamento <br> 3. Clicar em "Reservar" <br> 4. Clicar em "Cancelar" <br> 5. Confirmar com "Sim" | A corrida foi cancelada. | Reprovado | [KAN-21](https://gleniofilhoo.atlassian.net/browse/KAN-21) |
| t-3 | Validar o não cancelamento da reserva | Mesmo cenário anterior | 1. Adicionar carteira <br> 2. Adicionar forma de pagamento <br> 3. Clicar em "Reservar" <br> 4. Clicar em "Cancelar" <br> 5. Clicar em "Não" | A corrida
****

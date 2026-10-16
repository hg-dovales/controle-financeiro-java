# Sistema de Controle Financeiro em Java

Projeto de controle financeiro familiar em Java, com foco em orçamento mensal, compras parceladas e acompanhamento do dinheiro reservado para despesas futuras.

## Sobre o projeto

Atualmente, organizo as finanças da minha família em uma planilha com receitas, despesas fixas e despesas variáveis, separadas por mês.

Esse processo exige conferir faturas, classificar gastos e atualizar informações manualmente. Além de ser trabalhoso, muitas vezes preciso fazer cálculos para descobrir quanto dinheiro ainda posso gastar, o que aumenta a possibilidade de erros.

O saldo da conta nem sempre representa dinheiro disponível: parte dele pode estar destinada a despesas que ainda serão pagas.

A proposta deste projeto é facilitar o registro das movimentações e automatizar esses cálculos, permitindo acompanhar as finanças com mais clareza.

## Objetivo

Identificar quanto dinheiro está realmente disponível para novas despesas, considerando os compromissos já assumidos, mesmo quando o pagamento acontecer em uma data futura.

O sistema também deverá organizar previsões de gastos, compras parceladas, faturas e valores reservados.

## Objetivos de aprendizagem

Sou estudante de Análise e Desenvolvimento de Sistemas e estou desenvolvendo este projeto para resolver uma necessidade pessoal e construir meu portfólio.

Durante o desenvolvimento, pretendo praticar:

- Programação em Java e raciocínio lógico.
- Análise de requisitos e planejamento de soluções.
- Orientação a objetos.
- Validação de dados e tratamento de erros.
- Testes e debugging.
- Boas práticas e refatoração.
- Versionamento com Git e GitHub.

## Funcionalidades planejadas

- Cadastrar receitas e despesas.
- Classificar despesas por categoria, data e forma de pagamento.
- Cadastrar despesas recorrentes com frequência definida.
- Comparar valores previstos e realizados.
- Diferenciar despesas pagas por Pix e cartão.
- Acompanhar compras parceladas e parcelas pagas e pendentes.
- Organizar faturas conforme o fechamento e o vencimento dos cartões.
- Controlar reservas destinadas ao pagamento de parcelas.
- Acompanhar reserva de emergência e previdência privada.
- Mostrar o saldo das contas e o saldo disponível para gastar.
- Consultar movimentações por período e categoria.
- Manter os registros salvos após encerrar o programa.

A integração com transações bancárias é uma possibilidade futura, ainda sujeita a análise de viabilidade.

## Regras de negócio definidas

### Compras parceladas

- O valor integral da compra compromete o orçamento do mês em que ela foi realizada.
- A reserva inicial destinada à compra deve corresponder ao seu valor integral.
- O dinheiro reservado será utilizado para pagar as parcelas.
- O pagamento de uma parcela reduz a reserva e a dívida restante, sem descontar novamente o valor do orçamento disponível.
- A transferência para a caixinha não representa uma segunda despesa.

### Previsões de gastos

- Os valores previstos já comprometem o saldo disponível.
- Para despesas com uma cobrança única, como a conta de luz, o valor real substitui a previsão quando for conhecido.
- Para categorias com várias compras, como supermercado, a previsão permanece como compromisso mínimo durante o mês.
- Se os gastos de uma categoria ultrapassarem a previsão, o valor comprometido passa a acompanhar o total gasto.

## Exemplo de funcionamento esperado

Uma compra de R$ 900,00 é realizada em outubro, em três parcelas de R$ 300,00, com primeiro vencimento em novembro.

- Em outubro, os R$ 900,00 comprometem o orçamento e são separados para pagar a compra.
- Em novembro, o pagamento da primeira parcela reduz a reserva para R$ 600,00.
- Em dezembro, o pagamento da segunda parcela reduz a reserva para R$ 300,00.
- Em janeiro, a última parcela é paga, encerrando a reserva destinada à compra.

Esses pagamentos não comprometem novamente o orçamento, pois o valor integral já foi considerado no mês da compra.

Este exemplo descreve o comportamento planejado. A funcionalidade ainda não foi implementada.

## Tecnologia e interface inicial

A primeira versão será desenvolvida em Java, com interação pelo console.

A forma de armazenamento dos dados e as demais ferramentas serão definidas durante o planejamento.

## Status

**Em planejamento — análise de requisitos.**

Ainda não há uma versão executável. As funcionalidades descritas representam a visão do sistema completo e serão desenvolvidas em etapas.

## Próximas etapas

1. Consolidar os requisitos e os exemplos de funcionamento.
2. Definir o escopo da versão 0.1.
3. Modelar os dados e planejar a lógica.
4. Configurar o projeto Java.
5. Implementar, testar e revisar uma funcionalidade por vez.

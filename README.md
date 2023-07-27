# Análise de dados - Cancelamento de clientes
 
# Objetivo

Este projeto foi desenvolvido como parte de um intensivo de Python, com foco na análise de dados. O objetivo principal é investigar as razões do cancelamento de serviços por parte dos clientes de uma determinada empresa. O intuito é identificar as principais causas desses cancelamentos, permitindo assim a implementação de estratégias eficazes para minimizar a taxa de desistência. Além de obter insights valiosos que possam orientar as tomadas de decisões da empresa.

**Enunciado →** Você foi contratado por uma empresa com mais de 800 mil clientes para um projeto de Dados. Recentemente a empresa percebeu que da sua base total de clientes, a maioria são clientes inativos, ou seja, que já cancelaram o serviço.

Precisando melhorar seus resultados ela quer conseguir entender os principais motivos desses cancelamentos e quais as ações mais eficientes para reduzir esse número.

# Como funciona

O código recebe um arquivo da base de dados dos cancelamentos dos clientes da empresa, possuindo dados de todos os 800 mil clientes e se cancelaram ou não. A base possui informações como:

- ID do cliente
- Idade
- Sexo
- Tempo como cliente
- Frequência de uso do serviço
- Ligações do CallCenter
- Dias de atraso do pagamento
- Assinatura
- Duração do contrato
- Total gasto pelo cliente
- Meses desde a última interação
- Se cancelou ou não (1.0 pra sim e 0.0 pra não)

Após a leitura dos dados, o código trata os dados removendo colunas inúteis para a análise e valores NA, depois calcula a quantidade de clientes que cancelaram e sua porcentagem, tendo aproximadamente 56.7% de cancelamento. Após isso, fiz gráficos e insights para descobrirmos quais os principais motivos do cancelamento, e com algumas descobertas, vimos que a taxa de cancelamento diminuiu com a retirada dos problemas.

# **Principais motivos do cancelamento**

Com base na análise dos dados, descobri as principais causas do cancelamento dos serviços da empresa:

1. Forma de Pagamento: Observei que a forma de pagamento mensal é um fator predominante no cancelamento de assinaturas. É possível que essa modalidade de pagamento possa levar a uma maior inconstância por parte dos assinantes, resultando em um maior número de cancelamentos.

2. Atraso no Pagamento: Descobri que assinantes com mais de 20 dias de atraso no pagamento tendem a cancelar suas assinaturas em uma taxa mais elevada. Este comportamento pode ser um indicativo de dificuldades financeiras, levando ao cancelamento.

3. Contato do Call Center: Assinantes que receberam mais de 5 ligações do call center também demonstraram uma tendência maior ao cancelamento. Este fato sugere que um número excessivo de chamadas pode ser contraproducente e resultar em insatisfação.

Vale ressaltar que após uma implementação de estratégias para lidar com esses problemas identificados, haveria uma redução significativa na taxa de cancelamento. Atualmente, a taxa de cancelamento está em 56.7%, e com as medidas necessárias para a resolução, a taxa de cancelamento diminuiria para 12.1%, o que representaria uma melhora expressiva na retenção de assinantes.

# Detalhes

- Por conta da grande quantidade de gráficos, o arquivo do código ficou grande com mais de 100 Mb, e por isso tive que usar o Git Large File Storage (*LFS*) para postar o projeto, já que o GitHub não permite arquivos acima de 100 Mb.
- Lembre-se de deixar o arquivo da base de dados na mesma pasta do arquivo do código para o Python reconhecer, com o nome de “cancelamentos.csv”.
- As bibliotecas usadas foram: Pandas e Ploty.
- Caso você encontre um erro sobre nbformat quando for criar gráficos, pode fazer a instalação desse recurso no terminal do programa (pip install nbformat) e reinicie o kernel ou a IDE. Dessa forma vai conseguir criar os gráficos normalmente.

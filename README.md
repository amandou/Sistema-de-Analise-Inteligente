# 📊 Banco de Dados de Análise de Crédito (SQL)

Este repositório contém o processo de modelagem física e carga de dados de um banco de dados relacional baseado no dataset clássico *German Credit Data*. 

O banco foi desenvolvido inteiramente em **MySQL** utilizando nomenclatura em **Português Brasileiro (pt-BR)** e seguindo as melhores práticas de escrita SQL (padrão snake_case, sem espaços e sem caracteres especiais).

## 🛠️ Tecnologias Utilizadas
- **SGBD:** MySQL 8.0+
- **Linguagem:** SQL
- **Processo ETL:** Python (utilizado para a limpeza e tradução a partir do arquivo bruto)

## 📁 Estrutura do Projeto
- /data: Contém o arquivo original bruto em formato .csv.
- /sql: Script .sql contendo os comandos de CREATE DATABASE, CREATE TABLE e as inserções estruturadas de todas as 1.000 linhas do dataset original.

## 📝 Dicionário de Dados Traduzido

- **status_conta_corrente - Categoria do status da conta corrente do cliente**

1: Sem conta corrente
2: … < 0 DM 
3: 0 <= … < 200 DM 
4: … >= 200 DM / salário por pelo menos 1 ano
 
- **duracao_meses - Duração do crédito solicitado em meses**


- **historico_credito - Histórico de pagamento de créditos anteriores**

0: Atraso no pagamento no passado; 
1: Conta crítica/outros créditos em outros bancos;
2: Nenhum crédito obtido/todos os créditos pagos em dia;
3: Créditos existentes pagos em dia até o momento;
4: Todos os créditos neste banco pagos em dia.

- **proposito - Motivo/finalidade da solicitação do crédito**
 
0: outros
1: carro (novo)
2: carro (usado)
3: móveis/equipamentos
4: rádio/televisão
5: eletrodomésticos
6: consertos
7: educação
8: férias
9: requalificação profissional
10: negócios

- **valor_credito - Valor total do crédito solicitado**

 
- **poupanca_investimento - Saldos em contas de poupança/investimentos** 
 
1: desconhecido/sem conta poupança
2: … < 100 DM 
3: 100 <= … < 500 DM 
4: 500 <= … < 1000 DM 
5: … >= 1000 DM

- **tempo_emprego_atual - Tempo de permanência no emprego atual**
 
1: desempregado
2: < 1 ano 
3: 1 <= … < 4 anos 
4: 4 <= … < 7 anos 
5: >= 7 anos

- **taxa_parcelamento_renda - Percentual de parcelamento em relação à renda disponível**

1 : >= 35
2 : 25 <= … < 35
3 : 20 <= … < 25
4 : < 20

- **status_pessoal_sexo - Estado civil e sexo do cliente**
 
1: masculino: divorciado/separado;
2: feminino:  não solteira ou masculino: solteiro;
3: masculino: casado/viúvo;
4: feminino: solteiro

- **outros_fiadores - Presença de fiadores ou cossignatários**

1: nenhum
2: correquerente
3: fiador

 - **residencia_atual_desde - Tempo em que reside no endereço atual**

1 : < 1 ano 
2 : 1 <= … < 4 anos 
3 : 4 <= … < 7 anos 
4 : >= 7 anos

- **propriedade - Bens e ativos que o cliente possui (ex: imóveis)**

1: desconhecido / sem propriedade
2: carro ou outro
3: cooperativa de crédito imobiliário, poupança/seguro de vida
4: imóvel

- **idade - Idade do cliente** 

- **outros_planos_parcelamento - Outros parcelamentos ativos (bancos, lojas, etc.)** 

1: banco
2: lojas
3: nenhum

- **habitação - Tipo de moradia (própria, alugada, etc.)**

1: de graça
2: para alugar
3: próprio

- **numero_creditos_existentes - Quantidade de créditos ativos neste banco**
 
1 : 1
2 : 2-3
3 : 4-5
4 : >= 6

- **trabalho - Categoria de ocupação profissional**
 
1: Desempregado/não qualificado - não residente
2: Não qualificado - residente
3: Empregado qualificado/funcionário público
4: Gerente/autônomo/empregado altamente qualificado

- **dependentes - Número de dependentes financeiros**

1 : 3 ou mais
2 : 0 a 2

- **telefone - Se o cliente possui telefone fixo registrado**

1: não
2: sim (sob o nome do cliente)

- **trabalhador_estrangeiro - Se o cliente é um trabalhador estrangeiro** 
 
1: sim
2: não

- **risco_credito - Variável alvo**

0: ruim
1: bom

--------------------------------------------------------------------------------------------------------


# Análise Exploratória de Vendas — Superstore

## Objetivo
Realizar uma análise exploratória dos dados de vendas da Superstore, com foco em **estatística descritiva**, **limpeza de dados**, **criação de features de negócio** e **validação de consistência**, visando compreender padrões de vendas e comportamento por categoria.

## Dataset
- **Fonte:** Superstore Dataset  
- **Registros:** ~9.800  
- **Granularidade:** item por pedido  
- **Principais variáveis:**
  - `Sales`
  - `Order Date`, `Ship Date`
  - `Order ID`
  - `Category`, `Segment`

O dataset não contém informações de custo ou lucro, o que limita análises financeiras mais profundas, como margem de lucro.

## Limpeza e Preparação dos Dados
As seguintes etapas de data cleaning foram realizadas:

- Conversão das colunas de data para o formato `datetime`, considerando o padrão dia/mês/ano.
- Verificação de valores inválidos ou inconsistentes em vendas.
- Identificação de valores ausentes em datas de envio.
- Inspeção geral das variáveis numéricas e categóricas.
Pedidos sem data de envio foram mantidos com valores ausentes no tempo de entrega, evitando suposições incorretas.

## Criação de Features de Negócio
Foram criadas features derivadas para enriquecer a análise:

- **Delivery Time:** diferença, em dias, entre a data do pedido e a data de envio.
- **Order Total:** valor total de cada pedido, calculado a partir da soma das vendas por `Order ID`.
- Features temporais auxiliares para análise de comportamento ao longo do tempo.

## Validação das Features
As features criadas passaram por validações de consistência, incluindo:

- Verificação de tempos de entrega negativos ou inconsistentes.
- Análise da distribuição do tempo de entrega para identificação de outliers.
- Confirmação de que cada pedido possui um único valor de `Order Total`.
- Testes de coerência matemática entre agregações e valores originais.

Essas validações garantem confiabilidade nas análises realizadas.

## Análise Exploratória
As principais análises exploratórias incluem:

- Estatísticas descritivas da variável `Sales`.
- Análise de distribuição de vendas (histogramas e boxplots).
- Comparação do comportamento de vendas entre categorias.
- Avaliação da variabilidade e presença de outliers por categoria.

## Principais Insights
- A variável **Sales** apresenta forte assimetria positiva, com grande concentração de valores baixos.
- A **mediana** se mostrou mais representativa que a média devido à presença de outliers.
- A categoria **Technology** concentra as maiores vendas e maior variabilidade.
- O tempo de entrega apresenta padrão relativamente estável, com poucos casos extremos.
  
## Limitações
- Ausência de dados de custo ou lucro impossibilita análises de margem.
- Alguns pedidos não possuem data de envio.
- A análise é descritiva e não inclui modelos preditivos.
  
## Próximos Passos
- Análise de vendas por região e segmento.
- Exploração de sazonalidade ao longo do tempo.
- Construção de modelos preditivos simples como extensão do projeto.

## Tecnologias Utilizadas
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

## ▶️ Como Executar
1. Clone o repositório.
2. Abra o notebook da etapa de sua escolha em um ambiente Jupyter ou Google Colab.
3. Faça o download do dataset **Superstore** e ajuste o caminho do arquivo, se necessário.
4. Execute o notebook do início ao fim.

### Resultado Final
Este projeto demonstra habilidades em **análise exploratória de dados**, **engenharia de features** e **validação de consistência**, seguindo boas práticas aplicadas em projetos reais de dados.

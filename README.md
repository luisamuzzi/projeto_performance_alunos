# **Projeto Análise Estatística da Performance de Alunos**

### Resumo

Este projeto analisou dados de performance de alunos de uma escola na disciplina de matemática a pedido do time pedagógico. O objetivo da análise foi verificar se a implementação de um curso preparatório poderia melhorar o desempenho dos alunos nas avaliações de matemática. Para coletar dados para análise, o curso preparatório foi disponibilizado gratuitamente para uma amostra de alunos. Com base na análise estatística dos resultados do teste, foi possível prover informações para subsidiar o negócio na decisão de expandir o curso preparatório para todos os alunos da escola.

A análise realizada permitiu verificar que a implementação do curso preparatório geraria um aumento entre 3,69 e 7,55 pontos na média de notas; um aumento entre 6,7 e 18,3 pontos percentuais no percentual de aprovações em matemática; e um aumento entre 14,2% e 14,7% no lucro da escola. Assim, recomendou-se a implementação do curso preparatório na escola.

Os produtos da análise foram uma apresentação de negócios com os principais insights obtidos e um notebook comentado em Python contendo toda a análise estatística e de custo-benefício realizada.

[Apresentação - Performance alunos]()

Leia mais sobre o projeto abaixo.

### Índice

- [1. Contexto](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#1-contexto)
- [2. Premissas assumidas para a análise](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#2--premissas-assumidas-para-a-an%C3%A1lise)
- [3. Ferramentas utilizadas](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#3-ferramentas-utilizadas)
- [4. Estratégias de solução](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#4-estrat%C3%A9gias-de-solu%C3%A7%C3%A3o)
- [5. O produto final do projeto](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#5-o-produto-final-do-projeto)
- [6. Principais insights de dados](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#6-principais-insights-de-dados)
- [7. Conclusão](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#7-conclus%C3%A3o)
- [8. Próximos passos](https://github.com/luisamuzzi/projeto_performance_alunos/tree/main?tab=readme-ov-file#8-pr%C3%B3ximos-passos)

### 1. Contexto

O time pedagógico de uma escola gostaria de saber se a implementação de um curso preparatório pode melhorar o desempenho dos alunos nas avaliações. Para coletar dados para análise, o curso preparatório foi disponibilizado gratuitamente para uma amostra de alunos. Com base nos resultados do teste, o negócio irá decidir se o curso deve ou não ser expandido para todos os alunos da escola. Inicialmente, o foco da análise deve ser nas notas de matemática.

Objetivos da análise:

- Verificar se há evidência estatística de que a média das notas de matemática dos alunos que fizeram o curso preparatório é maior do que daqueles que não fizeram.

- Verificar se há evidência estatística de que a proporção de alunos aprovados em matemática (nota ≥ 60) é maior entre os que fizeram o curso preparatório.

- Caso se verifique que a média de notas e a proporção de aprovação são maiores com a aplicação do curso, analisar se o tamanho do efeito é suficientemente relevante para justificar a expansão da oferta do curso preparatório. O negócio considera que o "ganho mínimo" corresponde a um aumento de pelo menos 5 pontos na média de notas e de pelo menos 10 pontos percentuais no percentual de aprovação.

- Estimar o custo-benefício da expansão do curso preparatório para a escola. Os cursos da escola são vendidos por 200 reais cada, exceto o preparatório, que seria vendido por 100 reais; os custos com o curso preparatório são de 50 reais por aluno (material, horas-aula de professor, etc); e alunos aprovados em uma disciplina tem 10% mais probabilidade de se inscreverem em outras matérias.

Utilizou-se Python para tratamento e análise dos dados.

Os principais insights obtidos foram inseridos em uma apresentação de negócios.

### 2.  Premissas assumidas para a análise

1. Ganho mínimo que o negócio espera alcançar com a implementação do curso preparatório: aumento de pelo menos 5 pontos na média de notas e de pelo menos 10 pontos percentuais no percentual de aprovação;
2. Preço de venda do curso preparatório: R$ 100,00 por aluno;
3. Preço de venda dos demais cursos da escola: R$ 200,00 por aluno;
4. Custos com o curso preparatório: R$ 50,00 por aluno (material, horas-aula de professor, etc);
5. Probabilidade de um aluno aprovado se matricular em outro curso da escola: 10%.
6. Os dados utilizados foram obtidos no EBA: https://renatabiaggi.com/eba-estatistica/
7. A imagem utilizada no portfólio foi retirada de: https://storyset.com/

### 3. Ferramentas utilizadas

- Python para a EDA e análise estatística:
    - Pandas
    - Seaborn
    - Matplotlib
    - Scipy
    - Statsmodels
- Canva para a apresentação

### 4. Estratégias de solução

O projeto foi desenvolvido por meio de análises estatísticas, considerando-se as seguintes etapas:

1. Análise exploratória dos dados:
   
    Nessa etapa, os dados foram explorados a fim de entender os tipos de variável, investigar valores únicos, verificar valores ausentes ou nulos, verificar a qualidade dos dados (por exemplo: escrita inconsistente, zeros onde não deveriam existir, unidades inconsistentes) e analisar a distribuição de variáveis categóricas e numéricas.

1. Teste de hipóteses para a diferença das médias de notas dos alunos que fizeram e que não fizeram o curso preparatório:
    
    Nessa etapa, foi aplicado um teste t para a média de duas amostras com desvio padrão populacional desconhecido e amostras independentes após verificação de que os dados atendiam aos pressupostos do teste.
   
3. Teste de hipótese para a diferença de proporções de aprovação dos alunos que fizeram e que não fizeram o curso preparatório:
    
    Nessa etapa, foi aplicado um teste z para a proporção de 2 amostras independentes após verificação de que os dados atendiam aos pressupostos do teste.

4. Análise de custo-benefício da implementação do curso preparatório:

    Nessa etapa, foram estimados os custos e três cenários para o lucro que poderia ser obtido com a implementação definitiva do curso preparatório com base no intervalo de confiança calculado para a diferença entre as proporções de aprovações dos alunos.    

### 5. O produto final do projeto

Apresentação de negócios com os principais insights sobre a implementação do curso preparatório tanto do ponto de vista pedagógico (aumento de notas e aprovações) quanto financeiro (aumento do lucro da escola). Notebook com análise completa dos dados.
        
1. [Apresentação - Performance alunos]().
    
2. [Notebook](performance_alunos.ipynb) contendo a análise completa dos dados.

### 6. Principais insights de dados

**Aumento da média das notas de matemática com a implementação do curso preparatório:**

Há evidências estatísticas de que, para a população, a média de notas de matemática dos alunos que realizaram o curso preparatório é maior que a dos alunos que não realizaram.

Considerando-se o intervalo de confiança para o tamanho do efeito, ou seja, que a diferença entre as médias populacionais, a 95% de confiança, está entre 3,69 e 7,55, o ganho mínimo considerado pelo negócio (aumento de pelo menos 5 pontos na média de notas de matemática) poderia não ser atingido com a expansão do curso preparatório.

Assim, antes de tomar uma decisão sobre a expansão do curso, precisamos verificar também a proporção de aprovados e estimar financeiramente o custo benefício da expansão do curso preparatório.

**Aumento do percentual de aprovações em matemática com a implementação do curso preparatório:**

Há evidências estatísticas de que, para a população, a proporção de aprovados em matemática dos alunos que realizaram o curso preparatório é maior que a dos alunos que não realizaram.

Considerando-se o intervalo de confiança para o tamanho do efeito, ou seja, que a diferença entre as proporções populacionais, a 95% de confiança, está entre 6,7 e 18,3, o ganho mínimo considerado pelo negócio (aumento de pelo menos 10 pontos percentuais nas aprovações em matemática) poderia não ser atingido com a expansão do curso preparatório.

Assim, cabe ao negócio decidir se um aumento em pontos percentuais mais próximo ao limite inferior ainda justificaria a expansão do curso preparatório considerando os ganhos financeiros.

**Estimativa do custo-benefício da expansão do curso preparatório:**

Espera-se um aumento no lucro da escola considerando a expansão do curso preparatório entre 14,2% e 14,7%.

Mesmo considerando o cenário pessimista, o aumento no lucro ainda é significativo. Ainda, o aumento no lucro não é tão diferente considerando os três cenários testados. Logo, mesmo que o aumento no percentual de aprovação fique abaixo dos 10 pontos percentuais almejados pelo negócio, o aumento no lucro compensa a expansão do curso preparatório.

### 7. Conclusão

Foi solicitada uma análise do impacto da implementação de um curso preparatório nas notas e aprovações da disciplina de matemática. Para tanto, analisou-se dados de aplicação do curso para uma amostra de estudantes da escola. O negócio considerava que um ganho mínimo seria uma aumento de pelo menos 5 pontos na média de notas e de pelo menos 10 pontos percentuais no percentual de aprovações em matemática.

Para verificação da diferença entre as médias de notas e percentual de aprovação dos alunos que realizaram e que não realizaram o curso, foram realizados testes de hipóteses. Os testes comprovaram estatísticamente, que a média de notas e percentual de aprovação são maiores para os alunos que realizaram o curso preparatório. No entando, o cálculo do intervalo de confiança para a média e percentual de aprovação demonstrou que o aumento pode estar abaixo do "ganho mínimo" almejado pelo negócio.

Apesar disso, a análise de viabilidade financeira demonstrou que, mesmo no cenário pessimista para o tamanho do aumento do percentual de aprovação, o lucro da escola com a implementação do curso ainda seria significativo (14,2%).

**Impacto do curso preparatório**:
- **Aumento** na média de notas de matemática entre 3,69 e 7,55 pontos.
- **Aumento** no percentual de aprovações em matemática entre 6,7 e 18,3 pontos percentuais.
- **Aumento** no lucro da escola entre 14,2% e 14,7%.

**Recomendações**:
- **Expandir o curso preparatório** para todos os alunos, considerando tanto a evidência de impacto positivo nas notas e aprovações, quanto o aumento no lucro da escola.
- **Monitorar continuamente** os resultados após a expansão, avaliando se os cenários estimados se mantêm.
- **Investigar** o custo benefício da expansão do curso preparatório também para as outras disciplinas da escola, como escrita e leitura.

### 8. Próximos passos

Monitorar a implementação do curso preparatório para verificar se os resultados obtidos condizem com os cenários estimados. 

Verificar a viabilidade e benefícios da expansão do curso preparatório para abranger mais disciplinas da escola além da matemática.


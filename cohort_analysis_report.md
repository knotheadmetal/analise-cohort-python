# Análise de Cohort do Online Retail Dataset

## Introdução

Este projeto tem como objetivo analisar o comportamento de retenção de clientes de uma empresa de varejo online, utilizando a metodologia de análise de cohort. A análise de cohort permite agrupar usuários com base em uma característica comum (neste caso, o mês da primeira compra) e acompanhar o seu comportamento ao longo do tempo. Isso nos ajuda a entender como diferentes grupos de clientes se engajam com o negócio e a identificar tendências de retenção.

## Metodologia

O dataset utilizado é o "Online Retail Dataset" do UCI Machine Learning Repository, que contém dados transacionais de um varejista online do Reino Unido entre 01/12/2010 e 09/12/2011.

As etapas seguidas para a análise foram:

1.  **Preparação e Limpeza dos Dados**: Tratamento de valores ausentes (especialmente `CustomerID`), conversão de tipos de dados, remoção de duplicatas e filtragem de transações inválidas (quantidades e preços negativos/zero).
2.  **Criação das Cohortes**: Cada cliente foi atribuído a uma cohorte com base no mês da sua primeira compra (`CohortMonth`).
3.  **Cálculo do Índice de Cohorte**: Para cada transação, foi calculado o número de meses decorridos desde o `CohortMonth` do cliente (`CohortIndex`).
4.  **Cálculo da Retenção**: A retenção mensal foi calculada como a porcentagem de clientes de uma cohorte que permaneceram ativos (realizaram uma compra) em meses subsequentes, em relação ao tamanho original da cohorte.
5.  **Visualização**: Os resultados foram apresentados em um heatmap, que visualiza a matriz de retenção, facilitando a identificação de padrões.

## Interpretação dos Resultados (Heatmap de Retenção)

O heatmap gerado (`cohort_retention_heatmap.png`) mostra a porcentagem de retenção para cada cohorte ao longo dos meses. As linhas representam o mês da cohorte (mês da primeira compra), e as colunas representam o número de meses desde a primeira compra (índice de cohorte).

**Observações Gerais:**

*   **Queda Inicial Significativa**: A retenção cai drasticamente do mês 0 (mês da primeira compra, sempre 100%) para o mês 1. Por exemplo, a cohorte de Dezembro de 2010 retém apenas 36.6% dos seus clientes no mês seguinte. Isso é um padrão comum em muitos negócios, mas a magnitude da queda sugere que a primeira experiência do cliente ou as estratégias de engajamento pós-compra inicial podem ser melhoradas.
*   **Estabilização Gradual**: Após a queda inicial, a taxa de retenção tende a se estabilizar, embora em níveis relativamente baixos (geralmente entre 15% e 30%). Isso indica que os clientes que permanecem após o primeiro mês têm uma probabilidade maior de continuar ativos por mais tempo.
*   **Variações entre Cohortes**: Algumas cohortes apresentam melhor desempenho de retenção do que outras. Por exemplo, a cohorte de Dezembro de 2010 parece ter uma retenção ligeiramente melhor e mais consistente em comparação com as cohortes de Janeiro ou Fevereiro de 2011 nos primeiros meses. A cohorte de Dezembro de 2010 também mostra um pico de retenção no mês 11 (50.3%), o que pode indicar um comportamento sazonal ou uma campanha específica que reativou esses clientes.
*   **Impacto Sazonal (Dezembro)**: A cohorte de Dezembro de 2010 (mês de festas) demonstra uma retenção inicial mais alta (36.6% no mês 1) em comparação com as cohortes subsequentes (e.g., Janeiro 22.1%, Fevereiro 18.7%). Isso pode ser atribuído a compras de fim de ano, onde os clientes podem estar mais propensos a fazer compras repetidas em um curto período ou a serem presenteados e, posteriormente, se tornarem clientes diretos.
*   **Retenção a Longo Prazo**: A retenção diminui progressivamente ao longo do tempo. Após 6-7 meses, a maioria das cohortes retém menos de 20% dos seus clientes originais. Isso ressalta a importância de estratégias contínuas de engajamento para manter os clientes a longo prazo.

## Sugestões de Negócio

Com base nesta análise de cohort, as seguintes sugestões podem ser consideradas para melhorar a retenção de clientes:

1.  **Foco na Experiência Pós-Primeira Compra**: Dada a alta taxa de churn após o primeiro mês, é crucial otimizar a experiência do cliente imediatamente após a primeira compra. Isso pode incluir:
    *   **Comunicações de Boas-Vindas**: Enviar e-mails ou mensagens personalizadas com dicas de uso do produto, ofertas para a próxima compra ou convites para programas de fidelidade.
    *   **Suporte ao Cliente Proativo**: Oferecer suporte proativo para garantir que os clientes estejam satisfeitos e que quaisquer problemas sejam resolvidos rapidamente.
    *   **Incentivos para Segunda Compra**: Oferecer descontos ou frete grátis para a segunda compra, incentivando a repetição.

2.  **Segmentação e Personalização**: Identificar as características das cohortes com melhor desempenho (como a de Dezembro de 2010) e tentar replicar as condições ou estratégias que levaram a essa retenção. Além disso, segmentar os clientes com base no seu comportamento inicial e personalizar as comunicações e ofertas para cada segmento.

3.  **Programas de Fidelidade e Recompensa**: Implementar ou aprimorar programas de fidelidade que recompensem os clientes por compras repetidas e engajamento contínuo. Isso pode ajudar a manter a retenção em níveis mais altos após os primeiros meses.

4.  **Campanhas de Reengajamento**: Para clientes que estão prestes a se tornar inativos (por exemplo, após 2-3 meses sem compra), lançar campanhas de reengajamento com ofertas especiais, recomendações de produtos personalizadas ou lembretes de itens no carrinho.

5.  **Análise de Causa Raiz para Churn**: Aprofundar a análise para entender por que os clientes estão saindo. Isso pode envolver pesquisas de satisfação, análise de feedback de clientes ou a identificação de padrões em clientes que não retornam (e.g., produtos específicos, canais de aquisição).

6.  **Otimização de Campanhas Sazonais**: Aproveitar o sucesso de cohortes como a de Dezembro de 2010. Entender o que impulsionou a retenção nesse período e aplicar essas lições a outras épocas do ano ou a eventos promocionais.

## Conclusão

A análise de cohort é uma ferramenta poderosa para entender o ciclo de vida do cliente e a eficácia das estratégias de retenção. Embora o dataset mostre uma queda inicial de retenção, há oportunidades claras para melhorias através de intervenções focadas na experiência pós-compra, personalização e programas de fidelidade. Acompanhar essas métricas de retenção de forma contínua é fundamental para o crescimento sustentável do negócio.



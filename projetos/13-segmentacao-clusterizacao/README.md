**Fonte, período e tamanho da coleta:**

> Dados extraídos do TikTok via exportação em CSV, das hashtags/páginas #chic, #thingsifindchic, #thingsifinextremelychic e #chicthings. Total de 754 posts, com datas de publicação entre 06/09/2023 e 27/08/2026.


**As duas variáveis que você criou (a contínua da Parte A e o rótulo da Parte B), com a fórmula/critério de cada uma:**

> Parte A: taxa de engajamento = (likes+comments+shares)/plays. Parte B: 1 se `plays` está no percentil 90 ou acima (corte em 1.100.000 plays), 0 caso contrário — top 10% de alcance definido como "viral".


**As features usadas nas Partes A e B, e quais colunas você descartou por vazamento:**

> > Usadas: author_followers, author_likes, author_videos, hashtag_count, caption_len, is_ad_flag.
> Descartadas por vazamento: likes, comments, shares e plays


**Parte A — resultado:** MAE e R² do modelo bobo, da linear e da árvore. O seu melhor modelo bateu o bobo?

>  Bobo (média): MAE=0,04713, R²=-0,0269. LinearRegression: MAE=0,04381, R²=0,0848. DecisionTree(max_depth=5): MAE=0,04691, R²=-0,0937. 
> A LinearRegression bateu o modelo bobo nas duas métricas, mas por pouco (R² de só 8,5%). A árvore ficou pior que o bobo nas duas métricas, ou seja, as features de autor não tem a melhor capacidade pra prever engajamento post a post.

**Parte B — resultado:** a matriz de confusão e uma leitura: a favor de quem o modelo erra?

> Threshold 0,5 — matriz [[133,1],[17,0]]: Precision=0,000, Recall=0,000, F1=0,000. O modelo nunca classifica nenhum post como viral; erra 100% a favor da classe majoritária (não-viral), por causa do desbalanceamento (só ~11% dos posts são virais). 
> Threshold 0,10 — matriz [[68,66],[5,12]]: Precision=0,154, Recall=0,706, F1=0,253. Com o corte mais baixo, o modelo passa a errar a favor de "viral": pega 12 dos 17 virais reais, mas gera muitos falsos positivos (66). 

**Parte C — resultado:** quantos segmentos, como você escolheu `k`, e a descrição de cada segmento (uma frase com número).

> 3 segmentos (k=3), escolhido por trade-off: a silhueta era mais alta em k=2 (~0,74), mas isso só isolava 9 outliers extremos; k=3 manteve silhueta razoável (~0,37) com segmentos mais informativos. 
> Segmento A (86,5% dos autores): contas pequenas/médias (~32 mil seguidores em média), maior engajamento médio (16%) e mais hashtags por post (4,3). 
> Segmento B (12,4% dos autores): contas grandes (~533 mil seguidores), engajamento mais baixo (12%) e menos hashtags por post (2,1). 
> Segmento C (1,1% dos autores, 7 contas): mega-influenciadores (quase 2 milhões de seguidores em média), grupo pequeno demais pra conclusões estatísticas robustas. 

**Uma conclusão que os seus dados sustentam** (sem extrapolar para além da sua coleta):

> Os resultados mostram que os vídeos com mais visualizações não necessariamente representam o que os usuários do TikTok consideram “chic”. A análise mostrou que as características dos autores tiveram pouca relação com o desempenho dos posts e também identificou diferentes perfis de criadores dentro da base. Dessa forma, o número de visualizações pode indicar quais conteúdos tiveram maior alcance, mas não é suficiente para dizer quais representam melhor a percepção dos usuários sobre o que é “chic”. Por isso, para entender essa percepção, seria necessário considerar outros aspectos dos posts além do alcance.


**Revisão por pares:** nome do colega **da turma** que revisou, o que ele apontou, e o que você mudou (ou por que não mudou).

> Rafaella Cruz - Sugestão: deixar algumas explicações mais diretas, explicar melhor o que os resultados significam para a pesquisa, destacar melhor a diferença entre visualização e representatividade. O que mudei: simplifiquei algumas partes e deixei a conclusão mais clara e relacionada à pergunta inicial.


**Declaração de uso de IA:** ferramenta usada, em que trecho ou decisão, e o que você conferiu ou alterou depois (mesmo que seja "não usei IA nesta entrega"). Lembre: nesta entrega, IA não pode ser usada para gerar o código de análise.

> Utilizei a IA para corrigir códigos que estavam com algum tipo de problema e para tirar dúvidas sobre alguns conceitos específicos, mais pro final da análise pedi alguns insights para além do que eu tinha observado para deixar bem completo.
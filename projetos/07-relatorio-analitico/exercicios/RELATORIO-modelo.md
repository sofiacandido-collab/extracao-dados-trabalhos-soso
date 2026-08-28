# [Analise do significado social do que é considerado chique pelos usuários do Tik Tok.]

## Pergunta

> O que os usuários do Tik Tok entendem como chique?

## Dados

Fonte: Tik Tok 
Período coletado - Início: 2023-09-06 18:25:59
Fim: 2026-08-27 12:19:47

Tamanho da amostra: 754 posts
Limites conhecidos da coleta: Muitas hashtags que tinham o único propósito de subir o engajamento do vídeo (fyp, target audience, etc)  


## Método

>A partir da extração dos vídeos, comecei removendo as hashtags duplicadas, a partir disso calculei a taxa de engajamento com base na quantidade de postagens com essa hashtag e curtidas médias. Entretanto, inicialmente, encontrei um obstáculo na observação, já que ele analisava vídeos com uma visualização apenas, dessa maneira coloquei um filtro para ele analisar somente os vídeos com mais de 10 vídeos. Assim, foi possível uma investigação mais apurada do tema. Em seguida, criei um gráfico analisando as 20 hashtags com maior engajamento entre a amostra. O filtro das hashtags é: df_hashtags = df_hashtags[df_hashtags.groupby("hashtags")["id"].transform("count") >= 10].

## Achados

Liste cada achado como uma frase apoiada num número, uma linha de tabela ou um gráfico específico. Anexe ou referencie a tabela (`dados/resumo_hashtags.csv`) e o(s) gráfico(s) (`dados/grafico_relatorio.png` ou outro nome que você tenha usado).

- Atualmente, a melhor forma de visualização adotada por criadores de conteúdo sobre estéticas é o uso de moodboards, como pode ser vista estando em primeiro lugar com uma taxa de engajamento médio de 20%
- O conceito da palavra chic pelos usuários da plataforma está muito relacionada com o nicho de vestuário, sendo constantemente anexado com inspirações de roupas (16%), estilos (18%), moda (16%) e elegância (17%).
- Além disso, o Pinterest é a principal fonte de conteúdo chics para essas pessoas.


## Limitações

O que os dados **não** permitem concluir. Seja específico desta coleta, não genérico.

- Os dados não me permitem exatamente concluir o que todos os usuários entendem como coisas chiques. E sim, uma visão mais generalizada dessa configuração por meio de termos como style, niche, inspo.
- Não consigo saber qual estilo de roupa é considerado mais elegante.
- Presença de hashtags genéricas, como fyp, fy, target audience.


## Recomendações

O que fazer a partir disso. Para cada recomendação, indique de qual achado específico ela depende.

- Filtrar mais hashtags desnecessárias.
- Aumentar a quantidade da amostra.
- Verificar quais hashtags estão sendo agrupadas juntas.

## Revisão por pares

**Revisado por: Gabi Dorle**

**Comentários recebidos:**

>Aprofundar as limitações para uma melhor compreensão. Aumentar o número de hashtags analisadas no gráficod e 10  para 15.

**O que mudou no relatório por causa da revisão (ou por que nada mudou):**

> Eu mudei as limitações, pois concordei que dessa maneira a comunicação fica mais clara. Alterei a quantidade de tags para monatge do gráfico.

## Declaração de uso de IA

Ferramenta usada, em que trecho ou decisão desta entrega, e o que você conferiu ou alterou depois do resultado gerado. Se não usou IA, registre isso também. Nesse trabalho, está proibido usar IA para gerar códigos. 

> Utilizei como ferramenta de ajuda para compreender melhor os erros nos códigos e assim, conserta-los de forma eficiente. 

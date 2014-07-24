TopicModelppt
========================================================
author: Manoel Galdino
date: 22/07/2014
T�pic Models - Introdu��o

Topic Model - Introdu��o
========================================================
O que � a modelagem estat�stica de t�picos?

- Para entendermos a intui��o da LDA come�emos com um
exemplo fict�cio de 5 frases
- O exemplo foi criado por mim e n�o tem an�lise
estat�stica nenhuma.
- mas reflete o esp�rito da LDA


Exemplo (adapatado de E. Chen)
========================================================

- Gosto de Cerveja e Batata Frita
- Tamb�m curto tomar cerveja bem gelada com calabresa
- Corinthians e CSA s�o meus times do cora��o
- Meu irm�o torce pro Botafogo e CSA.
- Curto tomar uma vendo jogo do Corinthians.


Latent Dirichlet Allocation (LDA)
========================================================
Se LDA for inferir 2 t�picos para essas frases:

- Frases 1 and 2: 100% T�pico A
- Frases 3 and 4: 100% T�pico B
- Frase 5: 40% T�pico A, 60% T�pico B
- T�pico A: 30% cerveja, 15% Calabresa, 10% Batata, 10% Frita, � (e ent�o podemos concluir que se trata de comida)
- T�pico B: 20% Corinthians, 20% Botafogo, 20% meu, 15% time, � (e ent�o podemos concluir que se trata de futebol)
- Como LDA descobre os t�picos?



Topic Model - Introdu��o
========================================================
O que � a modelagem estat�stica de t�picos?

- Modelos estat�sticos de t�picos (temas) permitem
a descoberta de t�picos latentes em textos
- � conhecido como um m�todo de aprendizagem
n�o-supervisionado
- n�o supervisionado, pois infere o t�pico
- T�pico � uma distrib de probabilidade s/ palavras,
ou seja, cada palavra tem uma prob. de ocorrer num
dado t�pico

Topic Model - Introdu��o
========================================================
No Topic Models, tudo se passa como se quando vamos 
escrever um documento, n�s

- Decidimos o n�mero de palavras que o doc. ter� de 
acordo com algum distr. de prob. (ex. Poisson)
- Escolhemos uma mistura de t�picos para o doc.
- No nosso ex. acima, com 2 t�picos (comida e futebol),
podemos decidir que o doc. ter� 1/3 de futebol e 2/3 de 
comida.
- E geramos cada palavra w_i do doc. de acordo com a
seguinte regra:


Topic Model - Introdu��o
========================================================

- Primeiro escolhemos um t�pico (com as prob. acima)
- Gera a palavra de acordo com a distrib. do t�pico
- Lembrem-se que o t�pico nos d� uma prob. para a 
ocorr�ncia de cada palavra.
- no nosso exemplo, no t�pico futebol, Corinthians tem
30% de prob., Botafogo 1%, Cerveja 2% etc.
- Assumindo um modelo desse tipo, a LDA tenta descobrir
os t�picos mais prov�veis de terem gerado nossas frases


---
layout: post
title:  "O Code Review Maroto"
date:   2017-04-06 14:49:00
excerpt: Code Review é uma excelente oportunidade para ensinar e aprender na
mesma proporção.
description: "Code Review: uma excelente oportunidade para ensinar e aprender na
mesma proporção."
image: /images/polite-code-reviewer/buddha-try-to-not-be-an-asshat.jpg
categories:
  - pt-br
  - working-with-others
---

### Essa é uma tradução

O ![post original](blog.ricardovaleriano.com/en/working-with-others/2017/03/20/the-polite-code-reviewer.html) está em inglês, ![confira lá](blog.ricardovaleriano.com/en/working-with-others/2017/03/20/the-polite-code-reviewer.html).

### TL;DR

 - Code Review é uma oportunidade para ensinar
e aprender na mesma proporção.
 - Não comente antes de entender as motivações que levaram a uma mudança.
 - Gaste a mesma energia para reconhecer as coisas boas
(encorajando e elogiando)
que é usada para encontrar coisas ruins.
 - Discussões em um code review geram material de estudo
(e podem servir para futuras referências).
 - Seja específico com aquilo que não está tão bom assim
e use código para exemplificar o que pode ser melhor.
 - Reconheça que o autor fez o melhor que ele pôde.

![Buddha says: try to not be an asshat](/images/polite-code-reviewer/buddha-try-to-not-be-an-asshat.jpg){: .center-image }

## Que negócio é esse aqui, bicho!? OMG!

Seguinte... tem um tempinho
que alguns colegas vem me dizendo
que meus Code Reviews são um pouco "diferentes".
Sendo o rei da auto-estima que sou,
Comecei a me perguntar (e a perguntar para todo mundo)
o que eu estava fazendo errado.
Aí, para minha imensa surpresa,
descobrir que o "diferente" nesse caso
era na verdade algo batuta.

Vou tentar explicar o meu processo mental
e os passos que sigo para fazer
meus Code Reviews ultimamente.

### Leia o código (DUH! _e não "apenas o diff"_ )

Eu acho muito tentador só dar aquela passada de zóio 👀 no _diff_.
Mas me esforço para resistir a essa vontadinha
e *de fato*® ler as alterações.

É assim que eu entendo o contexto geral das mudanças,
e eu acho que isso é pré condição
para tirar qualquer tipo de conclusão.

#### O objetivo é esclarecer as motivações

 - Porque algo foi escrito desse jeito?
 - O que passou na cabeça do programista nesse momento?
 - Posso aprender algo aqui?
   (Não só tecnicamente, mas até mesmo sobre o negócio?)

Talvez aquele código ~~meio bosta~~
que parece irremediavelmente idiota
está lá por algum motivo histórico.
A primeira "leitura" que eu faço
é uma tentativa entender isso.
De me colocar em uma posição em que as mudanças
estão em um contexto dentro da minha cachola.

Então *de fato*® ler o _PR_ antes de comentar
é algo que **works for me** (eu acho).

![Obama drinking beer approves this!](/images/polite-code-reviewer/obama-thumbs-up.jpg){: .center-image }

### Enaltecer o bom antes de bater no ruim

Esse conceito pode parecer alienígena
mas eu quero (MUITO) acreditar que
o papel principal de quem está
pilotando o Code Review
é enfatizar as coisas boas que apareceram.
Esse ambiente de incentivo vai
alimentar as coisas boas e elas vão se multiplicar.

![WOOOW! Just blewed me away. Wink!](/images/polite-code-reviewer/wow-wink.gif){: .center-image }

Na minha humilde opinião
é bem mais efetivo evitar que coisas ruins apareçam
do que reclamar demais quando elas estão lá.
Mas, já sabe né? Sem falsas esperanças, amiguinhos:

#### _código ruim "vai acontecer"_

Se eu tenho um conselho para dar aqui é: relaxa.
Mantenha o foco do review em apreciar as coisas marotas.
Sabendo que isso é bem difícil para nós programistas
(de repente é mais certo dizer: para nós seres humanos),
aqui vai um mix de alguns exemplos que o tempo me ensinou
e eu uso nos meus comentários em reviews:

 - Massa isso aqui! Eu não sabia que dava para fazer isso.
 - Eita, usar _isso aqui_ desse jeito é novo para mim!
Da hora, vou usar na próxima chance que eu tiver.
 - Putz, muito inteligente esse trecho, hein?
 - Como eu vivi até hoje sem saber disso!? 😱

E claro, está dada aqui minha benção
para usar memes a gifs animados nesse ponto.
Palmas lentas é um dos meus preferidos da vida.

![Here some slow claps: you sure deserve it!](/images/polite-code-reviewer/slow-claps.gif){: .center-image }

### Reviews ficam registrados

Githubz e similares oferecem um gama de ferramentas
para organizar e deixar belas
as mensages e comentários em um Code Review.
Vira e mexe eu me vejo olhando "antigos" Pull Requests.
E na maioria das vezes para lembrar sugestões
que apareceram para resolver algo específico,
ou alterar o código de alguma forma (também específica).

Trate o Code Review como se alguém,
muito provavelmente você mesmo,
fosse voltar a ele no futuro.
Também acredito que é legal tratar
os Pull Requests em si da mesma forma,
mas isso é assunto para _todo um novo blog post_™.

### Bom... chegou aquela hora.

Eu realmente me esforço para apontar
tudo que eu acho que não está 100% em um Pull Request.
Mas acredito que isso tem que ser feito
da maneira mais polida possível.
E vamos combinar, né? Eu sou um gentleman.

Uma coisa que acho muito importante lembrar
(antes de trazer a tona as coisas que podem ser diferentes)
é:

#### _código ruim **vai "aconter"**_, lembra?

E quer saber? Tudo bem!
A gente erra o tempo todo.
Bom, pelo menos eu erro.

TALVEZ EU SEJA UMA MULA, QUEM É QUE SABE!?

Mas sem zoeira, se não estamos errando
provavelmente é porque não estamos tentando nada novo/melhor, certo?

Trazer a tona os problemas no _PR_
é criar oportunidades para enteder porque eles estão acontecendo:
 - Tem algo nublado sobre nossos padrões?
 - Estamos entendendo errado alguma lógica de negócio?
 - Alguém seria muito beneficiado por uma aulinha de design OO?

#### Nunca diga simplesmente: "o código está feio".

Não seja um ~~idiota~~ desagradável.
Primeiro porque isso não existe.
Mas também porque isso é COMPLETAMENTE subjetivo.

_A beleza está nos olhos de quem vê._

Eu sempre tento meu melhor para ser objetivo em relação a isso.

##### Quando algo está errado, eu tento mostrar como e porque.

Faço bastante uso do milagre moderno chamado syntax highlighting
e de todo o pacote de _h1_, _h2_ e _h3_ nos meus markdowns.
Tento tornar meus comentários legíveis.

Bom... EU TENTO, tá bom!? 😤

Outra dica é enriquecer os exemplos de código
com referências a outras experiências e
a outras pessoas que a galera no time respeita
(vamos de internetz: blog posts, livros, etc).

_Prove o seu ponto.
Se empenhe nisso.
Não economize tempo aqui._

Quando eu **sinto** que algo está errado
mas eu não consigo pensar em um exemplo claro de como fazer melhor,
eu prefiro chamar para um papo.
Manja? Aquele bagulho antiquado
feito de trocar algumas palavras?
Cara a cara?
Provavelmente algumas ideias vão surgir durante a conversa,
mas eu prefiro não escrever nada no _PR_ se sinto que
estou apenas com "ar quente" na cabeça💨.

##### Se você "só ACHA" que algo está errado, testa primeiro, faz favor.

Estou sempre me vigiando
para me dar aquele soco bem na orelha direita
se penso em escrever alguma coisa como:

_"Eu acho que isso não precisa estar aqui, tá ligado?
Mas tipo, eu não tenho certeza."_

Quem escreveu o código empenhou tempo na coisa,
pensou em abstrações para tornar a parada massa,
escreveu tests/specs para garantir que tudo está funcionando...
Então é bem zoado chegar lá e "só achar"
que tem alguma coisa no _PR_ que não foi feita do melhor jeito possível.
Ainda pior,
meio que delegar o trampo de provar ou refutar a hipótese
para a própria pessoa que trabalhou duro naquela feature.

E convenhamos que na maioria das vezes
eu descubro coisas bacanas quando eu vou ali rapidinho no terminal e testo.
Manja? Aquele tipo de dúvida
"`#third` é do _Active Support_ ou do _Ruby_ mesmo?".

![It was TOTALLY worth it. Even with all the punchs directly at the nose.](/images/polite-code-reviewer/worth-it.jpg){: .center-image }

## Agora vai lá, nenê. Aproveite o dia.

Estamos todos aqui pela diversão e pelo aprendizado.
Tome uma (breja ou suco, sei lá) com seus colegas sempre que puder.
Pergunte o que pode ser feito
para melhorar suas próprias interações.

Vamos ter alguma diversão enquanto trabalhamos.

Beijocas.

## Muito obrigado. SÉRIO. MUITO OBRIGADO.

Esse post (original) seria ainda pior
sem a cuidadosa leitura e revisão prévia,
além do apontar de defeitos muito polido feitos por

 - [@hosseintoussi](https://github.com/hosseintoussi)

Você é o cara, bicho! 💙

## References:

 + [github](http://github.com)
 + [brown bag sessions](https://www.quora.com/What-is-a-brown-bag-session)

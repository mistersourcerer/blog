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
  - en
  - working-with-others
---

### TL;DR

 - Code Review é uma oportunidade para ensinar
e aprender na mesma proporção.
 - Não comente antes de entender as motivações que levaram a uma mudança.
 - Gaste a mesma energia para reconhecer as coisas boas
(encorajando e elogiando isso)
que é gasta para encontrar coisas ruins.
 - Discussões em um code review geram material de estudo
(and podem servir para futuras referências).
 - Seja específico com que não está tão bom assim
e sempre códigos para exemplificar o que pode ser melhor.
 - Reconheça o esforço que o autor original empenhou
em fazer o melhor que ele pôde.

![Buddha says: try to not be an asshat](/images/polite-code-reviewer/buddha-try-to-not-be-an-asshat.jpg){: .center-image }

## Que negócio é esse aqui, bicho!? OMG!

Seguinte... tem um tempinho que alguns colegas vem me dizendo
que meus code reviews são um pouco "diferentes".
Sendo o rei da auto-estima que sou,
Comecei a me perguntar (e a perguntar para todo mundo)
o que eu estava fazendo errado, então.
Aí, para minha imensa surpresa,
descobrir que o "diferente" nesse caso
era na verdade algo batuta.

Eu vou tentar mostrar os passos que sigo
e também processo mental
que tenho usado em meus code reviews ultimamente.

### Leia o código (DUH! _e não "apenas o diff"_ )

Eu acho muito tentador só dar aquela passada de zóio 👀 no _diff_.
Mas me esforço para resistir a essa vontadinha
e *de fato*® ler as alterações.

É assim que eu entendo o contexto geral das mudanças,
e eu acho que isso é pré condição
para tirar qualquer tipo de conclusão.

#### O objetivo nessa parte é esclarecer as motivações

 - Porque algo foi escrito desse jeito?
 - Qual era a ideia do desenvolvedor nessa parte?
 - Posso aprender algo aqui?
   (não só tecnicamente, mas até mesmo sobre o negócio?)

Talvez aquele código ~~meio bosta~~
que parece irremediavelmente idiota
está lá por algum motivo histórico.
A primeira "leitura" que eu faço
é uma tentativa entender isso.
De me colocar em uma posição em que as mudanças
estão em um contexto que eu consigo ver como um todo.

Então *de fato*® ler o PR antes de comentar
é algo que **works for me** (eu acho).

![Obama drinking beer approves this!](/images/polite-code-reviewer/obama-thumbs-up.jpg){: .center-image }

### Enaltecer o bom antes de bater no ruim

Esse conceito pode parecer alienígena
mas eu quero (MUITO) acreditar que
a principal ideia de que está pilotando o code review
é enfatizar as coisas boas que aparecem.
Nesse ambiente de incentivo
essas coisas vão se multiplicar.

![WOOOW! Just blewed me away. Wink!](/images/polite-code-reviewer/wow-wink.gif){: .center-image }

Na minha humilde opinião
é bem mais efetivo evitar que coisas ruins apareçam
do que reclamar demais quando elas estão lá.
Mas, já sabe né? Sem falsas esperanças, amiguinhos:

#### _código ruim "vai acontecer"_

Se eu tenho um conselho para dar aqui é: relaxa.
Mantenha o foco do review em apreciar as coisas marotas.
Sabendo que isso é bem difícil para nós pramistas
(enfim... para nós seres humanos),
aqui vai um mix de alguns exemplos que o tempo me ensinou
e eu uso nos meus comentários em reviews:

 - Massa isso aqui! Eu não sabia que dava para fazer isso.
 - Eita, usar _isso aqui_ desse jeito é novo para mim!
Da hora, vou usar na próxima chance que eu tiver.
 - Putz, muito inteligente esse trecho, hein?
 - Como eu vivi até hoje sem saber disso!? 😱

E claro, toma aqui minha benção
para usar memes a gifs animados nesse ponto.
Palmas lentas é um dos meus preferidos da vida.

![Here some slow claps: you sure deserve it!](/images/polite-code-reviewer/slow-claps.gif){: .center-image }

### Reviews ficam registrados

Githubz e similares oferecem um gama de ferramentas
para organizar e deixar belas
as mensages e comentários em um code review.
Vira e mexe eu me vejo olhando "antigos" Pull Requests.
E na maioria das vezes para lembrar sugestões
que apareceram para resolver algo específico,
ou alterar o código de alguma forma (também específica).

Trate o code review como se alguém,
muito provavelmente você mesmo,
fosse voltar a ele no futuro.
Também acredito que é legal tratar
os Pull Requests em si da mesma forma,
mas isso a assunto para _todo um novo blog post_™.

### Bom... chegou aquela hora.

Eu realmente me esforço em encontrar
tudo que eu acho que não está 100% em um Pull Request.
Mas acredito que isso tem que ser feito
da maneira mais polida possível.
E vamos combinar, né? Eu sou um gentleman.

Uma coisa que acho muito importante lembrar
(antes de apontar as coisas que podem ser diferentes)
é:

#### _código ruim **vai "aconter"**_, lembra?

E quer saber? Tudo bem!
A gente erra o tempo todo.
Bom, pelo menos eu erro.
TALVEZ EU SEJA UMA MULA, QUEM É QUE SABE!?
Mas sem zoeira, se não estamos errando
provavelmente é porque não estamos tentando nada novo/melhor, certo?

Trazer a tona os problemas no PR
é criar oportunidades para enteder porque eles estão acontecendo:
 - Tem algo nublado sobre nossos padrões?
 - Estamos entendendo errado alguma lógica de negócio?
 - Alguém seria muito beneficiado por uma aulinha de design OO?

#### Nunca diga simplesmente que o código está feio

Primeiro porque isso não existe.
Não seja um ~~idiota~~ desagradável.
Mas também porque isso é COMPLETAMENTE subjetivo.

_A beleza está nos olhos de quem vê._

Eu sempre tento meu melhor para ser objetivo em relação a isso.

##### Quando algo está errado, eu tento mostrar porque e como

Faço bastante uso do milagre do syntax highlighting
e todo o pacote de _h1_, _h2_ e _h3_ nos meus markdowns
para tornar meus comentários legíveis.
Bom... EU TENTO, tá bom!? 😤

Outra dica é enriquecer os exemplos de código
com referências a outras experiências e
outras pessoas nas internetz que o time respeita
(blog posts, livros, etc).

_Prove o seu ponto.
Se empenhe nisso.
Não economize tempo aqui._

Quando eu **sinto** que algo está errado
mas eu não consigo pensar um exemplo claro de como fazer melhor,
eu prefiro chamar para um papo.
Manja? Aquele bagulho antiquado
feito de trocar algumas palavras?
Cara a cara?
Provavelmente algumas ideias vão surgir durante a conversa,
mas eu prefiro não escrever nada no _PR_ se sinto que
estou apenas com "ar quente" na cabeça💨.

##### When you "THINK" something is wrong, just test it first

I'm always watching myself to punch me in the right ear
before I write something like:

_"I guess this isn't really necessary, ya know?
But I'm, like, not sure."_

The person that wrote the code spent some time on it,
thought about some abstractions to make it cool,
wrote tests/specs to guarantee that it's working...
So I think it's just lame to "just guess"
that something in the PR isn't the best/right way to go.
And more than that,
kinda delegate all the job to prove or disprove
something to the same person
that is working hard on some feature.

And in the majority of the cases
I discover really nice stuff when I do a rapid test in the terminal.
You know? I'm talking about those
"`#third` method is on _Active Support_ or _Ruby_ itself "
type of questions.

![It was TOTALLY worth it. Even with all the punchs directly at the nose.](/images/polite-code-reviewer/worth-it.jpg){: .center-image }

## Now go there and just enjoy your day

We are all here for the fun and the learnings.
So hang around with your peers allways you can,
talk about what you can do better
to improve your interactions.

Let's have some fun on our working lifes.

xoxo

## Thank you very much. REALLY! BIG THANKS

This post would be even worst
without the carefull early reading, revision
and polite point fingers from

 - [@hosseintoussi](https://github.com/hosseintoussi)

You are the man, bruv! 💙

## References:

 + [github](http://github.com)
 + [brown bag sessions](https://www.quora.com/What-is-a-brown-bag-session)

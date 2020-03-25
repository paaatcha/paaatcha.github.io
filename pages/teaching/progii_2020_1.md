---
layout: page
title: Programação II 2020/1 - INF09330
---

___

Esta é a página destinada a monitoria de Programação II 2020/1. Aqui você encontra alguns materiais de apoio bem como dicas, sugestões e resolução de exercícios de laboratório.

___


<h3>Menu rápido</h3>
<ul>
 	<li><a href="#sobre">Sobre a monitoria</a></li>
 	<li><a href="#dicas">Dicas de sobrevivência</a></li>
	 <li><a href="#workspace">Ambiente de desenvolvimento</a></li>
 	<li><a href="#apoio">Material de apoio</a></li> 	
 	<li><a href="#exercicios">Exercícios</a></li>
 	<li><a href="#trabalhos">Trabalhos</a></li> 	 	
</ul>

<hr />

<h3 id="sobre">Sobre a monitoria</h3>
Serão dois monitores, um pela manhã e outro a tarde. O horário da monitoria ainda não foi definido, mas haverá 1h por semana na qual estarei disponível fisicamente ou online para dúvidas (Obs: durante essa crise do coronavírus, será online).

Para entrar em contato:
+ **Email**: `pacheco.comp@gmail.com`
+ **Onde me encontrar** `LABCIN, sala 17-b CT 10, UFES`
+ [Mapa da UFES](https://www.google.com/maps/d/u/0/viewer?ll=-20.277576%2C-40.302658&spn=0.016102%2C0.042872&hl=en&msa=0&z=16&source=embed&ie=UTF8&mid=1bceB-PnlVIgdZnTuy1KrpZ2-KPY)



<h3 id="dicas">Dicas de sobrevivência</h3>
Como um graduado em Engenharia de Computação, deixo aqui algumas dicas para vocês:

+ **Não deixe suas atividades** acumularem. Faça tudo o quanto antes, principalmente antes do fim do período (principalmente os trabalhos). 

+ **Programação é prática**. Não adianta ler conceitos e não colocar a mão na massa!

+ Pergunte! Não leve dúvidas para casa.

+ Crie o hábito de estudar com seus amigos. Isso vai te ajudar bastante.

+ Se possível (caso professor disponibilize) estude o material antes da aula. Ter dúvidas é excelente!

+ Não deixe sua vida social de lado (óbvio que ela não vai ser como antes). Pratique algum exercício semanalmente que esvazie sua cabeça. 

+ Ao longo do curso vocês vão perceber que existem disciplinas que vocês vão estudar e vão ser aprovados tranquilamente e outras que vocês vão estudar freneticamente e ainda assim acaba reprovando (espero que não, mas a estatística não está do lado de vocês lol). **Programação é uma disciplina que se você estudar é impossível reprovar!**

+ Você não está mais no Ensino Médio! Não espere que o professor ou monitor vá até você. Seja independente! Tente solucionar os seus próprios problemas.  Se você não levar a sério, você vai reprovar e ponto.


<h3 id="workspace">Ambiente de desenvolvimento</h3>
Para muitos de vocês este é o primeiro contato com programação. Logo é natural ter dúvidas sobre um ambiente de desenvolvimento. Basicamente, você pode programar utilizando qualquer sistema operacional. Aqui vou dar dicas para Windows e Linux (Mac OS deixa pra próxima)

### Windows
Acredito que a vasta maioria utiliza Windows. Embora isso vai mudar ao longo da trajetória de vocês, você pode continuar utilizando no momento. 

Para programar com este SO, eu recomento o uso do Code::Blocks. Você encontra um tutorial que eu gravei há alguns anos [neste link](http://pachecoandre.com.br/2015/07/31/instalar-code-blocks.html).

### Linux
O SO mais utilizado no curso será o Linux. No futuro, vocês terão trabalhos que vocês terão que, obrigatoriamente, utilizar este SO. Muitos de vocês, inclusive, vai preferi-lo. Por exemplo, atualmente, este é o único SO que utilizo. Caso você já queira instalá-lo, aqui vai um rápido tutorial.

O Linux possui várias distribuições. Ubuntu é uma delas. Eu, particularmente, gosto de duas distribuições, o Xubuntu e o Mint. Ambas são modificações do Ubuntu. Pra quem está iniciando e vindo do Windows, acredito que o Linux Mint é melhor. Vai atender a demanda e tem um visual bacana que não faz você sentir tanto a diferença. Você pode baixar ele daqui: [download Linux Mint](https://www.linuxmint.com/download.php).

Você pode instalar o Linux e ainda assim manter o Windows na sua máquina. Isso é chamado de dual boot. Para instalar o dual boot é bem tranquilo. Partindo do princípio que você tem o Windows instalado, a própria instalação da distribuição do Linux vai criar o Grub, que nada mais é do que uma tela que aparece ao ligar o computador com opções do SO para dar boot. 

![Exemplo menu Grub](https://2.bp.blogspot.com/-ul9zrxN1N0M/U-IeAcdvraI/AAAAAAAAIJg/7POnWRidzZE/s1600/grub.png)

Daí você seleciona o SO que deseja utilizar no momento.

O processo de instalação envolve os seguintes passos: 
1. Baixar a distribuição do Linux. No caso do Linux Mint, [neste link](https://www.linuxmint.com/download.php).
2. Criar um pendrive bootável. Em outras palavras, é criar uma distribuição linux dentro do pendrive, plugar no sua máquina para que ela se inicie a partir dele. Você pode seguir este [vídeo tutorial](http://codetheelephant.com/criando-um-pendrive-bootavel-com-linux-mint-com-windows/) para criar o pendrive bootável.
3. Bootar no pendrive. Como disse no passo anterior, você tem que forçar a sua máquina a iniciar pelo pendrive. O nome disso é boot. Normalmente o boot pe feito no seus HD, precisamos mudar isso. Para fazer isso é simples, mas varia de computador para computar. O processo é: ligar o seu PC, entrar no setup da BIOS e selecionar o boot primário para o pendrive. Alguns computadores precisa apertar DEL quando starta, outros F12, etc. Nesse ponto você tem que pesquisar como acessar a BIOS no modelo do seu PC. Você pode dar uma olhada [neste vídeo tutorial](https://www.youtube.com/watch?v=CwfS7UXbONM) que exemplifica este processo.
4. Após o boot no pendrive com o Linux Mint, você vai seguir a instalação padrão. O passo a passo também é descrito no [tutorial](https://www.youtube.com/watch?v=CwfS7UXbONM) do passo anterior.

É importante que você **não apague a partição de dados do Windows**, caso contrário você perde tudo que tem nela!

Questão de tamanho de partição para o Linux, ou seja, o quanto de espaço que você deixa no seu HD para ela, isso é bem pessoal. Mesmo que você queira só pra estudos, eu deixaria pelo menos 200GB. Como disse, ao longo do curso você vai utilizando mais e mais a distribuição até chegar o momento que você não utilizará Windows mais (a não ser que você jogue algum jogo). Se você deixar pouco espaço, vai ter que remanejar o disco lá na frente.



<h3 id="apoio">Material de apoio</h3>
Existe muito conteúdo em livros, apostilas e vídeos na internet. Deixo uma lista deles na sequência. Apesar dos professores e monitoria, desde cedo vocês precisam ser **independentes**. Muita coisa a solução está em uma busca no Google ou no [StackOverflow](stackoverflow.com). Essa vai ser a vida de vocês daqui pra frente.


<ul>
 	<li><strong>Livros:</strong>
<ul>
 	<li>Deitel, P. e Deitel, H., C – Como programar, Editora Deitel, 6ª edição, 2011.</li>
 	<li>Schildt,  H. C – Completo e Total, Editora Person, 3ª edição, 1997.</li>
</ul>
</li>
 	<li><strong>Material de apoio:</strong>
<ul>
 	<li>Algoritmo e Lógica de Programação - UFRN - <a href="http://www.dca.ufrn.br/~lmarcos/courses/DCA800/pdf/algoritmos_parte1.pdf" target="_blank" rel="noopener">Parte I</a> e <a href="http://www.dca.ufrn.br/~lmarcos/courses/DCA800/pdf/algoritmos_parte2.pdf" target="_blank" rel="noopener">Parte II</a></li>
 	<li><a href="http://user.das.ufsc.br/~jomi/das5334/Livro%20Aberto%20Aprendendo%20a%20Programar%20naLinguagem%20C.pdf" target="_blank" rel="noopener">Aprendendo a Programar Programando na Linguagem C Para Iniciantes - Jaime Evaristo UFSC</a></li>
 	<li><a href="http://www.inf.ufpr.br/cursos/ci067/Docs/NotasAula.pdf" target="_blank" rel="noopener">Programação Básica em C - UFPR</a></li>
 	<li><a href="http://pachecoandre.com.br/?p=121" target="_blank" rel="noopener">Como instalar e utilizar o Code::Blocks</a></li>
 	<li><a href="http://tecnologia.hsw.uol.com.br/programacao-em-c.htm" target="_blank" rel="noopener">Como funciona programação em C</a></li>
</ul>
</li>
 	<li><strong>Vídeo aulas:</strong>
<ul>
 	<li>Introdução à programação de computadores (recomendável que assista) - <a href="https://www.youtube.com/watch?v=iA_8W6saSsc" target="_blank" rel="noopener">Parte I</a>, <a href="https://www.youtube.com/watch?v=uHAHFZu5hSY" target="_blank" rel="noopener">Parte II</a> e <a href="https://www.youtube.com/watch?v=uBMjZe_EIbw" target="_blank" rel="noopener">Parte III</a>.</li>
 	<li><a href="https://www.youtube.com/watch?v=FH7YrE0RjWE&amp;list=PLesCEcYj003SwVdufCQM5FIbrOd0GG1M4" target="_blank" rel="noopener">Curso de programação em C</a>  - 41 aulas</li>
</ul>
</li>
</ul>

**Extra**: nesta semana, por conta do confinamento de pessoas a Udemy liberou uma lista cursos gratuitos. Dentre eles, dois podem ser úteis para vocês:
+ [Aprenda C e C++ - Fundamentos Para Lógica de Programação](https://www.udemy.com/course/c-e-c-fundamentos-para-logica-de-programacao/)
+ [Algoritmos e Lógica de programação](https://www.udemy.com/course/algoritmos-logica-programacao/)

<hr />



<h3 id="exercicios">Exercícios</h3>

**Importante**: se você tem dúvida em algum exercício e quer compartilhar o código comigo, faça via [Github](http://github.com/). Se você não conhece, não tem problema. [Aqui tem um tutorial que fiz de introdução ao Git](http://pachecoandre.com.br/2018/10/18/mini-tutorial-git.html). Acredite, Git é importantíssimo e exigência de qualquer emprego de programação.

Em breve exercícios.


<h3 id="trabalhos">Trabalhos</h3>
Em breve...

<!--
<h3 id="cronograma">Cronograma</h3>
A tabela a seguir mostra o cronograma geral da disciplina. O mesmo pode sofrer alterações dependendo da curva de aprendizagem da turma. A ideia é que não se modifique, principalmente nas datas de provas e trabalhos.
<pre><code>[table]
Data,Descrição
Seg. 3 de agosto, <del>Aula de apresentação do curso</del>
Qui. 6 de agosto, <del>Introdução ao ambiente de programação\, primeiro programa\, printf\, e variáveis</del>
Seg. 10 de agosto, <del><em>Continuação da aula anterior\, Introduzir o Scanf\, fazer mais exercícios</em></del>
Qui. 13 de agosto, <del><em>Primeira lista de exercícios\, resolução em sala</em></del>
Seg. 17 de agosto, <del><em>Primeira aula de laboratório</em></del>
Qui. 20 de agosto, <del>Operadores lógicos e estrutura de seleção if</del>
Seg. 24 de agosto, <del>Estruturas de repetição\, break \, continue e exercícios</del>
Qui. 27 de agosto, <del>Continuação loops e seleção</del>
Seg. 31 de agosto, <del><em>Segunda aula de laboratório </em></del>
Qui. 3 de setembro, <del><em>Segunda lista de exercícios</em>\, resolução em sala</del>
Seg. 7 de setembro, <del><strong>Feriado de independência</strong></del>
Qui. 10 de setembro, <del>Funções</del>
Seg. 14 de setembro, <del><em>Terceira aula de laboratório</em></del>
Qui. 17 de setembro, <del>Simulado da prova - Exercícios de revisão</del>
Seg. 21 de setembro, <del><strong>Prova 1</strong></del>
Qui. 24 de setembro, <del>Exercícios com a monitoria - Correção e revisão da prova</del>
Seg. 28 de setembro, <del>Vetores\, Strings e exercícios</del>
Qui. 1 de outubro, <del>Continuação aula anterior e matrizes</del>
Seg. 5 de outubro, <del>Struct e exercícios (matrizes\, vetores e strings)</del>
Qui. 8 de outubro, <del><em>Quarta aula de laboratório</em></del>
Seg. 12 de outubro, <del><strong>Feriado de Nossa senhora aparecida</strong></del>
Qui. 15 de outubro, <del>Bibliotecas externas e exercícios</del>
Seg. 19 de outubro, <del>Laboratório - Manipulação de arquivos e Bibliotecas externas</del>
Qui. 22 de outubro, <del>Exercícios</del>
Seg. 26 de outubro, <del><em>Quinta aula de laboratório</em></del>
Qui. 29 de outubro, <del>Algoritmo de ordenação</del>
Seg. 2 de novembro, <del><strong>Feriado de finados</strong></del>
Qui. 5 de novembro, <del>Exercícios</del>
Seg. 9 de novembro, <del>Terceira<em> lista de exercícios</em>\, resolução em sala</del> 
Qui. 12 de novembro, <del>Sexta aula de laboratório</del>
Seg. 16 de novembro, <del><strong>PROVA 2</strong></del>
Qui. 19 de novembro, <del>Correção prova 2</del>
Seg. 23 de novembro, <del>Extra MATLAB</del>
Qui. 26 de novembro, <del><em>Sétima aula de laboratório</em>\, reservado para o trabalho</del>
Seg. 30 de novembro, <del><b>Reservado para o trabalho</b></del>
Seg. 3 de dezembro, <del>Divulgação da prova final</del>
Qua. 10 de dezembro, <del>Prova Final</del>
[/table]</code></pre>
&nbsp;
-->
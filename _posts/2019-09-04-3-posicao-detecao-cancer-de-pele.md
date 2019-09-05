---
layout: post
title: Como eu alcancei o 3ª lugar no desafio internacional de deteção de cancer de pele
tags:
  - artigo
  - deep learning
skin:
  - url: assets/imgs/skin_cancer/12.jpg
    image_path: assets/imgs/skin_cancer/12.jpg
    
  - url: assets/imgs/skin_cancer/13.jpg
    image_path: assets/imgs/skin_cancer/13.jpg
---

Escrevo este post para falar um pouco do ótimo resultado que eu obtive no ISIC 2019. Escrevo basicamente por dois motivos: 1) eu estou satisfeito com o resultado e gostaria de compartilhar; 2) atualmente a ciência brasileira está sendo desmantelada. Eu sou (era, não sei vão me pagar já que houve novos cortes ontem) bolsista da CAPES e esse resultado não teria acontecido sem esse fomento. Portanto, quero mostrar que a pesquisa brasileira não vive de balbúrdia e sim de resultados.

Mas antes de começar, você deve estar se perguntando: o que é ISIC? É de comer? Bom, vamos começar com um pouco de contexto.

# ISIC 2019
Quem acompanha meu trabalho sabe que minha área de pesquisa atual envolve detecção de câncer de pele. Caso não saiba e tenha interesse no que eu faço você pode obter mais informações clicando em _research_ no menu lateral.

O ISIC é uma sigla em inglês para _International Skin Imaging Collaboration_. Desde 2016 eles possuem um desafio de detecção de câncer de pele utilizando imagens de lesões de pele e outras informações. Abaixo você pode ver dois exemplos de imagens que o algoritmo desenvolvido deve diagnosticar.

{% include gallery id="skin" layout="half" %}

Esse desafio ganhou bastante atenção ao longo dos últimos 3 anos. O principal motivo foi que pela primeira vez uma base de dados do tipo estava sendo aberta e colaborativamente construínda. Anualmente, essa base é incrementada e uma nova tarefa é incluída para desafiar os participantes. De maneira geral, participam desse desafio pesquisadores da área. Este ano foram 64 times e mais de 140 submissões únicas.

Neste ano o desafio disponibilizou 25331 imagens com 8 doenças a serem detectadas e uma classe que representava algo desconhecido. Além disso, havia 2 tarefas, uma usando apenas as imagens e outra agregando imagens e dados clínicos do paciente. Cada participante deveria executar o modelo desenvolvido para 8238 imagens, que obviamente, os seus respectivos diagnósticos não são revelados.

Você pode checar todas as informações em relação as desafio na sua [página oficial](https://challenge2019.isic-archive.com/).


# Alcançando o 3ª lugar
Como eu disse acima, havia duas tarefas. O time que eu liderei (DermaCode) ficou em **4ª na tarefa 1 e em 3ª na tarefa 2**. Esse resultado rendeu uma premiação de $1000 e um convite para apresentar o trabalho na mais respeitada conferencia da área, a [MICCAI](https://www.miccai2019.org/). O resultado completo com todos os participantes você encontra no [ranking oficial do desafio](https://challenge2019.isic-archive.com/leaderboard.html).

Em uma visão mais técnica, basicamente eu utilizei uma série de _convolutional neural networks_ (CNNs) juntamente com detecção de _outliers_ utilizando entropia e um de algoritmo baseado no teorema de Bayes para incorporar os dados clínicos. Eu não quero entrar a fundo na teoria pois está tudo descrito [aqui neste artigo](/assets/files/isic-2019.pdf). Para participar da competição é obrigatório você descrever o seu modelo. Portanto, caso você seja da área, você pode ler o artigo e caso tenha dúvidas sinta-se livre para entrar em contato. Além disso vou escrever um post técnico no [Computação Inteligente](http://computacaointeligente.com.br/) em breve.

Outro ponto importante é que vou disponibilizar o código para quem quiser utilizar. Parte dele já está no meu [GitHub](https://github.com/paaatcha/jedy), mas ainda vou organizar um repositório direitinho para descrever tudo lá. Vou atualizar esse post quando eu o finalizar.


# Ok, legal! Mas pra que isso serve?
Bom, como eu já disse essa é minha área de pesquisa. Atualmente eu trabalho juntamente com o Programa de Assistência Dermatológica (PAD) da UFES. Esse projeto existe desde 1986 e presta um serviço fundamental para comunidades do interior do estado do Espírito Santo. Existe uma reportagem extremamente bem feita sobre o projeto e eu recomendo que a assista para conhecer uma realidade que a maioria esmagadora da população não sabe que existe:

<iframe src="https://www.youtube.com/embed/5nwDBwNCrR0" width="615" height="415" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
&nbsp;


No interior do nosso país é difícil encontrar dermatologistas e equipamentos para detectar o câncer de pele. E caso não saiba, segundo o [Instituto do Câncer José Alencar](http://www1.inca.gov.br/estimativa/2018/), este é o tipo mais comum de câncer no país com cerca de um terço dos diagnósticos. Dessa maneira, nosso objetivo de pesquisa é auxiliar os profissionais de saúde com tecnologia embarcada em smartphones para agilizar/facilitar o diagnóstico. Portanto,entrar numa competição **internacional**, **competindo com o que há de melhor na área mundialmente e obtendo um resultado positivo**, só mostra que o nosso trabalho está no caminho certo. Em breve esperamos que a população brasileira possa usufruir de novas tecnologias como essa. 


Como uma mensagem final, gostaria de destacar o quão importante é apoiar o investimento em pesquisa e educação no país. Sem isso, nós **nunca** seremos um país desenvolvido e melhor para se viver. Temos muita pesquisa de ponta acontecendo nas universidades públicas. Temos também muitos projetos fundamentais para população, como o PAD. Portanto, os convido a conhecê-los antes de criticá-los.


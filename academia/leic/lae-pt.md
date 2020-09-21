---
layout: academia/leic/lae
lang: pt
goals: |
  Os estudantes que terminam com sucesso esta unidade curricular serão capazes de: 
  1. Comparar e utilizar diferentes construções comuns em linguagens de
     programação modernas, enquadrando diferentes paradigmas de programação, e o
     seu suporte no ambiente de execução.
  2. Entender os principais constituintes de um ambiente de execução para
     linguagens de alto nível, e saber comparar diferentes abordagens de
     sistemas de tipos destes ambientes.
  3. Usar metadados em tempo de execução (reflexão) para examinar tipos e usar
     metaprogramação para analisar e transformar programas em tempo de execução.
  4. Analisar o desempenho de programas _managed_ e usar eficientemente o
     suporte automático de gestão de memória (_garbage collection_).
syllabus: |
  <ol type="I">
    <li>
      Principais construções de linguagens suportadas em ambientes de execução
      para linguagens de alto nível (<em>managed runtimes</em>) e a sua contextualização
      em diferentes paradigmas de programação, tendo como principal caso de
      estudo a máquina virtual Java.
    </li>
    <li>
      Principais constituintes dos ambientes de execução <em>managed</em>, nomeadamente:
      <em>class</em>,<em>verifier</em>,<em>just-intime compiler</em>, metadados e gestão de
      memória.
    </li>
    <li>
      Comparação de sistemas de tipos para ambientes de execução <em>managed</em> quanto
      às regras de equivalência, compatibilidade e inferência.
    </li>
    <li>
      API de reflexão em Java e casos práticos de metaprogramação no
      desenvolvimento de software.
    </li>
    <li>
      Modelo de pilha e registos. Análise das principais instruções bytecode Java
      apoiada em ferramentas de suporte à reflexão estrutural (e.g. ASM,
      Javassist).
    </li>
    <li>
      Introdução à análise de desempenho de programas Java e uso de ferramentas
      de monitorização da JVM (e.g. <em>jconsole</em>).
    </li>
    <li>
      Introdução aos algoritmos de garbage collection na JVM.
    </li>
  <ol>
outcomes: |
  Esta unidade curricular identifica os principais problemas resolvidos por
  um ambiente de execução para linguagens de alto nível e o suporte que
  fornece ao desenvolvimento de aplicações.
  Em particular são analisadas diferentes construções disponíveis nestas
  linguagens e nos sistemas de tipos, usando como principal caso de estudo a
  linguagem Java.
  
  A coerência entre os conteúdos programáticos e os objetivos da unidade
  curricular é a seguinte:
  - O objetivo 1 é alcançado através dos conteúdos I e III;
  - O objetivo 2 é alcançado através dos conteúdos II, III, e IV;
  - Os conteúdos IV e V contribuem para o objetivo 3;
  - Os conteúdos V, VI e VII pretendem concretizar o objetivo 4.
---

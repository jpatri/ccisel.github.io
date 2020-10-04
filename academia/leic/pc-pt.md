---
layout: academia/leic/pc
lang: pt
goals: |
  Os estudantes que concluírem com sucesso esta unidade curricular serão capazes de:
  1. Desenvolver de forma correta programas para ambientes _multi-threaded_, com ênfase em plataformas como a JVM (_Java Virtual Machine_) e a plataforma .NET. Identificar e tratar de forma correta situações de concorrência, incluindo o desenho de sincronizadores e a utilização das garantias fornecidas pelo modelo de memória.
  2. Usar corretamente modelos de programação assíncrona, nomeadamente futures, métodos
  assíncronos, corotinas e _reactive streams_.
syllabus: |
  1. Conceitos fundamentais: _thread_ e comutação de contexto de execução, partilha de dados e problemas associados.
  2. Caracterização do modelo de _threading_ para tipos de aplicação mais comuns, nomeadamente
  aplicações com _user-interface_ e servidores HTTP.
  3. Identificação dos problemas associados à partilha de dados entre _threads_, e as técnicas para a sua
  resolução, nomeadamente imutabilidade, afinidade a threads, exclusão mútua e correta publicação de
  dados.
  4. Coordenação entre _threads_, o conceito de sincronizador e sua implementação usando monitores.
  5. O conceito de modelo de memória e a sua utilização para a correta implementação de programas
  concorrentes.
  6. Técnicas para gestão de _threads_ e _thread pools_.
  7. O conceito de I/O assíncrono e a motivação para modelos de programação assíncronos. Modelos e mecanismos para programação assíncrona: _futures_, métodos assíncronos, corotinas, e _reactive streams_. Coordenação assíncrona entre _threads_
outcomes: |
  Os items (1) a (5) do programa fornecem o conhecimento necessário para o desenvolvimento de programas em contextos com múltiplas _threads_, incluindo adequada sincronização e coordenação, garantindo dessa forma o primeiro objetivo de aprendizagem. Os items (6) e (7) do programa fornecem o conhecimento adicional para o desenvolvimento de programas assíncronos, garantindo dessa forma o segundo objetivo de aprendizagem, com especial ênfase entre a interação entre os modelos de assincronismo e _multi-threading_.
---

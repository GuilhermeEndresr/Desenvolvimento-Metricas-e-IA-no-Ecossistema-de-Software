# Tema 2 — Habilidades e formação: o artigo-âncora

> **Pergunta principal:** quais habilidades fazem alguém ser bom em programar usando IA? O uso da IA ajuda ou atrapalha quem está aprendendo?
>
> **Perguntas norteadoras:**
> 1. O que uma pessoa precisa saber para transformar uma ideia em software que funciona?
> 2. Se a máquina escreve o código, o que sobra para o humano saber?
> 3. Como se forma um profissional experiente, e o que acontece com essa formação se as tarefas de iniciante desaparecem?
>
> Material de estudo do grupo 2. As informações sobre o estudo vêm do próprio artigo, com a seção, a tabela ou a figura de origem indicada.

---

## Sumário

- [Tema 2 — Habilidades e formação: o artigo-âncora](#tema-2--habilidades-e-formação-o-artigo-âncora)
  - [Sumário](#sumário)
  - [O artigo](#o-artigo)
  - [O que foi feito](#o-que-foi-feito)
  - [Como foi feito](#como-foi-feito)
    - [Participantes](#participantes)
    - [Tarefas e plataforma](#tarefas-e-plataforma)
    - [Testes](#testes)
    - [Procedimento](#procedimento)
  - [Resultado](#resultado)
    - [Resultado principal](#resultado-principal)
    - [Outros resultados](#outros-resultados)
    - [Análises exploratórias](#análises-exploratórias)
  - [O que os autores concluem](#o-que-os-autores-concluem)
  - [Limites apontados pelos autores](#limites-apontados-pelos-autores)
  - [Cuidados ao citar](#cuidados-ao-citar)

---

## O artigo

THORGEIRSSON, S.; WEIDMANN, T. B.; SU, Z. *Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency.* In: Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems (CHI '26), Barcelona, 2026. Os três autores são da ETH Zurich.

- Versão oficial (ACM): https://doi.org/10.1145/3772318.3791666
- Versão aberta (arXiv): https://arxiv.org/abs/2603.14133 · PDF: https://arxiv.org/pdf/2603.14133

---

## O que foi feito

Os autores definem vibe coding como especificar programas em linguagem natural e iterar a partir do comportamento observado, sem editar o código-fonte diretamente. Segundo eles, ainda se sabe pouco sobre quais habilidades melhor preveem o sucesso nesse modo de trabalho (resumo).

O objetivo principal foi examinar em que medida a habilidade de escrita e o desempenho em computação preveem o desempenho em vibe coding, e quanto essas previsões são moderadas pelo raciocínio geral (seção 1).

O estudo foi pré-registrado com três perguntas de pesquisa (seção 7.1):

1. A escrita se relaciona mais com o desempenho na tarefa descontextualizada do que nas duas tarefas com contexto?
2. A escrita se correlaciona com o desempenho em vibe coding? A correlação se mantém quando se controla o raciocínio geral?
3. Na previsão do desempenho, como a escrita se compara ao desempenho em computação?

Os autores escolheram a variante "pura" do vibe coding: os participantes não viam nem editavam o código gerado (seção 2.1).

---

## Como foi feito

Estudo transversal, feito em laboratório (seção 7.2).

### Participantes

- 100 estudantes de ensino superior, recrutados em diversas universidades da mesma região metropolitana (seção 1). O recrutamento foi feito pelo banco de voluntários do Decision Science Laboratory (DeSciL), da ETH, que reúne alunos da ETH e da Universidade de Zurique (seção 7.2). O artigo não informa a universidade de cada participante.
- Para participar, era preciso ter concluído uma disciplina introdutória de computação, ter experiência com LLMs em tarefas de programação e ter inglês no mínimo nível C1 (seção 7.2).
- Eram 56 mulheres e 44 homens, com idade média de 25 anos. 51 eram de engenharia e tecnologia, 20 de ciências naturais, 11 de ciências sociais e humanidades, e os demais de outras áreas (seção 8.1).
- Cada participante fez uma sessão única de 1h45 e recebeu 55 francos suíços (seção 7.2).

### Tarefas e plataforma

Foram três tarefas de 15 minutos cada, todas envolvendo pequenos aplicativos web com interface gráfica (seção 1 e Figura 6).

| Tarefa | O que o participante fazia |
|---|---|
| Replicação | Replicava um app de exemplo |
| Adição de funcionalidade | Estendia um app existente com novas funcionalidades |
| Descontextualizada | Trabalhava com um pequeno app "brinquedo", de comportamento óbvio, cujos rótulos não revelavam, de propósito, para que ele servia |

- As duas tarefas com contexto vieram de um painel de oito especialistas, num processo de consenso em duas etapas. A tarefa descontextualizada foi criada pelos autores (seção 3).
- Os participantes não recebiam uma especificação escrita do app. Exploravam o app de exemplo e formulavam o pedido por conta própria. Segundo os autores, um texto pronto levaria os participantes a copiá-lo direto para o modelo (seção 3).
- A plataforma foi construída para o estudo, com o chat à esquerda e a prévia do app à direita. A barra lateral mostrava a descrição da tarefa, um cronômetro e um botão para abrir o app de exemplo. O código ficava escondido: o texto gerado pela IA aparecia borrado, só para indicar que ela estava trabalhando. O modelo usado foi o Claude Sonnet 4 (seção 5.2).
- Um integrante da equipe de autores corrigiu cada app manualmente e às cegas. Cada funcionalidade principal recebeu uma nota numa escala de 4 pontos: inaceitável, abaixo do esperado, atende, supera (seção 7.3).

### Testes

- Computação: 12 questões do SCS1, um teste validado escrito em pseudocódigo, com limite de 25 minutos (seção 4.2).
- Escrita: redação de 300 a 450 palavras, em 20 minutos, sobre um conceito técnico do próprio curso, voltada para um adulto com formação universitária, mas não especialista. Dois avaliadores independentes corrigiram às cegas, com uma rubrica de 100 pontos. Quando as notas diferiam em mais de 10 pontos, um terceiro avaliador corrigia a redação (seção 4.1).
- Raciocínio geral: ICAR16, com 16 questões e limite de 12 minutos (seção 4.3). Entrou como variável de controle, para que as relações entre computação, escrita e vibe coding não fossem explicadas apenas pelo raciocínio geral (seção 2.2).

### Procedimento

Os participantes foram divididos por sorteio em dois grupos. O grupo A fez os testes antes das tarefas, e o grupo B, depois. A ordem dos testes e das tarefas também foi sorteada para cada participante (Figura 6). Todas as medidas foram convertidas para uma escala de 0 a 1 (seção 7.3).

---

## Resultado

### Resultado principal

Computação e escrita previram de forma significativa o desempenho em vibe coding. Quando se controlou o raciocínio geral, a computação continuou significativa, mas a escrita não. Num modelo com as duas, a computação explicou cerca do dobro da variância única explicada pela escrita, e a escrita ainda acrescentou poder de previsão próprio (resumo e seção 8.2).

| | Computação | Escrita | Fonte |
|---|---|---|---|
| Correlação com o desempenho | r = 0,39 | r = 0,29 | Tabela 3a |
| Correlação controlando o raciocínio geral | r = 0,281 (p = 0,005), significativa | r = 0,186 (p = 0,066), não significativa | Tabela 3b |
| Variância única no modelo com as duas | ΔR² = 0,125 | ΔR² = 0,059 | Seção 8.2 |
| Coeficiente padronizado no mesmo modelo | β = 0,356 (p < 0,001) | β = 0,244 (p = 0,009) | Seção 8.2 |

### Outros resultados

- Pergunta 1: a correlação da escrita com a tarefa descontextualizada (r = 0,239) foi menor que com a de adição de funcionalidade (r = 0,245). A hipótese não se confirmou (seção 8.2 e Tabela 4).
- A correlação entre computação e escrita foi pequena e não significativa (r = 0,126) (Tabela 3a).
- Médias na escala de 0 a 1 (Tabela 2): vibe coding 0,45 (máximo de 0,83); replicação 0,46; adição de funcionalidade 0,55; descontextualizada 0,34.

### Análises exploratórias

O artigo apresenta estes resultados como exploratórios (seções 9 e 10.1).

- Uso de LLM: a frequência de uso declarada pelos participantes teve correlação negativa com o desempenho (r = −0,258; p = 0,010) e com a escrita (r = −0,282; p = 0,005). Não teve correlação com a computação (r = 0,001) nem com o raciocínio geral (r = −0,070). Os autores especulam três explicações: os LLMs prejudicarem a capacidade de se expressar; estudantes que escrevem pior usarem mais LLMs; ou as duas coisas (seção 10).
- Qualidade do prompt: um membro do painel de especialistas avaliou os prompts às cegas. A qualidade do prompt teve correlação com a nota da redação (r = 0,353) e com o desempenho (r = 0,479). Na análise de mediação, ela respondeu por cerca de 52% da associação entre escrita e desempenho. Os autores dizem que não tiram conclusão causal desse resultado (seção 9).
- Parte algorítmica: na tarefa do planejador de refeições, a parte de dados e cálculo também foi prevista pela computação (r = 0,320) e pela escrita (r = 0,202). Os autores tratam isso como evidência tentativa e pedem cautela, porque a análise se baseia em uma única tarefa (seção 10.1).

---

## O que os autores concluem

- Escrita e computação contribuem de forma positiva, significativa e independente para o desempenho em vibe coding de aplicativos com interface gráfica. No caso da computação, isso não se explica apenas pelo raciocínio geral (seção 10).
- A análise exploratória sugere que essa relação não vem de os estudantes com bom desempenho em computação terem mais experiência com LLMs. E, como o código não era visível, esses estudantes não tinham vantagem óbvia para interpretar a saída do modelo (seção 10).
- O estudo é correlacional e não permite conclusões causais. Os autores levantam hipóteses para estudos controlados (seção 10):
  - o pensamento estruturado aprendido em computação ajudaria a especificar o comportamento do programa;
  - o vibe coding usaria partes do "currículo oculto" da computação, como decompor problemas e pensar em algoritmos;
  - o domínio do vocabulário de computação ajudaria a escrever prompts melhores.
- Sobre a escrita, os autores acreditam que quem tira nota alta não só escreve com clareza, como também segue convenções de escrita estruturada, e por isso pode estruturar melhor os prompts (seção 10).
- Como o código ficava escondido, a estimativa do papel da computação deve ser vista como um limite inferior. Em fluxos que permitem ler e editar o código, as mesmas habilidades podem contribuir também por meio de edições no código. Os autores ressalvam que dar acesso ao código provavelmente não aumentaria o peso da computação e reduziria o da escrita de forma linear (seção 10.1).
- Os resultados podem orientar o desenho de ferramentas e de currículos, por exemplo, sobre quando enfatizar a escrita de prompts e quando enfatizar os fundamentos de computação (resumo). Ferramentas que ensinam a escrever prompts partem da premissa de que o principal gargalo é expressar requisitos com precisão em linguagem natural, e o estudo dá apoio tentativo a essa premissa (seção 10).
- Os resultados incentivam investigar, em estudos controlados futuros, a hipótese de que o ensino de computação leve a resultados melhores na programação guiada por LLM (seção 11).

---

## Limites apontados pelos autores

Seção 10.2, salvo indicação em contrário:

- O estudo se limita ao vibe coding de aplicativos com interface gráfica (seção 10.1). O vibe coding abrange outras tarefas, como análise de dados, e os resultados poderiam ser diferentes nelas.
- O teste de escrita não tinha sido usado antes, o que pode afetar sua validade de construto.
- O laboratório difere da maioria dos contextos reais, e o estudo cobre só o vibe coding "puro". Os resultados podem não se aplicar diretamente a fluxos em que o código pode ser revisado.
- Testes e tarefas tinham tempo controlado, e vários participantes ficaram sem tempo quando estavam perto da solução correta.
- O enquadramento das tarefas pode ter afetado as estratégias dos participantes, e alguns podem ter entendido mal o que deviam implementar.
- A amostra é de universitários, o que limita a generalização para outros públicos, como desenvolvedores profissionais.

---

## Cuidados ao citar

- A escrita prevê o desempenho (r = 0,29), mas deixa de ser significativa quando se controla o raciocínio geral (r = 0,186; p = 0,066).
- Os resultados sobre uso de LLM, qualidade do prompt e parte algorítmica vêm de análises exploratórias.

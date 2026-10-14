# Habilidades de Entrada, Débitos Cognitivo e o Futuro da Formação de Desenvolvedores de Software

**Autor: Pedro Rodrigues**

---

## Contextualização

A popularidade do uso de ferramentas baseadas em Grandes Modelos de Linguagem (LLMs) transformou a prática do desenvolvimento de software e a educação em computação. A promessa de criar aplicações funcionais a partir de descrições em linguagem natural trouxe uma nova dinâmica para o setor, alterando a forma como programadores iniciantes e experientes constroem sistemas.

No entanto, essa transição para um ecossistema assistido por IA gera uma tensão evidente: enquanto a produtividade imediata aumenta, surgem dúvidas cruciais sobre a retenção de conhecimento, o desenvolvimento de habilidades críticas e o futuro da formação profissional.

Este trabalho fundamenta-se em três estudos empíricos recentes e quantitativos para analisar o impacto da inteligência artificial na formação e nas competências do desenvolvedor de software. O primeiro trata de identificar quais capacidades humanas fazem alguém ser efetivamente bom em programar utilizando IA, comparando a comunicação escrita com o vocabulário técnico e fundamentos da Ciência da Computação. O segundo trata do uso de ferramentas gerativas que auxiliam na compreensão do conceitos criando uma dependência que prejudica o desenvolvimento cognitivo de quem esta aprendendo. E o último trata de qual a trajetória de um desenvolvedor sênior, se as tarefas de nível junior forem realizadas desde cedo pela IA.

</br>

## Habilidades Determinantes no Uso da Inteligência Artificial

A ideia do vibe coding, programar sem mexer no código-fonte, e do uso de IA na programação faz parecer que não precisamos mais dominar linguagens formais, bastando conversar em linguagem natural com os modelos de linguagem. No entanto, pesquisas mostram que programar com IA exige competências muito bem definidas: ter clareza no contexto e entender os conceitos básicos conta muito mais do que apenas usar termos técnicos difíceis ou ficar usando a IA toda hora sem orientação.

Existe um grande mito de que a dificuldade dos iniciantes em fazer a IA gerar o código correto é a falta de vocabulário técnico. Na prática, o que realmente importa é a presença de detalhes e contexto no prompt. Quando o aluno fornece todas as pistas essenciais sobre o que o programa deve fazer, a taxa de sucesso da IA chega a 90%, alcançando 86% no GPT-4o, 57% no Llama 3.1 70B e 50% no Llama 3.1 8B.

Por outro lado, se faltar um único detalhe crítico, esses números despencam para 46% no GPT-4o, 16% no Llama 3.1 70B e 14% no Llama 3.1 8B. Trocar palavras simples por termos técnicos (como usar "string" em vez de "palavra" ou "iterar" em vez de "fazer um loop") quase não altera o resultado se o prompt continuar vago. Sem perceber que falta informação, o estudante entra em um ciclo de reescritas superficiais: a chance de resolver o problema cai de 72% para 30% assim que ele entra nesse ciclo, e cai para apenas 14% se fizer mais de três edições sem adicionar dados novos, sendo que 90% dessas edições ocorrem por falta de pistas contextuais.

Para entender quais habilidades humanas realmente preveem o sucesso no vibe coding, um estudo com 100 universitários avaliou a bagagem técnica e a capacidade de escrita dos alunos. Os fundamentos de Ciência da Computação se mostraram o preditor mais forte para um bom desempenho (r = 0,39, p < 0,001), e continuaram sendo estatisticamente significativos (r = 0,281, p = 0,005) mesmo isolando a inteligência geral dos participantes. Na prática, saber lógica e decompor problemas explica o dobro do sucesso (Delta R^2 = 0,125) quando comparado às habilidades de escrita (Delta R^2 = 0,059). A boa comunicação escrita também ajuda (r = 0,29, p = 0,003), pois saber escrever bem permite explicar o que se quer sem gerar ambiguidade. Por fim, o estudo derrubou o mito de que usar IA todo dia torna alguém melhor nisso: a frequência de uso diário teve uma correlação negativa com o desempenho (r = -0,258, p = 0,010). Isso mostra que apenas usar a IA no cotidiano não desenvolve, por si só, o raciocínio e o pensamento computacional necessários para criar e validar sistemas.

</br>

## O Impacto Cognitivo e Neurofisiológico no Aprendizado

Apesar da sensação de facilidade e rapidez ao usar assistentes de Inteligência Artificial (IA) nos estudos, pesquisas mostram que esse alívio mental traz um custo oculto para o cérebro: diminuição da atividade neural, perda de memória e o acúmulo do chamado débito cognitivo. Um estudo do MIT Media Lab usou exames de eletroencefalograma (EEG) para comparar três grupos de alunos — sem ajuda externa (Brain-only), usando o Google (Search Engine) e usando o ChatGPT (LLM). Os dados mostraram que a atividade e conexão do cérebro caem na mesma proporção do suporte recebido. Enquanto o grupo sem ajuda ativou fortemente o cérebro para buscar memórias e organizar ideias, o grupo do Google teve uma redução de 34% a 48% na conectividade, e o grupo da IA teve uma queda de até 55%. Isso acontece porque quem usa IA deixa de criar conteúdo ativamente e passa apenas a supervisionar a resposta que o modelo entrega pronto.

Essa mudança afeta diretamente o quanto o estudante consegue lembrar do que fez e o quanto ele se sente dono do trabalho. Logo após terminarem o texto, 83,3% dos alunos que usaram IA não lembravam do que tinham escrito e 0% conseguiu fazer uma citação exata do próprio trabalho. No grupo sem ajuda externa, 88,9% lembrou e citou o texto corretamente. Isso ocorre porque a IA faz com que a informação passe "batido" pelo cérebro, sem ser processada no nível da memória de longo prazo. Além disso, metade dos alunos que usaram IA relataram não se sentir autores do próprio texto.

O experimento também testou inverter a dinâmica na quarta sessão do estudo. Os alunos que começaram escrevendo sozinhos e depois passaram a usar IA (Brain-to-LLM) conseguiram usar a ferramenta de forma crítica e eficiente, mantendo uma alta taxa de retenção do conteúdo (77,8%). Já os alunos que usaram IA desde o início e depois tiveram a ferramenta retirada (LLM-to-Brain) travaram: 78% não lembravam do texto e apenas 11,1% conseguiu citar algo. O estudo chama isso de débito cognitivo. A dependência contínua de ferramentas externas adia o esforço mental necessário para aprender e, no longo prazo, atrofia a capacidade de pensar sozinho, resolver problemas e analisar criticamente as informações.

</br>

## A Formação do Profissional Experiente e o Desaparecimento das Tarefas de Iniciante

Uma das grandes preocupações atuais na área de tecnologia é entender como os novos desenvolvedores vão se tornar sêniores se as tarefas de nível iniciante (júnior) forem assumidas pela Inteligência Artificial. Para responder a isso, é preciso observar como o cérebro aprende e se desenvolve ao resolver problemas, comparando esse processo com os riscos do uso precoce de ferramentas automatizadas.

Um profissional sênior não se forma apenas decorando a sintaxe de uma linguagem, mas criando modelos mentais sólidos para resolver problemas complexos, desenhar arquiteturas e auditar código. Pesquisas do MIT mostram que resolver problemas de forma autônoma ativa áreas essenciais do córtex pré-frontal: cada bug corrigido e cada código escrito à mão ajudam a consolidar aprendizados na memória. Além disso, estudos da ETH Zurich confirmam que os fundamentos de Ciência da Computação — como o raciocínio algorítmico — são o maior indicador de bom desempenho com a IA (r = 0,39), pois são esses conceitos que permitem ao desenvolvedor entender do que o sistema precisa e fazer os pedidos corretos.

O problema é que, no caminho tradicional, o desenvolvedor júnior aprendia justamente fazendo as tarefas mais simples, como escrever funções básicas, criar testes e corrigir bugs pequenos. Era errando nesses exercícios que ele entendia o funcionamento interno do software. Com a IA assumindo essas etapas, surge o risco de uma "fluência superficial": o iniciante entrega código rápido e parece competente, mas não aprendeu de verdade. Os testes do MIT apontam que terceirizar essa produção reduz a conectividade do cérebro em até 55% e zera a capacidade de lembrar o próprio código criado. Além disso, a frequência de uso diário de IA correlaciona-se negativamente com o desempenho (r = -0,258), mostrando que usar a ferramenta toda hora apenas acostuma o cérebro a não pensar.

Se as tarefas iniciantes desaparecerem sem uma mudança no ensino, o mercado enfrentará três grandes gargalos:

- Incapacidade de auditar o código da IA: Para saber se um código gerado é seguro e eficiente, o desenvolvedor precisa saber mais do que a própria ferramenta. Se ele nunca escreveu código manualmente, não conseguirá identificar falhas ou "alucinações" da IA.
- Ciclos de edições infrutíferas: Sem base conceitual, o profissional não percebe quais detalhes faltam no prompt e entra em ciclos repetitivos de reescrita superficial, onde a chance de sucesso cai para apenas 14%.
- Trava sem a ferramenta: O experimento do MIT provou que pessoas expostas continuamente à IA travam quando precisam atuar sozinhas: 78% não lembravam da estrutura do próprio trabalho e só 11,1% conseguiram fazer citações corretas.


A solução não é banir a IA, mas sim adotar a abordagem Brain-to-LLM. A evidência científica mostra que os alunos que primeiro aprenderam de forma autônoma e só depois começaram a usar IA mantiveram alta atividade cerebral e boa retenção de memória (77,8% de precisão), usando a ferramenta de forma estratégica. Em suma, o iniciante ainda precisa resolver tarefas básicas no começo da carreira — não porque a IA não consiga fazê-las, mas porque o cérebro humano precisa desse processo para desenvolver o raciocínio crítico de um futuro sênior.

</br>

## Conclusão

A investigação realizada a partir dos estudos empíricos recentes permite dismistificar premissas equivocadas sobre o uso da inteligência artificial no desenvolvimento de software e construir um posicionamento sólido sobre o tema Habilidades e Formação.

A inteligência artificial não elimina a necessidade de aprender Ciência da Computação, mas sim pelo contrário, aumenta a exigência sobre o domínio dos conceitos fundamentais. A ideia de que o vibe coding ou a programação orientada a IA transforma qualquer pessoa em um desenvolvedor competente apenas por saber "conversar" com a ferramenta é negada pelas evidências numéricas.

Desta forma, a IA atua como uma ferramenta capaz de ampliar e expandir a produtividade e o racíocinio crítico de um desenvolvedor, enquanto quem utiliza sem fundamentação prévia desenvolve uma fluência superficial acompanhada de débito cognitivo e atrofia a habilidade.

<br>

## Referências Bibliográficas

- KOSMYNA, N. et al. **Your Brain on ChatGPT: Accumulation of Cognitive Debt**. MIT Media Lab, 2025. Disponível em: <https://arxiv.org/abs/2506.08872>. Acesso em: 13 out. 2026.

- LUCCHETTI, F. et al. **Substance Beats Style: Why Beginning Students Fail to Code with LLMs**. In: *Proceedings of the 2025 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (NAACL)*, 2025. DOI: <https://doi.org/10.18653/v1/2025.naacl-long.433>.

- THORGEIRSSON, S.; WEIDMANN, T. B.; SU, Z. **Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency**. In: *Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems (CHI '26)*, Barcelona, Spain. New York: ACM, 2026. DOI: <https://doi.org/10.1145/3772318.3791666>.
# Conhecimento técnico na transformação de ideias em software assistido por IA

**Autor: Fernando Dalzotto**

---

## Contextualização

As plataformas de desenvolvimento assistido por IA passaram a permitir que uma aplicação seja descrita em linguagem natural e construída sem que o usuário edite o código-fonte. Andrej Karpathy chamou essa forma de trabalho de *vibe coding* em fevereiro de 2025 (KARPATHY, 2025). Nela, o programa é especificado por meio de prompts e ajustado a partir do comportamento observado.

A adoção dessas plataformas já é medida em milhões de usuários. Segundo os dados reunidos por Thorgeirsson, Weidmann e Su (2026):

- o Replit declara uma comunidade de mais de 40 milhões de usuários;
- o Lovable afirma que seus usuários já criaram mais de 10 milhões de projetos;
- o Cursor ultrapassou 1 milhão de usuários em 2025.

Parte dessas plataformas apresenta o *vibe coding* como uma forma de desenvolver software sem aprender linguagens de programação ou conceitos técnicos. O CEO do Replit afirmou que 75% dos usuários da plataforma nunca escrevem uma linha de código.

Se essa promessa se confirmasse, o conhecimento técnico deixaria de ser necessário para transformar uma ideia em software. Este documento analisa as evidências disponíveis sobre essa questão e defende a posição contrária. Ter a ideia não é suficiente: transformá-la em software que funciona exige compreender como software funciona, mesmo quando a pessoa não lê nem escreve o código.

## O que o estudo-âncora mediu

### Desenho do estudo

O artigo *Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency* relata um estudo pré-registrado com 100 estudantes da ETH Zurich e da Universidade de Zurique (THORGEIRSSON; WEIDMANN; SU, 2026). Todos haviam cursado ao menos uma disciplina introdutória de computação e já utilizavam LLMs para programar.

Cada participante realizou três tarefas de *vibe coding* de 15 minutos. As tarefas foram selecionadas por um painel de 8 especialistas:

1. Replicar um aplicativo de planejamento de refeições;
2. Adicionar funcionalidades a um aplicativo de matrícula em disciplinas;
3. Replicar um aplicativo "descontextualizado", cujos rótulos não revelavam o propósito.

Os participantes também responderam a três instrumentos de avaliação:

- **Conhecimento em Ciência da Computação:** subconjunto de 12 itens do SCS1, um teste validado e baseado em pseudocódigo.
- **Habilidade de escrita:** redação técnica de 20 minutos, corrigida por avaliadores independentes.
- **Raciocínio geral:** ICAR16, utilizado como variável de controle.

O ponto central do desenho é que a plataforma do estudo **escondia o código por completo**. O participante via apenas o chat e a prévia do aplicativo. A saída do modelo (Claude Sonnet 4) aparecia borrada, impedindo a leitura ou a cópia do código. A única intervenção disponível além do prompt era retornar a uma versão anterior do aplicativo.

### Resultados

| Preditor | Correlação com o desempenho (r) | Controlando raciocínio geral (r parcial) | Variância única explicada (ΔR²) |
|---|---|---|---|
| Conhecimento em computação | 0,39 (p < 0,001) | 0,281 (p = 0,005) | 12,5% |
| Habilidade de escrita | 0,29 (p = 0,003) | 0,186 (p = 0,066, não significativo) | 5,9% |

*Fonte: Thorgeirsson, Weidmann e Su (2026), tabela 3 e seção 8.2.*

- **Correlação (r):** indica o quanto duas medidas variam juntas, em uma escala de −1 a 1.
- **Correlação parcial:** repete o cálculo removendo a influência do raciocínio geral, que poderia afetar tanto o conhecimento técnico quanto a escrita.
- **Variância única (ΔR²):** parcela do desempenho explicada por um preditor que o outro não explica.

<br><br>

Os dados indicam que o conhecimento em computação explicou cerca do dobro da variância única explicada pela escrita. Ele também permaneceu estatisticamente significativo após o controle pelo raciocínio geral, o que não ocorreu com a escrita.

Como nenhum participante via o código, essa vantagem não pode ser atribuída à leitura de código. Os autores levantam como hipóteses a decomposição de problemas e o pensamento algorítmico. Em entrevista à ETH, Weidmann acrescenta que quem domina computação planeja a estrutura do aplicativo com mais precisão, depura erros mais rápido e conhece os termos técnicos para direcionar o agente (ELHARDT, 2026).

#### Desempenho por tarefa

| Tarefa | Nota média (0 a 1) |
|---|---|
| Adição de funcionalidades | 0,55 |
| Replicação | 0,46 |
| Descontextualizada | 0,34 |
| **Média geral** | **0,45** |

*Fonte: Thorgeirsson, Weidmann e Su (2026), tabela 2.*

A menor nota ocorreu na tarefa descontextualizada. Uma interpretação possível é que, quando a ideia não pode ser resumida por um nome conhecido como "planejador de refeições", o modelo não tem de onde preencher as lacunas. Nesse caso, a especificação precisa vir inteira da pessoa.

Cabe uma ressalva. Os autores haviam pré-registrado a hipótese de que a escrita teria peso maior nessa tarefa, e ela não se confirmou: a correlação foi de 0,239, contra 0,245 na tarefa de adição de funcionalidades.

## O que explica a vantagem do conhecimento técnico

### Conteúdo da especificação

O artigo *Substance Beats Style: Why Beginning Students Fail to Code with LLMs* investigou duas explicações para a dificuldade de iniciantes ao programar com LLMs (LUCCHETTI et al., 2025):

1. a falta de vocabulário técnico;
2. a falta de noção sobre quanta informação o modelo precisa para gerar o código correto.

Para testar a primeira explicação, os autores realizaram um experimento de intervenção causal sobre o vocabulário. O vocabulário técnico fraco apenas se correlacionou com a falha. O fator que previu o sucesso foi o conteúdo informacional do prompt. Prompts com informação ausente quase sempre falharam, e os estudantes tenderam a repetir reescritas que não acrescentavam informação.

Um exemplo do estudo, relatado pelo artigo-âncora, foi a troca de "print" por "return" no prompt, que alterou a taxa de acerto (THORGEIRSSON; WEIDMANN; SU, 2026). Exibir um valor e devolvê-lo são operações distintas: trata-se de uma diferença conceitual, não de escolha de palavra. A base técnica que pesa no resultado é, portanto, a compreensão do funcionamento, e não a memorização de termos.

### A IA como amplificador da base existente

O artigo *Studying the Effect of AI Code Generators on Supporting Novice Learners in Introductory Programming* acompanhou 69 iniciantes de 10 a 17 anos em 45 tarefas de Python (KAZEMITABAAR et al., 2023). Metade dos participantes teve acesso ao gerador de código Codex.

O grupo com acesso ao Codex apresentou taxa de conclusão 1,15 vez maior e notas 1,8 vez maiores, sem perda de desempenho nas tarefas de modificação manual de código. Entre os aprendizes com notas mais altas no pré-teste (Scratch), os que tiveram acesso ao Codex obtiveram desempenho significativamente melhor no teste de retenção, aplicado uma semana depois. Os autores concluem que quem chega com mais competência prévia tende a se beneficiar mais da ferramenta.

### Exemplo ilustrativo

A ideia "um PDV que emite nota fiscal" pode ser descrita em uma frase. Os elementos que a fazem funcionar, não:

- o comportamento do sistema quando a SEFAZ está indisponível (contingência);
- o tratamento de dois terminais vendendo o último item do estoque ao mesmo tempo (transação e concorrência);
- o armazenamento e a renovação do certificado digital.

Quem não sabe que esses elementos existem não consegue solicitá-los ao agente. Também não percebe sua ausência quando a demonstração aparenta funcionar.

## Limitações das evidências

- **Correlação, não causalidade:** o artigo-âncora é um estudo transversal, e os próprios autores evitam conclusões causais. A formulação adequada é que o conhecimento em computação *prediz* o desempenho.
- **Contribuição da escrita:** a escrita contribui de forma independente. As duas habilidades quase não se correlacionam entre si (r = 0,126, p = 0,213), de modo que uma não substitui a outra. A qualidade dos prompts respondeu por cerca de 52% da associação entre escrita e desempenho (THORGEIRSSON; WEIDMANN; SU, 2026).
- **População e tarefas:** o estudo envolveu universitários com inglês nível C1 e aplicativos com interface gráfica. A generalização para profissionais ou para outros tipos de software não foi testada.
- **Geração das ferramentas:** o estudo de Kazemitabaar et al. (2023) utilizou o Codex, de uma geração anterior de modelos, com participantes de 10 a 17 anos.
- **Uso frequente de LLMs:** o uso frequente se correlacionou negativamente com o desempenho em *vibe coding* (r = −0,258, p = 0,010) e com a escrita (r = −0,282, p = 0,005). Não houve correlação com o conhecimento em computação (r = 0,001) (THORGEIRSSON; WEIDMANN; SU, 2026). A direção dessa relação não foi determinada. O uso pode enfraquecer a capacidade de expressão, ou quem escreve pior pode recorrer mais à IA (ELHARDT, 2026).

## Conclusão

As evidências analisadas indicam que a possibilidade de construir software sem ler ou escrever código não elimina a necessidade de conhecimento técnico. Ela desloca o lugar onde esse conhecimento é aplicado: da escrita do código para a especificação do que deve existir e para a avaliação do comportamento obtido.

No estudo-âncora, o conhecimento em computação foi o preditor com maior variância única, mesmo sem acesso ao código. O estudo de Lucchetti et al. (2025) mostra que o sucesso depende do conteúdo da especificação, e não do vocabulário. O estudo de Kazemitabaar et al. (2023) indica que a ferramenta beneficia mais quem já possui uma base prévia.

Dessa forma, com base nos estudos analisados, uma pessoa preparada para transformar uma ideia em software com auxílio de IA:

- compreende como um programa se estrutura, sabendo decompor o problema em partes e fluxos;
- sabe quais elementos precisam existir além da funcionalidade visível, como tratamento de falhas, concorrência e configuração;
- consegue expressar requisitos com conteúdo completo, independentemente do vocabulário utilizado;
- consegue diagnosticar um comportamento incorreto a partir do que observa no software gerado.

### Como isso se relaciona com a gerência de configuração

Segundo Weidmann, no *vibe coding* a escrita dos prompts passa a ser uma forma de programação (ELHARDT, 2026). Se a especificação ocupa o lugar do código, os prompts, as regras persistentes e os requisitos passam a ser artefatos do projeto. Por isso, precisam ser identificados, versionados e rastreados da mesma forma que o código-fonte.

A própria plataforma do estudo-âncora oferecia retorno a versões anteriores do aplicativo, o que mostra que mesmo o *vibe coding* "puro" depende de controle de versão. No entanto, decidir qual versão está correta exige saber avaliar o comportamento do software, o que remete novamente ao conhecimento técnico.

Há ainda uma relação direta com a identificação dos itens de configuração. No exemplo do PDV, o certificado digital, os endereços da SEFAZ por ambiente (homologação e produção) e os parâmetros de contingência são itens de configuração. Quem não sabe que eles existem não os solicita ao agente e, consequentemente, não os coloca sob controle.

Dentre os mecanismos de gerência de configuração aplicáveis a esse cenário, podemos citar:

- versionamento de prompts, especificações e regras persistentes junto ao código;
- identificação dos itens de configuração do domínio, como certificados, endpoints e parâmetros por ambiente;
- baselines que permitam retornar a uma versão de comportamento conhecido;
- registro de requisitos não funcionais, como contingência e concorrência, como itens rastreáveis.

Esses mecanismos dependem de que a pessoa saiba o que precisa ser controlado. A gerência de configuração garante o controle sobre o que foi identificado, mas a identificação depende da base técnica de quem especifica o software.

## Referências

- KARPATHY, Andrej. *There's a new kind of coding I call "vibe coding"* [...]. X, 2 fev. 2025. Disponível em: <https://x.com/karpathy/status/1886192184808149383>. Acesso em: 13 out. 2026.
- THORGEIRSSON, Sverrir; WEIDMANN, Theo B.; SU, Zhendong. *Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency*. Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems, 2026. DOI: <https://doi.org/10.1145/3772318.3791666>. Disponível em: <https://arxiv.org/abs/2603.14133>. Acesso em: 13 out. 2026.
- ELHARDT, Christoph. *What skills do people need to successfully program with AI?* ETH News, 30 abr. 2026. Disponível em: <https://ethz.ch/en/news-and-events/eth-news/news/2026/04/what-skills-do-people-need-to-successfully-program-with-ai.html>. Acesso em: 13 out. 2026.
- LUCCHETTI, Francesca et al. *Substance Beats Style: Why Beginning Students Fail to Code with LLMs*. Proceedings of the 2025 Conference of the Nations of the Americas Chapter of the Association for Computational Linguistics (NAACL), 2025. DOI: <https://doi.org/10.18653/v1/2025.naacl-long.433>.
- KAZEMITABAAR, Majeed et al. *Studying the Effect of AI Code Generators on Supporting Novice Learners in Introductory Programming*. Proceedings of the 2023 CHI Conference on Human Factors in Computing Systems, 2023. DOI: <https://doi.org/10.1145/3544548.3580919>.

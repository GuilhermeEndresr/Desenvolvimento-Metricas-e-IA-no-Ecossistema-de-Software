# O que sobra para o humano: engenharia de software além da escrita de código

**Autor:** Daniel Pacheco Pires

## Contextualização

As partes anteriores deste trabalho mostraram que o conhecimento em Ciência da Computação e a habilidade de escrita preveem o desempenho em vibe coding, que a dependência precoce da IA pode gerar débito cognitivo e que o código gerado exige verificação. Esta parte trata da pergunta norteadora que fica entre esses resultados: **se a máquina escreve o código, o que sobra para o humano saber?**

Para responder, são usadas três fontes complementares indicadas para o tema:

- a distinção entre *vibe coding* e programação assistida por IA, proposta por Simon Willison;
- o corpo de conhecimento oficial da engenharia de software, o SWEBOK v4, mapeado para o framework de competências SFIA 9;
- as discussões da Thoughtworks sobre o futuro da engenharia de software.

A tese defendida é que **escrever código sempre foi apenas uma parte da engenharia de software**. A IA reduz o custo dessa parte, mas não elimina as demais. Elas passam a ocupar uma proporção maior do trabalho humano.

## Nem toda programação com IA é vibe coding

O termo *vibe coding* foi cunhado por Andrej Karpathy em fevereiro de 2025 (KARPATHY, 2025). Na descrição original, a pessoa aceita todas as alterações sem ler as diferenças, cola mensagens de erro sem comentário e deixa o código crescer além da própria compreensão. O próprio Karpathy limita o uso a projetos descartáveis de fim de semana.

Poucas semanas depois, Simon Willison publicou uma crítica ao uso ampliado do termo (WILLISON, 2025). Para ele, vibe coding significa **construir software com um LLM sem revisar o código que ele escreve**. Quando o código gerado é revisado, testado e compreendido a ponto de poder ser explicado a outra pessoa, o que se tem é desenvolvimento de software comum, e o fato de um LLM ter participado é irrelevante. Willison adota como regra pessoal não commitar no repositório nenhum código que não consiga explicar.

Willison não condena o vibe coding. Ele o considera adequado para protótipos e ferramentas pessoais de baixo risco e uma forma de iniciantes superarem a curva inicial de aprendizado. Mas lista os pontos em que ele deixa de ser seguro: projetos que podem causar dano a outras pessoas, código que manipula segredos (como chaves de API), dados privados e serviços cobrados por uso.

### Por que essa distinção importa para o artigo-âncora

O estudo de Thorgeirsson, Weidmann e Su (2026) estudou deliberadamente a variante "pura" do vibe coding: o código ficava borrado e o participante só via o chat e a prévia do aplicativo. Os próprios autores afirmam que os resultados podem não se aplicar diretamente a fluxos em que o código pode ser revisado (seção 10.2) e que a estimativa do papel da computação deve ser vista como um limite inferior (seção 10.1).

Ou seja, o estudo mede o caso em que o humano tem **menos** pontos de intervenção. Mesmo nesse caso, o conhecimento em computação fez diferença. No uso profissional descrito por Willison, em que o código é lido, testado e assumido por alguém, as oportunidades de aplicar esse conhecimento são maiores: revisar, depurar, rejeitar uma solução e explicar o que foi feito.

## O que o corpo de conhecimento diz que o engenheiro faz

O SWEBOK v4 (*Guide to the Software Engineering Body of Knowledge*), publicado pela IEEE Computer Society em 2024, organiza a profissão em **18 áreas de conhecimento**. O SFIA, framework internacional de competências profissionais, mapeia cada área para as competências do SFIA 9 (SFIA FOUNDATION, 2026).

| Grupo | Áreas de conhecimento do SWEBOK v4 |
|---|---|
| Entender o problema | Requisitos; Modelos e Métodos |
| Decidir a estrutura | Arquitetura; Design |
| Produzir | **Construção** |
| Garantir que funciona | Testes; Qualidade; Segurança |
| Manter funcionando | Operações; Manutenção; **Gerência de Configuração** |
| Organizar o trabalho | Gestão; Processo; Economia; Prática Profissional |
| Fundamentos | Computação; Matemática; Engenharia |

A escrita do código está concentrada na área de Construção, que o SWEBOK descreve como a criação de software funcional por meio de codificação, verificação, testes unitários e de integração e depuração. É nessa área, e principalmente na parte de codificação, que os assistentes de IA atuam com mais força. As outras dezessete áreas tratam de decisões que a IA pode apoiar, mas que exigem alguém que conheça o problema, responda pelo resultado e escolha entre alternativas.

Essa visão coincide com a de Willison. Para ele, o trabalho do desenvolvedor não é apenas produzir código e funcionalidades, mas produzir código que comprovadamente funciona, que outras pessoas entendem e que permite evolução futura, equilibrando desempenho, acessibilidade, segurança, manutenibilidade e custo.

### Os fundamentos como o que diferencia o profissional

Três das 18 áreas do SWEBOK são de fundamentos: Computação, Matemática e Engenharia. O mapeamento SFIA explica que, enquanto as outras quinze descrevem práticas, essas três descrevem as ferramentas de raciocínio que sustentam todas as práticas.

O mapeamento contrasta dois perfis de profissional:

| Com base nos fundamentos | Sem base nos fundamentos |
|---|---|
| Resolve problemas de forma robusta e flexível | Tem capacidade limitada de resolver problemas |
| Entende, explica e modifica métodos | Depende de padrões e modelos prontos |
| Enfrenta desafios novos e complexos | Tem dificuldade com o que é novo ou complexo |
| Age de forma proativa | Age de forma reativa |

Fonte: adaptado de SFIA Foundation (2026).

O perfil "sem fundamentos" descreve exatamente o risco de quem usa IA sem base: depender do que a ferramenta entrega, sem conseguir explicar nem modificar. É o mesmo comportamento encontrado por Lucchetti et al. (2025), em que iniciantes repetiam reescritas superficiais do prompt sem acrescentar informação. O resultado do artigo-âncora, em que o conhecimento em computação foi o preditor mais forte mesmo controlando o raciocínio geral, é coerente com a importância que o SWEBOK dá a essas áreas.

## A visão da indústria: o que a Thoughtworks está discutindo

Em 2026, a Thoughtworks organizou dois encontros chamados *The Future of Software Development* (ou *Future of Software Engineering*): o primeiro em Deer Valley (EUA), em fevereiro, marcando os 25 anos do Manifesto Ágil, e o segundo em Engelberg (Suíça), em junho (FOWLER, 2026). Os encontros reuniram profissionais da indústria para discutir como a IA e os LLMs afetam a profissão.

Duas conclusões publicadas a partir dessas discussões se relacionam diretamente com o tema.

**Volta aos fundamentos.** A edição de abril de 2026 do Technology Radar da Thoughtworks recomenda um retorno aos fundamentos de engenharia para enfrentar o débito cognitivo gerado pelo aumento da complexidade do software produzido com IA (THOUGHTWORKS, 2026). A indústria chega, por outro caminho, à mesma preocupação levantada pelo estudo de Kosmyna et al. (2025).

**Requisitos não funcionais como proteção.** Andrew Harmel-Law, diretor de tecnologia da Thoughtworks, argumenta que os LLMs entregam funcionalidades com facilidade, mas não consideram por conta própria as qualidades sistêmicas que mantêm essas funcionalidades confiáveis, seguras e escaláveis (HARMEL-LAW, 2026). Segundo ele, os modelos podem incorporar requisitos não funcionais, mas não os deduzem sozinhos, e esse ponto cego é o mesmo que já existia no desenvolvimento manual. Ele observa ainda que executivos que fazem vibe coding de protótipos tendem a confundir uma demonstração impressionante com um sistema pronto para produção.

A proposta dele é especificar requisitos não funcionais de forma explícita e testável **antes** de começar a usar o agente, e registrar as decisões de compromisso (*trade-offs*) em registros de decisão de arquitetura (ADRs). A decisão continua sendo humana; a IA reduz o esforço de documentá-la.

Essa visão reforça o exemplo do PDV apresentado na parte do Fernando: contingência, concorrência e certificado digital não aparecem se ninguém os pedir. O que sobra para o humano é saber que eles existem e especificá-los de forma verificável.

## Síntese: o que sobra para o humano saber

Juntando as três fontes, o trabalho humano no desenvolvimento assistido por IA se concentra em quatro responsabilidades:

1. **Definir o problema.** Levantar requisitos, inclusive os não funcionais, e expressá-los de forma completa e testável (SWEBOK: Requisitos; Harmel-Law).
2. **Decidir.** Escolher arquitetura e design, avaliar alternativas e registrar os compromissos assumidos (SWEBOK: Arquitetura, Design, Economia; ADRs).
3. **Responder pelo resultado.** Revisar, testar e conseguir explicar o que vai para produção (Willison; SWEBOK: Testes, Qualidade, Segurança).
4. **Controlar a evolução.** Saber o que mudou, por que mudou e como voltar atrás (SWEBOK: Gerência de Configuração, Manutenção, Operações).

Todas dependem dos fundamentos. Sem eles, o profissional não sabe o que especificar, não reconhece uma decisão ruim e não consegue explicar o código que aceitou.

## Conclusão

A IA não tira do humano a necessidade de saber engenharia de software. Ela muda a proporção do trabalho: a escrita do código, que é uma parte de uma das 18 áreas do SWEBOK, fica mais barata, e o peso relativo das outras aumenta.

O vibe coding "puro" é adequado para protótipos e ferramentas pessoais de baixo risco, como reconhecem o próprio Karpathy e Willison. Para software que outras pessoas vão usar, o código precisa ser revisado, testado e compreendido, e isso exige as mesmas competências que sempre definiram o engenheiro de software. O artigo-âncora mostra que essas competências já fazem diferença mesmo quando o código está escondido. Em fluxos profissionais, onde o código é revisado, elas têm ainda mais oportunidades de serem aplicadas.

## Como isso se relaciona com a gerência de configuração

A Gerência de Configuração é uma das 18 áreas do SWEBOK v4. O guia a define como os processos e técnicas para identificar, controlar, rastrear e auditar mudanças nos artefatos de software ao longo do ciclo de vida, mantendo a integridade e a rastreabilidade dos itens de configuração (SFIA FOUNDATION, 2026). No mapeamento SFIA, ela corresponde às competências de gerência de configuração (CFMG), integração e build (SINT), implantação (DEPL) e gestão de releases (RELM).

Com a IA produzindo mais código em menos tempo, essa área ganha importância por três motivos:

- **A regra de Willison depende dela.** "Não commitar o que não se consegue explicar" pressupõe controle de versão e revisão antes da integração. O commit é o ponto em que o humano assume a responsabilidade pelo que a IA gerou.
- **Os requisitos não funcionais viram itens de configuração.** Se, como propõe Harmel-Law, os requisitos não funcionais devem ser especificações testáveis e as decisões devem ser registradas em ADRs, esses documentos passam a ser artefatos do projeto, que precisam ser versionados e rastreados junto com o código.
- **Identificar exige conhecimento do domínio.** A gerência de configuração controla o que foi identificado, mas a identificação depende de quem conhece o sistema.

**Exemplo prático.** Na implantação de um ERP em uma indústria, os cadastros de itens precisaram ser refeitos do zero. Antes de cadastrar qualquer item, foi necessário definir regras de codificação e padronização, estruturar as listas de materiais dos produtos e validar os dados. Essas regras são, na prática, a identificação dos itens de configuração do sistema. Uma ferramenta de IA poderia gerar milhares de cadastros rapidamente, mas não decidiria sozinha qual deve ser a regra de codificação, e quem não conhece o processo produtivo não perceberia uma regra errada. É o mesmo princípio que se aplica ao código: a IA acelera a produção, e o humano continua responsável por definir o que deve existir e por verificar o que foi entregue.

Dentre os mecanismos de gerência de configuração aplicáveis a esse cenário, podem ser citados:

- revisão obrigatória antes do merge, garantindo que alguém consiga explicar cada alteração;
- versionamento de requisitos não funcionais, especificações e ADRs junto ao código;
- testes automatizados derivados dos requisitos não funcionais, executados no pipeline;
- baselines que permitam voltar a uma versão de comportamento conhecido;
- rastreabilidade entre requisito, decisão, alteração e teste.

## Referências

FOWLER, Martin. **Future Of Software Development**. martinfowler.com, 2 jul. 2026. Disponível em: https://www.martinfowler.com/bliki/FutureOfSoftwareDevelopment.html. Acesso em: 14 out. 2026.

HARMEL-LAW, Andrew. **Are non-functional requirements the missing guardrail for AI-generated code?** Thoughtworks, 8 jul. 2026. Disponível em: https://www.thoughtworks.com/insights/blog/architecture/non-functional-requirements-missing-guardrail-ai-generated-code. Acesso em: 14 out. 2026.

KARPATHY, Andrej. **There's a new kind of coding I call "vibe coding" [...]**. X, fev. 2025. Disponível em: https://x.com/karpathy/status/1886192184808149383. Acesso em: 14 out. 2026.

KOSMYNA, Nataliya et al. **Your Brain on ChatGPT: Accumulation of Cognitive Debt when Using an AI Assistant for Essay Writing Task**. MIT Media Lab, 2025. Disponível em: https://arxiv.org/abs/2506.08872. Acesso em: 14 out. 2026.

LUCCHETTI, Francesca et al. **Substance Beats Style: Why Beginning Students Fail to Code with LLMs**. In: Proceedings of the 2025 Conference of the Nations of the Americas Chapter of the Association for Computational Linguistics (NAACL), 2025. DOI: https://doi.org/10.18653/v1/2025.naacl-long.433.

SFIA FOUNDATION. **SFIA v9 and SWEBOK v4: The guide to the software engineering body of knowledge**. 2026. Disponível em: https://sfia-online.org/en/tools-and-resources/bodies-of-knowledge/swebok-software-engineering-body-of-knowledge/swebok4-sfia9-the-guide-to-the-software-engineering-body-of-knowledge. Acesso em: 14 out. 2026.

THORGEIRSSON, Sverrir; WEIDMANN, Theo B.; SU, Zhendong. **Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency**. In: Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems (CHI '26). New York: ACM, 2026. DOI: https://doi.org/10.1145/3772318.3791666.

THOUGHTWORKS. **As AI Accelerates Software Complexity, Thoughtworks Technology Radar Urges a Return to Engineering Fundamentals to Combat Cognitive Debt**. 15 abr. 2026. Disponível em: https://www.thoughtworks.com/about-us/news. Acesso em: 14 out. 2026.

WILLISON, Simon. **Not all AI-assisted programming is vibe coding (but vibe coding rocks)**. Simon Willison's Weblog, 19 mar. 2025. Disponível em: https://simonwillison.net/2025/Mar/19/vibe-coding/. Acesso em: 14 out. 2026.

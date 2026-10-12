# Habilidades essenciais no desenvolvimento de software assistido por IA

**Autor: Guilherme Endres**

---

## Contextualização

Inicialmente, é importante compreender a proporção atual de código produzido com o auxílio de ferramentas de inteligência artificial. O relatório *State of Code Developer Survey Report*, publicado pela Sonar, apresenta os resultados de uma pesquisa realizada com 1.149 profissionais de tecnologia, majoritariamente ligados à engenharia de software. Todos os participantes haviam utilizado IA em seu trabalho no período de um ano anterior à pesquisa.

Segundo a estimativa dos desenvolvedores entrevistados, 42% do código que eles commitam atualmente é gerado ou assistido por ferramentas de IA. Esse resultado é autodeclarado e, portanto, não corresponde a uma medição direta dos repositórios, mas oferece um indicativo da participação que essas ferramentas já possuem no processo de desenvolvimento de software.

![Proporção de código gerado ou assistido por IA](imagens/State%20of%20Code%20Developer%20Survey%20report-1.png)

<br><br>

O mesmo relatório investigou quais habilidades são consideradas mais importantes em um ambiente de desenvolvimento assistido por IA. As respostas de maior incidência estão relacionadas tanto à capacidade de fornecer instruções e contexto adequados às ferramentas quanto à habilidade de revisar, validar e corrigir suas saídas.

![Habilidades importantes no desenvolvimento assistido por IA](imagens/State%20of%20Code%20Developer%20Survey%20report-2.png)

<br><br>

A necessidade de validação torna-se ainda mais evidente quando se observa que apenas 48% dos entrevistados afirmaram sempre verificar o código assistido por IA antes de realizar o commit. Além disso, 96% não confiam completamente que o código gerado por IA esteja funcionalmente correto, enquanto 38% afirmam que sua revisão exige mais esforço do que a revisão de código escrito por outros desenvolvedores. Esses resultados indicam o surgimento de um gargalo de verificação: a capacidade de produzir código aumentou, mas a necessidade de avaliá-lo antes da integração permaneceu sob responsabilidade dos profissionais e das práticas de garantia de qualidade.

![Frequência de verificação do código gerado por IA](imagens/State%20of%20Code%20Developer%20Survey%20report-3.png)

![Frequência de desenvolvedores que não confiam em código gerado por IA](imagens/State%20of%20Code%20Developer%20Survey%20report-4.png)
<br><br>

Com base nesses resultados e no levantamento das operações que envolvem a interação com agentes baseados em LLM, o processo pode ser dividido, para fins desta análise, em duas etapas: entrada e saída.

## Entrada

A entrada compreende os elementos utilizados para fornecer instruções, contexto, restrições e recursos ao agente. Nessa etapa podem ser incluídos prompts, arquivos, regras persistentes, servidores MCP e os recursos disponibilizados pelo ambiente ou pela IDE utilizada.

O artigo *Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency* apresenta indícios de que o conhecimento em Ciência da Computação e a habilidade de comunicação escrita estão positivamente associados ao desempenho na construção de aplicações por meio de agentes baseados em LLM.

No estudo, o desempenho em Ciência da Computação apresentou correlação de 0,39 com o desempenho nas tarefas de *vibe coding*, enquanto a habilidade de escrita apresentou correlação de 0,29.

## Saída

A saída corresponde aos artefatos produzidos pelo agente, como código-fonte, testes, arquivos de configuração, documentação e propostas de alteração. Nessa etapa, as habilidades do desenvolvedor se concentram na supervisão, adaptação, verificação e integração desses artefatos.

O artigo *Human-Written vs. AI-Generated Code: A Large-Scale Study of Defects, Vulnerabilities, and Complexity* descreve essa transformação como uma redefinição estrutural do desenvolvimento de software. Nesse contexto, o papel do desenvolvedor passa gradualmente da autoria direta de cada trecho de código para a supervisão e adaptação das saídas dos modelos, aproximando-se do papel de curador dos artefatos produzidos.

Diante disso, compreender os padrões, as limitações e os pontos de atenção do código gerado por LLMs torna-se essencial para identificar quais habilidades o desenvolvedor precisa possuir a fim de utilizar essas ferramentas sem comprometer a qualidade, a segurança e a manutenibilidade das soluções desenvolvidas.

### Código escrito por humanos VS Código escrito por IAs

Com o objetivo de compreender as diferenças entre o código gerado por agentes baseados em LLM e o código produzido por humanos, o estudo classificou as amostras em três dimensões de qualidade de software:

1. Defeitos de código;
2. Vulnerabilidades de segurança;
3. Complexidade estrutural.

Como alvo da análise, foram reunidas mais de 500 mil amostras de código em duas linguagens amplamente utilizadas: Python e Java. O conjunto incluiu código humano extraído de mais de 17 mil projetos públicos do GitHub e implementações geradas pelo ChatGPT, DeepSeek-Coder e Qwen-Coder.

![Composição do conjunto de dados](imagens/Human-Written%20vs%20AI-Generated%20Code%20-%20Table%202.png)

#### Defeitos de código

O estudo considera defeito qualquer violação relacionada à correção, à lógica, ao desempenho ou ao projeto do código. Para identificar esses problemas, foram utilizadas as ferramentas Pylint, para Python, e PMD, para Java. Os resultados foram organizados com base na classificação ODC (*Orthogonal Defect Classification*), permitindo comparar categorias de defeitos entre linguagens e autores diferentes.

![Resultados da análise de defeitos](imagens/Human-Written%20vs%20AI-Generated%20Code%20-%20Table%203.png)

- **Amostra defeituosa:** contém pelo menos um problema detectado pela ferramenta de análise.
- **Amostra incorreta:** não pôde ser analisada adequadamente, por exemplo, por apresentar sintaxe inválida.

#### Vulnerabilidades de segurança

O estudo encontrou maior incidência de vulnerabilidades de alto risco em código gerado por IA, incluindo problemas como injeção de comandos e segredos inseridos diretamente no código.

![Resultados da análise de vulnerabilidades](imagens/Human-Written%20vs%20AI-Generated%20Code%20-%20Table%204.png)

#### Complexidade estrutural

Para comparar as características estruturais das amostras, o estudo utilizou as seguintes métricas:

![Resultados da análise de complexidade](imagens/Human-Written%20vs%20AI-Generated%20Code%20-%20Table%205.png)

- **Número de Linhas de Código (NLOC):** representa o tamanho do bloco de código, desconsiderando comentários.
- **Complexidade Ciclomática (CCN):** mede a quantidade de caminhos de controle independentes presentes em uma função, indicando seu nível de ramificação e tomada de decisão.
- **Contagem de Tokens (TC):** representa a quantidade de unidades lexicais, como identificadores, operadores, constantes e palavras-chave.
- **Comprimento do Nome da Função (FNL):** funciona como um indicador indireto da especificidade semântica dos nomes utilizados.
- **Tokens Únicos (UT):** representa a variedade de tokens distintos no conjunto analisado, funcionando como indicador de diversidade lexical.

#### Resultado da comparação

Os dados indicam que o código escrito por humanos tende a apresentar maior complexidade estrutural e maior concentração de problemas relacionados à manutenção, ao tratamento de exceções e ao projeto. Já o código gerado por IA tende a ser mais curto, simples e repetitivo, mas apresenta maior ocorrência de determinados defeitos e vulnerabilidades de segurança de alta gravidade.

## Conclusão

A análise dos três estudos indica que o crescimento do uso de ferramentas de IA não elimina a importância dos conhecimentos tradicionais de desenvolvimento de software. Em vez disso, modifica a maneira como essas competências são aplicadas ao longo do processo.

Na etapa de entrada, conhecimentos em Ciência da Computação e habilidades de escrita estão associados a um melhor desempenho na especificação de aplicações por meio de linguagem natural. Na etapa de saída, o aumento do volume de código gerado amplia a necessidade de revisão, validação e controle de qualidade, especialmente porque o código produzido por IA apresenta defeitos, repetição estrutural e vulnerabilidades de segurança.

Dessa forma, as seguintes características constituem fortes indicadores de um desenvolvedor preparado para atuar em ambientes assistidos por IA:

- possui conhecimentos fundamentais de Ciência da Computação;
- consegue transpor ideias e requisitos para textos completos, claros e coerentes;
- identifica erros funcionais, problemas de manutenção e vulnerabilidades;
- consegue indentificar erros funcionais, vulnerabiliades de segurança, mantendo um bom nivel de complexidade estrutural e manutenibilidade.

### Como isso se relaciona com a gerência de configuração

A necessidade de supervisionar e validar o código produzido por IA aproxima diretamente o tema deste relatório dos fundamentos da gerência de configuração. À medida que agentes baseados em LLM passam a produzir uma parcela maior dos artefatos do projeto, torna-se necessário garantir que essas alterações sejam identificáveis, controladas, verificadas e integradas de maneira segura.

A gerência de configuração fornece mecanismos para que o aumento da velocidade de geração não resulte em perda de controle sobre o produto. Dentre esses mecanismos podemos citar:

- configurações dos agentes;
- prompts e regras persistentes relevantes;
- testes unitários;
- análise estática
- controle de versão
- testes de integração;
- verificação de formatação;
- policies
- pipelines
- revisão de código

Esses elementos e outros unificados podem formar uma sequencia de controle que auxilia na mitigação de falhas produzidas por IA.

## Referências

- SONAR. *State of Code Developer Survey Report: The current reality of AI coding*. 2026. Disponível em: <https://www.sonarsource.com/blog/state-of-code-developer-survey-report-the-current-reality-of-ai-coding/>. Acesso em: 12 out. 2026.
- THORGEIRSSON, Sverrir; WEIDMANN, Theo B.; SU, Zhendong. *Computer Science Achievement and Writing Skills Predict Vibe Coding Proficiency*. Proceedings of the 2026 CHI Conference on Human Factors in Computing Systems, 2026. DOI: <https://doi.org/10.1145/3772318.3791666>.
- COTRONEO, Domenico; IMPROTA, Cristina; LIGUORI, Pietro. *Human-Written vs. AI-Generated Code: A Large-Scale Study of Defects, Vulnerabilities, and Complexity*. 2025. Disponível em: <https://arxiv.org/abs/2508.21634>. Acesso em: 12 out. 2026.
# MÓDULO 1 — FUNDAMENTOS DA REPRODUTIBILIDADE CIENTÍFICA

## Apresentação do módulo

A ciência depende da produção de conhecimentos fundamentados em evidências, métodos sistemáticos e procedimentos que permitam avaliar criticamente os resultados apresentados pelos pesquisadores. Uma descoberta científica não deve ser considerada confiável apenas porque foi publicada em uma revista especializada ou porque seus resultados parecem coerentes com determinada hipótese. É necessário que os procedimentos utilizados sejam suficientemente claros para que outros pesquisadores possam compreender como as conclusões foram obtidas, avaliar a adequação dos métodos e, quando possível, verificar os resultados por meio de novas análises ou investigações independentes.

Nesse contexto, a reprodutibilidade científica constitui um dos fundamentos da confiabilidade da pesquisa. Ela está relacionada à possibilidade de verificar resultados, compreender os procedimentos que os produziram e identificar as condições necessárias para sua obtenção. Sua importância tornou-se ainda maior com a incorporação de computadores, algoritmos, bancos de dados, modelos estatísticos e técnicas de inteligência artificial às atividades de pesquisa.

Em diversas áreas, os resultados científicos dependem de operações computacionais complexas. Um estudo pode utilizar conjuntos de dados extensos, bibliotecas de software, configurações específicas de hardware, algoritmos de processamento e parâmetros experimentais que influenciam diretamente os resultados. Quando essas informações não são adequadamente documentadas ou disponibilizadas, torna-se difícil verificar o trabalho publicado e avaliar a confiabilidade de suas conclusões.

Este capítulo apresenta os fundamentos conceituais da reprodutibilidade científica, diferencia termos frequentemente utilizados nesse contexto, discute a crise de reprodutibilidade e examina os desafios específicos das pesquisas computacionais e de Aprendizado de Máquina (Machine Learning). Também aborda a relação entre reprodutibilidade, Ciência Aberta e transparência científica, além de apresentar as principais barreiras que dificultam a verificação de resultados.

Ao final do módulo, espera-se que o leitor compreenda por que a reprodutibilidade é essencial à atividade científica e reconheça os elementos que permitem tornar uma pesquisa computacional verificável, transparente e passível de reutilização.

## 1.1. Conceito de reprodutibilidade científica

A reprodutibilidade científica está relacionada à possibilidade de verificar resultados de uma pesquisa por meio da aplicação novamente dos procedimentos utilizados em sua produção. Entretanto, o significado específico do termo varia entre disciplinas e comunidades científicas. Goodman, Fanelli e Ioannidis (2016) observam que não existe uma utilização terminológica completamente uniforme para expressões como reprodutibilidade, replicabilidade e repetibilidade. Essa diversidade pode gerar interpretações diferentes sobre o que significa reproduzir um resultado científico.

Para estabelecer uma distinção operacional, este material adota como referência as definições apresentadas pelo relatório Reproducibility and Replicability in Science, publicado pela National Academies of Sciences, Engineering, and Medicine (2019). Nesse enquadramento, a reprodutibilidade corresponde à obtenção de resultados computacionais consistentes utilizando os mesmos dados de entrada, procedimentos computacionais, métodos, códigos e condições de análise empregados no estudo original.

Essa definição é particularmente relevante para pesquisas que utilizam programação, análise estatística, simulações numéricas e Aprendizado de Máquina. Nesses casos, não basta apresentar uma descrição geral do método: é necessário disponibilizar informações suficientes para que os procedimentos computacionais possam ser examinados e executados novamente.

Por exemplo, considere uma pesquisa que desenvolveu um modelo de Aprendizado de Máquina para classificar imagens médicas. O artigo informa que foi utilizada uma rede neural convolucional, mas não apresenta o código-fonte, a versão da biblioteca utilizada, os parâmetros de treinamento, a divisão dos dados ou os procedimentos de pré-processamento.

Embora o artigo apresente os resultados obtidos, outro pesquisador não dispõe de informações suficientes para reconstruir precisamente o experimento. A descrição do algoritmo, isoladamente, não garante que os resultados possam ser reproduzidos.

A reprodutibilidade exige, portanto, uma combinação de elementos científicos e técnicos. Entre eles, destacam-se:

- Dados de entrada: correspondem aos conjuntos de dados utilizados na análise. Sua identificação, organização e disponibilização, respeitadas as restrições legais e éticas, permitem que outros pesquisadores utilizem a mesma fonte de informação.
- Métodos e procedimentos: descrevem as etapas realizadas para transformar os dados em resultados. Incluem protocolos experimentais, algoritmos, critérios de seleção e procedimentos estatísticos.
- Código computacional: contém as instruções responsáveis pela execução das operações. Sua disponibilização permite examinar como os métodos foram implementados.
- Ambiente computacional: compreende as condições técnicas necessárias à execução, como sistema operacional, linguagem de programação, bibliotecas, versões de software e recursos de hardware.
- Parâmetros e configurações: correspondem aos valores utilizados durante a execução de algoritmos e experimentos. Podem incluir hiperparâmetros, sementes aleatórias, critérios de parada e configurações de processamento.
- Documentação: registra as informações necessárias para compreender, executar e interpretar os procedimentos.

Esses elementos não devem ser tratados como componentes independentes. A ausência de qualquer um deles pode comprometer a capacidade de reconstruir o processo computacional.

### Reprodutibilidade como propriedade do processo científico

É importante compreender que a reprodutibilidade não é simplesmente uma característica do código-fonte ou de um arquivo disponibilizado em um repositório. Ela resulta da organização de todo o processo de pesquisa.

Um código pode estar publicamente disponível, mas não ser executável por falta de dependências. Um conjunto de dados pode estar acessível, mas não possuir documentação suficiente para que suas variáveis sejam interpretadas corretamente. Um experimento pode ser descrito detalhadamente, mas depender de parâmetros que não foram registrados.

Dessa forma, a reprodutibilidade deve ser considerada desde o planejamento da pesquisa, e não apenas como uma etapa posterior à publicação dos resultados.

Peng (2011) destaca a importância da pesquisa reproduzível na ciência computacional, argumentando que a disponibilização dos dados e dos procedimentos computacionais constitui uma condição fundamental para avaliar resultados produzidos por análises baseadas em computador.

Figura 1 — Elementos fundamentais da reprodutibilidade científica

Descrição do infográfico: apresentar um diagrama com seis blocos interligados, dispostos ao redor de um elemento central denominado “Resultado científico”. Os blocos devem representar: dados de entrada, métodos, código-fonte, ambiente computacional, parâmetros experimentais e documentação. Setas bidirecionais devem indicar que esses elementos se relacionam durante a execução e a verificação da pesquisa. Na parte inferior, apresentar a mensagem: “A reprodutibilidade depende da integração entre dados, métodos, código e condições de execução”.

### Exemplo 1 — Reprodução de uma análise estatística

Um pesquisador publica um artigo sobre a relação entre escolaridade e renda utilizando uma base de dados pública. No artigo, informa que realizou uma regressão linear e apresenta os coeficientes estimados.

Para permitir a reprodução da análise, disponibiliza:

1. O conjunto de dados original ou sua identificação e forma de acesso.
2. O código utilizado para importar e preparar os dados.
3. As instruções de execução da regressão.
4. As versões das bibliotecas estatísticas utilizadas.
5. Os resultados produzidos pelo programa.

Outro pesquisador pode executar os mesmos procedimentos e verificar se obtém os mesmos coeficientes, considerando as mesmas entradas e condições de análise.

Nesse exemplo, a reprodutibilidade está associada à possibilidade de executar novamente a análise original, e não necessariamente à realização de uma nova pesquisa com participantes diferentes.

## 1.2. Diferenças entre reprodutibilidade, replicabilidade, repetibilidade, robustez e transparência computacional

Os termos relacionados à verificação científica são frequentemente utilizados como sinônimos, embora representem aspectos distintos da avaliação de resultados. A falta de uma distinção clara pode levar a interpretações equivocadas, especialmente quando um estudo é considerado reproduzível apenas porque seus métodos foram descritos ou quando uma nova pesquisa é chamada de reprodução sem que seus procedimentos sejam devidamente caracterizados.

Goodman, Fanelli e Ioannidis (2016) discutem essas diferenças e demonstram que a terminologia varia entre áreas científicas. Para evitar ambiguidades, este capítulo utiliza as definições operacionais adotadas pela National Academies of Sciences, Engineering, and Medicine (2019), complementadas por uma distinção prática entre repetibilidade, robustez e transparência.

### Reprodutibilidade

A reprodutibilidade, no sentido computacional adotado neste material, consiste em obter resultados consistentes utilizando os mesmos dados, códigos, métodos e condições de análise do estudo original.

O objetivo é verificar se os procedimentos computacionais descritos e disponibilizados produzem os resultados apresentados pelos autores.

Exemplo: um pesquisador disponibiliza o código Python e os dados utilizados em uma análise de regressão. Outro pesquisador executa o mesmo código com os mesmos dados e verifica se os resultados são consistentes com aqueles apresentados no artigo.

### Replicabilidade

A replicabilidade consiste em obter resultados consistentes em estudos diferentes que investigam a mesma questão científica, mas utilizam novos dados.

Nesse caso, não se exige que o segundo estudo utilize exatamente os mesmos dados ou reproduza integralmente o ambiente computacional original. O objetivo é verificar se a evidência encontrada permanece consistente quando a investigação é realizada novamente.

Exemplo: uma pesquisa identifica associação entre determinada condição ambiental e o desenvolvimento de uma doença em uma população. Outro grupo realiza um estudo semelhante em uma população diferente, utilizando novos dados e procedimentos metodológicos comparáveis. Se os resultados forem compatíveis, haverá evidência de replicabilidade.

### Repetibilidade

A repetibilidade está relacionada à capacidade de obter resultados consistentes quando uma medição ou procedimento é realizado novamente sob condições essencialmente iguais.

Em geral, envolve a manutenção do mesmo método, instrumento, operador, local e intervalo de tempo relativamente curto, embora a definição operacional possa variar de acordo com a disciplina.

Exemplo: um laboratório realiza dez medições da concentração de uma substância em uma amostra utilizando o mesmo equipamento, o mesmo protocolo e as mesmas condições experimentais. A proximidade dos valores obtidos permite avaliar a repetibilidade do procedimento.

### Robustez

A robustez corresponde à estabilidade de um resultado diante de pequenas alterações nas condições de análise, nos parâmetros ou nas escolhas metodológicas.

Um resultado robusto não deve depender excessivamente de uma única configuração específica quando pequenas mudanças razoáveis não deveriam modificar substancialmente a conclusão.

Exemplo: um modelo de classificação apresenta desempenho semelhante quando são utilizadas diferentes sementes aleatórias, pequenas variações na divisão dos dados ou configurações próximas de hiperparâmetros. Essa estabilidade constitui evidência de robustez.

### Transparência computacional

A transparência computacional diz respeito à disponibilização e à documentação das informações necessárias para compreender como os resultados foram produzidos.

Ela envolve a descrição dos dados, códigos, métodos, parâmetros, ambientes computacionais e decisões tomadas durante a análise.

A transparência não garante, por si só, que os resultados sejam reproduzíveis. Entretanto, constitui uma condição importante para que a reprodução e a avaliação independente sejam possíveis.

Exemplo: um artigo disponibiliza o código-fonte, os dados, os arquivos de configuração, a documentação das bibliotecas e um roteiro de execução. Mesmo antes de executar o experimento, um leitor consegue examinar os procedimentos e compreender como os resultados foram produzidos.

### Quadro comparativo

| Conceito          | Característica central                           | Dados utilizados                                   | Objetivo                               |
| ----------------- | ------------------------------------------------ | -------------------------------------------------- | -------------------------------------- |
| Reprodutibilidade | Reexecução dos procedimentos originais           | Mesmos dados                                       | Verificar os resultados computacionais |
| Replicabilidade   | Nova investigação da mesma questão               | Novos dados                                        | Avaliar a consistência das evidências  |
| Repetibilidade    | Repetição sob condições semelhantes              | Mesma amostra ou material, conforme o procedimento | Avaliar a consistência das medições    |
| Robustez          | Estabilidade diante de pequenas alterações       | Podem ser os mesmos ou diferentes                  | Avaliar a sensibilidade dos resultados |
| Transparência     | Disponibilidade e documentação dos procedimentos | Dados e informações documentados                   | Permitir compreensão e verificação     |

Fonte: elaboração didática com base em Goodman, Fanelli e Ioannidis (2016) e National Academies of Sciences, Engineering, and Medicine (2019).

É importante destacar que esses conceitos não são mutuamente excludentes. Uma pesquisa pode ser transparente, reproduzível e robusta, mas ainda não ter sido replicada por outro grupo. Da mesma forma, uma pesquisa pode ser replicada com resultados consistentes, mesmo que seu processo computacional original não esteja completamente documentado.

A distinção também evita uma interpretação equivocada: reproduzir os resultados de uma análise não significa necessariamente comprovar que a hipótese científica está correta. A reprodução verifica a consistência dos procedimentos e resultados computacionais sob determinadas condições. A validade de uma conclusão científica depende também da qualidade dos dados, da adequação do método, das hipóteses e da interpretação das evidências.

Figura 2 — Relação entre os conceitos de verificação científica

Descrição do infográfico: representar cinco círculos parcialmente sobrepostos, identificados como reprodutibilidade, replicabilidade, repetibilidade, robustez e transparência computacional. No centro, inserir a expressão “Confiabilidade da evidência científica”. Utilizar setas para indicar que os conceitos contribuem de maneiras diferentes para a avaliação dos resultados, sem sugerir que sejam equivalentes.

## 1.3. Importância da reprodutibilidade para a confiabilidade e a credibilidade da ciência

A ciência é um processo cumulativo. Novos estudos são frequentemente desenvolvidos com base em resultados, métodos e teorias apresentados anteriormente. Quando uma pesquisa não pode ser adequadamente examinada ou seus procedimentos não são suficientemente documentados, torna-se mais difícil avaliar a confiabilidade das evidências utilizadas como fundamento para novas investigações.

A reprodutibilidade contribui para reduzir esse problema porque permite que outros pesquisadores examinem os procedimentos computacionais e verifiquem se os resultados apresentados são consistentes com os dados e métodos utilizados.

Munafò et al. (2017) argumentam que a confiabilidade e a eficiência da pesquisa científica dependem de melhorias em diferentes etapas do processo de investigação, incluindo métodos, relato dos resultados, disseminação, avaliação e incentivos institucionais.

A importância da reprodutibilidade pode ser compreendida a partir de diferentes dimensões.

### Verificação dos resultados

A reexecução dos procedimentos permite verificar se os resultados apresentados no artigo correspondem efetivamente àqueles produzidos pelos dados e pelo código disponibilizados.

Essa verificação pode revelar erros de programação, inconsistências na preparação dos dados, divergências entre os métodos descritos e implementados ou falhas na geração de tabelas e figuras.

### Identificação de erros metodológicos e computacionais

A disponibilização dos procedimentos permite que outros pesquisadores examinem as escolhas realizadas durante a análise.

Por exemplo, uma pesquisa pode apresentar uma divisão inadequada entre dados de treinamento e teste. Se informações do conjunto de teste forem utilizadas durante o treinamento, pode ocorrer vazamento de dados (data leakage), produzindo estimativas artificialmente elevadas de desempenho.

A análise independente dos procedimentos pode revelar esse problema, mesmo quando os resultados numéricos parecem convincentes.

### Aumento da confiança nos resultados publicados

A possibilidade de verificar uma análise oferece evidências adicionais de que os resultados não dependem exclusivamente da interpretação dos autores originais.

Isso não significa que toda pesquisa reproduzida esteja necessariamente correta. Significa que seus procedimentos podem ser examinados e que os resultados podem ser submetidos a uma avaliação independente.

### Facilitação do avanço científico

A pesquisa reproduzível permite que outros grupos aproveitem procedimentos já desenvolvidos, comparem métodos e construam novas investigações a partir de resultados anteriores.

Quando os códigos, dados e métodos estão organizados, documentados e disponíveis, diminui a necessidade de reconstruir integralmente etapas que já foram realizadas por outros pesquisadores.

### Redução de desperdício de recursos

A falta de documentação pode obrigar pesquisadores a repetir etapas de preparação, desenvolvimento e análise porque não conseguem compreender ou executar os procedimentos originais.

Uma pesquisa bem documentada facilita a reutilização de métodos e recursos computacionais, contribuindo para uma utilização mais eficiente do tempo, dos equipamentos e dos investimentos destinados à investigação científica.

### Contribuição para a integridade científica

A reprodutibilidade também contribui para a identificação de inconsistências e práticas inadequadas. A possibilidade de examinar dados, códigos e procedimentos torna mais difícil ocultar erros relevantes e facilita a avaliação crítica das decisões metodológicas.

Entretanto, é necessário distinguir erro científico de fraude. Resultados não reproduzidos podem decorrer de falhas técnicas, variabilidade natural, limitações metodológicas ou mudanças nas condições experimentais. A ausência de reprodução, isoladamente, não demonstra a existência de má conduta científica.

### Quadro — Principais contribuições da reprodutibilidade

| Dimensão               | Contribuição                                                                 |
| ---------------------- | ---------------------------------------------------------------------------- |
| Verificação            | Permite conferir se os resultados correspondem aos procedimentos executados. |
| Qualidade metodológica | Facilita a identificação de problemas nos métodos e nas análises.            |
| Credibilidade          | Oferece condições para avaliação independente dos resultados.                |
| Eficiência             | Favorece a reutilização de códigos, dados e procedimentos.                   |
| Integridade            | Facilita a identificação de inconsistências e erros.                         |
| Avanço científico      | Permite que novas pesquisas sejam construídas sobre resultados verificáveis. |

A reprodutibilidade deve, portanto, ser compreendida como parte da qualidade científica, e não apenas como uma exigência técnica de publicação. Ela contribui para que o conhecimento produzido possa ser examinado, questionado, utilizado e desenvolvido por outros pesquisadores.

## 1.4. A crise de reprodutibilidade na ciência contemporânea

A chamada crise de reprodutibilidade corresponde ao conjunto de preocupações relacionadas à dificuldade de reproduzir ou replicar resultados apresentados em publicações científicas.

O problema ganhou visibilidade em diferentes áreas, especialmente quando estudos sistemáticos passaram a investigar em que medida os resultados publicados poderiam ser confirmados por novas pesquisas.

A crise não significa que toda a ciência seja pouco confiável ou que a maioria das pesquisas esteja necessariamente errada. Ela indica que existem limitações importantes nos processos de produção, documentação, publicação e avaliação do conhecimento científico.

Munafò et al. (2017) identificam fatores estruturais que podem comprometer a confiabilidade da literatura científica, incluindo práticas metodológicas inadequadas, incentivos institucionais que privilegiam resultados positivos e limitações na divulgação dos procedimentos de pesquisa.

### Evidências da crise de reprodutibilidade

Um dos estudos mais conhecidos sobre o tema foi realizado pela Open Science Collaboration (2015). Os pesquisadores conduziram tentativas de replicação de 100 estudos experimentais e correlacionais publicados em periódicos de psicologia.

Os resultados demonstraram diferenças relevantes entre os estudos originais e as tentativas de replicação. Enquanto 97% dos estudos originais apresentavam resultados estatisticamente significativos, aproximadamente 36% das replicações obtiveram resultados estatisticamente significativos.

Esse resultado evidenciou dificuldades importantes na confirmação de achados publicados. Entretanto, os autores também destacaram que a avaliação da replicabilidade não deve depender exclusivamente da significância estatística: magnitude dos efeitos, intervalos de confiança e outras medidas de evidência também são importantes.

Figura 3 — Resultados do projeto de replicação em psicologia

Descrição do infográfico: construir um gráfico de barras com duas categorias. A primeira representa os estudos originais, dos quais 97% apresentaram resultados estatisticamente significativos. A segunda representa as replicações, das quais aproximadamente 36% apresentaram resultados estatisticamente significativos. A legenda deve esclarecer que os números representam a proporção de estudos com significância estatística, e não uma medida absoluta de verdade ou falsidade dos resultados.

Fonte: Open Science Collaboration (2015).

Esse estudo não deve ser interpretado como demonstração de que todos os resultados científicos são pouco confiáveis. Ele evidencia que, em determinado conjunto de pesquisas, a confirmação dos resultados originais foi menos frequente do que seria desejável.

### Fatores associados à crise

A dificuldade de reproduzir resultados científicos pode estar relacionada a diferentes fatores. Entre os mais relevantes, destacam-se:

- Baixo poder estatístico: ocorre quando o tamanho da amostra ou o desenho do estudo não são suficientes para detectar efeitos de interesse. Isso pode aumentar a instabilidade das estimativas e dificultar a confirmação dos resultados.
- Viés de publicação: acontece quando resultados positivos ou estatisticamente significativos têm maior probabilidade de publicação do que resultados negativos ou inconclusivos. Isso pode distorcer a percepção do conjunto de evidências disponíveis.
- Flexibilidade analítica: refere-se à possibilidade de realizar diversas escolhas de análise, seleção de variáveis, exclusão de observações e definição de desfechos sem que essas decisões sejam suficientemente justificadas ou documentadas.
- Documentação insuficiente: ocorre quando os métodos, dados, parâmetros e procedimentos não são descritos com detalhes suficientes para permitir a avaliação independente.
- Ausência de compartilhamento de dados e códigos: limita a possibilidade de verificar os procedimentos e resultados computacionais.
- Incentivos acadêmicos inadequados: sistemas de avaliação que privilegiam novidade, produtividade e resultados positivos podem reduzir o incentivo à confirmação de achados e à divulgação de resultados inconclusivos.
- Limitações técnicas: diferenças entre equipamentos, programas, bibliotecas e ambientes de execução podem dificultar a obtenção de resultados consistentes.

Esses fatores podem atuar isoladamente ou em conjunto. Um estudo pode apresentar resultados pouco estáveis devido ao tamanho reduzido da amostra e, simultaneamente, não disponibilizar dados e códigos que permitam verificar suas análises.

### Consequências para a comunidade científica

A crise de reprodutibilidade pode produzir consequências em diferentes níveis.

No nível metodológico, dificulta a avaliação da qualidade das evidências. No nível institucional, compromete a confiança nos processos de publicação e avaliação científica. No nível prático, pode levar pesquisadores, profissionais e gestores a tomar decisões com base em resultados cuja confiabilidade ainda não foi suficientemente estabelecida.

Por essa razão, diferentes iniciativas passaram a defender melhorias na transparência, no compartilhamento de dados e códigos, no planejamento experimental e nos critérios de avaliação científica.

A reprodutibilidade não elimina todos os problemas da ciência, mas oferece mecanismos para identificar, avaliar e reduzir parte das limitações que comprometem a confiabilidade dos resultados.

## 1.5. Particularidades da crise de reprodutibilidade em pesquisas computacionais e em Aprendizado de Máquina

A utilização crescente de métodos computacionais modificou profundamente a forma como diferentes áreas científicas produzem evidências. Atualmente, pesquisas em medicina, engenharia, biologia, economia, física, ciências sociais e outras disciplinas utilizam algoritmos, simulações, modelos estatísticos e técnicas de Aprendizado de Máquina.

Embora esses recursos ampliem as possibilidades de investigação, também introduzem desafios específicos para a reprodutibilidade.

Em uma pesquisa experimental tradicional, a descrição dos instrumentos, materiais e procedimentos pode permitir que outro laboratório reconstrua as condições do estudo. Em uma pesquisa computacional, entretanto, os resultados podem depender de uma combinação complexa de dados, códigos, bibliotecas, parâmetros, versões de software e infraestrutura de execução.

Peng (2011) destaca que a crescente importância da computação na ciência exige que os procedimentos utilizados para produzir resultados sejam disponibilizados de maneira que possam ser examinados e executados novamente.

### Particularidades das pesquisas computacionais

Uma pesquisa computacional pode apresentar resultados diferentes mesmo quando utiliza métodos teoricamente semelhantes. Isso acontece porque a implementação prática de um método depende de decisões técnicas que nem sempre são descritas no artigo.

Considere, por exemplo, duas equipes que implementam o mesmo algoritmo estatístico. Uma utiliza determinada versão de uma biblioteca, enquanto a outra utiliza uma versão mais recente. Se a implementação do algoritmo ou o tratamento de valores ausentes tiver sido modificado, os resultados poderão apresentar diferenças.

Entre os fatores que podem comprometer a reprodutibilidade computacional, destacam-se:

- Dependências de software: diferentes versões de bibliotecas podem modificar funções, algoritmos ou comportamentos numéricos.
- Configurações do ambiente: sistema operacional, compiladores e configurações de execução podem influenciar o funcionamento do programa.
- Hardware: diferenças entre processadores, placas gráficas e arquiteturas podem produzir variações em determinadas operações.
- Paralelismo: operações executadas simultaneamente podem apresentar resultados diferentes devido à ordem de processamento e às operações numéricas envolvidas.
- Aleatoriedade: algoritmos que utilizam processos aleatórios podem produzir resultados diferentes em execuções distintas.
- Dados: diferenças na coleta, seleção, limpeza ou transformação dos dados podem alterar os resultados.
- Implementação: duas implementações do mesmo método podem apresentar diferenças decorrentes de escolhas de programação e detalhes técnicos.

Essas particularidades demonstram que disponibilizar apenas o código-fonte não é suficiente para garantir a reprodutibilidade. É necessário registrar também as condições em que o código foi executado.

### Desafios específicos do Aprendizado de Máquina

O Aprendizado de Máquina apresenta desafios adicionais porque seus resultados dependem de processos de treinamento, validação, seleção de modelos e ajuste de hiperparâmetros.

Um modelo de Aprendizado de Máquina é construído a partir de dados e de um procedimento de treinamento. Durante esse processo, o algoritmo ajusta parâmetros internos para minimizar uma função de perda ou otimizar outro critério definido pelo pesquisador.

A obtenção do modelo final pode depender de inúmeras decisões, como:

- Arquitetura do modelo: define a estrutura utilizada, incluindo camadas, unidades, conexões e funções de ativação.
- Pré-processamento: determina como os dados serão tratados antes do treinamento.
- Divisão dos dados: estabelece quais observações serão utilizadas para treinamento, validação e teste.
- Hiperparâmetros: definem configurações externas ao processo de aprendizagem, como taxa de aprendizado, tamanho do lote e número de épocas.
- Inicialização dos parâmetros: influencia os valores iniciais utilizados durante o treinamento.
- Sementes aleatórias: controlam determinadas fontes de aleatoriedade.
- Critérios de parada: determinam quando o treinamento será encerrado.
- Métricas de avaliação: definem como o desempenho do modelo será medido.

A ausência de informações sobre essas decisões pode impedir que outro pesquisador reconstrua o experimento.

Henderson et al. (2018), ao investigarem a reprodutibilidade em Aprendizado por Reforço Profundo, demonstraram que a variabilidade dos resultados e o não determinismo dos ambientes de execução dificultam a interpretação e a comparação entre métodos.

### Aleatoriedade e variabilidade dos resultados

Muitos algoritmos de Aprendizado de Máquina utilizam operações aleatórias. Essas operações podem ocorrer durante a inicialização dos parâmetros, a seleção de exemplos, a reorganização dos dados e o treinamento do modelo.

Uma estratégia comum para controlar parte dessa variabilidade é definir uma semente aleatória (random seed). Entretanto, a fixação de uma semente não garante necessariamente que todas as operações computacionais sejam determinísticas.

Em determinados ambientes, especialmente aqueles que utilizam processamento paralelo em GPU, operações podem ocorrer em ordens diferentes, produzindo pequenas variações numéricas. Essas variações podem se acumular durante o treinamento e modificar o modelo obtido.

Portanto, é necessário distinguir entre controlar uma fonte de aleatoriedade e garantir que todo o processo computacional produza resultados idênticos.

### Exemplo 2 — Diferenças entre execuções de um modelo de classificação

Considere duas equipes que treinam uma rede neural para classificar imagens de animais.

As duas equipes utilizam a mesma arquitetura e o mesmo conjunto de dados, mas não registram todas as configurações do experimento.

A primeira equipe utiliza uma taxa de aprendizado de 0,001, executa 50 épocas e utiliza uma determinada versão do framework. A segunda utiliza uma taxa de aprendizado de 0,01, executa 100 épocas e utiliza outra versão do framework.

Embora ambas afirmem utilizar a mesma arquitetura, os resultados podem ser significativamente diferentes.

A diferença não demonstra necessariamente que o método original estava errado. Ela evidencia que a descrição da arquitetura, isoladamente, não é suficiente para reproduzir o experimento.

### Exemplo 3 — Reprodutibilidade de um modelo de previsão

Uma pesquisa desenvolve um modelo para prever a evasão de estudantes utilizando dados acadêmicos.

O artigo informa que o modelo alcançou 92% de acurácia. Entretanto, não esclarece:

- Como os dados foram divididos entre treinamento e teste.
- Se as variáveis foram normalizadas antes ou depois da divisão.
- Quais atributos foram utilizados.
- Como os valores ausentes foram tratados.
- Quais hiperparâmetros foram configurados.
- Qual versão da biblioteca foi utilizada.

Outro pesquisador tenta executar o experimento com a mesma base de dados, mas obtém 78% de acurácia.

A diferença pode decorrer de diversas causas, incluindo uma divisão diferente dos dados, pré-processamento inadequado ou vazamento de informações no estudo original. Sem documentação suficiente, não é possível determinar com segurança a origem da divergência.

### Exemplo 4 — Reprodutibilidade em processamento de imagens médicas

Uma equipe desenvolve um modelo para identificar alterações em exames radiológicos.

O estudo apresenta resultados promissores, mas não disponibiliza os critérios de seleção das imagens, as etapas de redimensionamento, a normalização dos valores de intensidade ou a configuração do treinamento.

Outro grupo tenta reproduzir o método utilizando a mesma base de imagens, mas obtém desempenho inferior.

A diferença pode estar relacionada às etapas de pré-processamento, à distribuição dos dados ou à implementação do modelo. Nesse caso, a ausência de documentação dificulta identificar se a divergência decorre de uma diferença metodológica, de uma limitação computacional ou de uma característica dos dados.

### Particularidades que devem ser registradas em pesquisas de Aprendizado de Máquina

| Elemento          | Informação necessária                                        | Importância para a reprodutibilidade               |
| ----------------- | ------------------------------------------------------------ | -------------------------------------------------- |
| Dados             | Origem, versão, critérios de seleção e divisão               | Permite identificar exatamente os dados utilizados |
| Pré-processamento | Transformações, normalizações e tratamento de dados ausentes | Permite reconstruir a preparação dos dados         |
| Arquitetura       | Estrutura e configuração do modelo                           | Permite reconstruir o modelo utilizado             |
| Hiperparâmetros   | Taxa de aprendizado, épocas, tamanho do lote etc.            | Permite reconstruir o treinamento                  |
| Aleatoriedade     | Sementes e configurações de determinismo                     | Permite controlar fontes conhecidas de variação    |
| Software          | Linguagens, bibliotecas e versões                            | Permite reconstruir o ambiente computacional       |
| Hardware          | Processador, GPU e demais recursos relevantes                | Permite compreender as condições de execução       |
| Avaliação         | Métricas e procedimentos de validação                        | Permite verificar os resultados apresentados       |

A reprodutibilidade em Aprendizado de Máquina exige, portanto, mais do que a disponibilização de um modelo treinado. É necessário documentar o processo que levou à sua construção, desde a preparação dos dados até a avaliação final.

## 1.6. Diferenças entre pesquisas experimentais, observacionais e computacionais

A pesquisa científica pode utilizar diferentes estratégias metodológicas para investigar fenômenos, testar hipóteses e produzir evidências. Entre essas estratégias, destacam-se as pesquisas experimentais, observacionais e computacionais.

Embora possam ser diferenciadas por suas características predominantes, essas categorias não são necessariamente excludentes. Uma mesma investigação pode combinar coleta observacional, experimentação controlada e análise computacional.

### Pesquisas experimentais

As pesquisas experimentais envolvem a manipulação deliberada de uma ou mais variáveis para investigar seus efeitos sobre determinado fenômeno.

Em geral, o pesquisador estabelece condições de comparação entre grupos, controla fatores relevantes e observa os resultados produzidos pela intervenção.

Um exemplo clássico é a avaliação de um tratamento médico. Os participantes podem ser distribuídos entre um grupo que recebe o tratamento e outro que recebe um placebo ou tratamento de comparação, seguindo um protocolo experimental.

A reprodutibilidade desse tipo de pesquisa depende de informações como:

- Materiais e instrumentos: identificação dos equipamentos, substâncias e recursos utilizados.
- Protocolo experimental: descrição das etapas e condições em que o experimento foi realizado.
- Amostra: caracterização dos participantes ou materiais investigados.
- Condições ambientais: registro de fatores como temperatura, umidade e tempo de exposição, quando relevantes.
- Procedimentos de análise: descrição dos métodos utilizados para interpretar os resultados.

A reprodução de uma pesquisa experimental pode exigir a realização de um novo experimento, enquanto sua reprodutibilidade computacional pode envolver a reexecução das análises realizadas sobre os dados originais.

### Pesquisas observacionais

As pesquisas observacionais investigam fenômenos sem que o pesquisador manipule diretamente as variáveis de interesse.

O pesquisador observa, registra e analisa informações provenientes de populações, instituições, sistemas ou ambientes naturais.

Um exemplo é uma investigação sobre a relação entre condições socioeconômicas e desempenho escolar. O pesquisador pode utilizar dados de estudantes, informações familiares e indicadores educacionais para analisar associações entre essas variáveis.

A reprodutibilidade desse tipo de pesquisa depende da documentação dos procedimentos de coleta, seleção, tratamento e análise dos dados.

É especialmente importante registrar os critérios de inclusão e exclusão, a definição das variáveis e os métodos utilizados para controlar possíveis fatores de confusão.

### Pesquisas computacionais

As pesquisas computacionais utilizam recursos de processamento, algoritmos, modelos matemáticos, simulações e programas para investigar problemas científicos.

Nessas pesquisas, o computador pode ser utilizado para analisar dados, executar simulações, resolver equações, construir modelos preditivos ou representar fenômenos complexos.

Um exemplo é a simulação computacional da propagação de uma doença em uma população. O pesquisador pode construir um modelo matemático, definir parâmetros epidemiológicos e executar simulações para avaliar diferentes cenários.

A reprodutibilidade exige que sejam documentados os algoritmos, os dados de entrada, as condições de execução, os parâmetros, o código e o ambiente computacional.

### Quadro comparativo

| Característica                        | Pesquisa experimental                              | Pesquisa observacional                        | Pesquisa computacional                               |
| ------------------------------------- | -------------------------------------------------- | --------------------------------------------- | ---------------------------------------------------- |
| Procedimento principal                | Manipulação de variáveis                           | Observação de fenômenos                       | Execução de métodos computacionais                   |
| Dados                                 | Obtidos por experimentos                           | Obtidos por observação ou registros           | Podem ser experimentais, observacionais ou simulados |
| Papel do pesquisador                  | Controla intervenções e condições                  | Observa e analisa variáveis                   | Desenvolve ou executa algoritmos e modelos           |
| Elementos importantes para reprodução | Protocolos, instrumentos e condições experimentais | Critérios de coleta, seleção e análise        | Dados, código, parâmetros e ambiente                 |
| Exemplo                               | Teste de um tratamento                             | Estudo de fatores associados à evasão escolar | Simulação de propagação de doenças                   |

### Integração entre diferentes tipos de pesquisa

Na prática científica, essas modalidades podem ser combinadas.

Por exemplo, uma pesquisa sobre a eficácia de um tratamento pode apresentar três componentes:

1. Experimental: realização de um ensaio clínico para coletar dados sobre os efeitos do tratamento.
2. Observacional: análise de informações complementares sobre características dos participantes.
3. Computacional: utilização de métodos estatísticos e modelos preditivos para interpretar os dados e estimar os efeitos da intervenção.

Nesse caso, a reprodutibilidade depende tanto da documentação dos procedimentos experimentais quanto da disponibilização dos métodos e recursos computacionais utilizados nas análises.

Figura 4 — Integração entre pesquisa experimental, observacional e computacional

Descrição do infográfico: apresentar três blocos principais, identificados como “Pesquisa experimental”, “Pesquisa observacional” e “Pesquisa computacional”. Os blocos devem estar conectados por setas bidirecionais, indicando que os diferentes métodos podem compartilhar dados, procedimentos e resultados. No centro, inserir “Produção de evidências científicas”. Na parte inferior, indicar que a documentação e a transparência são necessárias em todas as modalidades.

## 1.7. Ciência Aberta e seus princípios fundamentais

A Ciência Aberta (Open Science) corresponde a um conjunto de práticas e princípios que buscam ampliar a transparência, o acesso, a colaboração e a possibilidade de reutilização do conhecimento científico.

Tradicionalmente, parte dos resultados de pesquisas era disponibilizada principalmente por meio de artigos científicos, enquanto dados, códigos, materiais e procedimentos permaneciam restritos aos grupos responsáveis pelos estudos.

Esse modelo limita a possibilidade de verificar resultados, reutilizar recursos e desenvolver investigações complementares.

A Ciência Aberta procura reduzir essas limitações ao incentivar a disponibilização de diferentes componentes da pesquisa, respeitando as restrições éticas, legais, institucionais e de segurança aplicáveis.

Nosek et al. (2015) defendem a adoção de práticas e diretrizes editoriais que incentivem a transparência, a abertura e a reprodutibilidade. Os autores destacam que os princípios da Ciência Aberta precisam ser incorporados aos procedimentos de publicação e aos incentivos oferecidos aos pesquisadores.

### Princípios fundamentais da Ciência Aberta

A Ciência Aberta envolve diferentes dimensões, entre as quais se destacam:

Acesso aberto às publicações

Busca ampliar o acesso aos resultados científicos, reduzindo barreiras financeiras e técnicas à leitura e à disseminação de artigos, livros e outros materiais acadêmicos.

O acesso aberto permite que pesquisadores, estudantes, profissionais e a sociedade consultem os resultados de pesquisas sem depender necessariamente de assinaturas individuais ou institucionais.

Compartilhamento de dados

Consiste em disponibilizar dados de pesquisa de maneira organizada e documentada, respeitando as restrições relacionadas à privacidade, à confidencialidade, à segurança e aos direitos de terceiros.

O compartilhamento permite que outros pesquisadores examinem os dados, desenvolvam novas análises e utilizem os recursos em investigações complementares.

Compartilhamento de códigos e métodos

Envolve disponibilizar programas, algoritmos, scripts e procedimentos utilizados na pesquisa.

Essa prática é especialmente importante em investigações computacionais, pois permite examinar a implementação dos métodos e verificar os resultados apresentados.

Transparência metodológica

Consiste em apresentar de maneira clara as decisões metodológicas, os procedimentos experimentais e as condições utilizadas na investigação.

A transparência permite que os leitores compreendam como as evidências foram produzidas e identifiquem possíveis limitações.

Colaboração científica

Incentiva a participação de pesquisadores e instituições diferentes no desenvolvimento, na avaliação e na disseminação do conhecimento.

A colaboração pode favorecer a comparação de métodos, a realização de estudos independentes e o desenvolvimento de recursos compartilhados.

Participação social

Busca ampliar as possibilidades de participação de cidadãos e organizações da sociedade em determinadas etapas da pesquisa, incluindo a definição de problemas, a coleta de informações e a disseminação dos resultados.

### Relação entre Ciência Aberta e reprodutibilidade

A Ciência Aberta e a reprodutibilidade são conceitos relacionados, mas não equivalentes.

A Ciência Aberta estabelece práticas que ampliam o acesso e a transparência da pesquisa. A reprodutibilidade utiliza essas condições para permitir a verificação dos resultados computacionais.

Por exemplo, disponibilizar um artigo em acesso aberto facilita sua leitura, mas não garante que seus resultados possam ser reproduzidos. Para isso, pode ser necessário disponibilizar também os dados, o código, os parâmetros e as instruções de execução.

Da mesma forma, o compartilhamento de dados sem documentação adequada não garante que esses dados possam ser corretamente interpretados ou reutilizados.

### Princípios FAIR

Os princípios FAIR foram propostos para orientar a organização e a disponibilização de recursos digitais de pesquisa. A sigla representa quatro características fundamentais:

- Findable — Encontrável: os dados e demais recursos devem possuir identificação e metadados que facilitem sua localização. Isso pode envolver identificadores persistentes e mecanismos de indexação.
- Accessible — Acessível: os recursos devem poder ser recuperados por meio de protocolos definidos. A acessibilidade não significa necessariamente que todos os dados devam ser públicos, pois podem existir restrições de acesso.
- Interoperable — Interoperável: os recursos devem utilizar formatos, vocabulários e padrões que permitam sua integração com outros sistemas e conjuntos de dados.
- Reusable — Reutilizável: os recursos devem apresentar documentação, proveniência e condições de uso suficientemente claras para permitir sua reutilização.

É importante observar que os princípios FAIR não são sinônimos de acesso irrestrito. Um conjunto de dados pode seguir princípios FAIR e, ainda assim, ter seu acesso condicionado por exigências legais ou éticas.

### Quadro — Relação entre Ciência Aberta, FAIR e reprodutibilidade

| Conceito                   | Finalidade                                  | Contribuição para a pesquisa                            |
| -------------------------- | ------------------------------------------- | ------------------------------------------------------- |
| Ciência Aberta             | Ampliar transparência, acesso e colaboração | Facilita a disseminação e a avaliação do conhecimento   |
| Princípios FAIR            | Melhorar a gestão de recursos digitais      | Favorece localização, acesso, integração e reutilização |
| Reprodutibilidade          | Verificar resultados computacionais         | Permite reexecutar e avaliar procedimentos e resultados |
| Transparência metodológica | Explicitar decisões e procedimentos         | Permite compreender como os resultados foram produzidos |

Figura 5 — Relação entre Ciência Aberta e reprodutibilidade

Descrição do infográfico: apresentar a Ciência Aberta como um grande círculo externo contendo quatro elementos: acesso aberto, compartilhamento de dados, compartilhamento de códigos e transparência metodológica. No interior, inserir um segundo círculo com os princípios FAIR. No centro, posicionar “Reprodutibilidade científica”, conectada aos elementos anteriores. O objetivo é demonstrar que práticas abertas e organização adequada dos recursos favorecem a verificação dos resultados.

## 1.8. Pesquisa computacional como evidência científica

A pesquisa computacional tornou-se parte essencial da produção de conhecimento em diferentes áreas. Seu papel vai além da utilização de computadores como ferramentas auxiliares: em muitas investigações, os resultados científicos dependem diretamente da execução de algoritmos, modelos matemáticos, simulações e procedimentos de análise.

Nessas situações, o resultado computacional constitui uma parte importante da evidência apresentada no estudo.

Uma simulação pode estimar o comportamento de um sistema físico. Um modelo estatístico pode identificar associações entre variáveis. Um algoritmo de Aprendizado de Máquina pode classificar imagens ou realizar previsões. Uma análise computacional pode identificar padrões em grandes conjuntos de dados.

Em todos esses casos, a interpretação dos resultados depende da compreensão dos procedimentos que os produziram.

### Etapas de uma pesquisa computacional

Uma pesquisa computacional geralmente envolve uma sequência de etapas interdependentes.

1\. Definição do problema científico

O pesquisador identifica uma questão que pode ser investigada por meio de métodos computacionais. Essa etapa envolve a formulação do problema, a definição dos objetivos e a identificação das evidências necessárias.

2\. Obtenção dos dados

Os dados podem ser coletados diretamente, obtidos de repositórios públicos, extraídos de registros institucionais ou gerados por simulações.

É necessário documentar sua origem, os critérios de seleção e as condições de utilização.

3\. Preparação dos dados

Os dados são organizados e tratados para permitir a análise. Essa etapa pode incluir remoção de duplicatas, tratamento de valores ausentes, normalização, transformação de variáveis e seleção de atributos.

4\. Implementação dos métodos

O pesquisador desenvolve ou utiliza códigos e algoritmos para executar os procedimentos definidos na metodologia.

5\. Execução computacional

Os procedimentos são executados em determinado ambiente, utilizando recursos de hardware e software.

6\. Análise dos resultados

Os resultados são examinados para verificar se respondem à questão de pesquisa e se sustentam as conclusões propostas.

7\. Documentação e disponibilização

Os dados, códigos, parâmetros, resultados e demais informações relevantes são organizados para permitir a avaliação e a possível reprodução da investigação.

### Fluxo geral de uma pesquisa computacional

Figura 6 — Fluxo de produção de evidências em uma pesquisa computacional

Descrição do infográfico: construir um fluxograma horizontal com sete etapas conectadas por setas:

1. Problema científico.
2. Obtenção dos dados.
3. Preparação dos dados.
4. Implementação dos métodos.
5. Execução computacional.
6. Análise dos resultados.
7. Interpretação e publicação.

Abaixo do fluxo, incluir uma faixa transversal denominada “Documentação e rastreabilidade”, conectada a todas as etapas. Essa faixa deve indicar que a documentação não acontece apenas ao final da pesquisa, mas acompanha todo o processo.

### A importância da rastreabilidade

A rastreabilidade corresponde à capacidade de identificar e acompanhar os elementos e procedimentos que contribuíram para a produção de determinado resultado.

Em uma pesquisa computacional, isso significa conseguir identificar, por exemplo:

- Qual conjunto de dados foi utilizado.
- Qual versão do código produziu determinado resultado.
- Quais parâmetros foram configurados.
- Qual ambiente computacional foi utilizado.
- Quais transformações foram aplicadas aos dados.
- Qual execução gerou determinada tabela ou figura.
- Quais decisões metodológicas foram tomadas durante a análise.

Essas informações permitem reconstruir a trajetória entre os dados de entrada e os resultados apresentados.

Sandve et al. (2013) apresentam princípios práticos para o desenvolvimento de pesquisas computacionais reproduzíveis, enfatizando a importância de registrar as etapas da análise, organizar os dados, documentar o código e preservar as condições necessárias à execução dos procedimentos.

### Exemplo 5 — Simulação computacional de um fenômeno físico

Um pesquisador desenvolve uma simulação para investigar o comportamento de um sistema físico sob diferentes condições de temperatura.

O programa utiliza um modelo matemático, parâmetros de entrada e um algoritmo numérico para calcular a evolução do sistema ao longo do tempo.

Para que outro pesquisador possa verificar os resultados, é necessário disponibilizar:

1. As equações utilizadas no modelo.
2. Os valores dos parâmetros.
3. O código-fonte da simulação.
4. As configurações numéricas utilizadas.
5. As versões das bibliotecas relevantes.
6. Os dados de entrada.
7. As instruções necessárias para executar o programa.

A reprodução permite verificar se a implementação computacional gera resultados consistentes com aqueles apresentados no estudo.

Entretanto, mesmo que a simulação seja reproduzida com sucesso, isso não significa automaticamente que o modelo matemático represente perfeitamente o fenômeno real. A validade científica também depende da adequação das hipóteses e da comparação com evidências empíricas.

### Diferença entre reproduzir um cálculo e validar um modelo

Esse ponto é especialmente importante.

Um programa pode executar corretamente as instruções implementadas e produzir exatamente os mesmos resultados obtidos anteriormente. Ainda assim, o modelo utilizado pode conter hipóteses inadequadas ou simplificações que não representam suficientemente o fenômeno investigado.

Assim, é necessário distinguir:

- Verificação computacional: examina se o programa executa corretamente os procedimentos definidos e produz resultados consistentes.
- Validação científica: avalia se o modelo, os métodos e as hipóteses representam adequadamente o problema estudado.
- Reprodutibilidade: permite obter resultados computacionais consistentes a partir dos mesmos dados, métodos, códigos e condições de análise.

Essas dimensões são complementares e contribuem conjuntamente para a qualidade da pesquisa.

## 1.9. Barreiras técnicas, metodológicas e institucionais à reprodutibilidade

Apesar de sua importância, a reprodutibilidade ainda enfrenta obstáculos em diferentes áreas científicas. Esses obstáculos não estão relacionados exclusivamente à falta de conhecimento técnico dos pesquisadores. Muitas vezes, resultam de limitações de infraestrutura, práticas metodológicas inadequadas, ausência de políticas institucionais e incentivos acadêmicos que não valorizam suficientemente a documentação e o compartilhamento dos recursos científicos.

Munafò et al. (2017) destacam que a melhoria da confiabilidade científica exige mudanças não apenas nos procedimentos individuais de pesquisa, mas também nas práticas de publicação, avaliação e reconhecimento acadêmico.

As barreiras podem ser organizadas em três grandes categorias: técnicas, metodológicas e institucionais.

### Barreiras técnicas

As barreiras técnicas estão relacionadas às dificuldades de infraestrutura, software, hardware, armazenamento e gerenciamento dos recursos computacionais.

Entre as principais, destacam-se:

Incompatibilidade entre ambientes computacionais

Um programa pode funcionar em determinado computador, mas apresentar erros em outro devido a diferenças no sistema operacional, nas bibliotecas instaladas ou nas versões das dependências.

Ausência de controle de versões

Quando os códigos e dados não são versionados, torna-se difícil identificar qual versão foi utilizada para produzir os resultados apresentados no artigo.

Dependências não documentadas

Um programa pode depender de bibliotecas específicas que não foram registradas. Sem essas informações, outro pesquisador pode ter dificuldades para executar o código.

Limitações de hardware

Alguns experimentos exigem placas gráficas, memória ou capacidade de processamento que não estão disponíveis em todos os laboratórios.

Armazenamento inadequado

Dados extensos e modelos computacionais podem exigir infraestrutura específica para armazenamento, compartilhamento e preservação.

Ausência de automação

Quando as etapas de análise dependem de procedimentos manuais não documentados, aumenta o risco de erros e diminui a possibilidade de executar novamente o fluxo completo.

### Barreiras metodológicas

As barreiras metodológicas estão relacionadas à forma como a pesquisa é planejada, executada e documentada.

Entre as principais, encontram-se:

Descrição incompleta dos métodos

A publicação pode apresentar apenas uma descrição resumida dos procedimentos, sem detalhar as decisões necessárias para reconstruir a análise.

Ausência de registro dos parâmetros

A falta de informações sobre configurações experimentais e hiperparâmetros dificulta a reprodução dos resultados.

Critérios de seleção pouco claros

Quando não são documentados os critérios de inclusão, exclusão e preparação dos dados, diferentes pesquisadores podem trabalhar com conjuntos de dados distintos.

Flexibilidade analítica não documentada

A realização de várias análises e a seleção posterior dos resultados mais favoráveis podem produzir conclusões excessivamente dependentes das escolhas dos pesquisadores.

Vazamento de dados

Em pesquisas de Aprendizado de Máquina, informações do conjunto de teste podem ser utilizadas indevidamente durante o treinamento ou a preparação dos dados, comprometendo a avaliação do desempenho do modelo.

Ausência de análise de variabilidade

A apresentação de uma única execução de um algoritmo estocástico pode ocultar variações importantes no desempenho. Em muitos casos, é necessário realizar execuções independentes e apresentar medidas de dispersão ou incerteza.

### Barreiras institucionais

As barreiras institucionais decorrem das políticas, estruturas e incentivos que influenciam a atividade científica.

Entre elas, destacam-se:

Valorização excessiva da publicação

Quando os sistemas de avaliação acadêmica priorizam a quantidade de artigos publicados, pesquisadores podem ter menos tempo e incentivo para documentar e organizar adequadamente seus projetos.

Baixo reconhecimento do compartilhamento de recursos

A disponibilização de códigos, dados e materiais complementares pode exigir trabalho considerável, mas nem sempre recebe o mesmo reconhecimento acadêmico atribuído à publicação de artigos.

Falta de treinamento

Pesquisadores podem não ter formação suficiente em controle de versão, gerenciamento de dados, documentação de software e organização de ambientes computacionais.

Infraestrutura institucional insuficiente

A ausência de servidores, armazenamento, suporte técnico e recursos computacionais pode dificultar o desenvolvimento de pesquisas reproduzíveis.

Políticas editoriais limitadas

Alguns periódicos não exigem ou não incentivam suficientemente a disponibilização dos dados, códigos e materiais utilizados nas pesquisas.

### Quadro comparativo das barreiras à reprodutibilidade

| Categoria      | Exemplos de barreiras                                                             | Possíveis consequências                                     |
| -------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| Técnicas       | Incompatibilidade de software, ausência de versionamento e limitações de hardware | Dificuldade de executar novamente os procedimentos          |
| Metodológicas  | Métodos incompletos, parâmetros não registrados e critérios pouco claros          | Divergência entre os resultados originais e os reproduzidos |
| Institucionais | Falta de treinamento, infraestrutura e incentivos                                 | Baixa adoção de práticas reproduzíveis                      |

### Estratégias para reduzir as barreiras

A superação dessas dificuldades exige ações coordenadas entre pesquisadores, instituições, periódicos e agências de financiamento.

No âmbito individual, os pesquisadores podem adotar boas práticas de organização de projetos, documentação de código, controle de versão e registro de parâmetros.

No âmbito institucional, universidades e centros de pesquisa podem oferecer treinamento, infraestrutura computacional e suporte especializado.

No âmbito editorial, periódicos podem estabelecer diretrizes para disponibilização de dados, códigos e materiais suplementares, além de adotar mecanismos de avaliação da transparência metodológica.

No âmbito das agências de financiamento, políticas de Ciência Aberta podem incentivar o planejamento da gestão de dados e o compartilhamento de recursos científicos.

Figura 7 — Estratégias para superar barreiras à reprodutibilidade

Descrição do infográfico: apresentar três colunas: “Pesquisadores”, “Instituições” e “Periódicos e financiadores”. Na primeira, inserir boas práticas de programação, documentação e versionamento. Na segunda, inserir treinamento, infraestrutura e suporte técnico. Na terceira, inserir políticas de compartilhamento, diretrizes editoriais e incentivos à Ciência Aberta. As três colunas devem convergir para um bloco final denominado “Pesquisa científica mais transparente e reproduzível”.

# Síntese do capítulo

A reprodutibilidade científica constitui um dos fundamentos da confiabilidade da pesquisa, especialmente em um cenário no qual métodos computacionais são utilizados de maneira crescente na produção de evidências.

Neste capítulo, foram apresentados os principais conceitos relacionados à reprodutibilidade e suas diferenças em relação à replicabilidade, repetibilidade, robustez e transparência computacional. Também foram discutidas a crise de reprodutibilidade, as particularidades das pesquisas computacionais e os desafios específicos do Aprendizado de Máquina.

A discussão demonstrou que a reprodutibilidade não depende apenas da disponibilização do código-fonte ou dos dados. Ela exige que os procedimentos, parâmetros, métodos e condições de execução sejam suficientemente documentados para permitir a verificação dos resultados.

Também foi apresentada a relação entre reprodutibilidade e Ciência Aberta. Práticas como compartilhamento de dados, disponibilização de códigos, documentação metodológica e adoção dos princípios FAIR favorecem a avaliação independente e a reutilização dos recursos científicos.

Por fim, foram identificadas barreiras técnicas, metodológicas e institucionais que dificultam a adoção dessas práticas. Sua superação exige mudanças na organização dos projetos, na formação dos pesquisadores, na infraestrutura institucional e nas políticas de publicação científica.

A principal conclusão é que a reprodutibilidade deve ser incorporada ao planejamento e à execução da pesquisa, e não tratada apenas como uma exigência posterior à publicação. Uma investigação cientificamente consistente precisa permitir que seus métodos sejam compreendidos, que seus resultados sejam avaliados e que suas evidências possam ser utilizadas de maneira crítica por outros pesquisadores.

# Questões para fixação da aprendizagem

1\. Explique o conceito de reprodutibilidade científica e sua importância para a confiabilidade dos resultados de uma pesquisa.

2\. Diferencie reprodutibilidade e replicabilidade, considerando os dados utilizados em cada processo.

3\. Por que a disponibilização do código-fonte, isoladamente, não garante a reprodutibilidade de uma pesquisa computacional?

4\. Explique como a fixação de sementes aleatórias pode contribuir para a reprodutibilidade de experimentos de Aprendizado de Máquina. Por que essa prática não garante necessariamente resultados idênticos?

5\. Apresente três fatores que contribuem para a crise de reprodutibilidade científica e explique suas consequências.

6\. Diferencie pesquisas experimentais, observacionais e computacionais, apresentando um exemplo de cada modalidade.

7\. Explique a relação entre Ciência Aberta, princípios FAIR e reprodutibilidade científica.

8\. Por que a reprodução de uma simulação computacional não garante, necessariamente, que o modelo utilizado represente corretamente o fenômeno real?

9\. Identifique três barreiras técnicas, três metodológicas e três institucionais à reprodutibilidade.

10\. Considere um artigo científico que apresenta resultados de um modelo de Aprendizado de Máquina, mas não disponibiliza os dados, o código ou os hiperparâmetros. Discuta quais informações seriam necessárias para permitir a verificação dos resultados.

# Glossário

| Termo                       | Definição                                                                                                                            |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| Aprendizado de Máquina      | Área da inteligência artificial que desenvolve métodos capazes de identificar padrões e aprender a partir de dados.                  |
| Código-fonte                | Conjunto de instruções escritas em uma linguagem de programação que define o funcionamento de um programa.                           |
| Ciência Aberta              | Conjunto de princípios e práticas que promovem transparência, acesso, colaboração e reutilização do conhecimento científico.         |
| Dados de entrada            | Informações utilizadas por um programa, algoritmo ou modelo para realizar uma operação ou análise.                                   |
| Hiperparâmetros             | Configurações definidas pelo pesquisador antes ou durante a preparação de um modelo, que influenciam seu processo de treinamento.    |
| Repetibilidade              | Capacidade de obter resultados consistentes ao repetir um procedimento sob condições essencialmente iguais.                          |
| Replicabilidade             | Capacidade de obter resultados consistentes em estudos independentes que investigam a mesma questão científica com novos dados.      |
| Reprodutibilidade           | Obtenção de resultados computacionais consistentes utilizando os mesmos dados, métodos, códigos e condições de análise.              |
| Robustez                    | Estabilidade dos resultados diante de pequenas alterações razoáveis nas condições de análise.                                        |
| Semente aleatória           | Valor inicial utilizado para controlar determinadas sequências de operações pseudoaleatórias.                                        |
| Transparência computacional | Disponibilização e documentação das informações necessárias para compreender os procedimentos computacionais utilizados na pesquisa. |
| Vazamento de dados          | Utilização indevida de informações durante o treinamento ou desenvolvimento de um modelo, comprometendo sua avaliação.               |

# Referências bibliográficas

As referências a seguir correspondem a artigos científicos publicados em periódicos ou anais de conferências acadêmicas e a uma publicação de referência institucional. Foram selecionadas por sua relação direta com os conceitos e discussões apresentados no capítulo.

GOODMAN, Steven N.; FANELLI, Daniele; IOANNIDIS, John P. A. What does research reproducibility mean? Science Translational Medicine, Washington, DC, v. 8, n. 341, p. 341ps12, 2016. DOI: [https://doi.org/10.1126/scitranslmed.aaf5027](https://doi.org/10.1126/scitranslmed.aaf5027?utm_source=chatgpt.com).

HENDERSON, Peter et al. Deep reinforcement learning that matters. In: AAAI CONFERENCE ON ARTIFICIAL INTELLIGENCE, 32., 2018. Proceedings [...]. Palo Alto: AAAI Press, 2018. v. 32, n. 1. DOI: [https://doi.org/10.1609/aaai.v32i1.11694](https://doi.org/10.1609/aaai.v32i1.11694?utm_source=chatgpt.com).

MUNAFÒ, Marcus R. et al. A manifesto for reproducible science. Nature Human Behaviour, London, v. 1, art. 0021, 2017. DOI: [https://doi.org/10.1038/s41562-016-0021](https://doi.org/10.1038/s41562-016-0021?utm_source=chatgpt.com).

NATIONAL ACADEMIES OF SCIENCES, ENGINEERING, AND MEDICINE. Reproducibility and replicability in science. Washington, DC: The National Academies Press, 2019. DOI: [https://doi.org/10.17226/25303](https://doi.org/10.17226/25303?utm_source=chatgpt.com).

NOSEK, Brian A. et al. Promoting an open research culture. Science, Washington, DC, v. 348, n. 6242, p. 1422-1425, 2015. DOI: [https://doi.org/10.1126/science.aab2374](https://doi.org/10.1126/science.aab2374?utm_source=chatgpt.com).

OPEN SCIENCE COLLABORATION. Estimating the reproducibility of psychological science. Science, Washington, DC, v. 349, n. 6251, art. aac4716, 2015. DOI: [https://doi.org/10.1126/science.aac4716](https://doi.org/10.1126/science.aac4716?utm_source=chatgpt.com).

PENG, Roger D. Reproducible research in computational science. Science, Washington, DC, v. 334, n. 6060, p. 1226-1227, 2011. DOI: [https://doi.org/10.1126/science.1213847](https://doi.org/10.1126/science.1213847?utm_source=chatgpt.com).

SANDVE, Geir Kjetil et al. Ten simple rules for reproducible computational research. PLoS Computational Biology, San Francisco, v. 9, n. 10, art. e1003285, 2013. DOI: [https://doi.org/10.1371/journal.pcbi.1003285](https://doi.org/10.1371/journal.pcbi.1003285?utm_source=chatgpt.com).
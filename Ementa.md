# Programa de Estudos — Reprodutibilidade Computacional em Pesquisas Científicas

Versão corrigida e ampliada

## Módulo 1 — Fundamentos da Reprodutibilidade Científica

1.1. Conceito de reprodutibilidade científica.

1.2. Diferenças entre reprodutibilidade, replicabilidade, repetibilidade, robustez e transparência computacional.

1.3. Importância da reprodutibilidade para a confiabilidade e a credibilidade da ciência.

1.4. A crise de reprodutibilidade na ciência contemporânea.

1.5. Particularidades da crise de reprodutibilidade em pesquisas computacionais e em Aprendizado de Máquina (Machine Learning).

1.6. Diferenças entre pesquisas experimentais, observacionais e computacionais.

1.7. Ciência Aberta e seus princípios fundamentais.

1.8. Pesquisa computacional como evidência científica.

1.9. Barreiras técnicas, metodológicas e institucionais à reprodutibilidade.

## Módulo 2 — Fundamentos de Programação para Pesquisa Científica

2.1. Fundamentos de programação aplicados à pesquisa científica.

2.2. Linguagens de programação utilizadas em pesquisas computacionais.

2.3. Estruturação, modularização e organização de projetos científicos.

2.4. Boas práticas de programação e legibilidade de código.

2.5. Documentação de código e elaboração de comentários técnicos.

2.6. Tratamento de erros, validação de entradas e testes básicos.

2.7. Bibliotecas, pacotes e frameworks científicos.

2.8. Desenvolvimento de código computacional organizado, documentado e reutilizável.

## Módulo 3 — Ciência Aberta e Princípios FAIR

3.1. Fundamentos e dimensões da Ciência Aberta.

3.2. Acesso aberto a publicações, dados e códigos científicos.

3.3. Princípios FAIR: encontrabilidade, acessibilidade, interoperabilidade e reutilização.

3.4. Aplicação dos princípios FAIR a dados, códigos e modelos computacionais.

3.5. Metadados e documentação de recursos científicos.

3.6. Identificadores persistentes e rastreabilidade de recursos.

3.7. Repositórios e infraestruturas de Ciência Aberta.

3.8. Transparência, compartilhamento e reutilização de resultados científicos.

## Módulo 4 — Gerenciamento e Organização de Dados Científicos

4.1. Tipos e formatos de dados utilizados em pesquisas científicas.

4.2. Ciclo de vida dos dados de pesquisa.

4.3. Organização de diretórios, arquivos e conjuntos de dados.

4.4. Limpeza, transformação e pré-processamento de dados.

4.5. Proveniência e rastreabilidade dos dados.

4.6. Metadados e documentação de conjuntos de dados.

4.7. Versionamento de dados científicos.

4.8. Documentação de conjuntos de dados por meio de Dataset Cards.

4.9. Identificação de vieses, inconsistências e problemas de qualidade dos dados.

4.10. Compartilhamento, preservação e reutilização de dados.

## Módulo 5 — Desenvolvimento de Códigos Computacionais Reproduzíveis

5.1. Princípios de desenvolvimento de código reproduzível.

5.2. Organização e modularização de scripts e programas científicos.

5.3. Padronização e legibilidade do código.

5.4. Documentação de funções, classes, bibliotecas e algoritmos.

5.5. Separação entre dados, parâmetros, configurações e código-fonte.

5.6. Parametrização de experimentos computacionais.

5.7. Testes de software aplicados à pesquisa científica.

5.8. Validação de resultados e detecção de erros computacionais.

5.9. Reutilização e manutenção de códigos científicos.

5.10. Documentação de modelos computacionais por meio de Model Cards.

## Módulo 6 — Controle de Versão e Gerenciamento de Código, Dados e Modelos

6.1. Fundamentos do controle de versão.

6.2. Git: conceitos, instalação e configuração.

6.3. Repositórios locais e remotos.

6.4. GitHub e outras plataformas de hospedagem de código.

6.5. Commits, branches, merges e resolução de conflitos.

6.6. Boas práticas de versionamento e mensagens de commit.

6.7. Versionamento de código-fonte versus versionamento de dados e modelos.

6.8. Gerenciamento de arquivos grandes em projetos científicos.

6.9. DVC (Data Version Control) e ferramentas equivalentes.

6.10. Versionamento de conjuntos de dados, modelos treinados e artefatos computacionais.

6.11. Integração entre Git e DVC.

6.12. Armazenamento remoto e compartilhamento de dados e modelos versionados.

## Módulo 7 — Ambientes Computacionais e Dependências de Software

7.1. Ambientes computacionais e sua influência na reprodutibilidade.

7.2. Sistemas operacionais, arquiteturas e configurações de hardware.

7.3. Dependências, bibliotecas e gerenciamento de pacotes.

7.4. Ambientes virtuais com venv e Conda.

7.5. Gerenciamento de dependências com Poetry.

7.6. Arquivos de configuração e especificação de dependências: requirements.txt e environment.yml.

7.7. Contêineres e isolamento de ambientes computacionais.

7.8. Docker e criação de ambientes reproduzíveis.

7.9. Compatibilidade entre versões de linguagens, bibliotecas e frameworks.

7.10. Execução de experimentos em diferentes ambientes computacionais, incluindo Google Colab.

7.11. Limitações e desafios da reprodução de resultados em ambientes heterogêneos.

## Módulo 8 — Infraestrutura Computacional e Recursos de Execução Científica

8.1. Infraestrutura computacional para pesquisas científicas.

8.2. Processamento em CPU e GPU.

8.3. Computação de alto desempenho e processamento paralelo.

8.4. Computação em nuvem aplicada à pesquisa científica.

8.5. Ambientes locais, remotos e distribuídos.

8.6. Gerenciamento de recursos computacionais.

8.7. Configuração e documentação da infraestrutura de execução.

8.8. Impacto da infraestrutura nos resultados e no desempenho dos experimentos.

## Módulo 9 — Reprodutibilidade de Experimentos Computacionais

9.1. Fundamentos da experimentação computacional reproduzível.

9.2. Planejamento, execução e documentação de experimentos.

9.3. Aleatoriedade em algoritmos e experimentos computacionais.

9.4. Fixação de sementes aleatórias (random seeds).

9.5. Controle de aleatoriedade em NumPy, PyTorch, TensorFlow e scikit-learn.

9.6. Determinismo e não determinismo em operações computacionais.

9.7. Limitações da reprodutibilidade em GPU, paralelismo e operações não determinísticas.

9.8. Registro de parâmetros, hiperparâmetros, métricas e resultados.

9.9. Rastreamento de experimentos com MLflow e Weights & Biases.

9.10. Comparação de resultados entre diferentes execuções.

9.11. Análise de variabilidade e incerteza experimental.

9.12. Documentação das condições de execução e dos resultados obtidos.

## Módulo 10 — Automação de Fluxos de Trabalho Científicos

10.1. Conceito e importância dos fluxos de trabalho (workflows) científicos.

10.2. Estruturação de pipelines computacionais.

10.3. Automação de etapas de processamento e análise de dados.

10.4. Dependências entre tarefas e etapas de execução.

10.5. Automação de experimentos computacionais.

10.6. Construção de pipelines com DVC.

10.7. Rastreamento e gerenciamento de execuções com ferramentas de automação.

10.8. Integração entre código, dados, modelos e ambientes computacionais.

10.9. Monitoramento, validação e registro de resultados.

10.10. Reexecução automatizada de fluxos de trabalho científicos.

## Módulo 11 — Armazenamento, Compartilhamento e Preservação de Artefatos Científicos

11.1. Conceito de artefatos científicos digitais.

11.2. Organização e armazenamento de códigos, dados, modelos e resultados.

11.3. Repositórios de código e dados científicos.

11.4. Zenodo e publicação de artefatos científicos.

11.5. Kaggle Datasets e compartilhamento de conjuntos de dados.

11.6. Hugging Face Datasets e compartilhamento de recursos para Aprendizado de Máquina.

11.7. UCI Machine Learning Repository e repositórios de referência.

11.8. Publicação e preservação de modelos computacionais.

11.9. Identificadores persistentes, versões e metadados.

11.10. Licenciamento de códigos, dados e modelos.

11.11. Direitos autorais, propriedade intelectual e condições de reutilização.

11.12. Estratégias de preservação digital e acesso de longo prazo.

## Módulo 12 — Documentação, Transparência e Relato de Métodos Computacionais

12.1. Importância da documentação na pesquisa computacional.

12.2. Documentação de procedimentos, métodos e algoritmos.

12.3. Registro de decisões metodológicas e computacionais.

12.4. Documentação de dados, códigos, modelos e ambientes.

12.5. Relato de configurações experimentais e parâmetros.

12.6. Transparência na apresentação de resultados computacionais.

12.7. Relatórios técnicos e documentação complementar de artigos científicos.

12.8. Checklists e diretrizes para relato de pesquisas computacionais.

12.9. Limitações metodológicas e computacionais.

## Módulo 13 — Aspectos Éticos, Legais e de Governança na Pesquisa Computacional

13.1. Ética e integridade na pesquisa científica.

13.2. Transparência e responsabilidade na produção de resultados computacionais.

13.3. Direitos autorais e propriedade intelectual.

13.4. Licenças de software livre e de código aberto.

13.5. Licenciamento e compartilhamento de dados científicos.

13.6. Licenciamento de modelos computacionais.

13.7. Privacidade, proteção de dados e segurança da informação.

13.8. Governança e uso responsável de dados e modelos.

13.9. Questões éticas relacionadas ao uso de Inteligência Artificial e Aprendizado de Máquina.

## Módulo 14 — Avaliação e Auditoria da Reprodutibilidade Computacional

14.1. Critérios para avaliação da reprodutibilidade computacional.

14.2. Verificação de códigos, dados e ambientes de execução.

14.3. Auditoria de fluxos de trabalho científicos.

14.4. Avaliação da documentação e da disponibilidade dos artefatos.

14.5. Reexecução independente de experimentos.

14.6. Comparação entre resultados originais e reproduzidos.

14.7. Identificação de falhas e obstáculos à reprodução.

14.8. Análise de robustez e sensibilidade dos resultados.

14.9. Relato de limitações e evidências de reprodutibilidade.

## Módulo 15 — Aplicação Prática: Desenvolvimento de uma Pesquisa Computacional Reproduzível

15.1. Planejamento de um projeto de pesquisa computacional reproduzível.

15.2. Seleção e documentação dos dados utilizados.

15.3. Organização do projeto e versionamento do código com Git e GitHub.

15.4. Versionamento de dados e modelos com DVC.

15.5. Configuração de ambientes computacionais reproduzíveis.

15.6. Fixação de sementes aleatórias e registro das condições experimentais.

15.7. Desenvolvimento e execução de um pipeline computacional.

15.8. Rastreamento de experimentos com MLflow ou ferramenta equivalente.

15.9. Registro de hiperparâmetros, métricas e resultados.

15.10. Reprodução do experimento em outro ambiente computacional, como Google Colab.

15.11. Elaboração de Dataset Cards e Model Cards.

15.12. Publicação dos dados, códigos, modelos e demais artefatos em repositórios científicos.

15.13. Definição de licenças e condições de reutilização.

15.14. Verificação independente da reprodução dos resultados.

15.15. Elaboração de documentação técnica e materiais suplementares.

15.16. Preparação de artigo científico com procedimentos computacionais transparentes e reproduzíveis.
# NLP para Análise de Impacto Ambiental na Saúde Cardiovascular 🩺🌱

Este projeto demonstra como técnicas de **Processamento de Linguagem Natural (NLP)** podem ser aplicadas a artigos científicos para extrair *insights* críticos sobre a relação entre a poluição do ar ($MP_{2,5}$), vulnerabilidade social e mortalidade cardiovascular.

---

## 📋 Visão Geral do Processo de Extração

O pipeline de NLP transforma textos científicos não estruturados em dados acionáveis, permitindo que sistemas de IA em saúde identifiquem padrões epidemiológicos automaticamente.

> **Nota:** Este fluxo é essencial para converter evidências científicas em políticas públicas baseadas em dados.

---

## 🛠️ Técnicas de NLP Aplicadas

### 1. Classificação de Tópicos (Topic Classification)
Identifica automaticamente as áreas de domínio do artigo para indexação e busca inteligente.
* **Categorias Identificadas:** Poluição do Ar, Epidemiologia, Desigualdade Social, Doenças Cardiovasculares.
* **Algoritmos:** `BERT`, `BioBERT`, `LDA` (Latent Dirichlet Allocation).

### 2. Reconhecimento de Entidades Nomeadas (NER)
Extração de termos técnicos e biomédicos específicos presentes no texto.
* **Doenças:** DAC (Aparelho circulatório), DIC (Isquêmicas), DCBV (Cerebrovasculares).
* **Fatores Ambientais:** Partículas inaláveis finas ($MP_{2,5}$), Limites da OMS.
* **Modelos:** `SciSpacy`, `ClinicalBERT`.

### 3. Extração de Relações (Relation Extraction)
O algoritmo conecta as entidades para entender a causalidade descrita no estudo.
* **Relação Identificada:** `[Exposição MP2,5]` ⮕ `[Aumento de Risco]` ⮕ `[Mortalidade em Grupos Vulneráveis]`

### 4. Análise de Sentimento e Alerta
Detecta o tom de urgência e o nível de risco à saúde pública mencionado pelos autores.
* **Aplicação:** Priorização de leitura para gestores de saúde pública em casos de "Alto Risco".

### 5. Sumarização Automática
Gera resumos executivos focados em desfechos clínicos, economizando tempo de pesquisadores e médicos.

---

## 🚀 Relevância para IA em Saúde

A aplicação destas técnicas permite:

1.  **Apoio à Decisão:** Identificação rápida de regiões vulneráveis e fatores de risco.
2.  **Vigilância Epidemiológica:** Monitoramento automatizado de novos estudos e tendências.
3.  **Bases de Conhecimento:** Construção de grafos de conhecimento que alimentam sistemas de diagnóstico assistido.

---

## 💻 Exemplo de Implementação (Python)

Para extrair as entidades mencionadas, utilizamos o `scispaCy`, uma biblioteca otimizada para textos biomédicos.

# NLP para Análise de Prevalência e Fatores de Risco em Doenças Cardiovasculares (PNS) 🩺📊

Este projeto demonstra como técnicas de **Processamento de Linguagem Natural (NLP)** podem ser aplicadas a artigos científicos e dados epidemiológicos para extrair conhecimentos críticos sobre Doenças Cardiovasculares (DCV) no Brasil, utilizando como base os dados da Pesquisa Nacional de Saúde (PNS).

---

## 📋 Como o NLP explora este conteúdo?

O uso de algoritmos de inteligência artificial permite transformar o texto científico do artigo em dados estruturados e insights acionáveis.

### 1. Classificação de Tópicos (Topic Classification)
O algoritmo organiza o conteúdo em categorias temáticas, facilitando a indexação e busca em grandes bases de dados médicos.
* **Temas identificados no artigo:** Epidemiologia, Doenças Crônicas Não Transmissíveis (DCNT), Saúde Pública Brasileira, Fatores Sociodemográficos.
* **Importância:** Permite que gestores de saúde filtrem rapidamente estudos por áreas de impacto (ex: "estudos sobre estilo de vida e coração").

### 2. Extração de Entidades Nomeadas (NER)
Identifica automaticamente termos técnicos, condições de saúde e variáveis estatísticas dentro do texto.
* **Diagnósticos:** Doença do coração, Hipertensão, Colesterol alto, Diabetes.
* **Procedimentos:** Revascularização miocárdica, Angioplastia coronariana.
* **Variáveis:** Idade avançada, Raça/cor branca, Nível de escolaridade, Plano de saúde.
* **Estilo de Vida:** Consumo de frutas e hortaliças, Tabagismo (ex-fumante), Atividade física.



### 3. Extração de Relações (Relation Extraction)
Identifica conexões lógicas entre os fatores de risco e os desfechos de saúde mencionados no estudo.
* **Conexão identificada:** `[Autoavaliação de saúde ruim]` ⮕ `[Maior prevalência de DCV]`.
* **Conexão identificada:** `[Sexo masculino]` ⮕ `[Associação positiva com diagnóstico de DCV]`.

### 4. Análise de Sentimento e Alerta (Sentiment & Urgency Analysis)
Detecta o "tom" do artigo para priorizar ações de saúde pública.
* **Insight:** O texto demonstra uma linguagem de **alerta e urgência**, destacando que a DCV é a principal causa de morte e que as metas de redução precisam de apoio em políticas públicas.

---

## 🚀 Por que isso é relevante para IA na Saúde?

A aplicação de NLP neste tipo de literatura é o que alimenta os sistemas de **Inteligência Artificial Médica**:

1.  **Vigilância Epidemiológica:** Permite monitorar automaticamente tendências (ex: o aumento de 5,3% na prevalência autorreferida) sem a necessidade de leitura manual de milhares de páginas.
2.  **Sistemas de Apoio à Decisão:** Ao extrair que "ex-fumantes" e "diabéticos" possuem maior associação com DCV, a IA pode ajudar médicos a estratificar o risco de pacientes em tempo real.
3.  **Personalização de Políticas Públicas:** A extração de dados sobre raça e escolaridade permite que a IA identifique desigualdades sociais na saúde, direcionando recursos para populações mais vulneráveis.
4.  **Construção de Grafos de Conhecimento:** Transforma o artigo em uma rede de informações conectadas, permitindo consultas complexas como: *"Quais fatores de estilo de vida mais influenciam a limitação intensa por doenças cardíacas no Brasil?"*



---

## 📊 Resumo de Dados Estruturados (Saída de NLP)

| Entrada (Texto do Artigo) | Técnica NLP | Dado Extraído |
| :--- | :--- | :--- |
| "5,3% dos adultos referiram DCV" | Extração Estatística | `prevalence: 0.053` |
| "Hipertensão, colesterol e diabetes" | NER | `comorbidities: [HBP, Chol, Diab]` |
| "Limitação intensa nas atividades" | Análise de Impacto | `severity_index: high` |

---

## 🛠️ Ferramentas Sugeridas
* **SpaCy (scispaCy):** Para processamento de termos biomédicos.
* **BioBERT:** Para entendimento contextual de artigos científicos.
* **Pandas & Regressão de Poisson:** Para validação dos dados estatísticos extraídos.

---
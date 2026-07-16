# Caderno Temático no NotebookLM - Banco de Dados para Concursos de TI (FGV)

## 📖 Sobre o Projeto

Este projeto foi desenvolvido como parte do desafio **"Criando um Caderno Temático com NotebookLM"** da DIO.

O objetivo foi utilizar o NotebookLM como ferramenta de aprendizagem ativa para produzir uma apostila de Banco de Dados baseada no conteúdo programático de um edital específico de concurso público organizado pela banca **FGV**. A proposta foi transformar cada tópico previsto no edital em um material de estudo aprofundado, organizado em módulos e adequado para uma preparação de longo prazo.

Ao longo do desenvolvimento, foi possível identificar limitações na geração de relatórios do NotebookLM. Por isso, diferentes estratégias de engenharia de prompts foram aplicadas para obter materiais cada vez mais completos e úteis para os estudos.

---

# 🎯 Objetivos de Estudo

Os principais objetivos deste caderno foram:

- desenvolver uma apostila completa a partir do conteúdo programático de um edital específico da FGV;
- aprofundar cada tópico previsto no edital, indo além de simples resumos;
- organizar o conteúdo em uma sequência lógica de aprendizagem;
- utilizar IA como ferramenta de apoio ao estudo, sem substituir a análise crítica do estudante;
- criar um material reutilizável para futuras revisões.

---

# 📚 Curadoria das Fontes

Inicialmente foram adicionadas ao NotebookLM algumas fontes abertas relacionadas ao tema Banco de Dados.

Posteriormente, foi inserido o conteúdo programático do edital como consulta ao NotebookLM. A partir desse programa, a ferramenta identificou e adicionou automaticamente novas fontes relacionadas aos tópicos previstos, ampliando significativamente a base de conhecimento utilizada na construção da apostila.

As fontes passaram a abranger assuntos como:

- Modelagem de Dados;
- Modelo Relacional;
- Normalização;
- SQL;
- Sistemas Gerenciadores de Banco de Dados (SGBD);
- Bancos de Dados NoSQL;
- Modelagem Dimensional;
- Data Lakes;
- Big Data.

### Fontes utilizadas

- *[Introdução a Banco de Dados](https://www.ime.usp.br/~jef/apostila.pdf)*
- *[Introdução a Modelagem de Dados](https://www.cin.ufpe.br/~rrbs/pronatec/Introdução%20a%20Modelagem%20de%20Dados.pdf)*
- *[Fundamentos de Banco de Dados](https://professor.ufop.br/sites/default/files/george/files/2020-2_apostila_cdd003.pdf)*
- *[Capítulo 3 do "Data Warehouse Toolkit"](http://wiki.icmc.usp.br/images/0/00/SCC0245_capitulo3.pdf)*
- *[Modelação de um Data Warehouse]([Inserir links](https://run.unl.pt/bitstream/10362/5366/1/TEGI0271.pdf))*
- *[Sistemas de Banco de Dados de Elmasri e Navathe)](https://www.kufunda.net/publicdocs/Sistemas%20de%20Banco%20de%20Dados%20(Ramez%20Elmasri,%20Shamkant%20B.%20Navathe).pdf)*
- *[Armazenamento de Big Data: Uma Abordagem Didática](https://fatece.edu.br/arquivos/arquivos-revistas/perspectiva/volume8/Dayse%20Silveira%20de%20Almeida;%20Danilo%20Borges%20Dutra.pdf)*

---

# 🧠 Engenharia de Prompts

## Primeira abordagem

Após adicionar as fontes iniciais, foi solicitado ao NotebookLM que produzisse um relatório completo sobre Banco de Dados.

### Prompt

> Produza um relatório completo sobre Banco de Dados utilizando todas as fontes disponíveis e seguindo o conteúdo programático a seguir: (conteúdo programático colado).

### Resultado

O relatório apresentou uma boa organização, porém ficou superficial para o objetivo do projeto, que era produzir uma apostila de estudos.

---

## Segunda abordagem (Refinamento)

Em vez de continuar utilizando apenas as fontes inicialmente selecionadas, foi utilizado o conteúdo programático do edital como guia para expandir automaticamente a base de documentos do NotebookLM.

Após a ampliação no repertório, foi elaborado um prompt muito mais detalhado, instruindo o NotebookLM a atuar como um professor especialista em concursos públicos.

Entre as principais instruções estavam:

- explicar conceitos do básico ao avançado;
- explicar todas as siglas;
- apresentar contexto histórico;
- explicar o funcionamento interno dos mecanismos;
- incluir exemplos práticos;
- destacar pegadinhas de concursos;
- criar questões comentadas;
- evitar resumos excessivos.


### Resultado

O número de fontes aumentou significativamente, cobrindo praticamente todos os tópicos previstos no edital utilizado como referência.

Mesmo com uma quantidade maior de documentos, o relatório permaneceu relativamente resumido.

Isso levou à hipótese de que o NotebookLM possui um limite prático para o tamanho dos relatórios gerados.

---

## Terceira abordagem (Solução adotada)

Como estratégia para contornar a limitação observada, o conteúdo programático foi dividido em módulos.

Cada módulo passou a gerar um relatório independente, permitindo explicações muito mais detalhadas.

A estrutura adotada foi:

- Módulo 1 — Fundamentos e Modelagem de Dados;
- Módulo 2 — Modelagem Dimensional;
- Módulo 3 — SQL;
- Módulo 4 — SGBDs, Propriedades e NoSQL;
- Módulo 5 — Big Data e Data Lakes.

Na prática, cada relatório passou a representar um capítulo da apostila construída a partir do conteúdo programático do edital.

### Prompt

> Você é um professor renomado especializado na preparação para concursos públicos de TI, com foco na banca FGV.
Seu objetivo é produzir uma apostila completa e aprofundada sobre os assuntos informados, suficiente para que o aluno consiga resolver questões de concurso com segurança. Se o conteúdo for extenso, divida-o em quantas partes forem necessárias. Nunca reduza a profundidade para caber em uma única resposta.
Escreva como um excelente professor presencial: linguagem clara, didática e progressiva. Não economize explicações nem faça resumos excessivos. Explique do básico ao avançado, sem assumir conhecimentos prévios além do que já foi apresentado anteriormente e o listado neste prompt.

Sempre apresente o significado das siglas antes de utilizá-las e explique cada termo técnico antes de empregá-lo.
Sempre que apresentar uma tecnologia, protocolo, comando, mecanismo, ferramenta ou conceito, responda:

O que é;
Por que surgiu;
Qual problema resolve;
Como funciona internamente;
Quando é utilizado;
Como costuma ser cobrado pela FGV;
Quais são as pegadinhas mais frequentes.

Sempre que pertinente, inclua:

contexto histórico;
funcionamento interno;
exemplos práticos;
analogias apenas quando realmente facilitarem o entendimento;
diferenças entre conceitos semelhantes;
vantagens, desvantagens e limitações.

Dê preferência a explicações em texto corrido, conectando as ideias. Evite listas fragmentadas quando uma explicação contínua for mais didática.

Destaque explicitamente:

pegadinhas clássicas de concursos;
erros conceituais explorados pela FGV;
diferenças entre conceitos parecidos;
motivos pelos quais alternativas incorretas estariam erradas.

Ao final de cada parte, apresente obrigatoriamente:

resumo dos pontos mais importantes;
questões inéditas no estilo FGV;
comentários detalhados justificando cada alternativa correta e incorreta.

Conteúdo programático já dado:

MÓDULO 1 – Fundamentos e Modelagem de Dados
1.1 Modelagem de dados (conceitual, lógica e física) 
1.2 Abordagem relacional 
1.3 Normalização das estruturas de dados 
1.4 Integridade referencial 
1.5 Metadados 
MÓDULO 2 – Modelagem Dimensional (Foco em BI — direto ligado ao perfil "Inteligência da Informação")
2.1 Modelagem dimensional — Item 6
MÓDULO 3 – Linguagens de Banco de Dados (SQL)
3.1 Linguagem de consulta estruturada (SQL) 
3.2 Linguagem de definição de dados (DDL)
3.3 Linguagem de manipulação de dados (DML) 
MÓDULO 4 – SGBD, Propriedades e Novos Modelos
4.1 SGBD 
4.2 Propriedades de banco de dados
4.3 Banco de dados NoSQL 
4.4 Banco de dados em memória 

Conteúdo desta apostila:
MÓDULO 5 – Big Data e Data Lakes
5.1 Data lakes e soluções para big data
Data Lake x Data Warehouse (diferenças de estrutura, schema-on-read x schema-on-write)
Os "V"s do Big Data (Volume, Velocidade, Variedade, Veracidade, Valor)
Ferramentas típicas de ecossistema Big Data (Hadoop, HDFS, Spark — bom ter noção geral mesmo não estando explícito no edital)
Conceito de Data Lakehouse (tendência atual que une DW + Data Lake)

---

## Tentativa de utilização do Deep Search

Também foi realizado um experimento utilizando o recurso Deep Search com o seguinte prompt:

> Questões de concursos sobre Bancos de Dados feitas de 2020 até hoje.

### Resultado esperado

Obter questões reais de concursos recentes para complementar o material de estudos.

### Resultado obtido

Em vez disso, o NotebookLM gerou um documento chamado:

> **"Análise Estritamente Técnica das Questões de Bancos de Dados em Certames de Tecnologia da Informação de 2020 a 2026"**

Entretanto:

- nenhuma fonte foi citada;
- nenhuma questão real foi apresentada;
- o documento consistia apenas em uma análise produzida pela IA.

Apesar dessa limitação, o material foi mantido como complemento, acompanhado da ressalva de que não representa uma compilação de questões reais.

---

# ⚠️ Troubleshooting (Lições Aprendidas)

Durante o projeto foram observadas algumas limitações importantes:

- relatórios muito extensos tendem a perder profundidade;
- aumentar apenas a quantidade de fontes não garante respostas mais completas;
- dividir um assunto grande em módulos produz resultados significativamente melhores;
- prompts detalhados ajudam, mas não eliminam limitações relacionadas ao tamanho das respostas;
- o Deep Search nem sempre recupera documentos reais, podendo gerar apenas análises produzidas pela própria IA.

Essas observações foram fundamentais para definir a estratégia final utilizada.

---

# 📖 Miniguia de Estudos

O resultado final não foi apenas um relatório sobre Banco de Dados, mas uma apostila organizada seguindo a estrutura do conteúdo programático do edital utilizado como referência.

## Estrutura Final Produzida

- Relatório geral (utilizado como visão geral e revisão);
- Apostila do Módulo 1;
- Apostila do Módulo 2;
- Apostila do Módulo 3;
- Apostila do Módulo 4;
- Apostila do Módulo 5;
- Análise complementar produzida pelo Deep Search.

---

# 📚 Glossário

| Termo | Definição |
|--------|-----------|
| MER | Modelo Entidade-Relacionamento |
| DER | Diagrama Entidade-Relacionamento |
| SGBD | Sistema Gerenciador de Banco de Dados |
| SQL | Structured Query Language |
| DDL | Data Definition Language |
| DML | Data Manipulation Language |
| ACID | Atomicidade, Consistência, Isolamento e Durabilidade |
| NoSQL | Bancos de dados não relacionais |
| Data Warehouse | Repositório estruturado para análise de dados |
| Data Lake | Repositório para armazenamento de dados estruturados e não estruturados |

---

# 🔁 Prompts Reutilizáveis

## Criar apostila

> Atue como um professor especialista em concursos públicos de TI da banca FGV e produza uma apostila completa sobre este assunto. Explique todos os conceitos do básico ao avançado, apresente exemplos, funcionamento interno, pegadinhas de prova e questões comentadas.

---

## Revisão

> Faça um resumo estruturado destacando os conceitos mais importantes deste módulo, enfatizando as relações entre os assuntos e os pontos de maior atenção para revisão.

---

## Questões

> Elabore 10 questões inéditas no estilo FGV com comentários detalhados justificando todas as alternativas corretas e incorretas.

---

## Comparação de conceitos

> Compare detalhadamente os conceitos abaixo, destacando diferenças, vantagens, desvantagens e pegadinhas de concurso.

---

## Revisão Final

> Crie uma revisão completa deste conteúdo destacando os conceitos essenciais, erros conceituais frequentes e possíveis pegadinhas que podem aparecer em provas.

---

# 💡 Considerações Finais

O principal aprendizado deste projeto foi compreender que o uso eficiente de Inteligência Artificial depende não apenas da qualidade das fontes, mas também da estratégia utilizada na formulação dos prompts.

Ao longo do desenvolvimento, foi necessário testar diferentes abordagens, identificar limitações do NotebookLM e adaptar continuamente a estratégia de geração dos relatórios. O resultado foi a construção de uma apostila organizada a partir do conteúdo programático do edital, permitindo estudar cada tópico de forma independente e com maior profundidade do que seria possível em um único relatório.

A experiência demonstrou, na prática, que dividir um assunto extenso em módulos guiados pelo programa do concurso produz materiais de estudo mais completos e úteis do que tentar sintetizar todo o conteúdo em um único documento, evidenciando a importância da engenharia de prompts como habilidade para potencializar ferramentas baseadas em Inteligência Artificial.

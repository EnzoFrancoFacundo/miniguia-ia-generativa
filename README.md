# miniguia-ia-generativa

📓 Caderno Temático: IA Generativa para Devs
🎯 Contexto e Objetivos
Assunto escolhido: Fundamentos de Inteligência Artificial Generativa (IAGen) com foco em desenvolvedores que desejam integrar modelos como GPT, Gemini ou LLaMA em suas aplicações.

Objetivos de estudo:

Compreender os conceitos fundamentais por trás dos modelos generativos (transformers, tokens, embeddings, atenção).

Diferenciar abordagens: prompt engineering, fine-tuning e RAG (Retrieval-Augmented Generation).

Identificar boas práticas e limitações éticas e técnicas ao usar IAGen em software.

Criar um conjunto de prompts reutilizáveis para acelerar o aprendizado contínuo.

📚 Curadoria de Fontes (PDFs/TXT utilizados no NotebookLM)
Selecionei fontes abertas, confiáveis e com profundidade técnica adequada:

"Attention Is All You Need" (Vaswani et al., 2017) – Paper original do Transformer.
🔗 Link para PDF

"Generative AI: A Developer’s Guide" (capítulo introdutório) – Microsoft Learn.
🔗 Link para PDF

"What is RAG?" (AWS documentation) – Explicação prática sobre Retrieval-Augmented Generation.
🔗 Link para PDF

"Prompt Engineering Guide" (Anthropic) – Guia oficial com exemplos e armadilhas.
🔗 Link para PDF

"Ethical Guidelines for Generative AI" (UNESCO, 2023) – Resumo executivo.
🔗 Link para PDF

Nota: Baixe os PDFs e faça o upload no NotebookLM para criar seu caderno temático interativo.

🧠 Engenharia de Prompts e "Cicatrizes" (Troubleshooting)
Aqui documentei as perguntas estratégicas, variações de prompt e dificuldades encontradas ao extrair o melhor das IAs.

✅ Prompts que funcionaram bem
Objetivo	Prompt testado	Resultado obtido
Entender transformers de forma simples	"Explique o conceito de 'atenção' no Transformer como se eu fosse um desenvolvedor que conhece loops e matrizes, mas não ML"	Resposta clara com analogia de banco de dados e pesos.
Comparar fine-tuning vs RAG	"Quais são as vantagens de usar RAG em vez de fine-tuning para um chatbot que precisa responder sobre documentação interna que muda toda semana?"	Ótima tabela comparativa de custo, atualização e latência.
Identificar viés	"Dê 3 exemplos concretos de viés que podem aparecer num modelo generativo usado para gerar código"	Exemplos: viés de linguagem (Python > R), segurança (injeção de SQL) e estereótipos em comentários.
⚠️ Cicatrizes (o que deu errado e como resolvi)
Problema	Tentativa	Correção
Resposta muito genérica sobre ética	"Fale sobre ética na IA generativa"	Refinei para: "Cite 3 riscos específicos para aplicações empresariais que usam dados de clientes em prompts" – aí veio algo útil.
Alucinação sobre datas de papers	"Qual foi o primeiro modelo generativo de código?"	IA inventou "CodeGPT-2019". Pedi fontes e refiz com: "Com base APENAS nos PDFs enviados, qual foi o primeiro..." – melhorou.
Explicação muito densa sobre tokens	"Como funciona tokenização?"	Adicionei: "Mostre com um exemplo em Python pseudo-código" – clareza aumentou muito.
💡 Dica de ouro
Use "Com base nos documentos enviados..." sempre que quiser evitar alucinações.
Peça "Mostre onde no texto você encontrou essa informação" para rastreabilidade.

📘 Miniguia de Estudo (Entrega Final)
📝 Resumos estruturados
1. Transformers e Atenção
O mecanismo de atenção permite que o modelo pondere a importância de cada palavra/token em relação aos outros.

Diferente de RNNs, o Transformer processa a sequência toda em paralelo (graças à atenção multi-head).

Q, K, V = Query, Key, Value – cada token projeta esses três vetores para calcular similaridade.

2. RAG vs Fine-tuning
Critério	RAG	Fine-tuning
Atualização de conhecimento	Imediata (basta trocar a base)	Requer novo treinamento
Custo computacional	Baixo (só busca + inferência)	Alto (backpropagation)
Ideal para	Documentos dinâmicos, poucos exemplos	Estilo/tom fixo, muitos exemplos
3. Boas práticas de prompt engineering
Seja específico: "Responda como se fosse um sênior revisando código"

Dê exemplos (few-shot)

Defina formato de saída (JSON, tabela, apenas código)

Use delimitadores (###, """) para separar instrução do contexto.

📖 Glossário de conceitos principais
Termo	Definição
Token	Unidade mínima de texto (palavra, subpalavra ou caractere) que o modelo processa.
Embedding	Representação numérica (vetor) de um token em um espaço semântico.
Atenção (Attention)	Mecanismo que calcula relevância entre tokens para guiar a geração.
Alucinação	Quando o modelo gera informação falsa com alta confiança.
Contexto (Context window)	Número máximo de tokens que o modelo consegue "enxergar" de uma vez.
RAG	Busca em uma base externa para enriquecer o prompt antes da geração.
Fine-tuning	Treinamento adicional de um modelo pré-treinado com dados específicos.
Prompt engineering	Arte de formular entradas para obter saídas desejadas.
🔁 Conjunto de prompts reutilizáveis (para futuras revisões)
Copie e cole estes prompts no NotebookLM ou qualquer LLM:

text
1. RESUMO RÁPIDO:
   "Com base nos materiais enviados, me explique [conceito X] em 3 parágrafos. Depois, me dê uma analogia com programação."

2. COMPARAÇÃO TÉCNICA:
   "Compare [termo A] e [termo B] em uma tabela com 4 critérios: definição, quando usar, vantagem e desvantagem."

3. EXTRAÇÃO DE CITAÇÕES:
   "Liste 3 ideias centrais do documento [nome do PDF] com a página onde cada uma aparece."

4. GERAÇÃO DE EXERCÍCIOS:
   "Crie 3 questões de múltipla escolha sobre [tópico] para eu testar meu entendimento. Forneça respostas depois."

5. ARQUITETURA DE CÓDIGO:
   "Baseado nos conceitos de RAG, escreva um pseudo-código de uma função que busca documentos relevantes antes de chamar uma API de LLM."

6. REVISÃO ÉTICA:
   "Dadas as diretrizes da UNESCO nos materiais, liste 3 checklists que um dev deveria aplicar antes de lançar um feature com IA generativa."
🚀 Como usar este repositório para evoluir
Importe os PDFs das fontes para o NotebookLM.

Recrie os prompts da seção de engenharia e veja se as respostas batem.

Adapte o miniguia para seu próprio assunto – troque conceitos, glossário e prompts.

Commit frequente no GitHub registrando novas "cicatrizes" conforme você avança.

📎 Links úteis
[NotebookLM (Google Labs)](https://notebooklm.google.com/notebook/f4066bc1-920b-4bf8-87ef-837c1370ac31)

Meu perfil na DIO: Enzo Facundo

Repositório(https://github.com/EnzoFrancoFacundo/miniguia-ia-generativa/edit/main/README.md)


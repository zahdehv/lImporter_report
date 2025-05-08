<!-- instrucciones (meta-informacion, no va en el latex):
- usar las referencias tal como aparecen entre []
- no usar listas, las listas de abajo son secuencias de informaciones a incluir
- usar \citep en lugar de \cite. Si se menciona explicitamente (e.g. como fue investigado en {cita}) si se puede usar \cite
- actua como un investigador confeccionando un trabajo de tesis
- es un trabajo de relevancia para el fin de la carrera universitaria del autor
- siempre usa Grandes Modelos de Lenguaje (el grandes al final queda muy feo)
- # chapter, ## section, ### subsection #### subsubsection a no ser que haya otra indicacion -->

# introduccion:
- usar info del libro second brain y taking notes para la importancia de la gestion del conocimiento
- hablar del potencial de los LLM para lo de arriba y de la utilidad de la automatizacion de esta integracion de conocimiento

<!-- state of the art (): -->

## gestion de conocimiento personal(second brain):
- introducir la ancestral accion de tomar notas (use wiki: Note-taking) (en \paragraph{Note-taking}) (de aqui quiero que cites a [jansenIntegrativeReviewCognitive2017] cuando menciones que "Note-taking is a good strategy to enhance learning and memory")
- introducir la gestion de conocimiento personal (PKM) usando adjunto de wikipedia: Personal knowledge management citando a [grundspenkisAgentBasedApproach2007]
    - aqui es importante que introduzcas a los Knowledge workers (wiki: Knowledge worker) como el sector principal relacionado a esta area

### Metodologias de toma de notas (de la wiki: Note-taking):
- Usar la lista de Systems, dividiendo en lineales y no lineales
    - en cornell notes citar a [paukHowStudyCollege2010]
- incluir tambien luego:
    - mention zettelstaken mentioned in How to take smart notes (slip-box) [ahrensHowTakeSmart2017]
    - mention the PARA method from Building a Second Brain[forteBuildingSecondBrain2022]

### bases de conocimiento personal
- introducir las bases de conocimiento personal (PKB) (usando adjunto de wikipedia: Personal knowledge base)
- mencionar memex (memory extension) [bushWeMayThink1979], usando adjunto de (wiki: Memex)
- menciona 'Data models' (de wikipedia: Personal knowledge base) 
    - las referencias aqui son [1] -> [daviesBuildingMemexSixty], [2] -> [daviesStillBuildingMemex2011], en los estudios de Davies

#### grafos de conocimiento personal (esto va en un \paragraph{})
- introducir los grafos de conocimiento personal (PKG) (usando adjunto de wikipedia: Personal knowledge base) citando, donde [8] - > [pyneMetaworkHowWe2022]

#### Sistemas digitales de toma de notas
- introducir con el articulo de la wiki
De los tres principales me gustaria que trataras la informacion introducida en 'Data models', incluyendo el proceso de transclusion:
    - Obsidian (usando wiki: Obsidian),
    - Notion (usando wiki: Notion)
    - Roam Research (usando wiki: Roam)
- usar el articulo de la wiki: Comparison of note-taking software, para ampliar ejemplos (mencionar unas pocas)

## Grandes Modelos de lenguaje (LLM)
- Introducir los modelos de lenguaje y citar reportes tecnicos (gpt4[openaiGPT4TechnicalReport2024], gemini[teamGeminiFamilyHighly2024], y la competencia foss deepseek[deepseek-aiDeepSeekV3TechnicalReport2024], qwen[baiQwenTechnicalReport2023], llama[grattafioriLlama3Herd2024])

### prompting techniques:
- mencionar que es necesario conocer las formas de interactuar con estos modelos de lenguaje para sacar partido a sus capacidades
- mencionar la capacidad de generalizacion a traves de pocos ejemplos de estos modelos de lenguaje (sin ajustar sus parametros) [brownLanguageModelsAre2020], el estudio de las partes de los ejemplos que permiten al modelo llevar a cabo la tarea, que no necesariamemte es la etiqueta lo fundamental [minRethinkingRoleDemonstrations2022 (la idea es explicar que puede resultar mucho mas util que muestre al modelo la distribucion del texto, formato, forma de proceder, que contener la etiqueta correcta)], y con el crecimiento de la ventana de contexto el paso a aprendizaje con muchos ejemplos [agarwalManyShotInContextLearning2024]
- incluir role-prompting[kongBetterZeroShotReasoning2024] y style prompting[luBoundingCapabilitiesLarge2023], como formas de que el modelo resuelva la tarea siguiendo una forma de proceder o un estilo determinado, de acuerdo a las necesidades
    - Role Prompting assigns a specific role to the GenAI in the prompt. For example, the user might prompt it to act like "Madonna" or a "travel writer". This can create more desirable outputs for open-ended tasks and in some cases may improve accuracy on benchmarks
    - Style Prompting involves specifying the desired style, tone, or genre in the prompt to shape the output of a GenAI. A similar effect can be achieved using role prompting.
- mencionar que esta generalizacion puede ser aprovechada para pedirle a los modelos que generen pasos intermedios para mejorar la calidad de las respuestas [nyeShowYourWork2021, weiChainofThoughtPromptingElicits2023]
- explicar que se ha explorado tambien este paradigma sin el uso de ejemplos [kojimaLargeLanguageModels2023, wangPlanandSolvePromptingImproving2023], haciendo que el modelo genere los pasos por alguna frase o instruccion que promueva este formato de respuesta
- mencionar que existen tecnicas basadas en el aprovechamiento de la complejidad y descomposicion [fuComplexityBasedPromptingMultiStep2023, zhouLeasttoMostPromptingEnables2023]
- mencionar que algunas estrategias usan la consistencia entre varias generaciones de texto del mismo modelo [wangSelfConsistencyImprovesChain2023]
- mencionar el Uso de estructuras que permiten la exploracion del espacio de busqueda despues de la descomposicion para la solucion de los problemas [yaoTreeThoughtsDeliberate2023, bestaGraphThoughtsSolving2024]
- mencionar buffer of thought [yangBufferThoughtsThoughtAugmented2024], que va acumulando cadenas de razonamiento en un buffer, y los recupera acordemente segun la tarea nueva, de manera similar a analogical reasoning, que trata de aprovechar experiencias sobre el pasado y la capacidad humana de hallar similes [yasunagaLargeLanguageModels2024]
- mencionar step back prompting, que hace q el modelo resuelva una instancia mas general y abstracta del problema (a step-back question), que suele ser mas sencilla y evita desviarse del problema central por el exceso de detalles, antes de resolver el problema original
- inducir al modelo a hacer un analisis del modo a proceder antes de generar la cadena de razonamiento[gaoMetaReasoningLarge2024]
- Self-Ask prompts LLMs to first decide if they need to ask follow up questions for a given prompt. If so, the LLM generates these questions, then answers them and finally answers the original question[pressMeasuringNarrowingCompositionality2023]
- Self-Refine is an iterative framework where, given an initial answer from the LLM, it prompts the same LLM to provide feedback on the answer, and then prompts the LLM to improve the answer based on the feedback. This iterative process continues until a stopping condition is met (e.g., max number of steps reached)[madaanSelfRefineIterativeRefinement2023]
- mencionar las tecnicas que reformulan o hacen que el modelo se replantee la entrada o problema [mishraReframingInstructionalPrompts2022, dengRephraseRespondLet2024]
- mencionar las tecnicas que aprovechan representaciones graficas usando texto (Minds Eye)[wuMindsEyeLLMs] o procesos cognitivos, como sketch of thought [aytesSketchofThoughtEfficientLLM2025] o Metacognitive Prompting[wangMetacognitivePromptingImproves2024]
- (esta lista potencialmente podria ser ordenada para una mayor coherencia con las fechas o conceptos(estos son mas importantes, muchas ideas similares han aparecido en este campo))
- Cumulative Reasoning first generates several potential steps in answering the question. It then has a LLM evaluate them, deciding to either accept or reject these steps. Finally, it checks whether it has arrived at the final answer. If so, it terminates the process, but otherwise it repeats it[zhangCumulativeReasoningLarge2025]

### agents:
- Mencionar que el potencial de los LLM radica principalmente en la autonomia y capacidad de realizar tareas usando herramientas en lugar del humano, aprovechando las ventajas que tienen para el manejo de la informacion
    - As LLMs have improved rapidly in capabilities companies and researchers have explored how to allow them to make use of external systems. This has been necessitated by shortcomings of LLMs in areas such as mathematical computations, reasoning, and factuality
- Modular Reasoning, Knowledge, and Language (MRKL) System [karpasMRKLSystemsModular2022] is one of the simplest formulations of an agent. It contains a LLM router providing access to multiple tools. The router can make multiple calls to get information such as weather or the current date. It then combines this information to generate a final response. 
- Program-aided Language Model (PAL) [gaoPALProgramaidedLanguage2023] translates a problem directly into code, which is sent to a Python interpreter to generate an answer and Tool-Integrated Reasoning Agent (ToRA) (Gou et al., 2024b) that instead of a single code generation step, it interleaves code and reasoning steps for as long as necessary to solve the problem
- Reasoning and Acting (ReAct) [yaoReActSynergizingReasoning2023] generates a thought, takes an action, and receives an observation (and repeats this process) when given a problem to solve. All of this information is inserted into the prompt so it has a memory of past thoughts, actions, and observations (observation based agent); and Reflexion[shinnReflexionLanguageAgents2023] (which builds upon react), a novel framework to reinforce language agents not by updating weights, but instead through linguistic feedback. Concretely, Reflexion agents verbally reflect on task feedback signals, then maintain their own reflective text in an episodic memory buffer to induce better decision-making in subsequent trials.
- Retrieval Augmented Generation (RAG) In the context of GenAI agents, RAG is a paradigm in which information is retrieved from an external source and inserted into the prompt. This can enhance performance in knowledge intensive tasks [lewisRetrievalAugmentedGenerationKnowledgeIntensive2021]. When retrieval itself is used as an external tool, RAG systems are considered to be agents

## Integracion de herramientas basadas en LLM en applicaciones de toma de notas
- here i want you to include tools using LLM in the KBM context (use files llm_tools_dr_gm.md and llm_tools_dr_gp.md)

## Objetivos
- aqui quiero que menciones que el objetivo del trabajo es dar un paso en la automatizacion de la construccion incremental y progresiva de bases de conocimiento (como fue tratado en [fragaAutomaticGenerationKnowledge2023]), pero usando las ventajas de los modelos de lenguaje con el fin de generar informacion en el contexto de las bases de conocimiento, particularmente el caso de notas semiestructuradas (usando un lenguaje markup) relacionadas entre si, formando un grafo de conocimiento, y cubriendo, por la libertad de las mismas, las diferentes metodologias y sistemas de toma de notas. 
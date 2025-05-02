<!-- instrucciones (meta-informacion, no va en el latex):
- usar las referencias tal como aparecen entre []
- no usar listas, las listas de abajo son secuencias de informaciones a incluir
- usar \citep en lugar de \cite
- actua como un investigador confeccionando un trabajo de tesis
- es un trabajo de relevancia para el fin de la carrera universitaria del autor
- siempre usa Grandes Modelos de Lenguaje (el grandes al final queda muy feo) -->

# introduccion:
- mencionar el afan del ser humano de obtener informacion para entender el mundo a su alrededor, la necesidad de tener una forma accesible para el mismo a la informacion, y las limitaciones de la memoria de trabajo del humano [millerMagicalNumberSeven1956]
- mencionar el cambio que supone la llegada de los grandes modelos de lenguaje para la interaccion del trabajador del conocimiento con estas herramientas y con el conocimiento mismo (cambios en la interfaz humano maquina)

<!-- state of the art (): -->
## toma de notas (requiere esto siquiera una introduccion? (sarcasmo, incluir))
- introducir la ancestral accion de tomar notas (use wiki)

### Metodologias de toma de notas:
- cornell notes [paukHowStudyCollege2010]
- PARA [buscar cita]
- seguir lista

## gestion de conocimiento personal:
- introducir la gestion de conocimiento personal (PKM) usando adjunto de wikipedia

### bases de conocimiento personal
- introducir las bases de conocimiento personal (PKB) usando adjunto de wikipedia
- mencionar memex [buscar cita]

#### grafos de conocimiento personal
- introducir los grafos de conocimiento personal (PKG) usando adjunto de wikipedia

#### Sistemas digitales de toma de notas
- Obsidian
- Notion
- etc (mencionar algunos pero es extensa la lista)

## Grandes Modelos de lenguaje (LLM)
- Introducir los modelos de lenguaje y citar reportes tecnicos (principalmente claude, gpt4, gemini, y la competencia foss deepseek, qwen, mistral, llama)
- Introducir el potencial de los LLM como posible cambio de paradigma en la misma interfaz humano maquina
- Mencionar las principales formas de uso y herramientas existentes: a list (se incluyen esta forma y esta con tal y tal objetivo)

### prompting the models:
- mencionar que es necesario conocer las formas de interactuar con estos modelos de lenguaje para sacar partido a sus capacidades
- mencionar la capacidad de generalizacion a traves de pocos ejemplos de estos modelos de lenguaje (sin ajustar sus parametros) [brownLanguageModelsAre2020] 
- mencionar el estudio de las partes de los ejemplos que permiten al modelo llevar a cabo la tarea, que no necesariamemte es la etiqueta lo fundamental [minRethinkingRoleDemonstrations2022], y con el crecimiento de la ventana de contexto el paso a aprendizaje con muchos ejemplos [agarwalManyShotInContextLearning2024] (la idea es explicar que puede resultar mucho mas util que muestre al modelo la distribucion del texto, formato, forma de proceder, que contener la etiqueta correcta)
- incluir role-prompting y style prompting [buscar citas], como formas de que el modelo resuelva la tarea siguiendo una forma de proceder o un estilo determinado, de acuerdo a las necesidades
- mencionar que esta generalizacion puede ser aprovechada para pedirle a los modelos que generen pasos intermedios para mejorar la calidad de las respuestas [nyeShowYourWork2021, weiChainofThoughtPromptingElicits2023]
- explicar que se ha explorado tambien este paradigma sin el uso de ejemplos [kojimaLargeLanguageModels2023, wangPlanandSolvePromptingImproving2023], haciendo que el modelo genere los pasos por alguna frase o instruccion que promueva este formato de respuesta
- mencionar que existen tecnicas basadas en el aprovechamiento de la complejidad y descomposicion [fuComplexityBasedPromptingMultiStep2023, zhouLeasttoMostPromptingEnables2023]
- mencionar que algunas estrategias usan la consistencia entre varias generaciones de texto del mismo modelo [wangSelfConsistencyImprovesChain2023]
- mencionar el Uso de estructuras que permiten la exploracion del espacio de busqueda despues de la descomposicion para la solucion de los problemas [yaoTreeThoughtsDeliberate2023, bestaGraphThoughtsSolving2024]
- mencionar buffer of thought [cita here], que va acumulando cadenas de razonamiento en un buffer, y los recupera acordemente segun la tarea nueva, de manera similar a analogical reasoning, que trata de aprovechar experiencias sobre el pasado y la capacidad humana de hallar similes [cita]
- Tecnicas que hacen q el modelo resuelva una instancia mas general y abstracta del problema (a step-back question), que suele ser mas sencilla y evita desviarse del problema central por el exceso de detalles, antes de resolver el problema original, y otras que promueven que el modelo haga un metaanalisis sobre el razonamiento a seguir [gaoMetaReasoningLarge2024]
- mencionar las tecnicas que reformulan o hacen que el modelo se replantee la entrada o problema [mishraReframingInstructionalPrompts2022, dengRephraseRespondLet2024]
- mencionar las tecnicas que aprovechan representaciones graficas usando texto (Minds Eye) o procesos cognitivos, como sketch of thought
- (esta lista potencialmente podria ser ordenada para una mayor coherencia con las fechas o conceptos(estos son mas importantes, muchas ideas similares han aparecido en este campo))

### agents:
- Mencionar que el potencial de los LLM radica principalmente en la autonomia y capacidad de realizar tareas usando herramientas en lugar del humano, aprovechando las ventajas que tienen para el manejo de la informacion
- lista con tecnicas de agentes y ejemplos de agentes para la investigacion, desarrollo, analisis de datos, etc
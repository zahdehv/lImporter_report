instrucciones (meta informacion, no va en el latex):
- usar las referencias tal como aparecen entre []
- no usar listas, las listas de abajo son secuencias de informaciones a incluir
- usar \citep en lugar de \cite

- mencionar el afan del ser humano de obtener informacion para entender el mundo a su alrededor, la necesidad de tener una forma accesible para el mismo a la informacion, y las limitaciones de la memoria de trabajo del humano [millerMagicalNumberSeven1956]
- introducir los sistemas de gestion de conocimiento personal (PKM) y mencionar que juegan un papel crucial
- mencionar el cambio que supone la llegada de los grandes modelos de lenguaje para la interaccion del trabajador del conocimiento con estas herramientas y con el conocimiento mismo (cambios en la interfaz humano maquina)

## state of the art (no debe ser creada una seccion de estado del arte):
note taking methodologies:
- here a list
- here include mentioning the apps

ai tools (mainly including the means of interaction and the intended usage):
- here a list

prompting techniques:
- mencionar la capacidad de generalizacion a traves de pocos ejemplos de estos modelos de lenguaje (sin ajustar sus parametros) [brownLanguageModelsAre2020] 
- mencionar el estudio de las partes de los ejemplos que permiten al modelo llevar a cabo la tarea, que no necesariamemte es la etiqueta lo fundamental [minRethinkingRoleDemonstrations2022], y con el crecimiento de la ventana de contexto el paso a aprendizaje con muchos ejemplos [agarwalManyShotInContextLearning2024] (la idea es explicar que puede resultar mucho mas util que muestre al modelo la distribucion del texto, formato, forma de proceder, que contener la etiqueta correcta)
- mencionar que esta generalizacion puede ser aprovechada para pedirle a los modelos que generen pasos intermedios para mejorar la calidad de las respuestas [nyeShowYourWork2021, weiChainofThoughtPromptingElicits2023]
- explicar que se ha explorado tambien este paradigma sin el uso de ejemplos [kojimaLargeLanguageModels2023, wangPlanandSolvePromptingImproving2023], haciendo que el modelo genere los pasos por alguna frase o instruccion que promueva este formato de respuesta
- mencionar que existen tecnicas basadas en el aprovechamiento de la complejidad y descomposicion [fuComplexityBasedPromptingMultiStep2023, zhouLeasttoMostPromptingEnables2023]
- mencionar que algunas estrategias usan la consistencia entre varias generaciones de texto del mismo modelo [wangSelfConsistencyImprovesChain2023]
- mencionar el Uso de estructuras que permiten la exploracion del espacio de busqueda despues de la descomposicion para la solucion de los problemas [yaoTreeThoughtsDeliberate2023, bestaGraphThoughtsSolving2024]
- Tecnicas como Step-Back Prompting, a simple prompting technique that enables LLMs to do abstractions to derive high-level concepts and first principles from instances containing specific detail (el modelo resuelve una instancia mas general y abstracta del problema (the step-back question), que suele ser mas sencilla y evita desviarse del problema central por el exceso de detalles)
- mencionar las tecnicas que reformulan o hacen que el modelo se replantee la entrada o problema [mishraReframingInstructionalPrompts2022] asi como hacer un metaanalisis sobre el procedimiento a seguir [gaoMetaReasoningLarge2024]

agents:
- here a list
<img src="/banner.png">

# CEIA - Procesamiento del Lenguaje Natural 1

En este repositorio se encuentran los desafíos realizados para la materia Procesamiento del Lenguaje Natural 1, de la especialización en Inteligencia Artificial de FIUBA.
A continuación se brinda un resumen del alcance de cada uno.

## Desafío 1: BoW sobre 20 Newsgroups

Se exploró la capacidad del enfoque BoW (*Bag of Words*) para capturar similaridad entre documentos y clasificarlos.

[[Link al notebook]](/Desafio_1.ipynb)

* Se trabajó con el dataset 20 newsgroups
* Se implementó un clasificador 0-shot utilizando similaridad coseno y 1-NN sobre vectorizaciones TF-IDF de los artículos.
* Se entrenaron modelos de la familia Naïve Bayes, donde se observó la ventaja del ComplementNB para estos casos.
* Se estudió la similaridad entre términos, a partir de la traspuesta de la matriz término-documento.

## Desafío 2: Word2Vec sobre canciones de Eminem

Se entrenó un modelo de Word2Vec sobre letras de canciones de Eminem y se estudiaron propiedades emergentes.

[[Link al notebook]](/Desafio_2.ipynb)

* Se analizó el efecto de la dimensionalidad y tamaño de la ventana en la capacidad explicativa de las representaciones vectoriales.
* Para una selección de términos se analizaron los más y menos similares en base a similaridad coseno.
* Se estudiaron gráficos de dispersión (no apreciables en el visor online de GitHub) 2d y 3d de los vectores de palabras.

## Desafío 3: Generación de texto con tokens por caracteres

Se estudió la capacidad de un modelo de generación de texto en PyTorch, utilizando redes recurrentes y tokens a nivel de caracter.

[[Link al notebook]](/Desafio_3.ipynb)

* Se entrenó el modelo sobre literatura clásica.
* Se aplicó tokenización a nivel de caracter.
* Se ajustó por Perplexity, con early stopping sobre un set de validación.
* Se compararon celdas de Elman, LSTM y GRU en términos de performance y velocidad.
* Se estudió el impacto del ancho (cantidad de neuronas por capa) vs la profundidad (cantidad de capas recurrentes) en la performance de modelo.
* Se estudió la diferencia en la generación de secuencias entre métodos de sampleo greedy, beam search determinísticos y beam search estocástico. Para este último, se verificó el impacto de la temperatura en la diversidad de secuencias generadas.

## Desafío 4: Traductor inglés → español

Se entrenó un modelo seq2seq en PyTorch de traducción de frases de inglés a español basado en redes recurrentes (LSTM).

[[Link al notebook]](/Desafio_4.ipynb)

* Se estudió el efecto de la cantidad de capas, su ancho, regularización y learning rate en la performance del modelo.
* Se implementó un esquema de sampling estocástico con top_p, top_k y temperatura ajustables.
* Se utilizaron embeddings de fastText preentrenados para cada idioma, manteniéndolos freezeados para reducción drástica de parámetros entrenables.

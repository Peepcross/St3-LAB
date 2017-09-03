# Laboratorio 03 - Ensamblaje de genomas y predicción de genes

## Parte 1: El artículo genoma

### Genoma de interes 	Canis lupus familiaris

¿Cuántos genomas han sido depositados en GOLD? ¿Son los mismos de GENBANK?

Si observamos en Sequencing Projects existen 11598 ya completados, lo que indicaria que existe la misma cantidad de genomas completos depositados, asi mismo los proyectos incompletos, 53156, señalan que eventualemnete existira el mismo numero de genomas adicionandose a los mencionados anterirmente. En GENBANK, se señalan 80576 proyectos de secuenciacion entre eucaria, bacteria, etc.  

¿Cuál es la distribución de procariontes y eucariontes secuenciados?

En la seccion "Organisms" podemos observar que existen 249.701 secuenciaciones para procariontes y tan solo 18.241 para eucariontes. Entre ambas podemos calcular una relacion aproximada de 14:1 respectivamente.

¿Qué es el N50, L50, NG50?

El N50 es una medida estadistica que indica el largo del contig o fragmento ubicado justo cuando la suma, de mayor a menor longitud, de todos los contig alcanza la mitad del total de la misma suma. Por ejemplo si tenemos la suma de contigs de largo 7,6,5,4,3,1. El resultado de la suma es 26, por lo que la mitad serian 13, sumando 7 + 6 llegamos a este valor. Por esto el N50 de esta secuencia seria N50=6.

El L50 usando el mismo ejemlo anterior seria el menor numero de contigs usados para llegar a la mitad de la suma, o sea L50=2, porque solo usamos el 7 y el 6.

El NG50 sigue el mismo principio que el N50 solo que es en relacion a la longitud total del genoma.

¿Cuál es el propósito de calcular estas estadísticas?

El proposito de estos calculos es relacionar el largo de los contigs, reads o scaffolds con el largo original de la secuencia para juzgar la calidad del procedimiento de secuenciacion.

¿Cuál es el genoma que escogiste? Adjunta la referencia.

Escogi el genoma de Canis Lupus Familiaris o perro domestico.

Referencia: https://www.ncbi.nlm.nih.gov/genome/?term=txid9615%5BOrganism:noexp%5D

![perro domestico](https://github.com/Peepcross/St3-LAB/blob/master/canis.png)

¿Cuál es el N50 del genoma que escogiste? ¿Y el NG50?
  
|Statistics|Value|
|-|-|
N50 |180 kb
NG50 |1.2225 gb|

¿Qué tipo de tecnología se uso para secuenciar el genoma que escogiste?

Se secuencio via whole-genome shotgun (WGS) y ensamblado con ARACHNE2+.

¿Qué organismo escogiste, cuántos cromosomas tiene tu organismo y cuál es su tamaño?
	
Canis Lupus Familiaris, 38 cromosomas haploides mas uno sexual y el tamaño total es 2.445 gb.

## Parte 2: Predicción de genes

Secuencia problema

 ATGAGTATCAAAATCTTATCTGAATCAGAAATTAAACAAGTAGCAAATTCATATCAAGCCCCAGCGGTTTTATTTGCCAATCCTAAAAATCTTTACCAACGCAGAGCGAAACGTTTAAGAGACTTAGCACAAAATCATCCTCTATCTGATTATTTATTATTTGCTGCAGACATAGTTGAAAGCCAACTTTCCACGTTAGAAAAAAATCCTTTACCGCCACAACAGCTTGAACAGTTAAATACTATCGAGCCACTAAATGCCAAAACCTTTAAGAGAAACAGTATCTGGCGTGAATACTTAACAGAAATTCTTGATGAAATAAAGCCCAAAGCTAACGAGCAAATTGCTGCAACAATTGAATTTCTTGAAAAAGCCTCTTCCGCTGAATTAGAAGAAATGGCAAATAAACTCTTAGCACAAGAATTTAACTTAGTCAGCAGTGATAAAGCCGTCTTTATTTGGGCTGCACTTTCCCTTTATTGGTTACAAGCAGCTCAACAAATTCCTCATAATAGCCAAGTTGAAAACGCTGAAAATTTACATCACTGCCCTGTTTGTGGTTCTTTACCTGTGGCAAGTATGGTACAAATTGGTACATCACAAGGTTTACGCTACTTACATTGTAATTTATGTGAAAGTGAATGGAATTTGGTACGCGCACAATGCACCAATTGTAATAGTCATGACAAACTCGAAATGTGGTCACTAAATGAAGAACTTGCGCTTGTTCGTGCCGAAACCTGTGGTAGTTGTGAAAGTTACTTGAAAATGATGTTCCAAGAAAAAGATCCTTACGTAGAACCTGTAGCCGATGATTTGGCTTCTATTTTCTTAGATATTGAAATGGAAGAAAAAGGTTTCGCCCGAAGTGGATTAAATCCATTTATTTTTCCTGCAGAAGAAGCATAAAAATATAGCCTAGAAATATCTAGGCTAATTATTTAAATCTATAGATAACACGCCATTACCACTGCATTTTCTCGTCCACCACTGGGTTTCGGATAATAATTTTTCCGAATATCCACTTCATTAAAACCAATTTTTTCATACAAGAAACGAGCAGAGTTAGACTCTCTGACTTCTAGCCATAAGGTTTGGACACCTTTTTCCTTTAATTGAAAGATTAATTTTCCTAACAATAATTTGCCAAATCCACAACCTTGATAAGTAGGCAAAATCGCAATATTAAACAAAGTCGCTTCATCCAATACTGTTTGGCAAATAGCAAAACCGATAATCTGATTATTCTCTATTAATTTTAAATTGAGATAACGCTCCCCTTGATTATTTTTTAACGTACCAAATGACCAAGGCACCAGATGGGCTTGCTGTTCGATTTCATACAATCGCTCGAAATCACAGGCTTCAATTTGAGAAATAATAGACATAATTAAGGCTGCTGAATTTGTTGCCACAACGCTCGTTTGGCTTGATGATTAGATTGAAATTGCTGCCAACTTGGCGAGCGATAAACCTGCTCAGCCTGCTTGCAAAATGGCAAAGTGCGGTCAATTTGGTCGCTATTTTCTGATAGTAACCAATAACGAATAGGCTGTTTACATTCCATATGCTGGATTTGATCGTAATTCAAACATAAACAATTTTCTTTTTTAAGATTAAGGCTTAACAGCACATCAGCCAACAAAGGCGAGCTACTGATATTTTCATCGGAAACAGTGATAAGGCGAATATTCTCTGCCACACTAATTCCTACTGAACCTTGCAGTACCTCGGGGCGATATAATTCCCACTGGGAAATGCCCATTTCTTGTAAAAGAAGATCGCGTCTGTTCATAAGTGAATTTTTAAAAACGTTGCTTGAAAAATAGTGTTAATTTCTTTTATTAATCTTTGCTAAAATGGTGCGTAATTTTAACCAATAACCCACAGGATTCAAAGCG
 
### ORFinder y Glimmer

¿Cuántos ORF o genes encontró ORFfinder?

![orfinder](https://github.com/Peepcross/St3-LAB/blob/master/orfinder.png)

¿Cuántos ORF o genes encontró Glimmer?

Glimer encontro 10 ORF, 3 mas que ORFinder.

¿Alguno de los genes predichos por estas herramientas coinciden?

Ninguno coincide.

¿En qué hebra están codificados?

En ORFinder los ORF 1, 2 y 3 estan en la hebra adelantada y el resto en la retrasada. En cambio, en Glimmer los ORF 1, 3, 5, 7 estan ubicados en la hebra adelantada y los demas en la retrasada.

¿Qué tipo de programa es GLIMMER? ¿Ab initio o por homología?

Es un sistema para encontrar ADN microbial, pero tambien una version para eucariotas. Funciona por homologia.

### BLAST




# Ensamblaje de secuencias de ADN mediante grafos de De Bruijn 

## Ejercicio 2: 

Imagina que estás trabajando en un proyecto de investigación genómica y has recibido datos de  secuenciación de ADN fragmentado. La secuenciación te ha proporcionado una lista de lecturas cortas, cada una de longitud 4. Tu tarea es ensamblar estas lecturas cortas para reconstruir la  secuencia original utilizando un grafo de De Bruijn. En este caso partirás de los 3-mers de cada uno de ellos.

- **Datos del ejercicio**:
1. El alfabeto que representa las bases del ADN es {A,C,G,T}. 
2. Se han secuenciado los siguientes fragmentos: 
- GACG
- GCTT
- TTAC
- ACTA
- TATG
- TGTG

- **Objetivo**: 
1. **Construir el grafo de De Bruijn** a partir de las lecturas k-mers (lecturas de longitud 3) para modelar las superposiciones de las lecturas y generar el ensamblaje de la secuencia.

- Descomponer los fragmentos en sufijos y prefijos.
  - GACG -> GAC, ACG
  - GCTT -> GCT, CTT
  - TTAC -> TTA, TAC
  - ACTA -> ACT, CTA
  - TATG -> TAT, ATG
  - TGTG -> TGT, GTG

- División de los 3-mers en prefijos y sufijos de longitud k−1=2
  - GAC: GA -> AC
  - ACG: AC -> CG
  - GCT: GC -> CT
  - CTT: CT -> TT
  - TTA: TT -> TA
  - TAC: TA -> AC
  - ACT: AC -> CT
  - CTA: CT -> TA
  - TAT: TA -> AT
  - ATG: AT -> TG
  - TGT: TG -> GT
  - GTG: GT -> TG
 
  El grafo de De Bruijn es el siguiente:

  <div align="center">
  <img src="grafo_2.png" alt="Grafo Ej 2" width=700 />
    <p><strong>Figura 1.</strong> Grafo resultante del ejercicio 2.</p> 
</div>



2. Determinar la **secuencia original** de ADN que mejor se ensambla a partir de estas lecturas.
  
3. Explicar el proceso paso a paso, indicando cómo el grafo ayuda a ensamblar fragmentos y cómo se resuelven las superposiciones.

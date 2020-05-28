# Set

## ```Set<T>```
* Representa um conjunto de elementos (similar ao da Álgebra)
  * Não admite repetições
  * Elementos não possuem posição
  * Acesso, inserção e remoção de elementos são rápidos
  * Oferece operações eficientes de conjunto: interseção, união, diferença.
  * Principais implementações:
    * **HashSet -** mais rápido (operações O(1) em tabela hash) e não ordenado
    * **TreeSet -** mais lento (operações O(log(n)) em árvore rubro-negra) e ordenado pelo compareTo do objeto (ou Comparator)
    * **LinkedHashSet -** velocidade intermediária e elementos na ordem em que são adicionados


* https://docs.oracle.com/javase/10/docs/api/java/util/Set.html

## Alguns métodos importantes 
* add(obj), remove(obj), contains(obj) 
  * Baseado em equals e hashCode
  * Se equals e hashCode não existir, é usada comparação de ponteiros
  
* clear() 
* size() 
* removeIf(predicate)

* addAll(other) - **união:** adiciona no conjunto os elementos do outro conjunto, sem repetição
* retainAll(other) - **interseção:** remove do conjunto os elementos não contitos em other
* removeAll(other) - **diferença:** remove do conjunto os elementos contidos em other

### Problema exemplo

Um site de internet registra um log de acessos dos usuários. Um
registro de log consiste no nome de usuário (apenas uma palavra) e o
instante em que o usuário acessou o site no padrão ISO 8601,
separados por espaço, conforme exemplo. Fazer um programa que leia
o log de acessos a partir de um arquivo, e daí informe quantos usuários
distintos acessaram o site.

### Example 
**input file:**
> amanda 2018-08-26T20:45:08Z  
alex86 2018-08-26T21:49:37Z   
bobbrown 2018-08-27T03:19:13Z   
amanda 2018-08-27T08:11:00Z   
jeniffer3 2018-08-27T09:19:24Z   
alex86 2018-08-27T22:39:52Z   
amanda 2018-08-28T07:42:19Z   

**Execution:**
> Enter file full path: c:\temp\in.txt  
Total users: 4   

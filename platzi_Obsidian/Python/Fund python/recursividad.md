
Cualquier función recursiva se puede escribir como un [[ciclos]]
Los algoritmos recursivos deben obedecer tres leyes importantes:
- Un algoritmo recursivo debe tener un caso base.  
- Un algoritmo recursivo debe cambiar su estado y moverse hacia el caso base.  
- Un algoritmo recursivo debe llamarse a sí mismo, recursivamente.

“El límite por omisión es de 1000 llamadas recursivas. Es posible modificar el tamaño máximo de la pila de recursión mediante la instrucción  sys.setrecursionlimit(n)  Sin embargo, si se está alcanzando este límite suele ser una buena idea pensar si realmente el algoritmo recursivo es el que mejor resuelve el problema.”
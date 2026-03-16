# Funções de Alta Ordem e Funções Lambda
## Funções de Alta Ordem
As **funções de alta ordem** (High Order Functions) podem receber uma ou mais funções como parâmetro, e/ou devolvem outra função como resultado. Ou seja, ela utiliza funções como valores, exatamente igual a outros tipos de dados como int ou string. Isso torna o código mais flexível e reutilizável.

EXEMPLOS:

`Haskell`

- any: verifica se algum elemento da lista satisfaz uma condição.
```hs
temNegativo x = x < 0
any temNegativo [1,2,-3,4]
```
Resultado: `True`

- all: verifica se todos os elementos satisfazem uma condição.
```hs
todosPositivos x = x > 0
all todosPositivos [1,2,3,4]
```
Resultado: `True`

- zipWith: aplica uma função a elementos correspondentes de duas listas.
```hs
soma x y = x + y
zipWith soma [1,2,3] [4,5,6]
```
Resultado: `[5,7,9]`


`Python`

```py
# função de alta ordem
def aplicar(funcao, valor):
    return funcao(valor)

# função passada como argumento
def dobro(x):
    return x * 2

resultado = aplicar(dobro, 5)
print(resultado)
```
Resultado: `10`

## Funções Lambda
As **funções lambda** (funções anônimas) são definidas “na hora”, sem nome, e geralmente usadas apenas uma vez, por exemplo como argumento para outra função. São bastante utilizadas em operações simples, como cálculos rápidos. 
O símbolo utilizado em Haskell para indicar que é uma função lambda: `\`

EXEMPLO:

`Haskell`

- Função normal:
```hs
quadrado x = x * x
map quadrado [1,2,3,4,5]
```

- Função usando lambda:
```hs
map (\x -> x * x) [1, 2, 3, 4, 5]
```

As funções lambda também podem ser armazenadas em variáveis.

EXEMPLO:

`Python`
```py
square = lambda x: x * x # cria uma função lambda e atribui à variável 'square'
print(square(7))  # 49
```

# Exercícios

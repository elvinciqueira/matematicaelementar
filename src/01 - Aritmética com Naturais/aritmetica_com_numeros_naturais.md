# Aritmética com Números Naturais
Conjunto dos números naturais:
$$\mathbb{N}=\{0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, ...\}$$

# Adição, +
Propriedades
1. Comutatividade
2. Associatividade
3. Fechamento
4. Elemento Neutro

```javascript
//comutatividade
1 + 2 === 2 + 1 // true

//Associatividade
1 + (2 + 3) //6

//Associatividade e comuatividade
2 + (1 + 3) == 3 + (2 + 1) //true

//Fechamento - a soma entre dois números naturais resulta em um número natural
8 + 8

//Elemento neutro não modifica o resultado
7 + 0
```

# Subtração


```javascript
//Não é comutativa
7 - 3 !== 3 - 7 //true

//Não é associativa
2 - (1 - 3) !== 3 - (2 - 1) //true

//Contém um elemento neutro
7 - 0 //7
```

# Multiplicação
Propriedades
1. Comutatividade
2. Associatividade
3. Fechamento
4. Elemento Neutro

```javascript
//Associatividade
8 * 9 == 9 * 8 //true

//Comutatividade
7 * (8 * 9) == 9 (8 * 7) //true

//Elemento neutro
8 * 1 //8

```

# Divisão 

```julia
8 ÷ 2 #4

* 8 - dividendo

* 2 - divisor

* 4 - quociente

* 0 - resto
```

Como o resto é 0, podemos dizer que 2 divide 8; ou que 8 **é divisível** por 2

```javascript
//resto da divisão com operador % - módulo
9 % 2 //1

// 4 é o quociente
// 1 é o resto 

// resto é sempre menor que o divisor 
```

## Sucessor de um número natural

0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13...

```javascript

/**
 * Retorna o sucessor de um número
 * * @example
 *    sucessor(1) =>  2
 *    sucessor(3) => 4
*/

const sucessor = n => n + 1

```

## Antecessor de um número natural


```javascript

/**
 * Retorna o antecessor de um número
 * * @example
 *    antecessor(2) =>  1
 *    antecessor(3) => 2
*/

const antecessor = n => {
  if (n === 0) {
    throw new Error('0 não tem antecessor')
  } else {
    return n - 1
  }
}

```

# Múltiplos

Os múltiplos de um número, são aqueles números que são divisiveis por ele

### **Quais são os múltiplos de 2?**

- São todos os números que são divisíveis de 2
- São os números da forma 2 * algumacoisa


```javascript
  8 == 2 * 4 //true
```

```javascript
  /**
 * Retorna os multiplos de um número
 * * @example
 *    multiplos(2, 10) =>  [0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
 *
*/

  function multiplos(n, k = 10) {
    const result = []
    
    for (let i = 0; i <= k; i++) {
      result.push(n*i)
    }

    return result
  }
```

# Divisores

O divisor de um número **$n$** é um número que **divide $n$**; em outras palavras, **$n$** é divisivel pelos seus divisores.

****
# Noções de Lógica
### Matemática Elementar para Computação #0"

# Proposição

 Uma sentença que só pode ser verdadeira ou falsa

```javascript

let idade = 18

idade >= 18 // true
idade > 21 // false

if (idade >= 18) {
  console.log('é obrigado a votar')
}
```

## Conectivo "E"

Pode ser escrito como **E**, **AND**, **^**, **&&**, **&** dependendo do contexto.
**Verdadeiro** apenas quando os dois lados são verdadeiros. 
**Falso**, caso contrário.
| p | q | p ^ q |
| --- |:---:| :---:|
| V | V | V |
| V | F | F |
| F | V | F |
| F | F | F |

```javascript
    
if (idade >= 18 && idade < 70) {
  console.log('é obrigado a votar')
}

```

# Conectivo OU
Pode ser escrito como **OU**, **OR**, **v**, **||**, **|** dependendo do contexto.
**Verdadeiro** se ao menos um dos dois lados for verdadeiro.
**Falso**, caso contrário.
| p | q | p v q |
| --- |:---:| :---:|
| V | V | V |
| V | F | V |
| F | V | V |
| F | F | F |

```javascript
if ((idade >= 16 && idade < 18) || idade >= 70) {
  console.log('voto é facultativo')
}
```

```julia
if (idade ∈ [16, 17]) || idade ≥ 70
	md"voto é facultativo!"
end
```

# Condicionais
p -> q lê-se "se p, então q"

| p | q | p -> q |
| --- |:---:| :---:|
| V | V | V |
| V | F | F |
| F | V | V |
| F | F | V |

p <-> q lê-se "p se, e somente se, q"

| p | q | p <-> q |
| --- |:---:| :---:|
| V | V | V |
| V | F | F |
| F | V | F |
| F | F | V |

# Negação
Pode ser escrito como **NÃO**, **NOT**, **~**, **!** dependendo do contexto.
**Inverte o valor lógico** de uma proposição. V torna-se F e F torna-se V.

| p | ~p |  
| --- |:---:| 
| V | F | 
| F | V | 


```julia

### Negando o E"

if !(idade ≥ 18 && idade < 70)
	md"não é obrigado a votar"
end

# ~(p ^ q) <-> ~p v ~ q
if !(idade ≥ 18) || !(idade < 70)
	md"não é obrigado a votar"
end

### Negando o OU"

if !(idade ∈ [16, 17] || idade ≥ 70)
	md"seu voto NÃO é facultativo!"
end

# ~(p v q) <-> ~p ^ ~ q
if !(idade ∈ [16, 17]) && !(idade ≥ 70)
	md"seu voto NÃO é facultativo!"
end
```
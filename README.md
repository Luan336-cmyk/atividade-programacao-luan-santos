# atividade-programacao-seu-nome
Explorar como diferentes prompts podem gerar explicações, exemplos e soluções de programação, ajudando o estudante a compreender melhor conceitos e práticas da área.

# Atividade – Prompt Mestre em Programação de Computadores
 
## Tema: Estruturas de Repetição
 
### Prompt Mestre Inicial
"Escreva um programa em Python que calcule a soma dos números pares de 1 a 100."
 
### Variação 1
"Escreva o programa em Python e explique passo a passo como funciona."
**Resposta do LLM:**
Aqui está um programa em Python que calcula a soma dos números pares de 1 a 100, seguido de uma explicação passo a passo:

```python
soma = 0

for numero in range(1, 101):
    if numero % 2 == 0:
        soma += numero

print("A soma dos números pares de 1 a 100 é:", soma)
```

## Explicação passo a passo

1. **`soma = 0`**
   Criamos uma variável chamada `soma` e iniciamos com o valor 0.
   Ela será usada para acumular a soma dos números pares.

2. **`for numero in range(1, 101):`**
   Aqui criamos um laço (`for`) que percorre os números de 1 até 100.

   * O `range(1, 101)` gera números de 1 até 100 (o 101 não é incluído).

3. **`if numero % 2 == 0:`**
   Verificamos se o número é par.

   * O operador `%` calcula o resto da divisão.
   * Se `numero % 2 == 0`, significa que o número é divisível por 2, ou seja, é par.

4. **`soma += numero`**
   Se o número for par, ele é somado à variável `soma`.

   * Isso é equivalente a: `soma = soma + numero`.

5. **`print(...)`**
   Ao final do laço, mostramos o resultado na tela.

---

## Forma mais simples (otimizada)

```python
soma = sum(range(2, 101, 2))
print("A soma dos números pares de 1 a 100 é:", soma)
```

### Como funciona:

* `range(2, 101, 2)` gera apenas números pares (2, 4, 6, ..., 100).
* `sum()` soma todos esses valores automaticamente.

Se quiser, posso mostrar uma versão com entrada do usuário ou até transformar isso em uma função.

 
### Variação 2
"Otimize o programa em Python usando compreensão de listas."
**Resposta do LLM:** 
Aqui está uma versão otimizada usando **compreensão de listas**:

```python id="k3f9pz"
soma = sum([numero for numero in range(1, 101) if numero % 2 == 0])
print("A soma dos números pares de 1 a 100 é:", soma)
```

## Como funciona

1. **`range(1, 101)`**
   Gera os números de 1 até 100.

2. **`[numero for numero in range(...) if numero % 2 == 0]`**
   Isso é uma **compreensão de lista**:

   * Percorre todos os números
   * Filtra apenas os pares (`% 2 == 0`)
   * Cria uma lista com esses números

   Resultado intermediário:

   ```python
   [2, 4, 6, ..., 100]
   ```

3. **`sum(...)`**
   Soma todos os valores da lista gerada.

---

## Versão ainda mais eficiente (sem criar lista)

Você pode usar uma **expressão geradora**, que economiza memória:

```python id="1g7h2q"
soma = sum(numero for numero in range(1, 101) if numero % 2 == 0)
print("A soma dos números pares de 1 a 100 é:", soma)
```

✔ Essa versão é mais eficiente porque não cria a lista inteira na memória.

 
### Variação 3
"Explique o programa em linguagem simples, como se fosse para um iniciante."
**Resposta do LLM:** 
Aqui vai uma explicação bem simples, como se você estivesse começando agora 😊

Vamos usar esta versão do programa:

```python
soma = sum(numero for numero in range(1, 101) if numero % 2 == 0)
print("A soma dos números pares de 1 a 100 é:", soma)
```

## Explicação simples

### 1. O que o programa faz?

Ele pega todos os números de 1 até 100, escolhe só os **pares** (2, 4, 6, …) e soma tudo.

---

### 2. `range(1, 101)`

Isso cria uma sequência de números de **1 até 100**.

---

### 3. `numero for numero in range(...)`

Aqui o programa passa por cada número, um por um.
É como dizer: “pegue cada número dessa lista”.

---

### 4. `if numero % 2 == 0`

Essa parte verifica se o número é **par**:

* `%` significa “resto da divisão”
* Se um número dividido por 2 dá resto 0, ele é par

Exemplo:

* 4 ÷ 2 → resto 0 → par ✅
* 5 ÷ 2 → resto 1 → ímpar ❌

---

### 5. `sum(...)`

Depois de escolher só os números pares, o `sum()` **soma todos eles** automaticamente.

---

### 6. `print(...)`

Mostra o resultado na tela.

---

## Resumindo em uma frase:

👉 O programa pega números de 1 a 100, filtra os pares e soma tudo.

---

Se quiser, posso te mostrar isso funcionando passo a passo como se fosse uma simulação 👍

 
### Reflexão
(Análise do estudante sobre os aprendizados e percepções.)

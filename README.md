# Atividade – Prompt Mestre em Programação de Computadores
 
## Tema: Funções
 
### Prompt Mestre Inicial
"Escreva um programa em Python que exemplifique o uso da função random()."
 
### Variação 1
"Escreva o programa em Python e explique passo a passo como funciona."
**Resposta do LLM:** 
Aqui está um programa simples em Python usando `random()` e, em seguida, a explicação detalhada passo a passo:

```python id="p9a2k1"
import random

# 1. Gerar um número aleatório entre 0 e 1
numero = random.random()

# 2. Exibir o número gerado
print("Número aleatório entre 0 e 1:", numero)

# 3. Criar uma lista de opções
cores = ["vermelho", "azul", "verde", "amarelo"]

# 4. Escolher um item aleatório da lista
cor_escolhida = random.choice(cores)

# 5. Mostrar o resultado
print("Cor escolhida aleatoriamente:", cor_escolhida)

# 6. Gerar um número inteiro aleatório entre 1 e 6 (simulando um dado)
dado = random.randint(1, 6)

# 7. Exibir o valor do dado
print("Resultado do dado:", dado)
```

---

## 🔍 Explicação passo a passo

### 1. `import random`

Importa a biblioteca `random`, que contém funções para gerar valores aleatórios.

---

### 2. `random.random()`

```python
numero = random.random()
```

* Gera um número decimal aleatório entre **0.0 e 1.0**.
* Exemplo de saída: `0.3748291`

---

### 3. `print(...)`

```python
print("Número aleatório entre 0 e 1:", numero)
```

* Mostra o valor gerado na tela.

---

### 4. Lista de cores

```python
cores = ["vermelho", "azul", "verde", "amarelo"]
```

* Cria uma lista com algumas opções.

---

### 5. `random.choice()`

```python
cor_escolhida = random.choice(cores)
```

* Escolhe **um elemento aleatório** da lista.
* Cada item tem a mesma chance de ser escolhido.

---

### 6. `random.randint(1, 6)`

```python
dado = random.randint(1, 6)
```

* Gera um número inteiro entre **1 e 6**, incluindo ambos.
* Muito usado para simular jogos de dados.

---

### 7. Saída final

O programa pode gerar algo como:

```
Número aleatório entre 0 e 1: 0.5821
Cor escolhida aleatoriamente: verde
Resultado do dado: 4
```

---

## 💡 Resumo

Esse programa mostra três usos comuns da aleatoriedade:

* Número decimal → `random()`
* Escolha de lista → `choice()`
* Número inteiro → `randint()`

Se quiser, posso transformar isso em um joguinho simples 🎲 ou em um programa interativo.

 
### Variação 2
"Otimize o programa em Python usando compreensão de listas."
**Resposta do LLM:** 
Boa ideia — dá para deixar o código mais conciso usando **compreensão de listas**. Aqui vai uma versão otimizada:

```python id="k3f8lm"
import random

# Lista de cores
cores = ["vermelho", "azul", "verde", "amarelo"]

# Gerando vários números aleatórios de uma vez
numeros = [random.random() for _ in range(3)]

# Escolhendo várias cores aleatórias
cores_escolhidas = [random.choice(cores) for _ in range(3)]

# Simulando vários lançamentos de dado
dados = [random.randint(1, 6) for _ in range(3)]

# Exibindo resultados
print("Números aleatórios:", numeros)
print("Cores escolhidas:", cores_escolhidas)
print("Resultados dos dados:", dados)
```

---

## 🔍 O que mudou (e por quê)

### ✔ Antes

Você gerava um valor por vez:

```python
numero = random.random()
```

### ✔ Agora (com list comprehension)

```python
numeros = [random.random() for _ in range(3)]
```

* Cria uma **lista com 3 números aleatórios de uma só vez**.
* `_` é usado quando não precisamos da variável do loop.
* `range(3)` define quantas vezes o processo será repetido.

---

## 🧠 Vantagens dessa abordagem

* Código mais **curto e elegante**
* Evita repetição de linhas
* Facilita gerar múltiplos valores rapidamente
* Muito usado em Python profissional

---

## 💡 Resultado esperado

Exemplo de saída:

```
Números aleatórios: [0.12, 0.87, 0.45]
Cores escolhidas: ['azul', 'verde', 'vermelho']
Resultados dos dados: [2, 6, 1]
```

---

Se quiser, posso ir além e transformar isso em uma simulação (tipo estatística de dados 🎲 ou sorteios mais complexos).

 
### Variação 3
"Explique o programa em linguagem simples, como se fosse para um iniciante."
**Resposta do LLM:** 
Claro! Vamos explicar esse programa de forma bem simples, como se você estivesse começando agora 😊

---

## 🧾 O que esse programa faz?

Ele gera coisas aleatórias:

* Alguns **números**
* Algumas **cores**
* Alguns **resultados de dado**

---

## 🔢 Passo a passo

### 1. Importar a biblioteca

```python
import random
```

👉 Aqui estamos dizendo: “Python, quero usar funções de sorte (aleatórias)”.

---

### 2. Criar uma lista de cores

```python
cores = ["vermelho", "azul", "verde", "amarelo"]
```

👉 Isso é só uma lista com opções que o programa pode escolher.

---

### 3. Gerar números aleatórios

```python
numeros = [random.random() for _ in range(3)]
```

👉 Isso pode parecer complicado, mas é simples:

* `random.random()` → cria um número aleatório entre 0 e 1
* `range(3)` → repete 3 vezes
* `for _ in range(3)` → “faça isso 3 vezes”
* Os colchetes `[ ]` → guardam tudo em uma lista

💡 Resultado: uma lista com 3 números aleatórios

---

### 4. Escolher cores aleatórias

```python
cores_escolhidas = [random.choice(cores) for _ in range(3)]
```

👉 Aqui o programa:

* Pega a lista `cores`
* Escolhe uma cor aleatória
* Repete isso 3 vezes

💡 Resultado: 3 cores sorteadas

---

### 5. Simular um dado 🎲

```python
dados = [random.randint(1, 6) for _ in range(3)]
```

👉 Aqui:

* `randint(1, 6)` → número inteiro entre 1 e 6
* Repete 3 vezes

💡 Resultado: como se você jogasse um dado 3 vezes

---

### 6. Mostrar os resultados

```python
print("Números aleatórios:", numeros)
print("Cores escolhidas:", cores_escolhidas)
print("Resultados dos dados:", dados)
```

👉 O programa exibe tudo na tela.

---

## 🧠 Resumindo

O programa:

* Usa “sorte” (`random`)
* Repete ações usando uma forma curta chamada **compreensão de lista**
* Guarda os resultados em listas

---

## 💡 Dica importante

Essa parte:

```python
[random.random() for _ in range(3)]
```

significa basicamente:
👉 “Faça isso 3 vezes e guarde os resultados”

---

Se quiser, posso te mostrar como transformar isso em um joguinho simples ou até um sorteador interativo 👍

 
### Reflexão
No prompt inicial a LLM fez uma lista resumida das utilizações da função random(), porém para um iniciante fica massivo e confuso. Quanto mais eu prossigo no exercício de utilizar
prompts mais específicos, mais destrinchados ficam os exemplos de utilização da função, o que me ajuda a estudar uma utilização por vez.

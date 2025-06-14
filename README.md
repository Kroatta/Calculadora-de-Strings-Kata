# 🧮 String Calculator Kata – Python

Este projeto é a solução do desafio **String Calculator Kata**, onde implementamos uma função `add()` capaz de somar números fornecidos em formato de string, respeitando diversas regras e casos especiais.

---

## 🧠 O Desafio

A função `add(string)` deve:
1. Somar números separados por vírgula (`,`) ou quebra de linha (`\n`)
2. Aceitar delimitadores personalizados
3. Lançar exceção se houver números negativos (mostrando todos)
4. Ignorar números maiores que 1000
5. Suportar múltiplos delimitadores com qualquer tamanho

---

## ✅ Exemplos

| Entrada                     | Resultado | Observações                              |
|----------------------------|-----------|------------------------------------------|
| `""`                       | `0`       | String vazia                             |
| `"1,2"`                    | `3`       | Dois números com vírgula                 |
| `"1\n2,3"`                 | `6`       | Suporte a quebra de linha                |
| `"//;\n1;2"`               | `3`       | Delimitador personalizado `;`            |
| `"2,1001"`                 | `2`       | Números > 1000 são ignorados             |
| `"//[***]\n1***2***3"`     | `6`       | Delimitador com vários caracteres        |
| `"//[*][%]\n1*2%3"`        | `6`       | Múltiplos delimitadores simples          |
| `"//[***][##][@@]\n1***2##3@@4"` | `10`  | Múltiplos delimitadores longos           |
| `"1,-1"`                   | Exceção   | Lança erro com mensagem: `-1`            |
| `"1,-1,-4"`                | Exceção   | Lança erro com mensagem: `-1, -4`        |

---

## 🧾 Estrutura dos Arquivos

string_calculator/
│
├── string_calculator.py # Função principal add()
├── test_string_calculator.py # Testes usando pytest


---

## 🔍 Explicando a Lógica

- Usa `regex` para tratar múltiplos delimitadores e caracteres especiais
- Verifica se a string começa com `//` para identificar delimitadores personalizados
- Converte cada número em `int`, ignora vazios
- Verifica e lança exceção para negativos
- Ignora números maiores que 1000 na soma final

---









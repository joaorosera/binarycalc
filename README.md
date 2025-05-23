# Calculadora Binária 8 bits

[![Python](https://img.shields.io/badge/python-3.6%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Build Status](https://img.shields.io/badge/tests-passing-brightgreen)]()

## 📌 Sobre

Este projeto é uma **calculadora binária** que opera com números de 1 byte (8 bits), suportando números positivos e negativos no formato de complemento de dois.  
Ela realiza as operações básicas:

- Soma (`+`)
- Subtração (`-`)
- Multiplicação (`x`)

## ⚙️ Funcionalidades

- Entrada e saída em formato binário (strings de 8 bits, ex: `"00000001"`)
- Suporte a números negativos (usando complemento de dois)
- Detecção e tratamento de overflow em operações
- Validação rigorosa de entradas (tamanho, caracteres, operação)
- Exceções claras em caso de erros (`overflow`, `valor invalido`, `tamanho da entrada invalido`)
- Código todo em Python sem conversão direta para decimal nas operações (opera bit a bit)

## 🛠️ Como usar

### Requisitos

- Python 3.6 ou superior

### Executando a calculadora interativa

1. Clone ou baixe o projeto
2. No terminal, navegue até a pasta do projeto
3. Execute:

```bash
python3 calculadora_binaria.py
```

4. Siga as instruções na tela para digitar dois números binários de 8 bits e a operação desejada.
5. Digite `sair` para encerrar o programa.

---

### Usando a função `calcular` diretamente

No seu código Python, importe e utilize a função:

```python
from calculadora_binaria import calcular

resultado = calcular("00000011", "00000010", "+")
print(resultado)  # Saída: "00000101"
```

---

## 🧪 Testes automatizados

Incluímos um conjunto completo de testes usando o módulo `unittest` para garantir a confiabilidade do código.

Para rodar os testes:

```bash
python3 -m unittest test_calculadora.py
```

Você deve ver uma saída indicando que todos os testes passaram.

---

## 📁 Estrutura do projeto

```
.
├── calculadora_binaria.py   # Código principal da calculadora
├── test_calculadora.py      # Testes unitários completos
├── README.md                # Este arquivo
└── LICENSE                  # Licença MIT
```

---

## ⚠️ Tratamento de erros

O código levanta exceções específicas para diferentes erros:

| Exceção                  | Quando ocorre                             |
|--------------------------|-----------------------------------------|
| `overflow`               | Resultado ultrapassa limite de 8 bits   |
| `valor invalido`         | Entrada com caracteres inválidos ou operação inválida |
| `tamanho da entrada invalido` | Entrada com tamanho diferente de 8 bits |

---

## 📜 Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para detalhes.

---

## 👤 Autor

João Vitor Rosera | Vinicius Werner.

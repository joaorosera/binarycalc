# Calculadora Binária 8 bits

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Python Version](https://img.shields.io/badge/python-3.6%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Descrição

Calculadora binária que suporta números de 8 bits com sinal (complemento de dois), realizando operações de soma, subtração e multiplicação.

## Requisitos

- Python 3.6 ou superior

## Como usar

Execute o arquivo `calculadora.py` para usar a calculadora via terminal:

```bash
python3 calculadora.py
```

Digite os números binários (8 bits, com sinal) e a operação desejada (+, -, x).

## Função principal

A função principal `calcular(n1, n2, operacao)` recebe:

- `n1` e `n2`: strings binárias de 8 bits (ex: "00000001")
- `operacao`: string, podendo ser "+", "-" ou "x"

Retorna a string binária de 8 bits resultado.

## Testes

Para rodar os testes automatizados com unittest, use:

```bash
python3 -m unittest test_calculadora.py
```

Todos os testes devem passar sem erros.

## Licença

MIT License - veja o arquivo LICENSE para detalhes.

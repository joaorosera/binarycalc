
# Calculadora Binária (8 bits)

## Descrição

Projeto desenvolvido para o desafio acadêmico de criar uma calculadora binária que suporta números de 1 byte (8 bits) em complemento de dois, incluindo positivos e negativos. A calculadora realiza as operações básicas de **soma**, **subtração** e **multiplicação** diretamente sobre bits, sem conversões para inteiros, garantindo manipulação bit a bit.

## Funcionalidades

- Entrada de números binários de 8 bits em complemento de dois (ex: `"00000001"` para +1, `"11111111"` para -1).
- Operações suportadas: `+` (soma), `-` (subtração), `x` (multiplicação).
- Validação rigorosa das entradas:
  - Tamanho deve ser exatamente 8 bits.
  - Apenas caracteres `0` e `1` são permitidos.
  - Operação deve ser uma das três especificadas.
- Detecção e tratamento de **overflow** para todas as operações.
- Exceções específicas para erros de entrada e overflow:
  - `"valor invalido"`
  - `"tamanho da entrada invalido"`
  - `"overflow"`
- Toda operação é feita em nível binário, sem conversão para int.
- Código totalmente comentado explicando cada parte do processo.

## Como usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/calculadora-binaria.git
   cd calculadora-binaria
   ```

2. Rodar manualmente:
   ```bash
   python3 calculadora.py
   ```
   Siga as instruções para digitar os números binários e operação. Digite `sair` para encerrar.

3. Rodar os testes automatizados:
   ```bash
   python3 -m unittest test_calculadora.py
   ```

## Estrutura dos arquivos

- `calculadora.py`: implementação da calculadora binária.
- `test_calculadora.py`: conjunto completo de testes unitários cobrindo operações, erros e casos limite.

## Exemplo de uso

```bash
Digite o primeiro número binário (8 bits): 00000010
Digite o segundo número binário (8 bits): 11111110
Digite a operação (+, -, x): +
Resultado: 00000000
```

Nesse exemplo, `00000010` = +2, `11111110` = -2, e o resultado da soma é `00000000` (0).

## Considerações técnicas

- Os números binários são representados no formato **complemento de dois**, permitindo representar valores negativos.
- A soma e subtração usam algoritmos de adição binária com detecção de overflow baseada no bit de sinal.
- A multiplicação é feita somando e deslocando os operandos, também com tratamento de overflow.
- O código foi projetado para ser robusto contra entradas inválidas e operações fora do escopo.

## Testes

Os testes unitários cobrem:

- Operações básicas com números positivos e negativos.
- Operações com overflow, garantindo que a exceção apropriada seja lançada.
- Validação de entradas inválidas (tamanho errado, caracteres inválidos, operações inválidas).
- Casos limite de -128 até 127 (faixa dos números de 1 byte em complemento de dois).

---

**Autor:** João Vitor Rosera e Vinicius Werner
**Data:** Maio 2025

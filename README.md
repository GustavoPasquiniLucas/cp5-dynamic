# 💰 Problema da Troca de Moedas

## 👤 Integrante
- Gustavo Pasquini — RM: 555454

## 🎯 Objetivo
Determinar a menor quantidade de moedas necessárias para formar um montante `M`, usando moedas de valores inteiros positivos e ilimitados.

## 🧠 Abordagens Implementadas

| Função                  | Estratégia                     | Solução Ótima | Complexidade Tempo |
|------------------------|--------------------------------|----------------|---------------------|
| `qtdeMoedas`           | Gulosa (Iterativa)             | ❌             | O(n)                |
| `qtdeMoedasRec`        | Recursiva Pura                 | ✅             | O(m^M)              |
| `qtdeMoedasRecMemo`    | Recursiva com Memoização       | ✅             | O(M × m)            |
| `qtdeMoedasPD`         | Programação Dinâmica Bottom-Up | ✅             | O(M × m)            |

## 📌 Observações
- A abordagem gulosa pode falhar em encontrar a solução ótima.
- As versões com memoização e programação dinâmica garantem eficiência e resultado correto.
- A abordagem com PD Bottom-Up é a mais recomendada para grandes valores de `M`.

## ✅ Exemplo de Teste
```python
qtdeMoedas(6, [1, 3, 4])        # Retorna 3 (não ótimo)
qtdeMoedasRec(6, [1, 3, 4])     # Retorna 2 (ótimo)
qtdeMoedasRecMemo(6, [1, 3, 4]) # Retorna 2 (ótimo)
qtdeMoedasPD(6, [1, 3, 4])      # Retorna 2 (ótimo)

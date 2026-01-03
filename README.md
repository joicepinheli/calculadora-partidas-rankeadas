# 🛡️ Classificador de Nível de Herói - Calculadora de Partidas Rankeadas

Este projeto foi desenvolvido em **JavaScript** para calcular o saldo de vitórias e derrotas de um jogador e classificar o nível do herói com base na quantidade de vitórias.  
O programa utiliza **variáveis, operadores, laços de repetição, estruturas de decisão e funções**.

---

## 📋 Regras de Classificação

- Vitórias < 10 → **Ferro**
- 11 ≤ Vitórias ≤ 20 → **Bronze**
- 21 ≤ Vitórias ≤ 50 → **Prata**
- 51 ≤ Vitórias ≤ 80 → **Ouro**
- 81 ≤ Vitórias ≤ 90 → **Diamante**
- 91 ≤ Vitórias ≤ 100 → **Lendário**
- Vitórias ≥ 101 → **Imortal**

---

## ⚙️ Lógica do Programa

1. O usuário informa a quantidade de **vitórias** e **derrotas**.  
2. O programa calcula o **saldo de vitórias**:  
   ```javascript
   saldoVitorias = vitorias - derrotas;
   ```
3. Com base na quantidade de vitórias, o programa determina o **nível do herói**.  
4. Ao final, exibe a mensagem:  
   ```
   O Herói tem de saldo de {saldoVitorias} está no nível de {nivel}
   ```

---

## 🚀 Execução no Node.js

### Versão utilizada
- **Node.js v22.21.0**

### Linha de comando
Para executar o código no terminal, utilize:

```bash
node calculadoraRankeada.js
```

Durante a execução, o programa solicitará:
1. Quantidade de vitórias.  
2. Quantidade de derrotas.  

E exibirá o saldo e o nível correspondente.

---

## 🌐 Alteração para rodar no navegador

Se desejar rodar no navegador, substitua a entrada via `readline` por `prompt` e a saída por `alert` ou `console.log`.

### Exemplo para navegador:

```javascript
let vitorias = parseInt(prompt("Digite a quantidade de vitórias:"));
let derrotas = parseInt(prompt("Digite a quantidade de derrotas:"));

function calcularNivel(vitorias, derrotas) {
    let saldoVitorias = vitorias - derrotas;
    let nivel = "";

    if (vitorias < 10) nivel = "Ferro";
    else if (vitorias >= 11 && vitorias <= 20) nivel = "Bronze";
    else if (vitorias >= 21 && vitorias <= 50) nivel = "Prata";
    else if (vitorias >= 51 && vitorias <= 80) nivel = "Ouro";
    else if (vitorias >= 81 && vitorias <= 90) nivel = "Diamante";
    else if (vitorias >= 91 && vitorias <= 100) nivel = "Lendário";
    else if (vitorias >= 101) nivel = "Imortal";

    return { saldoVitorias, nivel };
}

let resultado = calcularNivel(vitorias, derrotas);
alert(`O Herói tem de saldo de ${resultado.saldoVitorias} está no nível de ${resultado.nivel}`);
```

---

## 📂 Estrutura do Projeto

```
desafio-calculadora-rankeada/
│
├── classificadorHeroi.js   # Código principal para execução no Node.js
└── README.md               # Documentação do projeto
```

---

## ✨ Objetivo

Exibir ao final a mensagem:

```
O Herói tem de saldo de {saldoVitorias} está no nível de {nivel}
```

E permitir calcular o nível de forma interativa.

1. Escreva um programa que mostre na tela a seguinte contagem: 6 7 8 9 10 11 Acabou!
   // 1. Contagem de 6 até 11
for (let i = 6; i <= 11; i++) {
    process.stdout.write(i + " ");
}
console.log("\nAcabou!");
2.Faça um algoritmo que mostre na tela a seguinte contagem: 10 9 8 7 6 5 4 3 Acabou!
// 2. Contagem de 10 até 3 (regressiva)
for (let i = 10; i >= 3; i--) {
    process.stdout.write(i + " ");
}
console.log("\nAcabou!");

3.Crie um aplicativo que mostre na tela a seguinte contagem: 0 3 6 9 12 15 18 Acabou!
// 3. Contagem de 0 até 18 pulando de 3 em 3
for (let i = 0; i <= 18; i += 3) {
    process.stdout.write(i + " ");
}
console.log("\nAcabou!");
4.Desenvolva um programa que mostre na tela a seguinte contagem: 100 95 90 85 80 ... 0 Acabou!
// 4. Contagem de 100 até 0 pulando de 5 em 5
for (let i = 100; i >= 0; i -= 5) {
    process.stdout.write(i + " ");
}
console.log("Acabou!");
5.Faça um algoritmo que pergunte ao usuário um número inteiro e positivo qualquer e mostre uma contagem até esse valor: Ex: Digite um valor: 35 Contagem: 1 2 3 4 5 6 7 ... 33 34 35 Acabou!
// 5. Contagem até número digitado
const prompt = require("prompt-sync")();
let valor = Number(prompt("Digite um valor inteiro positivo: "));

for (let i = 1; i <= valor; i++) {
    process.stdout.write(i + " ");
}
console.log("\nAcabou!");
6.Desenvolva um algoritmo que mostre uma contagem regressiva de 30 até 1, marcando os números que forem divisíveis por 4, exatamente como mostrado abaixo: 30 29 [28] 27 26 25 [24] 23 22 21 [20] 19 18 17 [16]...
// 6. Contagem regressiva de 30 até 1 marcando divisíveis por 4
for (let i = 30; i >= 1; i--) {
    if (i % 4 === 0) {
        process.stdout.write("[" + i + "] ");
    } else {
        process.stdout.write(i + " ");
    }
}
7.Crie um algoritmo que leia o valor inicial da contagem, o valor final e o incremento, mostrando em seguida todos os valores no intervalo: Ex: Digite o primeiro Valor: 3 Digite o último Valor: 10 Digite o incremento: 2 Contagem: 3 5 7 9 Acabou!
// 7. Contagem com valor inicial, final e incremento
let inicio = Number(prompt("Digite o primeiro valor: "));
let fim = Number(prompt("Digite o último valor: "));
let incremento = Number(prompt("Digite o incremento: "));

for (let i = inicio; i <= fim; i += incremento) {
    process.stdout.write(i + " ");
}
console.log("\nAcabou!");
8.O programa acima vai ter um problema quando digitarmos o primeiro valor maior que o último. Resolva esse problema com um código que funcione em qualquer situação.
// 8. Funciona tanto crescente quanto decrescente
inicio = Number(prompt("Digite o primeiro valor: "));
fim = Number(prompt("Digite o último valor: "));
incremento = Number(prompt("Digite o incremento: "));

if (inicio < fim) {
    for (let i = inicio; i <= fim; i += incremento) {
        process.stdout.write(i + " ");
    }
} else {
    for (let i = inicio; i >= fim; i -= incremento) {
        process.stdout.write(i + " ");
    }
}
console.log("\nAcabou!");
9.Crie um programa que calcule e mostre na tela o resultado da soma entre 6 + 8 + 10 12 + 14 + ... + 98 + 100.
// 9. Soma de 6 até 100 (pares)
let soma = 0;
for (let i = 6; i <= 100; i += 2) {
    soma += i;
}
console.log("Resultado:", soma);
10.Desenvolva um aplicativo que mostre na tela o resultado da expressão 500 + 450 + 400 + 350 + 300 + ... + 50 + 0.
// 10. Soma regressiva de 500 até 0 pulando de 50
soma = 0;
for (let i = 500; i >= 0; i -= 50) {
    soma += i;
}
console.log("Resultado:", soma);
11.Faça um programa que leia 7 números inteiros e no final mostre o somatório entre eles.
// 11. Soma de 7 números
soma = 0;
for (let i = 1; i <= 7; i++) {
    let num = Number(prompt("Digite um número: "));
    soma += num;
}
console.log("Somatório:", soma);
12.Crie um programa que leia 6 números inteiros e no final mostre quantos deles são pares e quantos são ímpares.
// 12. Contar pares e ímpares
let pares = 0, impares = 0;

for (let i = 1; i <= 6; i++) {
    let num = Number(prompt("Digite um número: "));
    if (num % 2 === 0) pares++;
    else impares++;
}

console.log("Pares:", pares);
console.log("Ímpares:", impares);
13.Desenvolva um programa que faça o sorteio de 20 números entre 0 e 10 e mostre na tela: a) Quais foram os números sorteados b) Quantos números estão acima de 5 c) Quantos números são divisíveis por 3
// 13. Sorteio de 20 números entre 0 e 10
let acima5 = 0, divisivel3 = 0;

for (let i = 1; i <= 20; i++) {
    let num = Math.floor(Math.random() * 11);
    process.stdout.write(num + " ");

    if (num > 5) acima5++;
    if (num % 3 === 0) divisivel3++;
}

console.log("\nAcima de 5:", acima5);
console.log("Divisíveis por 3:", divisivel3);
14.Faça um aplicativo que leia o preço de 8 produtos. No final, mostre na tela qual foi o maior e qual foi o menor preço digitados.
// 14. Maior e menor preço
let maior = 0;
let menor = Infinity;

for (let i = 1; i <= 8; i++) {
    let preco = Number(prompt("Digite o preço: "));
    if (preco > maior) maior = preco;
    if (preco < menor) menor = preco;
}

console.log("Maior preço:", maior);
console.log("Menor preço:", menor);
15.Crie um algoritmo que leia a idade de 10 pessoas, mostrando no final: a) Qual é a média de idade do grupo b) Quantas pessoas tem mais de 18 anos c) Quantas pessoas tem menos de 5 anos d) Qual foi a maior idade lida
// 15. Idades
let somaIdade = 0, maiorIdade = 0, mais18 = 0, menos5 = 0;

for (let i = 1; i <= 10; i++) {
    let idade = Number(prompt("Digite a idade: "));
    somaIdade += idade;

    if (idade > maiorIdade) maiorIdade = idade;
    if (idade > 18) mais18++;
    if (idade < 5) menos5++;
}

console.log("Média:", somaIdade / 10);
console.log("Maiores de 18:", mais18);
console.log("Menores de 5:", menos5);
console.log("Maior idade:", maiorIdade);
16.Faça um programa que leia a idade e o sexo de 5 pessoas, mostrando no final: a) Quantos homens foram cadastrados b) Quantas mulheres foram cadastradas c) A média de idade do grupo d) A média de idade dos homens e) Quantas mulheres tem mais de 20 anos
// 16. Idade e sexo
let homens = 0, mulheres = 0, somaGrupo = 0, somaHomens = 0, mulheres20 = 0;

for (let i = 1; i <= 5; i++) {
    let idade = Number(prompt("Idade: "));
    let sexo = prompt("Sexo (M/F): ").toUpperCase();

    somaGrupo += idade;

    if (sexo === "M") {
        homens++;
        somaHomens += idade;
    } else {
        mulheres++;
        if (idade > 20) mulheres20++;
    }
}

console.log("Homens:", homens);
console.log("Mulheres:", mulheres);
console.log("Média grupo:", somaGrupo / 5);
console.log("Média homens:", homens > 0 ? somaHomens / homens : 0);
console.log("Mulheres > 20:", mulheres20);
17.Desenvolva um aplicativo que leia o peso e a altura de 7 pessoas, mostrando no final: a) Qual foi a média de altura do grupo b) Quantas pessoas pesam mais de 90Kg c) Quantas pessoas que pesam menos de 50Kg tem menos de 1.60m d) Quantas pessoas que medem mais de 1.90m pesam mais de 100Kg.
// 17. Peso e altura
let somaAltura = 0, mais90 = 0, menos50e160 = 0, mais190e100 = 0;

for (let i = 1; i <= 7; i++) {
    let peso = Number(prompt("Peso: "));
    let altura = Number(prompt("Altura: "));

    somaAltura += altura;

    if (peso > 90) mais90++;
    if (peso < 50 && altura < 1.60) menos50e160++;
    if (altura > 1.90 && peso > 100) mais190e100++;
}

console.log("Média altura:", somaAltura / 7);
console.log("Mais de 90kg:", mais90);
console.log("Menos 50kg e <1.60:", menos50e160);
console.log("Altura >1.90 e peso >100:", mais190e100);
18.desafio Vamos melhorar o jogo. A partir de agora, o computador vai sortear um número entre 1 e 10 e o jogador vai ter 4 tentativas para tentar acertar.
// 18. Jogo de adivinhação
let numeroSecreto = Math.floor(Math.random() * 10) + 1;
let tentativas = 4;
let acertou = false;

console.log("Tente adivinhar o número entre 1 e 10!");
for (let i = 1; i <= tentativas; i++) {
    let palpite = Number(prompt("Tentativa " + i + ": "));

    if (palpite === numeroSecreto) {
        console.log("Parabéns! Você acertou!");
        acertou = true;
        break;
    } else {
        console.log("Errou!");
    }
}

if (!acertou) {
    console.log("Suas tentativas acabaram. O número era:", numeroSecreto);
}

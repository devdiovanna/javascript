// Verifica se um número é positivo, negativo ou zero.
function verificaNumero(numero) {
  if (numero >= 0) {
    console.log("O número é positivo.");
  } else if (numero < 0) {
    console.log("O número é negativo.");
  } else {
    console.log("O número é zero.");
  }
}

// Determina se um número é par ou ímpar.
function verificaParOuImpar(numero) {
  if (numero % 2 === 0) {
    console.log("O número é par.");
  } else {
    console.log("O número é ímpar.");
  }
}

// Implementa uma calculadora que recebe dois números e uma operação (adição, subtração, multiplicação, divisão) e retorna o resultado.
function calculadora(numero1, numero2, operacao) {
  let resultado;
  switch (operacao) {
    case "+":
      resultado = numero1 + numero2;
      break;
    case "-":
      resultado = numero1 - numero2;
      break;
    case "*":
      resultado = numero1 * numero2;
      break;
    case "/":
      resultado = numero1 / numero2;
      break;
  }
  return resultado;
}

// Determina a categoria de uma pessoa baseada na idade (criança, adolescente, adulto, idoso).
function determinaCategoria(idade) {
  let categoria;
  if (idade <= 12) {
    categoria = "criança";
  } else if (idade <= 18) {
    categoria = "adolescente";
  } else if (idade <= 65) {
    categoria = "adulto";
  } else {
    categoria = "idoso";
  }
  return categoria;
}

// Converte notas numéricas em conceitos (A, B, C, D, F) baseado em um sistema de pontuação.
function converteNota(notaNumerica) {
  let nota;
  if (notaNumerica >= 90) {
    nota = "A";
  } else if (notaNumerica >= 80) {
    nota = "B";
  } else if (notaNumerica >= 70) {
    nota = "C";
  } else if (notaNumerica >= 60) {
    nota = "D";
  } else {
    nota = "F";
  }
  return nota;
}

// Calcula o valor final após aplicar um desconto a um determinado preço.
function calculaDesconto(preco, desconto) {
  let valorFinal = preco - (preco * desconto / 100);
  return valorFinal;
}

// Valida se três segmentos formam um triângulo e, se sim, determina seu tipo (equilátero, isósceles, escaleno).
function validaTriangulo(a, b, c) {
  let tipo = "nulo";

  if (a <= 0 || b <= 0 || c <= 0) {
    return tipo;
  }

  if (a + b <= c || a + c <= b || b + c <= a) {
    return tipo;
  }

  if (a === b && b === c) {
    tipo = "equilátero";
  } else if (a === b || a === c || b === c) {
    tipo = "isósceles";
  } else {
    tipo = "escaleno";
  }

  return tipo;
}

// Verifica se um ano é bissexto ou não.
function verificaAnoBissexto(ano) {
  return ano % 400 === 0 || (ano % 4 === 0 && ano % 100 !== 0);
}

// Cria um jogo onde o programa escolhe um número aleatório e o jogador tem que adivinhar qual é. O programa deve fornecer dicas se o número fornecido é maior ou menor.
function jogoAdivinhacao() {
  let numeroAleatorio = Math.floor(Math.random() * 100) + 1;

let atletas = [
  {
    nome: "Cesar Abascal",
    notas: [10, 9.34, 8.42, 10, 7.88]
  },
  {
    nome: "Fernando Puntel",
    notas: [8, 10, 10, 7, 9.33]
  },
  {
    nome: "Daiane Jelinsky",
    notas: [7, 10, 9.5, 9.5, 8]
  },
  {
    nome: "Bruno Castro",
    notas: [10, 10, 10, 9, 9.5]
  }
];

function calcularMedia(objAtletas) {
  for (let i = 0; i < objAtletas.length; i++) {
    let atleta = objAtletas[i];
    let notasOrdenadas = atleta.notas.sort((a, b) => a - b);
    
    // Remove a menor e a maior nota (pega do índice 1 ao 3)
    let notasValidas = notasOrdenadas.slice(1, 4);
    
    // Calcula a média
    let soma = 0;
    notasValidas.forEach(nota => {
      soma += nota;
    });
    let media = soma / notasValidas.length;
    
    // Exibe o resultado
    console.log(`Atleta: ${atleta.nome}`);
    console.log(`Notas Obtidas: ${atleta.notas}`);
    console.log(`Média Válida: ${media}`);
    console.log("");
  }
}

calcularMedia(atletas);

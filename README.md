// Definição da classe Heroi
class Heroi {
    constructor(nome, idade, tipo) {
        this.nome = nome;
        this.idade = idade;
        this.tipo = tipo;
    }

    atacar() {
        let ataque;

        // Verifica o tipo e define o ataque correspondente
        switch (this.tipo) {
            case "mago":
                ataque = "usou magia";
                break;
            case "guerreiro":
                ataque = "usou espada";
                break;
            case "monge":
                ataque = "usou artes marciais";
                break;
            case "ninja":
                ataque = "usou shuriken";
                break;
            default:
                ataque = "usou um ataque indefinido";
        }

        // Exibe a mensagem de ataque
        console.log(`O ${this.tipo} ${this.nome} atacou usando ${ataque}`);
    }
}

// Usando prompt para obter informações do herói
let nomeHeroi = prompt("Digite o nome do herói:");
let idadeHeroi = prompt("Digite a idade do herói:");
let tipoHeroi = prompt("Digite o tipo do herói (guerreiro, mago, monge, ninja):");

// Convertendo a entrada de idade para um número
idadeHeroi = parseInt(idadeHeroi);

// Criação de um objeto da classe Heroi com as informações fornecidas pelo usuário
let heroi = new Heroi(nomeHeroi, idadeHeroi, tipoHeroi);

// Chamando o método atacar para o herói
heroi.atacar();

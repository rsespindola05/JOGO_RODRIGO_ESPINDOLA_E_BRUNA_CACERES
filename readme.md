# Simulador de jogo da velha
Esse projeto é um simulador de jogo da velha 

O jogo se popularizou na Inglaterra do século 19, quando mulheres se reuniam nos finais de tarde para conversar e bordar. Porém, as mais idosas, por não conseguirem mais bordar em razão de suas vistas fracas, se entretiam com o jogo. que passou a ser chamado de Noughts and Crosses (nós e cruzes, em português. Uma referência ao bordado). E como era jogado por mulheres inglesas idosas, quando o jogo veio para o Brasil, ficou conhecido como Jogo da Velha.

## Tecnologias utilizadas: 

1.**HTML**: HTML significa HiperText Markup Language, e em português seria, Linguagem de Marcação de Hipertexto. 

2.**CSS**: CSS significa Cascading Style Sheets que, e em português, é Folha de Estilo em Cascatas.

3.**JAVASCRIPT**: JavaScript é uma linguagem de programação que permite a você implementar itens complexos em páginas web.

### Funcões principais 
$(function(){
	var vez = 1;
	var vencedor = "";
	
	function casasIguais(a, b, c){
		var casaA = $("#casa"+a);
		var casaB = $("#casa"+b);
		var casaC = $("#casa"+c);
		var bgA = $("#casa"+a).css("background-image");
		var bgB = $("#casa"+b).css("background-image");
		var bgC = $("#casa"+c).css("background-image");
		if( (bgA == bgB) && (bgB == bgC) && (bgA != "none" && bgA != "")){
			if(bgA.indexOf("1.jpg") >= 0)
				vencedor = "1";
			else
				vencedor = "2";
			return true;
		}
		else{
			return false;
		}
	}
	
	function verificarFimDeJogo(){
		if( casasIguais(1, 2, 3) || casasIguais(4, 5, 6) || casasIguais(7, 8, 9) ||
			casasIguais(1, 4, 7) || casasIguais(2, 5, 8) || casasIguais(3, 6, 9) ||
			casasIguais(1, 5, 9) || casasIguais(3, 5, 7)
			){
			$("#resultado").html("<h1>O jogador " + vencedor + " venceu! </h1>");
			$(".casa").off("click");
		}
	}
	
### Verificar final de jogo

function verificarFimDeJogo(){
		if( casasIguais(1, 2, 3) || casasIguais(4, 5, 6) || casasIguais(7, 8, 9) ||
			casasIguais(1, 4, 7) || casasIguais(2, 5, 8) || casasIguais(3, 6, 9) ||
			casasIguais(1, 5, 9) || casasIguais(3, 5, 7)
			){
			$("#resultado").html("<h1>O jogador " + vencedor + " venceu! </h1>");
			$(".casa").off("click");
		}
	}

## Como rodar o código
1.**_Simplesmente baixe o código e abra o arquivo index.html no seu navegador_**

## Imagens da tela 
tela 1 : em branco
![tela 1](/imagem/tela%201.png)
tela 2 : jogador 1 venceu
![tela 2](/imagem/tela%202.png)
tela 3 ; jogador 2 venceu
![tela 3](/imagem/tela%203.png)

#### Referencias
* HTML: [homehost] (https://www.homehost.com.br/blog/tutoriais/o-que-e-html/)
* CSS: [hostinger] (https://www.hostinger.com.br/tutoriais/o-que-e-css-guia-basico-de-css)
* JavaScript: [developer.mozilla] (https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/What_is_JavaScript)
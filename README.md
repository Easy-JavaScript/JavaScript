# JavaScript
Conceitos e Implementações Básicas de JavaScript



## Selecionando Elementos DOM

document.ElementsByClassName(".classe")

document.ElementsById("#ID")

document.ElementsByName("p")

document.ElementsByTagName("p")

document.querySelector(".classe/#Id/tag") => só retorna o primeiro(a) classe do DOM

document.querySelectorAll(".teste")       => retorna todas as classes  ".teste"



## Criando Elemento DOM via JS

var div = document.createElement("div");


## Adicionando Elemento dentro de Outro.

var filho = document.createElement("filho");


filho.innerHTML = "filho";

document.querySelector(".pai").appendChild(filho);


## Removendo Elemento de dentro de Outro.

document.querySelector(".pai").removeChild(filho);


## Visualizando um nível acima ou mais dos elementos DOM.

document.querySelector(".pai").parentNode

document.querySelector(".pai").parentNode.parentNode


## Tipos de Dados

### String é tudo que estiver entre aspas, seja simples ou dupla.

"string" ou 'string'

### Boolean

true ou false

### Number

1,2,3...

### Undefined 

indefinido (não encontrado)

### Null

sem valor


## Criando OBJETO

var carro = { 
	placa: 'hux-0090', 
	cor: 'preto', 
	ano: '2017',
	opc:{
		cambio: 'automatico',
		combustivel: flex
	}
}
#### acessando os dados do objeto.
console.log(carro.placa,carro.opc.cambio);

## Arrays

#### pode utilizar strings, objetos, number etc. dentro de arrays.

var array = ['bruno', 22,{carro:'celta'}]

console.log(array[0]);


## Condicionais

- if
- else
- else if
- switch

var nome = 'bruno';
var pai  = 'jose';

if('bruno' == pai){
	console.log('bruno é o pai');
}else if('jose' == pai){
	console.log('verdade');
}else{
	console.log('não sei quem é');
}

---------------------------------------------

var time = 'flamengo';

switch (time){
	case 'brasil':
		console.log('isso é que é time');
		break;
	case 'argentina':
		console.log('isso não é time');
		break;
	case 'flamengo':
		console.log('o melhor do mundo');
		break;
	default:
		console.log('n existe esse time');
		break;

}
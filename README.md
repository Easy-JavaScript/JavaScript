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

---------------------------------------------

## Loops


### Utilizando For 

var js = document.getElementsByClassName('tec');

	for (let i = 0; i < js.length; i++) {
		let txt = js[i].innerHTML;
		js[i].innerHTML = 'curso ' + txt + ' js';
	}

--------------------------------------------

### Utilizando o forEach

	var array = ['casa','dado','elefante','faca'];

	// o forEach só funciona com array, não funciona com htmlColection.
	array.forEach( function(element, index) {
		if(element === 1){
			array[index] = 'vira outra coisa';
		}
	})
	console.log(array);

-----------------------------------------

	### Utilizando o map

	var array2 =['menino','menina','boneco'];

	var nova = array2.map( function(element, index){
		if(element === 1){
			element = 'outra coisa';
		}
		return element;
	})
	console.log(nova);

-----------------------------------------

	### Utilizando While

	var i = 0;

	while (i < 5) {
		console.log('oi');

		i++;
	}



## Carregando a página

window.onload = function(){
	alert("pagina carregou");
}


## Funções

function nomeFuncao(a, b){
		r = a * b;
		return r;
	}

//executando a função
nomeFuncao();


## Eventos

Interatividade com o usuário através dos eventos
Os eventos são mecanismos que se comunicam com as ações que o usuário executa em um determinado documento HTML, de onde provém alguma interatividade. 
Também pode ser pensado que os eventos são notificações JavaScript que permitem saber quando alguma ação aconteceu. 
O objetivo dos eventos é responder os acontecimentos de uma página web com o código JavaScript. 
Vejamos a lista dos principais eventos que essa linguagem possui:

**onBlur:** é ativado quando o usuário retira o foco da aplicação de um elemento da página. O foco da aplicação é o lugar onde está o cursor.

**onChange:** Muda o estado de um elemento de formulário, às vezes não se produz até que o usuário retire o foco da aplicação do elemento.

**onClick:** Quando clicado no botão do mouse sobre um elemento da página, geralmente um botão ou um link.

**onFocus:** Quando um elemento da página ou a janela recebe o foco da aplicação. Contrário do evento “onblur”.

**onKeydown:** Gerado no instante que um usuário pressiona uma tecla, independentemente de soltá-la ou não. A produção acontece no momento do clique.

**onKeypress:** Resultado de uma tecla clicada por um tempo específico. Antes disso, produz-se um “onekeydown” no momento que se pressiona a tecla.

**onKeyup:** Produzido quando o usuário deixa de apertar uma tecla, ou seja, no momento que libera a tecla.

**onLoad:** Quando a página e as imagens terminarem de carregar.

**onMousedown:** Quando o usuário clica sobre um elemento da página, produzindo no momento do clique do botão, independente de estar solto ou não.

**onMousemove:** Produz-se quando o mouse se move pela página.

**onMouseout:** Ocorre com a retirada da seta do mouse da área ocupada um elemento da página.

**onMouseover:** Quando a seta do mouse entra na área ocupada por um elemento da página.

**onMouseup:** Resulta do momento que o usuário solta o botão do mouse, que previamente havia clicado.

**onMove:** Ocorre com o movimento da janela do navegador ou um frame.

**onResize:** Quando a janela do navegador é redimensionada, ou o frame, no caso de que a página os tenha.

**onReset:** Ocorre quando um usuário clica no botão de reset de um formulário.

**onSelect:** Executa quando um usuário realiza uma seleção de um elemento de um formulário.

**onSubmit:** Quando o botão do tipo “submit” envia algum formulário. É executado antes do envio do formulário.


## A seguir são mostrados os métodos que podem ser usados para percorrer o documento, bem como:

**hasChildNodes** - retorna true se o elemento possui filhos;

**firstChild** - retorna uma referência ao primeiro elemento filho;

**lastChild** - retorna uma referência ao último elemento filho;

**nextSibling** - retorna uma referência ao irmão posterior ao elemento;

**previousSibling** - retorna uma referência ao irmão anterior ao elemento;

**nodeName** - retorna o nome da TAG do elemento (apenas para elementos nó);

**nodeValue** - retorna o valor do elemento (apenas para elementos texto);

**nodeType** - retorna o tipo do elemento;

**parentNode** - retorna uma referência ao elemento pai.

Essas propriedades são a chave para ser capaz de manipular a árvore de documentos para acessar dados específicos do nó.
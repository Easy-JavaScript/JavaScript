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

var filho = document.createElement("filho")
;
filho.innerHTML = "filho";

document.querySelector(".pai").appendChild(filho);


## Removendo Elemento de dentro de Outro.

document.querySelector(".pai").removeChild(filho);
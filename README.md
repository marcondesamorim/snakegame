# Recriando o jogo da cobrinha com JavaScript

	Já pensou em criar seu próprio jogo do zero? Aprenda a desenvolver de forma simples o clássico jogo da cobrinha utilizando HTML, CSS e JavaScript.

## Contribuições

	O jogo da cobrinha era encerrado quando a cobra mordeia a sí mesma, adicionei uma condição de ter um veneno no jogo, caso a cobrinha coma o veneno ela também morre e o jogo acaba.

### Código adicionado em index.html

```js
//Desenha o veneno
function drawPoison(){
    context.fillStyle = "black";
    context.fillRect(poison.x, poison.y, box, box)
}
```


### Código adicionado em main.css

```css
   .item div{
        position: absolute;
        bottom: 0;
        right: 0;
        background: black;
        color: white;
        margin-bottom: 5px;
        font-family: Arial, Helvetica, sans-serif;
        opacity: 0;
        visibility: hidden;
        -webkit-transition: visibility 0s, opacity 0.5s linear; 
        transition: visibility 0s, opacity 0.5s linear;
   }
   
   .item:hover{
        cursor: pointer;
   }
   
   .item:hover div{
        width: 100%;
        padding: 8px 15px;
        visibility: visible;
        opacity: 0.7; 
   }
```


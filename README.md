<h1>Recriando o jogo da cobrinha com JavaScript</h1>

	Já pensou em criar seu próprio jogo do zero? Aprenda a desenvolver de forma simples o clássico jogo da cobrinha utilizando HTML, CSS e JavaScript.

<h2>Contribuições</h2>

<blockquote>
	<p>
    O jogo da cobrinha era encerrado quando a cobra mordeia a sí mesma, adicionei uma condição de ter um veneno no jogo, caso a cobrinha coma o veneno ela também morre e o jogo acaba. Além disso foi modificado a mensagem de alerta que informa o fim do jogo, diferenciando a morte por comer veneno ou morde-se a sí propria.
	</p>
</blockquote>

### Código adicionado em script.js

```js
//Desenha o veneno
function drawPoison(){
    context.fillStyle = "black";
    context.fillRect(poison.x, poison.y, box, box)
}
```

```js
//Define a posição do veneno
let poison={
    x: Math.floor(Math.random() * 15 + 1) * box,
    y: Math.floor(Math.random() * 15 + 1) * box
}
```

```js
//Verifica se a cobrinha comeu o veneno
if(snake[0].x == poison.x && snake[0].y == poison.y){
    clearInterval(jogo);
    alert('Game Over - comeu veneno :(');
}
```

```js
drawPoison(); //Chama a função que desenha o veneno
```

### Código modificado em index.js

```js
alert('Game Over :(') -> alert('Game Over - mordeu o rabo :(')
```


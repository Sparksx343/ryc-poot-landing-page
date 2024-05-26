<div class="container">
    <div class="column">
        <h1>Preguntas frecuentes</h1>
    </div>
    <div class="column">
        <div class="acordeon">
            <div class="acordeon__item">
                <input type="radio" name="acordeon" id="item1">
                <label for="item1" class="acordeon__titulo">¿A quienes puedo asegurar?</label>
                <p class="acordeon__contenido">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nobis quod dolorem nam iste laudantium doloremque perspiciatis assumenda, corporis minima, eligendi molestiae dolorum facere iure cum excepturi inventore expedita magni dolores.</p>
            </div>
            <div class="acordeon__item">
                <input type="radio" name="acordeon" id="item2">
                <label for="item2" class="acordeon__titulo">¿Puedo generar puntos INFONAVIT?</label>
                <p class="acordeon__contenido">Accusantium et vel ipsam accusamus, quidem. Quisquam, sunt, alias doloribus fugiat accusantium dolores voluptatibus. Facere, enim, voluptatibus. Odio suscipit, possimus laboriosam debitis alias, nemo deleniti eius, recusandae architecto provident sit?</p>
            </div>
            <div class="acordeon__item">
                <input type="radio" name="acordeon" id="item3">
                <label for="item3" class="acordeon__titulo">¿Puedo estar registrados dos veces?</label>
                <p class="acordeon__contenido">Adipisci iure temporibus quae voluptate nemo ipsum aperiam ipsa ratione magni, quibusdam consequatur tempore illo, molestias illum eligendi labore necessitatibus cum minima. Et voluptatibus quos molestias dignissimos, officia minus, maxime.</p>
            </div>
            <div class="acordeon__item">
                <input type="radio" name="acordeon" id="item4">
                <label for="item4" class="acordeon__titulo">¿Puedo estar inscrito si tengo FOVISSTE?</label>
                <p class="acordeon__contenido">Quo voluptate deleniti, maiores natus, voluptas veniam, omnis fugit recusandae dignissimos dolores sequi quibusdam explicabo velit eligendi suscipit quod? Totam optio error odit, dicta facere et quae sint natus quaerat.</p>
            </div>
        </div>
    </div>
  </div>
<style>
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.column {
  padding: 20px;
  display: flex;
  align-self: center;
}
.acordeon{
    margin-bottom: 50px;
}
.acordeon input {
	display: none;
}

.acordeon__titulo {
	display: block;
	padding: 15px;
	background: #555;
	color: #fff;
	font-size: 20px;
	cursor: pointer;
	border-bottom: 1px solid #fff;
}
.acordeon__titulo:hover {
	background: #777;
}

.acordeon__contenido {
	height: 0;
	overflow: hidden;
	margin: 0;
	transition: all 0.5s;
}

.acordeon input:checked ~ .acordeon__contenido{
	height: auto;
	margin: 15px 0;
}

</style>
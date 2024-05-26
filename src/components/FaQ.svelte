<div class="container">
	<div class="column">
		<h1>Preguntas frecuentes</h1>
	</div>
	<div class="column">
		<div class="acordeon">
			<div class="acordeon__item">
				<input type="radio" name="acordeon" id="item1" />
				<label for="item1" class="acordeon__titulo">¿A quienes puedo asegurar?</label>
				<p class="acordeon__contenido">
					A tu esposa (o), hijos, padres, siempre y cuando se demuestre la dependencia económica, en
					algunos casos, a hijos mayores de edad que estén estudiando y dependan económicamente de
					ti.
				</p>
			</div>
			<div class="acordeon__item">
				<input type="radio" name="acordeon" id="item2" />
				<label for="item2" class="acordeon__titulo">¿Puedo generar puntos INFONAVIT?</label>
				<p class="acordeon__contenido">
					Tenemos varios servicios, tenemos uno que se adapte a tí.
				</p>
			</div>
			<div class="acordeon__item">
				<input type="radio" name="acordeon" id="item3" />
				<label for="item3" class="acordeon__titulo">¿Puedo estar registrados dos veces?</label>
				<p class="acordeon__contenido">
					Si ya está dado de alta, no se recomienda volver a darse de alta con nosotros, ya que el
					Imss no ve con buenos ojos que esté dado de alta en dos lugares al mismo tiempo.
				</p>
			</div>
			<div class="acordeon__item">
				<input type="radio" name="acordeon" id="item4" />
				<label for="item4" class="acordeon__titulo">¿Si cotizo con ISSSTE, puedo tener IMSS?</label>
				<p class="acordeon__contenido">
					Claro, ya que son diferentes dependencias, puedes tener tanto ISSSTE como IMSS
				</p>
			</div>
		</div>
	</div>
</div>

<style>
	.container {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
		gap: 20px;
	}

	.column {
		padding: 20px;
		display: flex;
		align-self: center;
		justify-self: center;
	}
	.acordeon {
		margin-bottom: 50px;
	}
	.acordeon input {
		display: none;
	}

	.acordeon__titulo {
		display: block;
		padding: 15px;
		background: linear-gradient(90deg, #182848, #4b6cb7);
		color: #fff;
		font-size: 20px;
		cursor: pointer;
		border-bottom: 1px solid #fff;
	}
	.acordeon__titulo:hover {
		background: #4b6cb6;
	}

	.acordeon__contenido {
		height: 0;
		overflow: hidden;
		margin: 0;
		transition: all 0.5s;
	}

	.acordeon input:checked ~ .acordeon__contenido {
		height: auto;
		margin: 15px 0;
	}
</style>

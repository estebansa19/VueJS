<template>
	<div class="test">
<!-- 		<span v-text="title"></span>
		<div v-if="showName">
			<p>{{ user.firstname }}</p>
		</div>
		<div v-else>
			<p>No se encuentra el usuario</p>
		</div>
		<hr>
		<ul>
			<li v-for="task in tasks">
				{{task.title}}
			</li>
		</ul> -->

	<!-- <input type="text" v-model="user.firstname">
		<button v-on:click="saludar(user.firstname)">Click me owo</button> -->

<!-- 	<input type="text" v-on:keyup.enter="typedEnter">
	<input type="text" readonly id="txt"> -->

	{{ msg}}

</div>
</template>

<script>
	export default {
		data(){
			return {
				title: 'Title component',
				user: {
					firstname: 'Esteban',
					lastname: 'Alzate'
				},
				myHtml: '<h2>Hola vue</h2>',
				showName: false,
				tasks: [
				{title: 'eat'},
				{title: 'dinner'},
				{title: 'clean'},
				]
			}
		},
		methods: {
			saludar(name){
				alert('Hello ' + name)
			},
			typing(e){
				document.getElementById('txt').value = e.target.value
			},
			typedEnter(){
				alert('Presionó un enter')
			}
		},
		computed: {
			fullName(){
				return this.user.firstname +  ' ' + this.user.lastname
			}
		},
		props: {
			msg: {
				type: String,
				default: "Mensaje por defecto"
			}
		}
	}
</script>

<style>
	.test{
		background-color: #eee;
	}
</style>
<template>
	<h2>{{title}}</h2>
	<h3>{{getCurrentTabName}}</h3>
	<form action="" method="post">
		<div class="input-group input-group-lg mb-3">
			<span class="input-group-text w-25">Log:</span>
			<input type="text" class="form-control" v-model="login" v-on:input="newTitle">
		</div>
		<div class="input-group input-group-lg mb-3">
			<span class="input-group-text w-25">Pass:</span>
			<input type="password" class="form-control" v-model="email">
		</div>
		<div class="p-2">
			<button type="button" class="btn btn-outline-info btn-lg w-75" v-on:click="sendForm">
				<i class="fa fa-check" aria-hidden="true"></i>
			</button>
		</div>
	</form>
	
	<div>
		<p>{{login}}</p>
		<p>{{email}}</p>
	</div>

</template>


<script>
	
	export default {
		name: 'LoginPage',
		emits: ["newTitle"],
		props: {
			getCurrentTabName: String,
			title: String,
		},
		methods: {
			sendForm: function () {
				console.log(this.login, this.email);
			},
			newTitle: function () {
				this.$emit('newTitle', this.login);
			}
		},
		data: function () {
			return {
				login: '',
				email: '',
				emits: ["newTitle"],
			};
		},
	};
</script>
<template>
	<h3>{{getCurrentTabName}}</h3>
</template>


<script>
	
export default {
		name: 'SigninForm',
		props: {
			getCurrentTabName: String
		},
}
</script>
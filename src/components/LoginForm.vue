<template>
	<h2>{{ msg }}</h2>
	
	<div class="container">
		<div class="row">
			<div class="col-lg-4 col-md-6 col-sm-12 offset-md-3 offset-lg-4">
				<div class="card">
					<div class="card-body">
						<nav>
							<div class="nav nav-tabs" id="nav-tab" role="tablist">
								<a v-for:="(item, index) in arrTab"
								v-bind:class="currentTab==index ? 'nav-link active' : 'nav-link'"
								v-on:click="swichTab(index)">
								{{item}}
							</a>
						</div>
					</nav>
					<div class="tab-content">
						<div v-for="(item, index) in arrTab" v-bind:key="index"
						v-bind:class="setClass(index)"
						>
						{{item}}
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
</div>
</template>

<script>
	export default {
		name: 'LoginForm',
		props: {
			msg: String
		},
		data: function () {
			return {
				currentTab:0,
				arrTab: ['Log in', 'Sign in']
			};
		},
		methods: {
			setClass: function (index) {
				var currentClass = 'tab-pane';
				if (index==this.currentTab) {
					currentClass = 'tab-pane active';
				}
				return currentClass;
			},
			swichTab: function (index) {
				this.currentTab = index;
				console.log(index);
			}
		}
	};
</script>

<style>
	.nav-link {
		cursor: pointer;
	}
</style>
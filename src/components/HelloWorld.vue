<template>
	<div class="hello">
		<van-button type="default">默认按钮</van-button>
		<van-button type="primary">主要按钮</van-button>
		<van-button type="info">信息按钮</van-button>
		<van-button type="warning">警告按钮</van-button>
		<van-button type="danger">危险按钮</van-button>


		<van-cell is-link @click="showPopup">展示弹出层</van-cell>
		<van-popup v-model="show" position="top" :style="{ height: '20%' }" />
	</div>
</template>

<script>
	export default {
		name: 'HelloWorld',
		props: {
			// msg: String,
			show: false
		},
		methods: {
			showPopup() {
				this.show = true;
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	h3 {
		margin: 40px 0 0;
	}

	ul {
		list-style-type: none;
		padding: 0;
	}

	li {
		display: inline-block;
		margin: 0 10px;
	}

	a {
		color: #42b983;
	}
</style>

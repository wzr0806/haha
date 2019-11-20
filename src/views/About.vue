<template>
	<div class="about">
		<h1>哈哈哈啊哈哈哈这是about</h1>


		<van-button @touchstart.stop="show = true">
			弹出默认键盘
		</van-button>

		<van-number-keyboard v-model="value" :show="show" :maxlength="6" @blur="show = false" />
		<van-number-keyboard :show="show" extra-key="." close-button-text="完成" @blur="show = false" @input="onInput" @delete="onDelete" />
	</div>
</template>


<script>
	export default {
		data() {
			return {
				show: false,
				value: ''
			}
		},

		methods: {
			onInput(value) {
				Toast(value);
			},
			onDelete() {
				Toast('删除');
			}
		}
	}
</script>

<template>
	<view class="scroll">
		<scroll-view class="list-scroll" enable-flex="true" scroll-y @scrolltolower="loadMore">
			<view>
				<slot></slot>
			</view>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		},
		methods: {
			loadMore() {
				this.$emit("loadMore")
			}
		}
	}
</script>

<style lang="scss">
	.scroll {
		height: 100%;
		flex: 1;
		overflow: hidden;
		box-sizing: border-box;

		.list-scroll {
			height: 100%;
			display: flex;
			flex-direction: column;
		}
	}
</style>

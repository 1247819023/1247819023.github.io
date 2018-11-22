<template>
	<div class='comment'>
		<span class='comment-name'>{{comment.name}}:</span>
		<span class='comment-content'>{{comment.content}}</span>
		<a href @click.prevent='deleteMe' class='comment-delete'>删除</a>
	</div>
</template>

<script>
export default {
	props:['comment'],
	methods: {
		deleteMe() {
			this.$emit('deletes',this.comment.id);
		}
	}
};

</script>
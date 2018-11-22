<template>
	<div class='cinput'>
			<label>
				<span>用户名:</span>
				<input v-model='name'>
			</label>
			<label>
					<span>评论内容:</span>
					<textarea v-model='content'></textarea>
			</label>
			<footer>
					<button @click='incr'>发布</button>
			</footer>
	</div>
</template>

<script>
var commentInput = {
	data() {
		return{
			name: '',
			content:''
		}
	},
	methods:{
		incr(){
			if(!this.name){
				return alert('用户名不能为空');
			}
			if(!this.content){
				return alert('评论内容不能为空');
			}
			
			localStorage.setItem('vvv-name' , this.name);
			
			this.$emit('dosave',{
				id: +new Date(),
				name: this.name,
				content: this.content
			});
			
			this.content = '';
		}
	},
	created() {
		const cs = localStorage.getItem('vvv-name');
		if(cs) {
			this.name = cs;
		}
	}
};

export default commentInput;

</script>
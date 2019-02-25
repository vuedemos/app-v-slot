<template>
  <button>
    <slot>提交</slot>
  </button>
</template>

<script>
export default {
  name: 'SubmitButton',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button{
	text-align:center;
	margin:10px;
	padding: 10px 0px;
	display:inline-block;
	min-height:30px;
	min-width:180px;
	font-size: 2rem;
	cursor:pointer;
	color:#F0F0F0;
	border-radius:10px;
	border-bottom:4px solid #0045A6;
	box-shadow: 6px 6px 6px #999;

	user-select: none;
  background: linear-gradient(#00C8F8, #0067F7);
  transition: background 0.05s linear;
	background-size:1px 200px;
	transition: all .05s linear;
}

button:hover{
	background-position:100px;
}

button:focus {
  outline: none;
}

button:active {
	box-shadow: 2px 2px 2px #777;
	border-bottom:1px solid #0045A6;
	transform: translateY(3px);
  outline: none;
}
</style>

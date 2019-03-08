<template>
	<div class="recipe__item">
		<p>{{recipe.title}}</p>
		<span>Image: </span><br />
		<span>Title: </span><br />
		<span>Ingredients: </span><br />
		<span>Href: </span><br />
	</div>
</template>


<script>
	export default {
		name: "RecipeItem",
		props: ["recipe", "Image", "Title", "Ingredients", "Href"]
	}
</script>


<style scoped>
	.recipe__item {
		background: #f4f4f4;
		padding: 30px;
		border-bottom: 1px solid #ccc;
		color: #333;
	}


</style>
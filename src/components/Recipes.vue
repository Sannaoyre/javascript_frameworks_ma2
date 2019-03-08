<template>
	<div>
		<div v-bind:key="recipe.id" v-for="recipe in recipes">
			<RecipeItem v-bind:recipe="recipe" 
						v-bind:Title="recipe.title"
						v-bind:Image="recipe.Image"
						v-bind:Ingredients="recipe.ingredients"
						v-bind:Href="recipe.Href"
			/>
			
		</div>
	</div>
</template>


<script>
import RecipeItem from './RecipeItem.vue';

	export default{
		name: "Recipes",
		components: {
			RecipeItem
		},
		props: ["recipes"]
	}

</script>

<style scoped>
</style>
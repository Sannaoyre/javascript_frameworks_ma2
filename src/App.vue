 <template>
  <div id="app">
    <Header />
    <Recipes v-bind:recipes="recipes" />
  </div>
</template>

<script>
import Header from './components/layout/Header';
import Recipes from './components/Recipes';
import axios from 'axios';


export default {
    name: 'app',
    components: {
      Header,
      Recipes
    
    },
    data(){
      return{
        recipes: []
    }
  },
  beforeMount: function(){
    const app = this;
    const conversionUrl = 'https://cors-anywhere.herokuapp.com/';
    const url = 'http://www.recipepuppy.com/api/';

      fetch(conversionUrl + url)
      .then(function(response) {
        return response.json();
    }) 
      .then(function(result) {
      app.recipes  = result;

      })
  } 
   


}
</script>

<style>
* {
box-sizing: border-box;
margin: 0;
padding: 0;
}

body{
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>

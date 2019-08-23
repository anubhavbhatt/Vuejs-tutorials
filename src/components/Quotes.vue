<template>
    <div class="quotes">
        <Category></Category>
        <div class="add-new-quote"> 
            <form id="new-quote">
                <input type="text" name="new-description" id="new-description">
                <input type="text" name="new-author" id="new-author">
                <input type="text" name="new-category" id="new-category">
                <button type="submit" @click="addNewQuote()">Add New Quote</button>
            </form>
        </div>
        <div v-for="quote in quotes" v-bind:key="quote.id" class="quote">
            <div class="category" :class="quote.category">{{quote.category}}</div>
            <p>"{{ quote.description }}"</p>
            <span class="posted-on">{{ quote.posted_on}}</span>
            <span class="author">{{ quote.author}}</span>
        </div>
    </div>
</template>
<script>
import Category from "./Category.vue";
export default {
    components: {
        Category
    },
    data(){
        return{
            quotes : [
                {"id":1001,"description": "It is not how much we have , but how much we enjoy, that makes happiness", "posted_on":" 16 Aug 2019", "author": "Charles Spurgeon","category":"motivation"},
                {"id":1002,"description": "Love is the greatest refreshment in life", "posted_on":" 17 Aug 2019", "author": "Pablo Picasso","category":"love"},
                {"id":1003,"description": "Circumstances are beyond the control of man, but his conduct is in his own power", "posted_on":" 18 Aug 2019", "author": "Benjamin","category":"life"},
                {"id":1004,"description": "You never regret being kind", "posted_on":" 19 Aug 2019", "author": "Nicole Shepherd","category":"motivation"},
                {"id":1005,"description": "Nothing succeeds like success", "posted_on":" 20 Aug 2019", "author": "Alexandra Dumas","category":"life"},
                {"id":1006,"description": "All our dreams can come true if we have the courage to pursue them", "posted_on":" 21 Aug 2019", "author": "Walt Disney","category":"technology"},
            ]
            
      }
  }
};
</script>
<style>
.quotes{
    width:60%;
    padding:0 20% 0 20%;
    display: grid;
    grid-template-columns: repeat(1fr);
}
.quote{
    background-color:rgb(235, 235, 238);
    box-shadow: 10px 10px 10px grey;
    text-align: left;
    padding: 0.5rem;
    margin: 10px;
    border-radius: 25px 5px 5px 10px;    
}
.quote p{
    font-size: 20px;
}
.posted-on{
    padding-right: 10px;
    font-weight: bold;
    font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif
} 
.author{
    font-weight: bold;
    padding-left: 20px;
    float:right;
    font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif
}
.category{
    background-color:#795ce0;
    color:azure;
    padding:5px 15px;
    font-weight: 600;
    border-radius: 15px 5px 5px 5px;
}
.motivation{
    background-color: #795ce0;
}
.love{
    background-color: #64c579;
}
.life{
    background-color: #c45fa5;
}
.technology{
    background-color: rgb(122, 252, 209);
}
</style>

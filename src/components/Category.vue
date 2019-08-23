<template>
    <div class="legends">   
        <div class="legend"
            v-for="category in categories" 
            v-bind:key="category.name">
            <span class="legend-color-box" :class="category.name"></span>{{ category.name | capitalize }}</div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            categories :[
                {"name":"motivation"},
                {"name":"love"},
                {"name":"life"},
                {"name":"technology"},
            ]
        }
    },
    filters: {
        capitalize: function (value) {
            if (!value) return ''
            value = value.toString()
            return value.charAt(0).toUpperCase() + value.slice(1)
        }
    }
}
</script>
<style>
    .legends{
        font-weight: 500;
        color:blueviolet;
    }
    .legend{
        height:40px;
        display: inline-block;
        padding-right: 10px;
    }
    .legend-color-box{
        display: inline-block;
        height:20px;
        width:20px;
        box-shadow: 5px 3px 3px grey;
        margin-right: 5px;
        vertical-align: sub; 
    }
</style>
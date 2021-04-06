<template>
    <section class="recipes">
        <Recipe 
            v-for="recipe in recipes"
            :key="recipe.id"
            :thumbnail="recipe.thumbnail" 
            :title="recipe.title"
            :id="recipe.id"
            :previewText="recipe.previewText" />

    </section>
</template>

<script>
import Recipe from '@/components/Recipe'
export default {
    components: {
        Recipe
    },
    asyncData() {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipes: [
                        {
                            id:"1",
                            title: "Italian Pizza",
                            previewText: "Delicious Pizza",
                            thumbnail: "https://previews.123rf.com/images/zhenyane/zhenyane2004/zhenyane200403226/145723262-delicious-italian-pizza-served-on-table-with-ingredients-cheese-and-vegetables.jpg"
                        },
                        {
                            id:"2",
                            title: "Italian Burger",
                            previewText: "Delicious Burger",
                            thumbnail: "https://images2.minutemediacdn.com/image/upload/c_crop,h_1126,w_2000,x_0,y_181/f_auto,q_auto,w_1100/v1554932288/shape/mentalfloss/12531-istock-637790866.jpg"
                        }
                    ]
                })
            }, 1500)
        })
    }
};
</script>

<style scoped>
.recipes {
    display: flex;
    flex-flow: row wrap;
}

</style>
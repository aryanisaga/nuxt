<template>
    <section class="single-recipe">
        <h1> {{ recipe.title }} </h1>
        <div>
            <img class="recipe-img" :src="recipe.thumbnail" :alt="recipe.title">
        </div>
        <p>{{recipe.descriptionText}}</p>
    </section>
</template>

<script>
export default {
    asyncData(context) {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({
                    recipe: [
                        {
                            id:"1",
                            title: "Italian Pizza",
                            previewText: "Delicious Pizza",
                            descriptionText: "This is really delicious meal!",
                            thumbnail: "https://previews.123rf.com/images/zhenyane/zhenyane2004/zhenyane200403226/145723262-delicious-italian-pizza-served-on-table-with-ingredients-cheese-and-vegetables.jpg"
                        },
                        {
                            id:"2",
                            title: "Italian Burger",
                            previewText: "Delicious Burger",
                            descriptionText: "This is really delicious meal!",
                            thumbnail: "https://images2.minutemediacdn.com/image/upload/c_crop,h_1126,w_2000,x_0,y_181/f_auto,q_auto,w_1100/v1554932288/shape/mentalfloss/12531-istock-637790866.jpg"
                        }
                    ].find(el => el.id === context.params.id)
                })
            }, 1500)
        })
    }
}
</script>

<style scoped>
.single-recipe {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 20px;
}

.recipe-img {
    width: 500px;

}
</style>
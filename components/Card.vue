<template>
  <div class="card shadow">
       <div v-if="background_image" class="card-img-top cover" :style="`background-image: url('${card.background}${Math.floor(Math.random() * 77)}')`"></div>
       <div v-if="!background_image" class="card-img-top cover" :style="`background-color:${getRandomColor()}`">
           <div class="d-flex align-items-center justify-content-center mt-6">
               <h3 class="p-2 text-white">{{ getFirstAndLastLetter(card.title) }}</h3>
           </div>
       </div>
        <div class="card-body">
            <div class="row h-50">
                <div class="col-md-12 col-12 col-lg-12">
                    <NuxtLink class="link-primary" :to="classes ? 'class/'+card.id : 'semester/'+card.id">
                        <h3>{{card.title}}</h3>
                    </NuxtLink>
                </div>
                <div class="row mt-3">
                    <div class="col-md-12 col-12 col-lg-12">
                        <NuxtLink class="btn btn-outline-danger rounded-pill order-0" :to="classes ? '/class/'+card.id : 'semester/'+card.id">Continue</NuxtLink>
                    </div>
                </div>
            </div>

        </div>
  </div>
</template>

<script>
export default {
    props: ['background_image','card','classes'],
    data(){
        return {
            names:{
                aqua: "#00ffff",
                azure: "#f0ffff",
                beige: "#f5f5dc",
                black: "#000000",
                brown: "#a52a2a",
                darkcyan: "#008b8b",
                darkgrey: "#a9a9a9",
                darkgreen: "#006400",
                darkkhaki: "#bdb76b",
                darkmagenta: "#8b008b",
                darkolivegreen: "#556b2f",
                darkorange: "#ff8c00",
                darkorchid: "#9932cc",
                darkred: "#8b0000",
                darksalmon: "#e9967a",
                darkviolet: "#9400d3",
                indigo: "#4b0082",
                khaki: "#f0e68c",
                lightblue: "#add8e6",
                lightcyan: "#e0ffff",
                lightgreen: "#90ee90",
                lightgrey: "#d3d3d3",
                lightpink: "#ffb6c1",
                lightyellow: "#ffffe0",
                maroon: "#800000",
                navy: "#000080",
                olive: "#808000",
                orange: "#ffa500",
                purple: "#800080",
                silver: "#c0c0c0",
            }
        }
    },
    methods: { 
        // getRandomColor() {
        //     var letters = '0123456789ABCDEF';
        //     var color = '#';
        //     for (var i = 0; i < 6; i++) {
        //         color += letters[Math.floor(Math.random() * 16)];
        //     }
        //     return color;
        // },
        getRandomColor() {
            var result;
            var count = 0;
            for (var prop in this.names)
                if (Math.random() < 1/++count)
                result = prop;
            return result;
        },
        getFirstAndLastLetter(word){
            return (word.charAt(0)+' '+word.slice(-1)).toUpperCase();
        }
    }
}
</script>

<style scoped>
.shadow {
    box-shadow: 0 .125rem .25rem rgba(0,0,0,.075)!important;
}

.cover {
    height: 180px;
    background-size: cover;
    background-position: center center;
}

.card-img-top {
    width: 100%;
    border-top-left-radius: calc(4px - 1px);
    border-top-right-radius: calc(4px - 1px);
}

.card:hover{
    box-shadow: 0px 0px 19px 4px rgba(0,0,0,.075)!important;
}
</style>
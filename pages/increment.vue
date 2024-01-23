<template>
    <div class="flex flex-row justify-center mt-20">
        <div>{{ count }}</div>
        <div class="mt-10">
            <button v-on:click="increment" class="px-5 py-2 bg-green-500 text-white rounded-xl">Increment</button>
        </div>
        <!-- Show POSTS -->
        <div v-if="!isLoading">
            <!-- Posts -->
            <!-- 
                Posys\
                Posys\
                Posys\
                Posys\
                Posys\
                Posys\
                Posys\
             -->
        </div>
        <div>

        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            count: 0,
            message: '',
            posts:[],
            isLoading: false
        }
    },

    methods: {
        increment() {
            this.count++
        },

        setLoading(value) {
            this.isLoading = value;
        },

        fecthPosts() {
            //load posts from API
            /* ============== Fetching Posts */  
            
            
        }
    },

    beforeMount: {
        //this.setLoading(true)
    },

    mounted() {
        this.fecthPosts();
    },
}
</script>

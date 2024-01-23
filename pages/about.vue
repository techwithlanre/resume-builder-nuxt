<template>
    <div class="flex flex-col justify-center mt-20">
        <div>
            My name is {{ nameToShow }}
        </div>
        <div>
            <button v-on:click="updateName('Kenny')" class="px-5 py-2 rounded-lg bg-green-600 text-white ">Change name</button>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            showTitle: false,
            nameToShow: "Sunmi",
            namesSource: [
                'Sunmi',
                'Kenny',
                'Azeez',
                'Aisha',
                'Olatunde',
                'Olaitan',
                'Richie',
                'Cynthia',
                'Subomi',
                'Rashidat'
            ],
            currentIndex: 0
        }
    },

    methods: {
        toggleTitle() {
            //this.showTitle = !this.showTitle;
            if(this.showTitle == true) {
                this.showTitle = false;
            } else {
                this.showTitle = true;
            }
        },

        updateName() {
            var totalNames = this.namesSource.length; // 10
            if(this.currentIndex < (totalNames - 1)) {
                this.currentIndex++;
                this.nameToShow = this.namesSource[this.currentIndex];
            }
        },

        initalName() {
            //this.name = this.names[0]
        }
    }
}
</script>
<script>
export default {
    data() {
        return {
            searchStr: "",
            searchArchetypes: "",
            archethypes: ["alien"]
        };
    },
    methods: {
        emitSearchEvent() {
            this.$emit('performSearch', {
                searchArchetypes: this.searchStr,
                archetype: this.searchArchetypes,
            });
        }
    }
}
</script>

<template>
    <div class="btn">
        <input type="text" placeholder="Search card" 
        v-model="searchStr" 
        @keyup.enter="$emit('performSearch', searchStr )">
        <select name="archetype" id="" v-moedl="searchArchetypes">
            <option :value="archetype">Select archetype</option>
            <option> Alien </option>
        </select>
        <button @click="$emit('performSearch', searchStr )">Search</button>
        <button>Reset</button>
    </div>
</template>

<style lang="scss" scoped>
    .btn {
        padding: 1rem;
        margin-left: 9rem;
        select {
            padding: .5rem;
            padding-right: 5rem;
            border-radius: 5px;
            margin-left: 1rem;
        }
    }

    button {
        margin-inline: 1rem;
        padding: 1rem;
    }
</style>
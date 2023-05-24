<script>

import { store } from "../store";
export default {
    data() {
        return {
            store,
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
        <select name="archetype" id=""
        v-model="store.selectedOption" 
        @change="this.$emit('filteredSearch')">
            <option value="#">Select archetype</option>
            <option> Alien </option>
        </select>
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
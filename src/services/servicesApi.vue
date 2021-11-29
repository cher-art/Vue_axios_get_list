<template>
<div id="app">
    <div class="search-wrapper">
       <label>
            <input type="text" v-model="search" placeholder="Search title.."/>
            Search hier:
            <p>{{ this.serach }}</p>
        </label>
    </div>
    <div class="wrapper">
        <li v-for="name in this.names " :key="name">
            {{ name }}
        </li>
    </div>
</div>
</template>

<script>

import axios from 'axios'

export default {
    data() {
        return {
            search: '',
            names: [],
        }
    },
    mounted() {
        axios
            .get('Вставить УРЛ' + this.search)
            .then((response) => {this.names = response.data.results})
            .catch(error => console.log(error));
            console.log(this.search);
            
    },
}

</script>
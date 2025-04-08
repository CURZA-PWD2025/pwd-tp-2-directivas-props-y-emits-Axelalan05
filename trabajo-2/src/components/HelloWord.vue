<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <p>
            For a guide and recipes on how to configure / customize this project,<br>
            check out the
            <a href="https://vuejs.org/guide/introduction.html" target="_blank" rel="noopener">Vue documentation</a>.
        </p>
        <h3>Installed CLI Plugins</h3>
        <ul>
            <li><a href="https://github.com/vuejs/vue-cli/tree/main/packages/%40vue/cli-plugin-babel" target="_blank"
                    rel="noopener">babel</a></li>
            <li><a href="https://github.com/vuejs/vue-cli/tree/main/packages/%40vue/cli-plugin-eslint" target="_blank"
                    rel="noopener">eslint</a></li>
        </ul>
        <h3>Essential Links</h3>
        <ul>
            <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
            <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
            <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
            <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
            <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
        </ul>
        <h3>Ecosystem</h3>
        <ul>
            <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">Vue Router</a></li>
            <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">Vuex</a></li>
            <li><a href="https://test-utils.vuejs.org" target="_blank" rel="noopener">Vue Test Utils</a></li>
            <li><a href="https://github.com/vuejs/devtools" target="_blank" rel="noopener">Vue Devtools</a></li>
        </ul>
    </div>
</template>

<script lang="ts">
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    }
}
</script>

<style scoped>
h1,
h2 {
    font-weight: normal;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #42b983;
}
</style>
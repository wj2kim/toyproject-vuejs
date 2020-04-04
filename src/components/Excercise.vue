<template>
    <div id = "welcome">
        <app-header></app-header>
    </div>
</template>

<script>
    var appHeader = {
        template: '<h1>header</h1>'
    };

    export default {
        el : '#welcome',
        components : {
            'app-header' : appHeader
        }
    }
</script>
<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot name="text"></slot>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['quotes']
    }
</script>

<style scoped>

    @import url('https://fonts.googleapis.com/css?family=Indie+Flower');

    .panel {
        margin: 1em;
        overflow: auto;
        max-height: 230px;
    }
    .panel-body {
        font-family: 'Indie Flower', cursive;
        cursor: pointer;
    }

    .panel:hover {
        background: #cc0000;
        color: white;
        text-align: center;
    }
</style>
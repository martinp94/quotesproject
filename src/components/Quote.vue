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
    .panel {
        margin: 1em;
    }
    .panel-body {
        font-family: Arizonia, sans-serif;
        cursor: pointer;
    }

    .panel:hover {
        background: #cc0000;
        color: white;
        text-align: center;
    }
</style>
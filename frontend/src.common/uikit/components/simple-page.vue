<template>
    <v-layout fill-height column>
        <div class="header mx-3 mt-3" v-if="!noHeader">
            <slot name="header"/>
        </div>

        <v-layout column>
            <slot/>
        </v-layout>
        
        <div class="pa-3" v-if="!noFooter">
            <slot name="footer"/>
        </div>
    </v-layout>
</template>

<script>
export default {
    props: {
        noHeader: { type: Boolean, default: false, },
        noFooter: { type: Boolean, default: false, },
    },
};
</script>


<style module lang="less">
@import "~style";

.header {
    .state-header();
}
</style>
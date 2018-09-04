<template>
    <div class="mainPageWrapper">
        <menu-bar></menu-bar>
        <list-content></list-content>
    </div>
</template>

<script lang="ts">
import {
    Component,
    Prop,
    Vue
} from "vue-property-decorator";
import MenuBar from './menu-bar.vue';
import ListContent from './list-content.vue';

@Component({
    components: {
        MenuBar,
        ListContent
    }
})
export default class Page extends Vue {}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.mainPageWrapper {
    width: 95%;
    border: 5px solid paleturquoise;
    position: absolute;
    bottom: 0px;
    top: 0px;
    left: 50%;
    transform: translate(-50%);
    display: flex;
}
</style>

<template>
    <div class="mainWrapper">
        <div class="add"
             @click="addList">add</div>
        <div class="contentWrapper">
            <div class="gap-h-40-px"></div>            
            <div v-for="item of list"
                :key="item">
                <div class="list"> {{item}} </div>
                <div class="gap-h-40-px"></div>            
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import {
    Component,
    Prop,
    Vue
} from "vue-property-decorator";

@Component
export default class ListContent extends Vue {
    list = ['list1', 'list2'];
    addList() {
        this.list.push('list' + (this.list.length + 1));
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.mainWrapper {
    width: 100%;
    border: 1px solid wheat;
}
.contentWrapper {
    overflow: scroll;
    height: 100%;
}
.list {
    width: 200px;
    height: 80px;
    margin: auto;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid rgba(70, 131, 180, 0.603);
}
.add {
    width: 40px;
    height: 20px;
    background-color: azure;
    position: absolute;
}
.gap-h-40-px {
    height: 40px;
}
</style>

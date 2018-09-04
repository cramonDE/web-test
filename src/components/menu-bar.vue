<template>
    <div class="mainWrapper">
        <div class="add"
             @click="addList">add</div>
        <div class="listWrapper">
            <div class="list"
                v-for="item of list"
                :key="item">
                <div> {{item}} </div>
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
export default class MenuBar extends Vue {
    list = ['list1', 'list2', 'list3', 'list4'];
    addList() {
        this.list.push('list' + (this.list.length + 1));
        console.log(this.list);
        
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.mainWrapper {
    width: 300px;
    height: 100%;
    border: 1px solid antiquewhite;
}
.listWrapper {
    display: flex;
    flex-direction: column;
    height: 100%;
}
.list {
    width: 200px;
    height: 40px;
    margin: auto;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid rgba(70, 131, 180, 0.603)
}
.add {
    width: 40px;
    height: 20px;
    background-color: azure;
    position: absolute;
}
</style>

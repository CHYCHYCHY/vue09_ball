<template>
<container>
    <graphics :x="mapX1"></graphics>
</container>
</template>

<script>
import {
    onMounted,
    onUnmounted,
    ref
} from "vue";
import {
    game
} from "../game";

// mapX1 在区间0~650之间动
const mapX1 = ref(0);
let speed = 10;
let dir = 1;

// 小球左右来回移动
function handleTicker() {
    mapX1.value += dir * speed;

    if (mapX1.value >= 650) {
        dir = -1;
    } else if (mapX1.value <= 0) {
        dir = 1;
    }
}
// 组件挂载
onMounted(() => {
    game.ticker.add(handleTicker);
});
// 组件卸载
onUnmounted(() => {
    game.ticker.remove(handleTicker);
});

export {
    mapX1
};
</script>

<style scoped></style>

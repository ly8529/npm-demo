# 一些npm包的使用demo

# tippy.js

## 安装
```
pnpm i tippy.js
```

## 使用
```
<template>
	<button id="myButton">My button</button>

	<button data-tippy-content="Tooltip">Text</button>
	<button data-tippy-content="Another Tooltip">Text</button>
</template>
<script setup lang="ts">
import { onMounted } from 'vue'
import tippy,{roundArrow} from 'tippy.js'
import 'tippy.js/dist/tippy.css'
import 'tippy.js/dist/svg-arrow.css';
import 'tippy.js/themes/light.css';


onMounted(() => {
	tippy('#myButton', {
		content: 'My tooltip!',
		duration: 0,
		arrow: roundArrow,
		delay: [1000, 6000], //延迟1000ms出现，延迟2000ms消失
        theme: 'light',
	})
	tippy('[data-tippy-content]',{
        theme: 'light',
    })
})
</script>

```

## 支持html展示

## 支持定制主题

## 支持动画

## 
<template>
    <div id="app">
        {{ message }}
    </div>
</template>

<script>
    import {createApp, ref} from 'vue'

    createApp({
        setup() {
            const message = ref('Hello vue')

            return {
                message
            }
        }
    }).mount('app')
</script>

<!-- <script setup>
    // 옵션 API 방식 (객체지향)
    /* export default {
        // data()에서 반환된 속성들은 반응적 상태가 되어 this에 노출됨
        data() {
            return {
                count : 0,
            }
        },

        methods : {
            // 속성 값 변경, 업데이트 가능한 함수
            // 템플릿 내에선 이벤트핸들러 바인딩 가능
            increment() {
                this.count++
            }
        },
    }; */

    // 컴포지션 API 방식 
    import { ref } from 'vue'

    const count = ref(0)

    function increment() {
        count.value++
    }

</script> -->
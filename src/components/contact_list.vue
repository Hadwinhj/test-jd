<template>

    <div>

        <!--标题-->
        <div>{{title}}</div>

        <!--通话记录列表-->
        <ul class="contact_list_area" style="padding: 0;">
            <!--通话记录 item -->
            <li class="contact_list_item" v-for="item in contact">
                <!--联系人名字-->
                <div class="contact_list_name">{{item.name}}</div>
                <!--联系人电话-->
                <div class="contact_list_phone" v-on:click="clickListenerPhone(item)">{{item.phone}}</div>
            </li>

        </ul>
    </div>

</template>

<script>
    export default {
        name: "contact_list",
        props: {
            title: String
        },
        data() {
            return {
                contact: [
                    {
                        "name": "豇豆",
                        "phone": 13677889900
                    },
                    {
                        "name": "充个",
                        "phone": 13677889900
                    },
                    {
                        "name": "都分手",
                        "phone": 13677889900
                    },
                    {
                        "name": "ss",
                        "phone": 13677889900
                    }
                ]
            }
        },

        created: function () {

        },

        methods: {


            /**
             * 拨打电话号码
             * @param item
             */
            clickListenerPhone(item) {
                console.log("给" + item.name + " 拨打电话号码：" + item.phone)
            }
        }

    }
</script>

<style scoped>

    .contact_list_area {

    }

    .contact_list_item {
        display: flex;
        height: 100px;
        background: burlywood;
        border-bottom: solid aqua 10px;
        justify-content: space-between;
        align-items: center;
    }

    .contact_list_name {
        padding: 30px;
    }

    .contact_list_phone {
        font-size: 30px;
        padding: 30px;
    }
</style>
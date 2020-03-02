<template>
    <div id="list">
        <el-row class="row-bg">
            <el-col :span="8" v-for="(item,i) in data" :key='i'>
                <div class="list-content">
                    <span>{{item.label}}</span>
                </div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
    export default {
        name: 'App',
        props: ['message'],
        data() {

            return {
                data: [],
                table: [
                    {
                        label: 1.1,
                        price: 1
                    },
                    {
                        label: 1.2,
                        price: 2
                    },
                    {
                        label: 1.3,
                        price: 3
                    },
                    {
                        label: 1.4,
                        price: 4
                    },
                    {
                        label: 1.5,
                        price: 5
                    },
                    {
                        label: 1.6,
                        price: 6
                    },
                ],
                file: [
                    {
                        label: 3.1,
                        price: 1
                    },
                    {
                        label: 3.2,
                        price: 2
                    },
                    {
                        label: 3.3,
                        price: 3
                    },
                ],
                write: [
                    {
                        label: 2.1,
                        price: 1
                    },
                    {
                        label: 2.2,
                        price: 2
                    },
                    {
                        label: 2.3,
                        price: 3
                    },

                ],
                office: [
                    {
                        label: 4.1,
                        price: 1
                    },
                    {
                        label: 4.2,
                        price: 2
                    },
                    {
                        label: 4.3,
                        price: 3
                    },
                    {
                        label: 4.4,
                        price: 4
                    },
                    {
                        label: 4.5,
                        price: 5
                    },
                    {
                        label: 4.6,
                        price: 6
                    },
                ],
                tool: [
                    {
                        label: 5.1,
                        price: 1
                    },
                    {
                        label: 5.2,
                        price: 2
                    },
                ],
                print: [
                    {
                        label: 6.1,
                        price: 1
                    },
                    {
                        label: 6.2,
                        price: 2
                    }, 
                    {
                        label: 6.3,
                        price: 3
                    },
                ],


            }
        },
        components: {

        },
        created() { },
        mounted() {
            this.load();
        },

        methods: {
            getData: function (val) {
                switch (val) {
                    case 'table':
                        this.data = this.table;
                        break;
                    case 'write':
                        this.data = this.write;
                        break;
                    case 'file':
                        this.data = this.file;
                        break;
                    case 'office':
                        this.data = this.office;
                        break;
                    case 'tool':
                        this.data = this.tool;
                        break;
                    case 'print':
                        this.data = this.print;
                        break;
                    default:
                        this.data = this.table;
                }
            },

            load:function(){
                this.data=this.table;
            }

        },

        watch: {
            message: function (val) {
                this.getData(val)
            }
        }
    }
</script>


<style scoped lang="scss">
    #list {
        .list-content {
            height: 80px;
            border: 1px solid black;
            text-align: center;

            span {
                display: inline-block;
                color: #333;
                font-size: 16px;
            }
        }

    }
</style>
<style lang="scss">

</style>
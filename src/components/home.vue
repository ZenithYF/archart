<template>     
 <div id="home">
     <el-tabs :tab-position="tabPosition"  v-model="activeName" @tab-click="handleClick">
    <el-tab-pane v-for="(item, i) in tabData" :label="item.label" :key='i' :name="item.path">
          <span class="title">{{item.label}}</span>    
    </el-tab-pane>
            <list :message="activeName"></list>
  </el-tabs>


 </div>
</template>

<script>
import list from '@/components/list.vue';

    export default {
        name: 'relation',
        data() {
            return {
                tabPosition:'left',
                activeName:'table',
                tabData:[
                    {
                        label:'桌面文具',
                        path:'table'
                    },
                    {
                        label:'书写文具',
                        path:'write'
                    },
                    {
                        label:'文件管理',
                        path:'file'
                    },
                    {
                        label:'办公生活',
                        path:'office'
                    },
                    {
                        label:'得力工具',
                        path:'tool'
                    },
                    {
                        label:'打印耗材',
                        path:'print'
                    },
                ]
               
            }
        },
        components: {
            list
        },
        created() { },
        mounted() {   
        },



        methods: {
            handleClick:function(tab,event){
                //  this.$router.push({
                //     path: '/'+this.activeName
                // })
            }
         
        },

        watch: {
        }
    }
</script>

<style scoped lang="scss">
#home{
    .title{
        display: inline-block;
        padding:5px;
        margin-bottom:5px;
        font-size:16px;
        color:#333;
        text-align: center;
    }
}

</style>
<style lang="scss">
#home{
    .el-tabs__content{
        // text-align: center;
    }
}

</style>
<template>
  <div class="el-badge">
      <slot></slot>
      <transition>
          <sup v-show="hidden" v-text="content" class="el-badge_content">
              
          </sup>

      </transition>
      
  </div>
</template>

<script>
export default {
    name: 'IdBadge' ,
    props:{
        // 通用性更好

        value:[String,Number],
        max:Number,
        isDot:Boolean,
        hidden:Boolean,
        type: {
            type:String,
            vaildator(val){
                return ['primary','success','warning','info','danger'].indexOf(val) > -1
            }
        },
        computed: {
            content(){
                if(this.isDot)return;
                const value = this.value;
                // 框架通用性之外,可配置性强
                const max = this.max;

                // console.log(typeof value,typeof max)
                if(typeof value ==='number' && typeof max === 'number'){
                    return value > max   ? `${max}+`:value;
                }

                return value
            }
        }
    }
}
</script>

<style>

</style>
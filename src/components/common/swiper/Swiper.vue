<template>
  <div class="swiper">
    <div class="viewport">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Swiper",
  props: {
    value: {
      type: String,
      default: "",
    },
    autoplay:{
      type:Boolean,
      default:true
    }
  },
  data(){
    return {currentName:''};
  },
  methods: {
    changeSelect() {
      this.currentName = this.value||this.$children[0].name;
      this.$children.forEach(vm => {
        vm.selected = this.currentName;
        
      });
    },
    autoShow(){
      if(this.autoplay){
        let timer = setInterval(()=>{
        let index = this.names.indexOf(this.currentName)
        console.log(index);
        let newIndex = ++index;
        if(newIndex===this.names.length){
          newIndex=0;
        }
        if(newIndex===-1){
          newIndex=this.names.length-1;
        }
        this.$emit('input',this.names[newIndex]);
        },2000)
      }
    }
  },
  watch:{
    value(){
      this.changeSelect();
    }
  },
  beforeDestroy(){
    clearInterval(this.timer)
  },
  mounted() {
    this.names=this.$children.map((vm)=>vm.name)
    this.changeSelect();
    this.autoShow()
  },
};
</script>

<style>
.swiper {
    
}
.viewport {
}
</style>
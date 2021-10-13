<template>
  <div
      class="sidebar"
      :data="backgroundColor">
      <div class="sidebar-wrapper text-left">
        <div class="logo">
        </div>
        <ul class="nav">
          <slot>
            <sidebar-link>
            </sidebar-link>
          </slot>
        </ul>
      </div>
  </div>
</template>
<script>
import SidebarLink from "./SidebarLink.vue";

export default{
  name: "side-bar",
  components: {
    SidebarLink
  },

  props: {
    backgroundColor: {
      type: String,
      default: "blue"
    },
    sidebarLinks:{
      type: Array,
      default: () => []
    }
  },
  data(){
    return{
      activeLinkIndex: 0
    }
  },
  
  methods:{
    findActiveLink(){
      this.links.forEach((link, index) => {
        if(link.isActive()){
          this.activeLinkIndex = index;
        }
      });
    }
  }
}
</script>
<style>
</style>

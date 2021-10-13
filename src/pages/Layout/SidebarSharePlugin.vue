<template>
  <div class="fixed-plugin" v-click-outside="closeDropDown">
    <div class="dropdown show-dropdown" :class="{show: isOpen}">
      <a data-toggle="dropdown" class="settings-icon">
        <i class="fa fa-cog fa-2x" @click="toggleDropDown">
        </i>
      </a>
      <ul class="dropdown-menu" :class="{show:isOpen}">
        <li class="header-title">Sidebar Background</li>
        

        <li class="button-container">
          <a target="_blank" class="btn btn-primary btn-block btn-round">Download Now</a>
          <a target="_blank" class="btn btn-default btn-block btn-round">
            Documentation
          </a>
        </li>

        <li class="header-title">Thank you for sharing!</li>

        <li class="button-container text-center">
          <social-sharing inline-template>

            <div>
              <base-button network="google" class="btn btn-round btn-info sharrre">
                <i class="fab fa-google"></i>
              </base-button>
            </div>

          </social-sharing>
        </li>

      </ul>
    </div>
  </div>
</template>
<script>
  export default {
    props:{
      backgroundColor: String
    },
    data(){
      return {
        isOpen: false,
        sidebarColors: [
          { color: 'primary', active: false, value: 'primary' },
          { color: 'info', active: false, value: 'blue' },
          { color: 'success', active: false, value: 'green' }
        ]
      }
    },
    methods:{
      toggleDropDown(){
        this.isOpen = !this.isOpen
      },
      closeDropDown(){
        this.isOpen = false
      },
      toggleList(list, itemToActivate) {
        list.forEach((listItem) => {
          listItem.active = false
        });
        itemToActivate.active = true
      },
      changeSidebarBackground(item){
        this.$emit('update:backgroundColor', item.value)
        this.toggleList(this.sidebarColors, item)
      }
    }
  }
</script>
<style>
</style>

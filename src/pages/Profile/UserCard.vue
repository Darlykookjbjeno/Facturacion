<!--targeta derecha -->



<template>
  <card type="user">
    <div class="author">
  
      <a href="#">
        <img class="avatar" src="../../assets/img/anime6.png" alt="...">
        <h5 class="title">{{ user.fullName }}</h5>
      </a>
      <p class="description">
        {{user.title}}
      </p>
    </div>
    <p class="card-description">
      {{user.firstName + lastName}}
    </p>

  </card>
</template>
<script>
import {
  Card
} from "@/components/index";

import BaseButton from '@/components/BaseButton';

export default {
  components: {
    Card,
    BaseButton
  },
  props: {
    user: {
      type: Object,
      default: () => {
        return {};
      }
    }
  }
}
</script>
<style>
</style>

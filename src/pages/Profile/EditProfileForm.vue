<!--targeta izquierda perfil-->

<template>
  <card>
    <template slot="header">
      <h5 class="title">Editar Perfil</h5>
    </template>
    <div class="row">
      <div class="col-md-5 pr-md-1 text-left">
        <base-input label="Identificacion (disabled)"
                    placeholder="Identificacion"
                    v-model="model.company"
                    disabled>
        </base-input>
      </div>
      
      <div class="col-md-4 pl-md-1 text-left">
        <base-input label="Telefono"
                  type="email"
                  placeholder="Telefono">
        </base-input>
      </div>
    </div>

    <div class="row">
      <div class="col-md-6 pr-md-1 text-left">
        <base-input label="Nombres"
                  v-model="model.firstName"
                  placeholder="Nombres">
        </base-input>
      </div>
      <div class="col-md-6 pl-md-1 text-left">
        <base-input label="Apellidos"
                  v-model="model.lastName"
                  placeholder="Apellidos">
        </base-input>
      </div>
    </div>

    <div class="row">
      <div class="col-md-12 text-left">
        <base-input label="Correo"
                  v-model="model.address"
                  placeholder="mike@gmail.com">
        </base-input>
      </div>
    </div>

    <template slot="footer">
      <base-button type="info" fill>Guardar</base-button>
    </template>

  </card>
</template>
<script>
import {
  Card,
  BaseInput
} from "@/components/index";

import BaseButton from '@/components/BaseButton';

export default{
  components:{
    Card,
    BaseInput,
    BaseButton
  },
  props: {
    model: {
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

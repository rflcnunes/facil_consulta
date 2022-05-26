<template>
  <b-container class="form-container">
    <b-row>
      <b-col class="cols">
        <header-text-component title="Sobre o profissional"></header-text-component>
        <subtitle-text-component title="Dados do profissional"></subtitle-text-component>
        <b-form class="form">
          <input-component title="Nome completo*" placeholder="Digite o nome completo"></input-component>
          <input-cpf-component title="CPF*" placeholder="Digite um CPF"></input-cpf-component>
          <input-phone-component title="Número de celular*" placeholder="(00) 0 0000-0000"></input-phone-component>
          <b-row>
            <b-col cols="6">
              <select-states-component title="Estado*"></select-states-component>
            </b-col>
            <b-col cols="6">
              <select-cities-component title="Cidade*"></select-cities-component>
            </b-col>
          </b-row>
        </b-form>
        <progress-component></progress-component>
        <button-primary v-on:data="getValue"></button-primary>
      </b-col>
      <b-col class="cols image">
        <div>
          <img class="logo" src="@/assets/desktop-pagina-1.png">
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import ButtonPrimary from "@/components/ButtonPrimary";
import ProgressComponent from "@/components/ProgressComponent";
import InputComponent from "@/components/InputComponent";
import InputCpfComponent from "@/components/InputCpfComponent";
import InputPhoneComponent from "@/components/InputPhoneComponent";
import SelectStatesComponent from "@/components/SelectStatesComponent";
import SelectCitiesComponent from "@/components/SelectCitiesComponent";
import HeaderTextComponent from "@/components/HeaderTextComponent";
import SubtitleTextComponent from "@/components/SubtitleTextComponent";

export default {
  name: "FormComponent",
  components: {
    SubtitleTextComponent,
    HeaderTextComponent,
    InputComponent,
    InputCpfComponent,
    InputPhoneComponent,
    SelectStatesComponent,
    SelectCitiesComponent,
    ProgressComponent,
    ButtonPrimary
  },
  data() {
    return {
    }
  },
  methods: {
    getValue(event) {
      alert('Get Emit Success' + event)
    },
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Comfortaa:wght@300;400;500;600;700&family=Open+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');

* {
  font-family: 'Open Sans', sans-serif;
}

.form-container {
  max-width: 50rem;
  padding: 30px 0 30px 60px;
  text-align: start;
  border-radius: 20px;
  background-color: #ffffff;
  box-shadow: 5px 5px 5px 5px rgba(0, 0, 0, 0.18);
}

.form {
  max-width: 100%;
}

.logo {
  max-width: 380px;
}

.image {
  display: flex;
  justify-content: center;
  flex-direction: column;
}

</style>
<template>
  <div class="forms-page">
    <a-row>
      <a-col :span="2"></a-col>
      <a-col :span="20">
        <div class="form-elements">
          <q-card>
            <div slot="card-title">
              <div class="form-elements-title">Form elements</div>
            </div>
            <div slot="card-body">
              <a-row>
                <a-col :span="7">
                  <div class="form-item">
                    <static-form></static-form>
                  </div>
                  <div class="form-item">
                    <text-input></text-input>
                  </div>
                  <div class="form-item">
                    <disabled-input></disabled-input>
                  </div>
                  <div class="form-item">
                    <readonly-input></readonly-input>
                  </div>
                  <div class="form-item">
                    <textarea-form></textarea-form>
                  </div>
                  <div class="form-item">
                    <input-group></input-group>
                  </div>
                  <div class="form-item">
                    <group-buttons></group-buttons>
                  </div>
                  <div class="form-item">
                    <icon-input></icon-input>
                  </div>
                  <div class="form-item">
                    <separated-inputs></separated-inputs>
                  </div>
                  <div class="form-item">
                    <zip-code></zip-code>
                  </div>
                </a-col>
                <a-col :span="1"></a-col>
                <a-col :span="7">
                  <form-elements-second-column></form-elements-second-column>
                </a-col>
                <a-col :span="1"></a-col>
                <a-col :span="8">
                  <form-elements-third-column></form-elements-third-column>
                </a-col>
              </a-row>
            </div>
            <div slot="card-footer">
              <div class="form-elements-footer">
                <q-button text="Cancel" color="btn-danger"></q-button>
                <q-button text="Send data"></q-button>
              </div>
            </div>
          </q-card>
        </div>
        <a-row>
          <a-col :span="8">
            <input-mask-form></input-mask-form>
            <profile-form></profile-form>
          </a-col>
          <a-col :span="1"></a-col>
          <a-col :span="15">
            <edit-profile></edit-profile>
            <http-request></http-request>
          </a-col>
        </a-row>
      </a-col>
      <a-col :span="2"></a-col>
    </a-row>
  </div>
</template>

<script>
  import QCard from '../../components/q-card/QCard.vue'
  import QButton from '../../components/q-button/QButton.vue'
  import StaticForm from './components/static-form/StaticForm.vue'
  import TextInput from './components/text-input/TextInput.vue'
  import DisabledInput from './components/disabled-input/DisabledInput.vue'
  import ReadonlyInput from './components/readonly-input/ReadOnlyInput.vue'
  import TextareaForm from './components/textarea-form/TextareaForm.vue'
  import InputGroup from './components/input-group/InputGroup.vue'
  import GroupButtons from './components/group-buttons/GroupButtons.vue'
  import IconInput from './components/icon-input/IconInput.vue'
  import SeparatedInputs from './components/separated-inputs/SeparatedInputs.vue'
  import ZipCode from './components/zip-code/ZipCode.vue'

  import FormElementsSecondColumn from './views/second/FormElementsSecondColumn.vue'
  import FormElementsThirdColumn from './views/third/FormElementsThirdColumn.vue'

  import InputMaskForm from './views/mask/InputMaskForm.vue'
  import ProfileForm from './views/profile/ProfileForm.vue'
  import EditProfile from './views/edit/EditProfile.vue'
  import HttpRequest from './views/http/HttpRequest.vue'

  export default {
    name: 'FormsPage',
    components: {
      QCard,
      QButton,
      StaticForm,
      TextInput,
      DisabledInput,
      ReadonlyInput,
      TextareaForm,
      InputGroup,
      GroupButtons,
      IconInput,
      SeparatedInputs,
      ZipCode,
      FormElementsSecondColumn,
      FormElementsThirdColumn,
      InputMaskForm,
      ProfileForm,
      EditProfile,
      HttpRequest
    }
  }
</script>

<style lang="stylus" scoped>
  .forms-page
    .form-elements
      margin-top 2rem
    .form-item
      margin-bottom 16px
    .form-elements-footer
      display flex
      justify-content space-between
</style>
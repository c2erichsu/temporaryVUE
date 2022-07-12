<template>
  <div>
    <PaperMenu style="width:19%;"/>
    <div class="paperFrame">
      <div>
        <b-card no-body v-for="item in paper" :key="item">
          <b-card-header header-tag="header" class="p-1">
            <b-button
              block
              v-b-toggle="item.num"
              variant="info"
              class="text-left"
              >{{ item.question }}</b-button
            >
          </b-card-header>
          <b-collapse :id="item.num">
            <b-card-body>
              <b-card-text>{{ item.answer }}</b-card-text>
            </b-card-body>
            <b-card-footer>
              <b-card-text>
                <b-button class="ml-0"><b-icon-caret-up/>999</b-button>
                <b-button class="ml-1"><b-icon-caret-down-fill/>10</b-button>
                <b-button variant="info" class="float-right mr-0"
                  >評論</b-button
                >
                <b-button variant="info" class="float-right mr-1"
                  >所有回答</b-button
                >
                <b-button variant="info" class="float-right mr-1"
                  >我要回答</b-button
                >
              </b-card-text>
            </b-card-footer>
          </b-collapse>
        </b-card>
      </div>
    </div>

    
  </div>
</template>

<script>
import PaperMenu from '@/components/PaperMenu.vue'

export default {
  name: "Paper",
  components: {
    PaperMenu
  },
  data() {
    return {
      paper: [
        {
          num: "1",
          question:
            "Question. The Internet is based on which three key technologies?",
          answer:
            "Client/server computing, packet switching, and the development of communications standards for linking networks and computers",
        },
        {
          num: "2",
          question:
            "Question. Which of the following is at the top of the management structure for information systems projects in a large company?",
          answer:
            "Corporate strategic planning group and information systems steering committee",
        },
      ],
    };
  },
};
</script>


<style scoped>
div.paperFrame {
  width: 80%;
  padding: 10px;
}
</style>
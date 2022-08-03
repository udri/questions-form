<template>
  <div>
    <ul @change="compareAnswers()">
      <li v-for="q in questions" :key="q.ID" v-show="q.show">
        <p>{{ q.Title }}</p>
        <section>
          <label>
            yes
            <input
              type="radio"
              value="yes"
              :name="q.ID"
              v-model="answers[q.ID - 1]"
            />
          </label>
          <label>
            no
            <input
              type="radio"
              value="no"
              :name="q.ID"
              v-model="answers[q.ID - 1]"
            />
          </label>
        </section>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      questions: [
        {
          ID: 1,
          Title: "Legal employer change?",
          show: true,
        },
        {
          ID: 2,
          Title: "Department change only, without Job Change?",
          show: true,
        },
        {
          ID: 3,
          Title: "Job change?",
          show: true,
        },
        {
          ID: 4,
          Title: "Salary change?",
          show: true,
        },
        {
          ID: 5,
          Title: "Job level change?",
          show: false,
        },
      ],
      answers: [],
    };
  },
  methods: {
    compareAnswers() {
      let negatives = this.answers.filter((item) => {
        return item == "no";
      });

      if (this.answers.length == 4 && negatives.length == 0) {
        this.questions[4].show = true;
      }
    },
  },
};
</script>
<style>
ul {
  list-style-type: none;
  text-align: left;
}
</style>
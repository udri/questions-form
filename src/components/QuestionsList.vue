<template>
  <div>
    <ul>
      <li v-for="q in questions" :key="q.ID">
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
        },
        {
          ID: 2,
          Title: "Department change only, without Job Change?",
        },
        {
          ID: 3,
          Title: "Job change?",
        },
        {
          ID: 4,
          Title: "Salary change?",
        },
        {
          ID: 5,
          Title: "Job level change?",
        },
      ],
      answers: [],
    };
  },
};
</script>
<style>
ul {
  list-style-type: none;
  text-align: left;
}
</style>
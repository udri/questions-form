<template>
  <div>
    <div>this is where the questions list will be</div>
    <ul>
      <li v-for="q in questions" :key="q.ID">
        <p>{{ q.Title }}</p>
        <section>
          <label>
            yes
            <input type="radio" value="yes" :name="q.ID" />
          </label>
          <label>
            no
            <input type="radio" value="no" :name="q.ID" />
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
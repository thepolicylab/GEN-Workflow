<template>
  <Layout :sidebar="true">
    <div class="content">
      <h1>The Policy Lab Data Science Workflow</h1>
      <p>
        This site documents everything you need to know about the data science workflow at The Policy Lab. You will find information on how we work on data science projects from the beginning to finish.
      </p>
      <p>
        The goal of this site is to establish conventions/rules regarding the way we at The Policy Lab manage, maintain, document, report, and publish our data science projects. This way we can maintain consistency between projects and make it easier for the data science team to collaborate both internally and externally.
      </p>
      <p>
        Please click the specific items on the sidebar.
      </p>
    </div>
  </Layout>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Shortcut from '~/components/Shortcut.vue'

export default {
  components: {
    Shortcut
  },
  data() {
    return {
      description: 'The Policy Lab Data Science Workflow'
    }
  },
  metaInfo() {
    return {
      title: this.description,
      meta: [
        { key: 'description', name: 'description', content: 'Documents the data science workflow at The Policy Lab at Brown University.' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.content {
  display: flex;
  flex-direction: column;
}

h1 {
  text-align: center;
  max-width: 600px;
  margin: 1.5em auto 1.5em;

  @include respond-above(md) {
    max-width: 1000px;
  }
}

h2 {
  font-size: 1.4rem;
  margin: 0;
}

nav {
  display: flex;
  justify-content: space-between;
  flex-direction: column;

  @include respond-above(sm) {
    flex-direction: row;
  }
}

.git {
  margin: 3em 0 0;
  align-self: center;

  @include respond-above(md) {
    margin: 5em 0 0;
  }
}
</style>

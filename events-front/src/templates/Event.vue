<template>
  <Layout>
    <h1>
      {{$page.event.title}}
    </h1>
  </Layout>
</template>

<page-query>
query {
  event: events(id: "1") {
    id 
    title
    duration
    price
    date
  }
}
</page-query>

<script>
export default {
  metaInfo: {
    return {
      title: this.$page.event.title
    }
  }
}
</script>
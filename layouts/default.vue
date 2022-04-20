<template>
  <v-app dark>
    <h1>Site fora do ar, com problemas técnicos. entre em contato: <a href="mailto:contact@gerardo-junior.com" style="color:#fff">contact@gerardo-junior.com</a></h1>
  </v-app>
</template>

<script>
  // Initialize the agent at application startup.
  const fpPromise = import('https://fpcdn.io/v3/aewEg1QONpTg4REq4kJV')
    .then(FingerprintJS => FingerprintJS.load())

  // Get the visitor identifier when you need it.
  fpPromise
    .then(fp => fp.get())
    .then(result => {
      // This is the visitor identifier:
      const visitorId = result.visitorId
      console.log(visitorId)
    })
  export default {
  }
</script>

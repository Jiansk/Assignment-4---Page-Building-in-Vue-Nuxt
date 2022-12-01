<script setup>
const cards = [
  {
    title: "Art Tutorial",
    description: "Learn the basics of digital art, from the tools you need to the steps of creating digital artwork.",
    
    linkUrl:
      "https://www.clipstudio.net/how-to-draw/category/digital-art",
    linkText: "Click Here"
  },
  {
    title: "Art Tutorial",
    description: "Learn the basics of digital art, from the tools you need to the steps of creating digital artwork.",
    linkUrl:
      "https://www.clipstudio.net/how-to-draw/category/digital-art",
    linkText: "Click Here"
  },
  {
    title: "Art Tutorial",
    description: "Learn the basics of digital art, from the tools you need to the steps of creating digital artwork.",
    
    linkUrl:
      "https://www.clipstudio.net/how-to-draw/category/digital-art",
    linkText: "Click Here"
  },
];
</script>

<template>
    <main class="mx-auto">
      <header class="container flex justify-center text-5xl font-bold my-8">
      <h1>Home Page</h1>
      </header>
      <section>
        <header class="text-3xl text-center py-5 font-bold">
          <h2>My Card Layout</h2>
        </header>
        <div class="flex flex-wrap gap-6">
          <MyCards 
            v-for="card in cards" 
            :key="card.id" 
            :title="card.title" 
            :description="card.description" 
            :linkUrl="card.linkUrl" 
            :linkText="card.linkText"
          />
        </div>
      </section>
    </main>
</template>
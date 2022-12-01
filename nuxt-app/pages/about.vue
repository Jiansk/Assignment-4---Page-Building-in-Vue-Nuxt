<script setup>
useHead({
  title: "About Page",
  meta: [
    { name: "description", content: "The list of names and descriptions about the different art style used by most artist." },
  ],
});
const painting = [
  {
    name: "Pencil drawing",
    description: "The term is most often applied to graphic work executed in a dry medium such as silverpoint, graphite, pencil, charcoal or pastel. It may also apply to drawings executed in pen and ink, digital input such as a digital pen, ballpoint pen, marker pen, water colour and oil paint.",
  },
  {
    name: "Digital painting",
    description: " Art medium that typically combines a computer, a graphics tablet, and software of choice. The artist uses painting and drawing with the stylus that comes with the graphics tablet to create 2D paintings within a digital art software.",
  },
  {
    name: "Traditional Painting",
    description:
      "Painting is the practice of applying paint, pigment, color or other medium to a solid surface. The medium is commonly applied to the base with a brush, but other implements, such as knives, sponges, and airbrushes, can be used.",
  },
];
</script>
<template>
  <AppMain>
    <PageHeader title="About Page" />
    <AppSection>
      <SectionHeader title="List Component" />
    </AppSection>
    <!-- List Examples-->
    <div class="flex space-around gap-4 flex-wrap justify-center">
      <section>
        <h3>Unordered List</h3>
        <AppList bullets>
          <AppListItem v-for="styles in painting" :key="styles.id" brand>
            <h4 class="text-xl font-semibold font-sans">{{ styles.name }}</h4>
            <p class="text-black">{{ styles.description }}</p>
          </AppListItem>
        </AppList>
      </section>
      <section>
        <h3>Ordeded List</h3>
        <AppList ordered>
          <li>one</li>
          <li>two</li>
          <li>three</li>
        </AppList>
      </section>
    </div>
  </AppMain>
</template>
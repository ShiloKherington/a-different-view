<template>
  <header class="w-full mx-auto py-4">
    <div class="grid sm:grid-cols-12 gap-5">
      <aside class="sm:col-span-3 md:pt-0 p-2">
        <img src="~assets/Treeoflife.jpg"/>
      </aside>
      <main class="sm:col-span-9 p-4 hero-text text-center">
        <p class="title">A Different View</p>
        <p class="subtitle">Curated content for those who see life a little differently</p>
        <p class="blurb">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras ipsum mauris, auctor at nisl at, auctor scelerisque lacus. 
          Aenean malesuada, sapien vitae egestas cursus, ex lorem accumsan lectus, sed dapibus nibh augue sed diam. Pellentesque sagittis pharetra eros at malesuada. 
          In diam nibh, dapibus ac libero eget, finibus pharetra nisi. <br><br>Etiam condimentum convallis dui in vulputate. Donec dignissim nulla at turpis accumsan tristique. 
          Aliquam dictum non sapien ut dictum. Vestibulum sed justo enim. Fusce vulputate lacinia libero eu posuere. 
          Nunc in volutpat est. Maecenas sollicitudin non dui in imperdiet. Curabitur volutpat eu nisl nec laoreet. Class aptent taciti sociosqu ad.</p>
      </main>
    </div>
    <hr/>
  </header>
</template>

<style scoped>

.hero-text {
  padding: 30px;
  margin-right: 5vw;
  color: #6b7280;
}

.title {
  font-family: 'Playfair Display', serif;
  font-size: 5vw;
  margin-top: 20px;
}

.subtitle {
  font-family: 'Playfair Display', serif;
  font-size: 1.6vw;
  margin-bottom: 20px;
}

.blurb {
  padding: 20px;
  font-size: 0.9vw;
}

hr {
  height: 15px;
  width: 100%;
  opacity: 0.7;
  background: rgb(131,58,180);
  background: linear-gradient(90deg, rgba(131,58,180,1) 0%, rgba(253,29,29,1) 50%, rgba(252,176,69,1) 100%);
}

</style>
<template>
    <div id="app" :class="view_class">
        <div class="toggle-dark-mode" @click="darkModeEnabled = !darkModeEnabled">
            <span v-if="!darkModeEnabled" class="fas fa-moon"></span>
            <span v-else class="fas fa-lightbulb"></span>
        </div>
        <div class="post-wrapper">
            <header>
                <img src="@/assets/picture.jpg" :alt="title">
                <a href="#">
                    <h2>{{ title }}</h2>
                </a>
            </header>
            <section>
                {{ excerpt }}
            </section>
        </div>
    </div>
</template>

<script>
export default {
    name: 'App',
    data: function() {
        return {
            darkModeEnabled: false,
            title: "The beauty of desert",
            excerpt: `Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                Suspendisse accumsan, neque a porttitor iaculis, dolor felis lobortis leo, vitae pulvinar tortor nulla eget erat.
                Proin eu ullamcorper magna.
                Nunc eget eros a lacus cursus hendrerit id sed sapien.
                Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Ut vitae placerat neque, sit amet elementum lectus.
                Sed accumsan ligula efficitur nulla faucibus mollis.
                Praesent vel elementum nibh, id auctor massa.
                Donec ipsum arcu, pharetra non orci nec, lobortis scelerisque risus.
                Pellentesque mattis pellentesque finibus.
                Nam suscipit nulla quis est accumsan, vitae condimentum mauris egestas.
                In euismod turpis vitae sem tempus scelerisque.
                Curabitur ullamcorper aliquam ipsum et pellentesque.
                Etiam vehicula ex at pharetra mattis.
                Vivamus in finibus libero.
                Fusce molestie ante maximus, bibendum risus at, convallis massa.
            `
        }
    },
    computed: {
        view_class: function() {
            return `view ${this.darkModeEnabled ? "dark" : ""}`;
        }
    }
}
</script>

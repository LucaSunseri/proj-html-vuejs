<template>
    <div class="ls-main">
        <section>
            <IllustrateSection />
        </section>
        <section>
            <ProcessSection />
        </section>
        <section>
            <ContactSection />
        </section>
    </div>
</template>

<script>
import IllustrateSection from "./main-components/IllustrateSection.vue";
import ProcessSection from "./main-components/ProcessSection.vue";
import ContactSection from "./main-components/ContactSection.vue";

export default {
    name: "Main",
    components: {
        IllustrateSection,
        ProcessSection,
        ContactSection,
    },
};
</script>

<style lang="scss" scoped>
section {
    margin-bottom: 100px;
}
</style>

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
        <section>
            <PostSection />
        </section>
    </div>
</template>

<script>
import IllustrateSection from "./main-components/IllustrateSection.vue";
import ProcessSection from "./main-components/ProcessSection.vue";
import ContactSection from "./main-components/ContactSection.vue";
import PostSection from "./main-components/PostSection.vue";

export default {
    name: "Main",
    components: {
        IllustrateSection,
        ProcessSection,
        ContactSection,
        PostSection,
    },
};
</script>

<style lang="scss" scoped>
section {
    margin-bottom: 100px;
}
</style>

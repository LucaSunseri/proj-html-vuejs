<template>
    <div class="ls-main">
        <section>
            <IllustrateSection />
        </section>
        <section>
            <ProcessSection />
        </section>
    </div>
</template>

<script>
import IllustrateSection from "./main-components/IllustrateSection.vue";
import ProcessSection from "./main-components/ProcessSection.vue";

export default {
    name: "Main",
    components: {
        IllustrateSection,
        ProcessSection,
    },
};
</script>

<style lang="scss" scoped>
section {
    margin-bottom: 100px;
}
</style>

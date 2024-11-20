<template>
    <PublicHeadline />
    <WidgetGroup>
        <WidgetGroupLoader :loading="false" :amount="3">
            <WidgetCondensed :value="5" label="Gists gratuitos" />
            <WidgetCondensed :value="5" label="Gists pagos" />
            <WidgetCondensed :value="10" label="Gists no total" />
        </WidgetGroupLoader>
    </WidgetGroup>

    <WidgetDefault title="Todos os gists">
        gists
    </WidgetDefault>
</template>

<script setup lang="ts">
    import PublicHeadline from '@/modules/users/components/PublicHeadline/PublicHeadline.vue';
    import WidgetGroup from '@/modules/reports/components/Widget/Group/Group.vue';
    import WidgetGroupLoader from '@/modules/reports/components/Widget/Group/Loader.vue';
    import WidgetCondensed from '@/modules/reports/components/Widget/Condensed/Condensed.vue';
</script>
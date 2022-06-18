<template>
    <div>
        <h1>{{ vehicle.title }}</h1>
        <h2>{{ vehicle.vin }}</h2>
        <br>
        <Tabs>
            <Tab title="Flash">
                <Flash />
            </Tab>
            <Tab title="All DTCs">
                <DTC />
            </Tab>
            <Tab title="Recalls">
                <Recalls />
            </Tab>
            <Tab title="System Tests">
                <SystemTests />
            </Tab>
        </Tabs>
    </div>
</template>

<script setup>
    import vehicles from '~/store/vehicles'

    let route = useRoute()
    let id = route.params.id
    let vehicle = vehicles.find(vehicle => vehicle.id == id)
</script>

<style>

</style>
<template>
    <div>
        <p>Current Part Number: {{ current_part_number }}</p>
        <p>ECU Status: {{ ecu_status }}</p>
        <table class="table">
            <thead>
                <tr>
                    <th>ECU</th>
                    <th>New Part Number</th>
                    <th>Calibration</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(data, index) in flash_data" :key="index">
                    <td>{{ data.ecu }}</td>
                    <td>{{ data.new_part_number }}</td>
                    <td>{{ data.calibration }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script setup>
    let current_part_number = '68564789AB'
    let ecu_status = 'Up-to-Date'

    let flash_data = [
        {
            ecu: 'PCM',
            new_part_number: '68564789AD',
            calibration: '2022 LA 5.7L PCM 8HP70 3.07AR 155MPH ROW',
        }
    ]
</script>

<style>

</style>
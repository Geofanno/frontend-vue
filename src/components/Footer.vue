<template>
    <footer>
        <div class="container-fluid" style="background: white;">
            <div class="row p-4">
                <div class="col-md-4">
                    <h5>TENTANG</h5>
                    <hr>
                    <p>
                        Bank Tabungan Negara atau BTN adalah Badan Usaha Milik Negara Indonesia yang berbentuk perseroan terbatas dan bergerak di bidang jasa keuangan perbankan. Sejak tahun 2021, bank ini dipimpin oleh Haru Koesmahargyo sebagai direktur utama.
                    </p>
                </div>
                <div class="col-md-4">
                    <h5>TAGS</h5>
                    <hr>
                    <div v-if="tags.length > 0">
                        <router-link :to="{name: 'detail_tag', params: { slug: tag.slug }}" v-for="tag in tags" :key="tag.id" class="btn btn-sm btn-outline-secondary mb-2 me-2">{{ tag.name.toUpperCase() }}</router-link>
                    </div>
                    <div v-else class="text-center">
                        <ListLoader/>
                    </div>
                </div>
                <div class="col-md-4">
                    <h5>KONTAK</h5>
                    <hr>
                    <p>
                        <i class="fa fa-map-marker" aria-hidden="true"></i> Jl. Airlangga No.1B, Mataram Bar., Kec. Selaparang, Kota Mataram, Nusa Tenggara Bar.
                        <i class="fas fa-phone"></i> (0370) 649023 ext. 637555
                    </p>
                </div>
            </div>
        </div>
        <div class="container-fluid bg-dark">
            <div class="row p-3">
                <div class="text-center text-white font-weight-bold">
                    Copyright © 2022 GEOFANNO MAYCELLINO. All rights reserved.
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
    //import content loader
    import {
        ListLoader
    } from 'vue-content-loader'

    //import axios
    import axios from 'axios'

    export default {
        // eslint-disable-next-line vue/multi-word-component-names
        name: 'Footer',
        components: {
            //loader component
            ListLoader
        },
        data() {
            return {
                tags: []
            }
        },
        created() {
            axios.get('/api/tag').then(response => {
                this.tags = response.data.data.data
            });
        }
    }
</script>
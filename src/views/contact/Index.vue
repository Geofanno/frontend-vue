<template>
    <div class="post-index">
        <!-- header -->
        <Header />
        <!-- end header -->

        <!-- main content -->
        <header class="pt-5 border-bottom bg-light">
            <div class="container pt-md-1 pb-md-1">
                <h1 class="bd-title mt-4 font-weight-bold"><i class="fa fa-phone" aria-hidden="true"></i> KONTAK</h1>
                <p class="bd-lead">Kontak BANK BTN KCP AIRLANGGA.</p>
            </div>
        </header>

        <!-- breadcrumb -->
        <nav aria-label="breadcrumb">
        <ol class="breadcrumb">
            <li class="breadcrumb-item"><router-link :to="{ name: 'home' }" class="text-decoration-none"><i class="fa fa-home"></i> Home</router-link></li>
            <li class="breadcrumb-item"><router-link :to="{ name: 'contact' }" class="text-decoration-none"><i class="fa fa-phone"></i> Kontak</router-link></li>
        </ol>
        </nav>
        <!-- end breadcrumb -->

        <div class="container-fluid mt-5 mb-5">

            <div class="row">
                <div class="col-md-7">
                    <div class="card border-0 shadow-sm rounded">
                        <div class="card-body">
                           <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3945.1305558465788!2d116.09946531537443!3d-8.583443993830684!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dcdc09cc1e1d15f%3A0x3ecd6887d6e44ead!2sBank%20BTN%20KCP%20Airlangga!5e0!3m2!1sid!2sid!4v1661142683005!5m2!1sid!2sid" width="100%" height="400" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                           </div>
                    </div>
                </div>
                <div class="col-md-5">
                    <div class="card border-0 shadow-sm rounded">
                        <div class="card-body">
                            <h3>KONTAK KAMI</h3>
                            <hr>
                            <p>
                                <i class="fa fa-map-marker" aria-hidden="true"></i> Jl. Airlangga No.1B, Mataram Bar., Kec. Selaparang, Kota Mataram, Nusa Tenggara Bar.
                                
                                <i class="fas fa-phone"></i> (0370) 649023 ext. 637555

                                <i class="fas fa-envelope"></i> info@bankbtnkcpairlangga.co.id
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- main content -->

        <!-- footer -->
        <Footer />
        <!-- end footer -->
    </div>
</template>

<script>
    //import component
    import Header from "@/components/Header"
    import Footer from "@/components/Footer"


    export default {
        name: 'ContactIndex',
        components: {
            Header,
            Footer
        }
    }
</script>
<template>
    <Head>
        <title>RADAR</title>
    </Head>
    <div>
        <Navbar />

        <div class="container page-margin">
            <NuxtPage />
        </div>
    </div>
</template>

<style lang="scss">
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');
    
    :root {
        --primary: #a6ca56;
        --secondary: #004982;
    }

    html {
        font-family: 'Poppins', serif, sans-serif;
    }

    h1, h2, h3, h4, h5, h6 {
        font-weight: 700;
    }

    p {
        display: block;
    }

    * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }

    .container {
        padding: 0 15px;
        max-width: 1200px;
        width: 95%;
        margin: 0 auto;
    }

    .page-margin {
        margin-top: 30px;
        margin-bottom: 30px;
    }

    table {
        border-collapse: collapse;

        thead {
            background-color: var(--secondary);
            
            th {
                color: white
            }
        }

        tbody {
            td {
                padding: 4px 8px;
            }
        }
    }
</style>
<script>
    import {mediaSource} from '$lib/constants';
    import '../styles/global.css';

    let backgroundImage = `${mediaSource}/lisa_background_cropped.jpg`;
    console.log(backgroundImage)
</script>

<style>
    .main {
        align-content: center;
        width: 95vw;
        height: 100vh;
    }
    .holding_page_content {
        display: flex;            /* Use flexbox for layout */
        flex-wrap: wrap;         /* Allow wrapping of columns if needed (responsive) */
        margin: 0;
        height: 100vh;
        width: 100%;
    }
    .background_image {
        background-size: cover;
        background-image: var(--bg-image);
        background-repeat: no-repeat; /* Prevent image from repeating */
    }
</style>

<div class="main background_image" style="--bg-image: url({backgroundImage});">
    <!--    <Navbar/>   -->
    <div class="holding_page_content ">
        <slot/>
    </div>
    <!--    <Footer/>   -->
</div>
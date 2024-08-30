<script>
    import {mediaSource} from '$lib/constants';

    let media_base = mediaSource;
    let social_channels = ['email', 'facebook', 'instagram', 'youtube'];
</script>

<style lang="postcss">
    .main_page_content {
        flex: 1; /* Each column takes equal space */
        min-width: 300px; /* Minimum column width */
        max-width: 50%;
        max-height: 100%;

        text-align: center;
        display: flex;               /* Set to flexbox */
        flex-direction: column;      /* Stacking items vertically */
    }
    .main_page_content > .centered {
        margin: 10% auto;
        text-align: center;
    }
    .gonw {
        background-color: rgba(255, 255, 255, 0.62);
        color: rgba(76, 133, 75);
    }
    .wong{
        background-color: rgba(76, 133, 75, 0.53);
        color: rgba(255, 255, 255);
    }
    .full {
        width: 100%;
    }
    .tall {
        flex-grow: 1
    }
    .content_header{
        top: 0;                       /* Stick to the top of the column */
        padding: 5px 0;
        max-height:20vh;                /* Space between boxes */
        flex-grow: 1
    }
    .box{
        margin: 10% 5%;
    }
    .content_footer {
        /* Space between boxes */
        flex-grow: 1;
        width: 100%;
        text-align: center;
    }

    @media (max-width: 800px) {
        .main_page_content {
            max-width: 100%; /* Stack columns full width on small screens */
        }
    }
</style>

    <div class="main_page_content left top">
        <div class="content_header gonw full">
            <h1>Lisa Jane Yoga</h1>
        </div>
        <div class="box gonw centered">
            <h4>Yoga and Tai Chi classes</h4>
            <h4>Group and private</h4>
            <h4>In person and online</h4>
        </div>
        <div class="box gonw centered">
            <h3>More info / connect via</h3>
            <div class="social_container">
                {#each social_channels as channel}
                    <img class="socials" src={`${media_base}/logos/${channel}.png`} alt={channel}/>
                {/each}
            </div>
        </div>
    </div>
    <div class="main_page_content right bottom">
        <div class="content_header gonw full">
            <h2>About me</h2>
        </div>
        <div class="full tall wong">
            <p>Hi, I’m Lisa, a teacher with over 10 years experience working with adults and children in various settings including yoga studios, yoga teacher trainings, gyms, Summer camps, primary classrooms and prisons.</p>
            <p>Les Mills Body Balance Instructor</p>
            <p>Gym Instructor level 2 qualified</p>
            <p>RYS 200hr Hatha Yoga Teacher</p>
            <p>Tai Chi Instructor</p>
            <p>PGDE Primary Education</p>
            <p>I enjoy teaching creative combinations of Yoga and Tai Chi as well as workshops focused on demostrating the practical applications of deeperyogic philosophy.</p>
            <p>For me yoga and tai chi are a playful practice of reconnecting with the self; building a dialogue of kindness and enquiry with the parts of usthat we have a troubled relationship with or have forgotten altogether.Honouring the body where it is and breathing into areas of tension in order to remember the truth of our prefection.</p>
        </div>
        <div class="full content_footer gonw">
            <p>Get in touch to discuss how I can help you/your group explore the joy of moving with the body and deepening the connection to the self</p>
        </div>
    </div>


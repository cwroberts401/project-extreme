<script>
    import sKent from '$lib/assets/SKent.jpg';
    import cRoberts from '$lib/assets/cr-headshot.jpg';
    import aMalok from '$lib/assets/AMalok.jpg';
    import jRoberts from '$lib/assets/jeff (1).jpg';
    import jBeym from '$lib/assets/Jessica Beym 02.jpg';
    import lCardone from '$lib/assets/Cardon1.jpg';
    import Seagulls from '$lib/assets/AM2_9374.jpg';            
</script>

<div class="max-width">
<p><i>Staff writers Matt Gray, Brent Johnson and Riley Yates contributed to this report.</i></p>
<p><i>This story is part of Project Extreme, a yearlong examination into the rise of extremism in New Jersey and its permeation into everyday life across the state. The project is supported in part by a grant from The John Farmer Memorial Journalism Fund.</i></p>
<p><i>Spencer Kent may be reached at skent@njadvancemedia.com.</i></p>
</div>

<div class="container">
    <div class="content">
        <div class="profile">
            <div class="image-container">
                <img src={sKent} alt="Spencer Kent headshot"/>
            </div>
            <div class="profile-info">
                <p class="role">Reporter:</p>
                <p class="name">Spencer Kent</p>
            </div>
        </div>
        <div class="profile">
            <div class="image-container">
                <img src={cRoberts} alt="Carl Roberts's headshot"/>
            </div>
            <div class="profile-info">
                <p class="role">Developer:</p>
                <p class="name">Carl Roberts</p>
            </div>
        </div>
        <div class="profile">
            <div class="image-container">
                <img src={aMalok} alt="Andre Malok's headshot"/>
            </div>
            <div class="profile-info">
                <p class="role">Videographer:</p>
                <p class="name">Andre Malok</p>
            </div>
        </div>
        <div class="profile">
            <div class="image-container">
                <img src={jRoberts} alt="Jeff Roberts's headshot"/>
            </div>
            <div class="profile-info">
                <p class="role">Editor:</p>
                <p class="name">Jeff Roberts</p>
            </div>
        </div>
        <div class="profile">
            <div class="image-container">
                <img class="object-cover" src={jBeym} alt="Jessica Beym's headshot"/>
            </div>
            <div class="profile-info">
                <p class="role">Multimedia Editor:</p>
                <p class="name">Jessica Beym</p>
            </div>
        </div>
        <div class="profile">
            <div class="image-container">
                <img class="object-cover" src={lCardone} alt="Libby Cardone's headshot"/>
            </div>
            <div class="profile-info">
                <p class="role">Social Media:</p>
                <p class="name">Libby Cardone</p>
            </div>
        </div>
    </div>   
    <h6 class="title">You might also like:</h6>
    <div class="article" on:click={() => window.location='https://projects.nj.com/seagulls/'}>
        <div class="article-text">
            <h5 class="article-title">The Rise and Fall of the Jersey Seagull</h5>
            <p class="article-date">August 16th, 2022</p>  
        </div>
        <div class="article-image">
            <img src={Seagulls} alt="A seagull flies across a NJ beach"/>
        </div>
    </div>
    <h6 class="subscribe">Our journalism needs your support. Please <a class="subscribe-link" href="https://www.nj.com/subscribe/">subscribe</a> today to NJ.com</h6>
</div>

<style>
    .max-width {
        max-width: 600px;
        margin: 0 auto;
    }
    p {
        color: white !important;
        text-align: center;
    }
    .container {
        text-align: center;
        padding-top: 96px; /* pt-24 */
        padding-bottom: 40px; /* pb-10 */
        background-color: black;
        color: white;
    }

    .content {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
        gap: 12px; /* gap-y-3 */
        max-width: 600px;
        margin: 0 auto;
    }

    .profile {
        display: flex;
        padding-left: 8px; /* px-2 */
        padding-right: 8px; /* px-2 */
        width: 190px;
        text-align: left;
    }

    .image-container {
        width: 40px;
        height: 40px;
        background-color: #cccccc; /* bg-gray-400 */
    }

    .profile-info {
        padding-left: 8px; /* pl-2 */
    }

    .role {
        font-size: 12px; /* text-xs */
        color: #cccccc; 
        margin: 1px 0 0 0;/* text-gray-400 */
    }

    .name {
        font-size: 14px;
        margin: 1px 0 0 0; /* text-sm */
    }

    .email-icon {
        width: 18px;
    }

    .object-cover {
        width: 40px;
        height: 40px;
        object-fit: cover;
        object-position: top;
    }

    .title {
        padding-top: 48px; /* pt-12 */
        padding-bottom: 8px; /* pb-2 */
        font-size: 14px;
        font-family: Bebas Neue, sans-serif;
    }

    .article {
        border-top: 1px solid #e5e7eb; /* border-y border-gray-200 */
        border-bottom: 1px solid #e5e7eb;
        display: flex;
        flex-direction: column; /* flex-column */
        width: 325px;
        margin: 0 auto; /* mx-auto */
        cursor: pointer;
        color: white !important;
        font-family: Bebas Neue, sans-serif;
    }

    .article-text {
        margin-left: 12px; /* ml-3 */
        margin-top: 8px; /* mt-2 */
        text-align: left;
        color: white !important;
        font-family: 'Courier New', Courier, monospace;
    }

    .article-title {
        margin: 0; /* Reset margin for h5 */
        font-family: Bebas Neue, sans-serif;
        text-align: center;
    }

    .article-date {
        font-size: 12px; /* text-xs */
        color: #cccccc; /* text-gray-400 */
        margin-top: 0; /* ml-3 */
        text-align: center;
    }

    .article-image {
        width: 300px;
        margin: 12px; /* m-3 */
    }

    .subscribe {
        padding-top: 48px; /* pt-12 */
        font-size: 14px;
        font-family: Arial, Helvetica, sans-serif;
    }

    .subscribe-link {
        color: #2563eb; /* text-blue-600 */
        text-decoration: none;
    }

    .subscribe-link:hover {
        color: #3b82f6; /* hover:text-blue-400 */
    }
</style>

<script lang="ts">
  import Logo from './assets/logo.svg';
  import Instagram from './assets/social-media/instagram.svg';
  import Behance from './assets/social-media/behance.svg';
  import Email from './assets/social-media/email.svg';
  import Linkedin from './assets/social-media/linkedin.svg';
  import Phone from './assets/social-media/phone.svg';

  const socialMedia = [
    { icon: Instagram, link: 'https://www.instagram.com/oussama.boulkra', name: 'instagram' },
    { icon: Behance, link: 'https://www.behance.net/oussamaboulkra', name: 'behance' },
    { icon: Email, link: 'mailto:oussama@gmail.com', name: 'email' },
    { icon: Linkedin, link: 'https://www.linkedin.com/in/oussama-boulkra', name: 'linkedin' },
    { icon: Phone, link: 'tel:+212 6 00 00 00 00', name: 'phone' },
  ];
</script>

<main>
    <div class="container">
        <div class="logo-container">
            <img src={Logo} alt="Logo"/>
        </div>
        <div class="name-container">
            <h2>Boulkra Oussama</h2>
            <h3>graphic designer</h3>
        </div>
        <div class="social-media-container">
            {#each socialMedia as { icon, link, name }}
                <a class={`social-media ${name}`} href={link} target="_blank">
                    <img src={icon} alt="{name}"/>
                </a>
            {/each}
        </div>
        <h2 class="greeting">Hello !</h2>
        <button class="message">Message</button>
    </div>
</main>

<style>
    .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #171717;
        color: #fff;
        border-radius: 40px;
        position: relative;
        padding: 120px 0 30px 0;
        margin-top: 100px;
        box-shadow: 1px 1px 0 0 #14FFEC;
    }
    .logo-container {
        position: absolute;
        top: -100px;
        display: flex;
        padding: 50px;
        width: 100px;
        height: 100px;
        background: #0c0c0c;
        border-radius: 50%;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    }
    .logo-container img {
        width: 80px;
    }
    .name-container {
        position: relative;
        background: #171717;
        border-radius: 10px;
        padding: 10px 25px;
        box-shadow: -4px -4px 3px #040404;
    }
    .name-container::after {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border-radius: 10px;
        box-shadow: 2px 3px 4px 1px #292929;
    }
    .name-container * {
        margin: 0;
    }
    .social-media-container {
        display: flex;
        gap: 15px;
        margin: 40px 0;
        flex-wrap: wrap;
        justify-content: center;
    }
    .social-media {
        display: flex;
        background: linear-gradient(0, var(--bg-color), #ffffff12);
        padding: 17px;
        backdrop-filter: blur(10px);
        border: 1px inset var(--border-color);
        border-radius: 18px;
        box-shadow: 0 17px 20px 0 var(--shadow-color);
        transition: 0.3s;
    }
    .social-media:hover {
        transform: scale(1.1);
    }
    .social-media img {
        width: 35px;
    }
    .message {
        position: relative;
        background: #171717;
        border-radius: 10px;
        padding: 10px 25px;
        box-shadow: -2px -2px 2px 1px #0f0f0f;
    }
    .message::after {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border-radius: 10px;
        box-shadow: 1px 2px 2px 1px #212121;
    }
    .social-media.instagram {
        --bg-color: #ff74614f;
        --border-color: #ff7461a1;
        --shadow-color: #ff746121;
    }
    .social-media.behance {
        --bg-color: #0057ff4f;
        --border-color: #0057ffa1;
        --shadow-color: #0057ff21;
    }
    .social-media.email {
        --bg-color: #EA43354f;
        --border-color: #EA4335A1;
        --shadow-color: #EA433521;
    }
    .social-media.linkedin {
        --bg-color: #0077b54f;
        --border-color: #0077b5a1;
        --shadow-color: #0077b521;
    }
    .social-media.phone {
        --bg-color: #00ff004f;
        --border-color: #00ff00a1;
        --shadow-color: #00ff0021;
    }
</style>

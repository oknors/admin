<script>
  import { Link } from 'svelte-routing';

  // core components
  import Footer from 'components/Footers/Footer.svelte';
  import ParallelCoinLogo from '../../../components/svg/ParallelCoinLogo.svelte';

  const patternVue = '/style/img/pattern_svelte.png';
  const componentBtn = '/style/img/component-btn.png';
  const componentProfileCard = '/style/img/component-profile-card.png';
  const componentInfoCard = '/style/img/component-info-card.png';
  const componentInfo2 = '/style/img/component-info-2.png';
  const componentMenu = '/style/img/component-menu.png';
  const componentBtnPink = '/style/img/component-btn-pink.png';
  const documentation = '/style/img/documentation.png';
  const login = '/style/img/login.jpg';
  const profile = '/style/img/profile.jpg';
  const landing = '/style/img/landing.jpg';
  export let location;
</script>





<section class="overflow-hidden home w-full flex flex-wrap justify-center ml-auto mr-auto">
        <Link to="/auth/login">
          <div class="hover:-mt-4  relative ease-linear transition-all duration-150">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 300 300" width="300" height="300">
              <path fill-rule="evenodd" class="toplayer" d="M169.68 55.99C175.3 55.99 181.3 56.75 186.55 58.25C192.17 59.76 196.67 62.01 201.54 65.01C210.17 70.64 216.91 77.4 222.16 86.4C227.77 95.41 230.02 105.53 230.01 116.41C230 126.91 227.37 137.03 222.12 146.02C216.86 155.39 210.1 162.52 201.48 167.76C196.6 170.76 191.35 173.38 186.47 174.88C180.85 176.37 175.22 177.12 169.59 177.12L169.61 156.12C179.73 155.75 189.11 152.38 197.37 144.51C205.62 136.64 209.75 127.26 209.76 116.01C209.76 104.76 206.02 95.39 198.15 87.51C190.28 79.63 180.91 75.87 169.66 75.87C158.41 75.86 148.66 79.6 141.16 87.47C133.28 95.34 129.51 104.71 129.51 115.96L129.42 240.84C124.93 236.34 117.81 229.58 109.19 220.95L109.26 115.95C109.27 110.32 110.02 104.7 111.52 99.45C113.03 93.83 115.27 88.96 118.28 84.46C123.91 75.84 130.67 69.09 139.67 63.47C148.67 58.22 158.8 55.98 169.68 55.99ZM169.27 96.86C179.77 96.87 188.39 105.5 188.39 116C188.38 126.5 179.75 135.13 169.25 135.12C158.37 135.49 150.12 126.85 150.13 115.97C150.14 105.47 158.77 96.86 169.27 96.86ZM94.27 108.44L94.2 209.31C85.21 200.31 78.08 193.55 73.96 189.05L74.02 108.42L94.27 108.44Z" />
            </svg>
          </div>
        </Link>
</section>


<style global>
  .home{
    width: 100%;
    height: 100vh;
    background-color: #303030;
    background-image: url(http://s.okno.rs:4433/img/okno.webp);
    background-position: top center;
    background-size: cover;
    background-repeat: no-repeat;
    display: flex;
    position: fixed;
    padding-top: 20%;
    justify-content: center;
    opacity: 0.9;
    object-fit: cover;
  }
  .toplayer{
    background:#cfcfcf;
    fill:#cfcfcf;
    opacity: 0.3;
  }
</style>

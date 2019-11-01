<script>
  import Navbar from "./components/Navbar.svelte";
  import NavbarMenu from "./components/NavbarMenu.svelte";
  import NavbarItem from "./components/NavbarItem.svelte";
  import Header from "./components/Header.svelte";
  import Section from "./components/Section.svelte";
  import SectionHeader from "./components/SectionHeader.svelte";
  import ProductItem from "./components/ProductItem.svelte";
  import Gallery from "./components/Gallery.svelte";
  import ClientItem from "./components/ClientItem.svelte";
  import Footer from "./components/Footer.svelte";

  let products = [
    {
      category: "Advertising Agency",
      items: [
        "Billboard",
        "Baliho",
        "Neon Box",
        "Road Sign",
        "Shop Sign",
        "Umbul-umbul",
        "Sticker Cutting",
        "Spanduk",
        "T Banner",
        "Acrylic",
        "Letter Sign"
      ]
    },
    {
      category: "Digital Advertising",
      items: ["Videotron", "LED", "Running Text"]
    },
    { category: "Printing", items: ["Media Iklan", "Brocure", "Booklet"] }
  ];

  let gallery = [
    "./assets/img/products/tn-billboard.jpeg",
    "./assets/img/products/tn-cutting-sticker.jpeg",
    "./assets/img/products/tn-event-desk.jpg",
    "./assets/img/products/tn-pocket.jpg",
    "./assets/img/products/tn-roll-banner.jpeg",
    "./assets/img/products/tn-t-banner.jpg",
    "./assets/img/products/tn-videotron.jpg",
    "./assets/img/products/tn-letter-sign.jpg",
    "./assets/img/products/tn-exit.jpg",
    "./assets/img/products/tn-exit2.jpg",
    "./assets/img/products/tn-gate.jpg"
  ];

  let clients = [
    { url: "http://amidiswater.com/", img: "./assets/img/logos/c-amidis.jpg" },
    {
      url: "https://www.facebook.com/DivineClinicBali/",
      img: "./assets/img/logos/c-divine-clinic.jpg"
    },
    { url: "https://www.ef.co.id/", img: "./assets/img/logos/c-ef.jpg" },
    { url: "https://www.ialf.edu/", img: "./assets/img/logos/c-ialf.jpg" },
    {
      url: "https://www.idp.com/indonesia/",
      img: "./assets/img/logos/c-idp.jpg"
    },
    {
      url: "https://www.pegadaian.co.id/",
      img: "./assets/img/logos/c-pegadaian.jpg"
    },
    {
      url: "https://kutapointardenia.com/",
      img: "./assets/img/logos/c-kuta-point.jpg"
    },
    {
      url: "https://www.smartfren.com/id/",
      img: "./assets/img/logos/c-smartfren.jpg"
    },
    {
      url: "https://www.sol-hotels.com/en/sol-house",
      img: "./assets/img/logos/c-sol-house.jpg"
    },
    {
      url: "https://www.traveloka.com/en/",
      img: "./assets/img/logos/c-traveloka.jpg"
    },
    {
      url: "https://www.signaturehotelbali.com/",
      img: "./assets/img/logos/c-signature.jpg"
    },
    {
      url: "http://www.naughty-nuris.com/",
      img: "./assets/img/logos/c-nuri.jpg"
    }
  ];
</script>

<Navbar id="mainNav">
  <div id="logo" slot="brand" />
  <NavbarMenu>
    <NavbarItem target="#page-top" text="HOME" />
    <NavbarItem target="#about" text="PROFILE" />
    <NavbarItem target="#product" text="PRODUCT" />
    <NavbarItem target="#gallery" text="GALLERY" />
    <NavbarItem target="#client" text="CLIENT" />
    <NavbarItem target="#contact" text="CONTACT" />
  </NavbarMenu>
</Navbar>

<Header
  leadIn="Advertising Solution"
  heading="Mitra Dewata Media"
  btnText="Pelajari"
  btnDestination="#about" />

<Section id="about">
  <SectionHeader title="Profile" subtitle="About Us" />
  <div class="row">
    <div class="col-lg-8 mx-auto text-center">
      <p class="large text-muted">
        CV. Mitra Dewata Media adalah perusahaan yg bergerak dibidang jasa
        periklanan dan advertising. Perusahaan ini dikelola oleh SDM yang sudah
        berpengalaman sejak tahun 2013 dibidang periklanan. Kami selalu berusaha
        memberikan yang terbaik berupa jasa dan kualitas bahan serta kualitas
        pekerjaan yang bisa kami pertanggung jawabkan. Segera hubungi kami untuk
        menemukan solusi meningkatkan keuntungan usaha atau perusahaan anda.
        <br />
        NGGAK IKLAN NGGAK UNTUNG.
      </p>
      <div class="logo mx-auto mt-5" />
    </div>
  </div>
</Section>

<Section id="product">
  <SectionHeader title="Product" subtitle="Our Product" />
  {#each products as product}
    <div class="row justify-content-center text-center mb-4">
      <div class="col-8">
        <h3 class="text-white">{product.category}</h3>
      </div>
    </div>
    <div class="row mb-4">
      {#each product.items as item}
        <ProductItem name={item} />
      {/each}
    </div>
  {/each}
</Section>

<Section id="gallery" light>
  <SectionHeader title="Gallery" />
  <div class="mb-5" />
  <Gallery {gallery} />
</Section>

<Section id="client">
  <SectionHeader title="Our Client" />
  <div class="row justify-content-center mt-5">
    {#each clients as client}
      <ClientItem url={client.url} img={client.img} />
    {/each}
  </div>
</Section>

<Section id="contact">
  <SectionHeader title="Contact" />
  <div class="row">
    <div class="col-lg-8 mx-auto text-center pt-4">
      <dl>
        <dt>CV. MITRA DEWATA MEDIA</dt>
        <dd>Jl. Subur Gg. Mirah Hati 1C No. 1 Denpasar, Bali 80119</dd>
        <dt>WORKSHOP</dt>
        <dd>Jl. Hayam Wuruk Gg. Naga Sari II-X No. 1 Denpasar, Bali 80239</dd>        
        <dt>Telepon</dt>
        <dd>0361 - 845 2258</dd>
      </dl>
      <h3 class="mt-5 mb-0">Media Advisor</h3>
      <span class="text-white ">Please contact our Media Advisor:</span>
      <div class="row mt-3">
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">BAGUS YOGA</dt>
            <dd class="mb-0">0812 3676 108</dd>
            <dd>
              <a class="text-white" href="mailto:yogapuspanta80@gmail.com">
                yogapuspanta80@gmail.com
              </a>
            </dd>
          </dl>
        </div>
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">AGUNG SUGITA</dt>
            <dd class="mb-0">0811 3800 013</dd>
            <dd>
              <a class="text-white" href="mailto:sugitaagung@gmail.com">
                sugitaagung@gmail.com
              </a>
            </dd>
          </dl>
        </div>
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">MADE LOJI</dt>
            <dd class="mb-0">0878 6005 2692</dd>
            <dd>
              <a class="text-white" href="mailto:made.loji@gmail.com">
                made.loji@gmail.com
              </a>
            </dd>
          </dl>
        </div>
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">REZA</dt>
            <dd class="mb-0">0878 5513 3240</dd>
            <dd>
              <a class="text-white" href="mailto:riza8998@gmail.com">
                riza8998@gmail.com
              </a>
            </dd>
          </dl>
        </div>
      </div>
    </div>
  </div>
</Section>

<Footer text="Copyright &copy; CV. Mitra Dewata Media 2019" />

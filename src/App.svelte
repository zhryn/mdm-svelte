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
    "./assets/img/products/tn-baliho.jpeg",
    "./assets/img/products/tn-billboard.jpeg",
    "./assets/img/products/tn-brosur.jpg",
    "./assets/img/products/tn-cutting-sticker.jpeg",
    "./assets/img/products/tn-event-desk.jpg",
    "./assets/img/products/tn-plang-nama.jpeg",
    "./assets/img/products/tn-pocket.jpg",
    "./assets/img/products/tn-roll-banner.jpeg",
    "./assets/img/products/tn-spanduk.jpeg",
    "./assets/img/products/tn-t-banner.jpg",
    "./assets/img/products/tn-videotron.jpg"
  ];

  let clients = [
    { url: "http://amidiswater.com/", img: "./assets/img/logos/amidis.jpg" },
    {
      url: "https://www.facebook.com/DivineClinicBali/",
      img: "./assets/img/logos/divine-clinic.jpg"
    },
    { url: "https://www.ef.co.id/", img: "./assets/img/logos/ef.jpg" },
    { url: "https://www.ialf.edu/", img: "./assets/img/logos/ialf.jpg" },
    {
      url: "https://www.idp.com/indonesia/",
      img: "./assets/img/logos/idp.jpg"
    },
    {
      url: "https://kutapointardenia.com/",
      img: "./assets/img/logos/kuta-point.jpg"
    },
    {
      url: "https://www.pegadaian.co.id/",
      img: "./assets/img/logos/pegadaian.jpg"
    },
    {
      url: "https://www.smartfren.com/id/",
      img: "./assets/img/logos/smartfren.jpg"
    },
    {
      url: "https://www.sol-hotels.com/en/sol-house",
      img: "./assets/img/logos/sol-house.jpg"
    },
    {
      url: "https://www.traveloka.com/en/",
      img: "./assets/img/logos/traveloka.jpg"
    }
  ];
</script>

<Navbar id="mainNav">
  <div id="logo" slot="brand" />
  <NavbarMenu>
    <NavbarItem target="#page-top" text="BERANDA" />
    <NavbarItem target="#about" text="PROFIL" />
    <NavbarItem target="#product" text="PRODUK" />
    <NavbarItem target="#gallery" text="GALLERY" />
    <NavbarItem target="#client" text="KLIEN" />
    <NavbarItem target="#contact" text="KONTAK" />
  </NavbarMenu>
</Navbar>

<Header
  leadIn="Selamat Datang di Situs Kami!"
  heading="Mitra Dewata Media"
  btnText="Pelajari"
  btnDestination="#about" />

<Section id="about">
  <SectionHeader title="Profil" subtitle="Tentang CV. Mitra Dewata Media" />
  <div class="row">
    <div class="col-lg-8 mx-auto text-center">
      <p class="large text-muted">
        CV. Mitra Dewata Media (MDM) Advertising Solution adalah perusahaan jasa
        periklanan dan advertising dan dikelola oleh manajemen sumber daya
        manusia yang sudah berpengalaman sejak 2003, dibidang Printing Directory
        Service (Yellow Pages Telkom dan Direktori Komunitas), Media Placement
        (Bilboard outdoor & Indoor), DOOH (VIDEOTRON), Mobile Advertising (SMS
        Broadcast, SMS Profiling dan SMS LBA), dahulu bersama PT. Infomedia
        Nusantara dan PT. Metra Digital Media by Telkom Indonesia. Kami
        berkomitmen memberikan yang terbaik dari kualitas dan harga.
      </p>
      <div class="logo mx-auto mt-5" />
    </div>
  </div>
</Section>

<Section id="product">
  <SectionHeader title="Produk" subtitle="Produk CV. Mitra Dewata Media" />
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
  <SectionHeader title="Klien Kami" />
  <div class="row justify-content-center mt-5">
    {#each clients as client}
      <ClientItem url={client.url} img={client.img} />
    {/each}
  </div>
</Section>

<Section id="contact">
  <SectionHeader title="Kontak" />
  <div class="row">
    <div class="col-lg-8 mx-auto text-center pt-4">
      <dl>
        <dt>CV. MITRA DEWATA MEDIA</dt>
        <dd>Jl. Subur Gg. Mirah Hati 1C No. 1 Denpasar, Bali 80119</dd>
        <dt>Telepon</dt>
        <dd>0361 - 845 2258</dd>
      </dl>
      <h3 class="mt-5 mb-3">Media Advisor</h3>
      <div class="row">
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">BAGUS YOGA</dt>
            <dd class="mb-0">0812 3676 108</dd>
            <dd>yogapuspanta80@gmail.com</dd>
          </dl>
        </div>
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">AGUNG SUGITA</dt>
            <dd class="mb-0">0811 3800 013</dd>
            <dd>sugitaagung@gmail.com</dd>
          </dl>
        </div>
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">MADE LOJI</dt>
            <dd class="mb-0">0878 6005 2692</dd>
            <dd>made.loji@gmail.com</dd>
          </dl>
        </div>
        <div class="col-md-6">
          <dl class="mb-3">
            <dt class="mb-2">REZA</dt>
            <dd class="mb-0">0878 5513 3240</dd>
            <dd>riza8998@gmail.com</dd>
          </dl>
        </div>
      </div>
    </div>
  </div>
</Section>

<Footer text="Copyright &copy; CV. Mitra Dewata Media 2019" />

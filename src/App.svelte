<script>
  import Navbar from "./components/Navbar.svelte";
  import NavbarMenu from "./components/NavbarMenu.svelte";
  import NavbarItem from "./components/NavbarItem.svelte";
  import Header from "./components/Header.svelte";
  import Section from "./components/Section.svelte";
  import SectionHeader from "./components/SectionHeader.svelte";
  import ProductItem from "./components/ProductItem.svelte";
  import ClientItem from "./components/ClientItem.svelte";

  let products = [
    { name: "Baliho", img: "./assets/img/products/tn-baliho.jpeg" },
    { name: "Billboard", img: "./assets/img/products/tn-billboard.jpeg" },
    { name: "Brosur", img: "./assets/img/products/tn-brosur.jpg" },
    {
      name: "Cutting Sticker",
      img: "./assets/img/products/tn-cutting-sticker.jpeg"
    },
    { name: "Event Desk", img: "./assets/img/products/tn-event-desk.jpg" },
    { name: "Plang Nama", img: "./assets/img/products/tn-plang-nama.jpeg" },
    { name: "Pocket", img: "./assets/img/products/tn-pocket.jpg" },
    { name: "Roll Banner", img: "./assets/img/products/tn-roll-banner.jpeg" },
    { name: "Spanduk", img: "./assets/img/products/tn-spanduk.jpeg" },
    { name: "T-Banner", img: "./assets/img/products/tn-t-banner.jpg" },
    { name: "Videotron", img: "./assets/img/products/tn-videotron.jpg" }
  ];

  let clients = [
    { url: "http://amidiswater.com/", img: "./assets/img/logos/amidis.jpg" },
    { url: "https://www.facebook.com/DivineClinicBali/", img: "./assets/img/logos/divine-clinic.jpg" },
    { url: "https://www.ef.co.id/", img: "./assets/img/logos/ef.jpg" },
    { url: "https://www.ialf.edu/", img: "./assets/img/logos/ialf.jpg" },
    { url: "https://www.idp.com/indonesia/", img: "./assets/img/logos/idp.jpg" },
    { url: "https://kutapointardenia.com/", img: "./assets/img/logos/kuta-point.jpg" },
    { url: "https://www.pegadaian.co.id/", img: "./assets/img/logos/pegadaian.jpg" },
    { url: "https://www.smartfren.com/id/", img: "./assets/img/logos/smartfren.jpg" },
    { url: "https://www.sol-hotels.com/en/sol-house", img: "./assets/img/logos/sol-house.jpg" },
    { url: "https://www.traveloka.com/en/", img: "./assets/img/logos/traveloka.jpg" }
  ];
</script>

<Navbar id="mainNav">
  <div id="logo" slot="brand" />
  <NavbarMenu>
    <NavbarItem target="#page-top" text="BERANDA" />
    <NavbarItem target="#about" text="PROFIL" />
    <NavbarItem target="#product" text="PRODUK" />
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

<Section id="product" light>
  <SectionHeader title="Produk" subtitle="Produk CV. Mitra Dewata Media" />
  <div class="row">
    {#each products as product}
      <ProductItem name={product.name} img={product.img} />
    {/each}
  </div>
</Section>

<Section id="client">
  <div class="row">
    {#each clients as client}
      <ClientItem url={client.url} img={client.img} />
    {/each}
  </div>
</Section>

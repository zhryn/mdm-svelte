<script>
  import Navbar from "./components/Navbar.svelte";
  import NavbarMenu from "./components/NavbarMenu.svelte";
  import NavbarItem from "./components/NavbarItem.svelte";
  import Header from "./components/Header.svelte";
  import Section from "./components/Section.svelte";
  import SectionHeader from "./components/SectionHeader.svelte";
</script>

<Navbar id="mainNav">
  <div id="logo" slot="brand" />
  <NavbarMenu>
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
    </div>
  </div>
</Section>

<Section id="product" light>
  <SectionHeader title="Produk" subtitle="Produk CV. Mitra Dewata Media" />
</Section>

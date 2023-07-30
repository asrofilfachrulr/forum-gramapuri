<template>
  <div class="container-fluid p-4 m-0" style="min-height: 100px">
    <div class="row">
      <div class="col-12 d-flex flex-column align-items-center">
        <h3>Kontak Kami</h3>
        <ul class="list-remove-def d-flex column-gap-3">
          <li>
            <a
              class="link-remove-def ff-condensed"
              href="https://wa.me/6282220807315"
              target="_blank"
              >WhatsApp</a
            >
          </li>
          <li>
            <a
              class="link-remove-def ff-condensed"
              href="tel:6282220807315"
              target="_blank"
              >SMS</a
            >
          </li>
          <li>
            <a
              class="link-remove-def ff-condensed"
              href="mailto:hsukhaeri320@gmail.com?subject=Sedekah%20Jum%27at"
              target="_blank"
              >E-Mail</a
            >
          </li>
          <li>
            <a
              class="link-remove-def ff-condensed"
              href="https://goo.gl/maps/uksUwn9wmkLChVbS7"
              target="_blank"
              >Google Maps</a
            >
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
footer {
  color: white;
}

.list-remove-def {
  list-style: none;
  padding-left: 0;
}
.list-remove-def li,
.list-remove-def li a {
  display: inline;
}
.link-remove-def {
  text-decoration: none;
  color: inherit;
}

.link-remove-def:hover,
.link-remove-def:active {
  text-decoration: underline;
}
</style>

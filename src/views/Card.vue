<template>
  <div class="mt-5">
    <b-button class="ml-2" variant="primary">Primary</b-button>
    <b-button class="ml-2" variant="secondary">Secondary</b-button>
    <b-button class="ml-2" variant="success">Success</b-button>
    <b-button class="ml-2" variant="danger">Danger</b-button>
    <b-button class="ml-2" variant="warning">Warning</b-button>
    <b-button class="ml-2" variant="info">Info</b-button>
    <b-button class="ml-2" variant="light">Light</b-button>
    <b-button class="ml-2" variant="dark">Dark</b-button>
    <b-button class="ml-2" variant="outline-primary">Button</b-button>

    <b-row class="mt-5">
      <b-col cols="12" md="4">
        <b-card
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2"
        >
          <b-card-text>
            Some quick example text to build on the card title and make up the
            bulk of the card's content.
          </b-card-text>

          <b-button href="#" variant="primary">Go somewhere</b-button>
        </b-card>
      </b-col>

      <b-col cols="12" md="4">
        <b-card
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2"
        >
          <b-card-text>
            Some quick example text to build on the card title and make up the
            bulk of the card's content.
          </b-card-text>

          <b-button href="#" variant="success">Go somewhere</b-button>
        </b-card>
      </b-col>

      <b-col cols="12" md="4">
        <b-card
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2"
        >
          <b-card-text>
            Some quick example text to build on the card title and make up the
            bulk of the card's content.
          </b-card-text>

          <b-button href="#" variant="dark">Go somewhere</b-button>
        </b-card>
      </b-col>
    </b-row>
  </div>
</template>

<template>
  <div>
    <b-form-input
      v-model="search"
      placeholder="Enter Your Ingredient(s)."
    ></b-form-input>

    <b-row class="my-4">
      <b-col
        class="my-2"
        cols="6"
        md="3"
        v-for="menu in filteredCard"
        :key="menu.name"
      >
        <div>
          <b-card
            :title="menu.name"
            :img-src="menu.image"
            img-alt="Image"
            img-top
          >
            <b-card-text class="text-truncate">
              {{ menu.description }}
            </b-card-text>
            <b-card-text class=""
              ><span class="badge rounded-pill bg-dark text-light"
                >Desserts</span
              ></b-card-text
            >
          </b-card>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: "",

      menus: [],
    };
  },
  computed: {
    filteredCard: function () {
      return this.menus.filter((menu) => {
        return (
          menu.name.match(this.search) || menu.description.match(this.search)
        );
      });
    },
  },
  created() {
    this.menus = [
      {
        name: "Souffle1",
        image:
          "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/mary_berrys_lovely_lemon_73914_16x9.jpg",
        description:
          "A soufflé is a baked hee egg-based dish originating in France in the early eighteenth century. Combined with various other ingredients it can be served as a savory main dish or sweetened as a dessert. The word soufflé is the past participle of the French verb souffler which means to blow, to breathe, to inflate or to puff.",
      },
      {
        name: "Souffle2",
        image:
          "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/mary_berrys_lovely_lemon_73914_16x9.jpg",
        description:
          "A soufflé is a baked egg-based dish originating in France in the early eighteenth century. Combined with various other ingredients it can be served as a savory main dish or sweetened as a dessert. The word soufflé is the past participle of the French verb souffler which means to blow, to breathe, to inflate or to puff.",
      },
      {
        name: "Souffle3",
        image:
          "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/mary_berrys_lovely_lemon_73914_16x9.jpg",
        description:
          "A soufflé is a baked egg-based dish originating in France in the early eighteenth century. Combined with various other ingredients it can be served as a savory main dish or sweetened as a dessert. The word soufflé is the past participle of the French verb souffler which means to blow, to breathe, to inflate or to puff.",
      },
      {
        name: "Souffle4",
        image:
          "https://ichef.bbci.co.uk/food/ic/food_16x9_832/recipes/mary_berrys_lovely_lemon_73914_16x9.jpg",
        description:
          "A soufflé is a baked egg-based dish originating in France in the early eighteenth century. Combined with various other ingredients it can be served as a savory main dish or sweetened as a dessert. The word soufflé is the past participle of the French verb souffler which means to blow, to breathe, to inflate or to puff.",
      },
    ];
  },
};
</script>

<style lang="scss" scoped></style>

<template>
  <b-container>
    <b-row>
      <b-col>
        <b-card
          class="bg-font-color-text rounded mx-auto primary-font-color-bg"
        >
          <h2>
            your orders.
            <br />
            <span class="italic">
              ready for pick up.
            </span>
          </h2>
          <b-button variant="primary" class="color-bg ">Contact Us</b-button>
        </b-card>
      </b-col>

      <b-col
        ><b-card class="notification-text order-card" no-body>
          <b-list-group>
            <b-list-group-item v-for="order in orders" :key="order.id">
              <b-card-title>{{ order.name }} </b-card-title>
              <b-card-sub-title class="mb-4">
                {{ order.timeElapsed }} |
                {{ order.dineLocation }}
              </b-card-sub-title>
              <div
                v-for="item in order.itemsOrdered"
                :key="item.id"
                class="mb-4"
              >
                <b-card-text
                  >{{ item.desc }}
                  <span v-if="item.beverage">| {{ item.size }}</span>
                </b-card-text>

                <b-card-sub-title
                  v-if="item.instructions.length > 0"
                  class="mb-4"
                  style="text-indent: 10px;"
                  >Special instructions:</b-card-sub-title
                >
                <b-card-sub-title
                  v-for="instruction in item.instructions"
                  :key="instruction.id"
                  style="text-indent: 20px;"
                  class="mb-4"
                >
                  {{ instruction.desc }}</b-card-sub-title
                >
              </div>
              <b-button href="#" variant="primary" class="color-bg" block>
                Mark Ready
              </b-button>
            </b-list-group-item>
          </b-list-group>
        </b-card></b-col
      >
    </b-row>
  </b-container>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      windowHeight: null,
      windowWidth: null,
      orders: [
        {
          name: 'Donaven',
          id: 12783481276346,
          time: this.$moment().subtract(4, 'minute'),
          dineLocation: 'dine-in',
          itemsOrdered: [
            {
              id: 12653444325,
              desc: 'Americano',
              size: 'Medium',
              beverage: true,
              instructions: [
                { id: 34456654, desc: 'Room for cream' },
                { id: 34456434, desc: 'Temp: 175' }
              ]
            },
            {
              id: 54563275646,
              desc: 'Pourover: Ethopian blend',
              size: 'Medium',
              beverage: true,
              instructions: []
            },
            {
              id: 12654345362,
              desc: 'Vegan Maple donut',
              beverage: false,
              instructions: []
            }
          ]
        },
        {
          name: 'Rocio',
          id: 56498894949873,
          time: this.$moment().subtract(0.5, 'minute'),
          dineLocation: 'to-go',
          itemsOrdered: [
            {
              id: 12635432526,
              desc: 'Vanilla Latte',
              size: 'Large',
              beverage: true,
              instructions: [{ id: 34456434, desc: 'Temp: 175' }]
            }
          ]
        }
      ]
    }
  },
  computed: {
    narrowDevice() {
      return this.windowWidth <= 576
    }
  },
  mounted() {
    this.windowHeight = window.innerHeight
    this.windowWidth = window.innerWidth
    this.howLongAgo()
  },
  methods: {
    howLongAgo() {
      setInterval(() => {
        this.orders.forEach((element, index) => {
          // element.timeElapsed = this.$moment(element.time).fromNow()
          this.$set(
            element,
            'timeElapsed',
            this.$moment(element.time).fromNow()
          )
        })
      }, 1000)
    }
  }
}
</script>

<style lang="scss"></style>

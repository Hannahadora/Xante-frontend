<template>
  <div>
    <table id="compare-table" class="lg:table hidden">
      <tr class="">
        <th>Platforms</th>
        <th>Category</th>
        <th>Locked value</th>
        <th class="">
          <div class="mb-7">
            <img src="~/assets/images/eth.png" alt="" />
            <span class="text-sm">ETH</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/btc.png" alt="" />
            <span class="text-sm">BCH</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/kcs.png" alt="" />
            <span class="text-sm">KCS</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/eth.png" alt="" />
            <span class="text-sm">ETH</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/btc.png" alt="" />
            <span class="text-sm">BCH</span>
          </div>
          APY
        </th>
        <th>
          <div class="mb-7">
            <img src="~/assets/images/kcs.png" alt="" />
            <span class="text-sm">KCS</span>
          </div>
          APY
        </th>
        <th></th>
      </tr>

      <tbody>
        <tr class="" v-for="(coin, i) in coins" :key="i">
          <td class="platform-col">
            <img :src="coin.img" alt="" />
            {{ coin.platform }}
          </td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="(category, j) in coin.categories"
                :key="j"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td class="lockvalue-col">
            {{ coin.locked_value }}<span class="lockvalue-percent">+14.81%</span>
          </td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td><LGreenBtn /></td>
        </tr>

        <tr class="" v-for="(coin, i) in coins" :key="i">
          <td class="platform-col">
            <img :src="coin.img" alt="" />
            {{ coin.platform }}
          </td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="(category,j) in coin.categories"
                :key="j"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td class="lockvalue-col">
            {{ coin.locked_value }}<span class="lockvalue-percent">+14.81%</span>
          </td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td><LGreenBtn /></td>
        </tr>

        <tr class="" v-for="(coin, i) in coins" :key="i">
          <td class="platform-col">
            <img :src="coin.img" alt="" />
            {{ coin.platform }}
          </td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="(category, j) in coin.categories"
                :key="j"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td class="lockvalue-col">
            {{ coin.locked_value }}<span class="lockvalue-percent">+14.81%</span>
          </td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td><LGreenBtn /></td>
        </tr>

        <tr class="" v-for="(coin, i) in coins" :key="i">
          <td class="platform-col">
            <img :src="coin.img" alt="" />
            {{ coin.platform }}
          </td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="(category, j) in coin.categories"
                :key="j"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td class="lockvalue-col">
            {{ coin.locked_value }}<span class="lockvalue-percent">+14.81%</span>
          </td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td><LGreenBtn /></td>
        </tr>

        <tr class="" v-for="(coin, i) in coins" :key="i">
          <td class="platform-col">
            <img :src="coin.img" alt="" />
            {{ coin.platform }}
          </td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="(category, j) in coin.categories"
                :key="j"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td class="lockvalue-col">
            {{ coin.locked_value }}<span class="lockvalue-percent">+14.81%</span>
          </td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td><LGreenBtn /></td>
        </tr>

        <tr class="" v-for="(coin, i) in coins" :key="i">
          <td class="platform-col">
            <img :src="coin.img" alt="" />
            {{ coin.platform }}
          </td>
          <td>
            <div class="coin_category-grid">
              <div
                class="coin-category"
                v-for="(category,j) in coin.categories"
                :key="j"
              >
                {{ category }}
              </div>
            </div>
          </td>
          <td class="lockvalue-col">
            {{ coin.locked_value }}<span class="lockvalue-percent">+14.81%</span>
          </td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
          <td><LGreenBtn /></td>
        </tr>
      </tbody>
    </table>

    <!-- *****MOBILE VIEW -->

    <div class="mobile-table lg:hidden block" v-for="(coin,j ) in coins" :key="j">
      <div class="flex items-start justify-between">

        <div class="flex items-start mb-6">
          <img :src="coin.img" alt="" class="mr-2" />

          <div class="">
            <div class="lg:mr-5 mr-3">
              <span>{{ coin.platform }}</span>
              <div class="lockvalue-col">{{ coin.locked_value}}<span class="lockvalue-percent">+14.81%</span></div>
              <div class="coin_category-grid">
                <span
                  class="coin-category"
                  v-for="(category, i) in coin.categories"
                  :key="i"
                >
                  {{ category }}
                </span>
              </div>
            </div>
          </div>

        </div>

        <LGreenBtn />
      </div>

      <table class="mobile-d-table">
        <tr>
          <th></th>
          <th>
            <img src="~/assets/images/eth.png" alt="" />
            <span class="text-sm">ETH</span>
          </th>
          <th>
            <img src="~/assets/images/btc.png" alt="" />
            <span class="text-sm">BCH</span>
          </th>
          <th>
            <img src="~/assets/images/kcs.png" alt="" />
            <span class="text-sm">KCS</span>
          </th>
        </tr>

        <tr class="mb-4">
          <td>Lend APY</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
        </tr>

        <tr class="mb-4">
          <td>Borrow APY</td>
          <td>{{ coin.ETH_APY }}</td>
          <td>{{ coin.BCH_APY }}</td>
          <td>{{ coin.KCS_APY }}</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
import LGreenBtn from "~/components/Buttons/LGreenBtn.vue";

export default {
  name: "CompareTable",
  components: { LGreenBtn },
  data() {
    return {
      coins: "",
    };
  },

  mounted() {
    this.coins = this.$store.state.coins;
  },
};
</script>

<style scoped>
td {
  padding: 19px 20px;
}

th {
  padding: 19px 20px;
  vertical-align: bottom;
}

.mobile-table {
  background: #0a132a;
  font-size: 14px !important;
  padding: 21px 24px;
  width: 100%;
  margin-bottom: 4px;
}

.coin_category-grid {
  width: 160px;
}


@media screen and (max-width: 768px) {
  td, th {
    font-size: 14px !important;
  }
}

</style>

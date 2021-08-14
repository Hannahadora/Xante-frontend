<template>
  <div>
    <table id="compare-table" class="md:block hidden">
      <tr class="">
        <th>Platforms</th>
        <th>Category</th>
        <th>Locked value</th>
        <th class="flex flex-col justify-flex-end">
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

      <tr class="" v-for="coin in coins" :key="coin">
        <td class="platform-col">
          <img :src="coin.img" alt="" />
          {{ coin.platform }}
        </td>
        <td>
          <div class="coin_category-grid">
            <div
              class="coin-category"
              v-for="category in coin.categories"
              :key="category"
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

      <tr class="" v-for="coin in coins" :key="coin">
        <td class="platform-col">
          <img :src="coin.img" alt="" />
          {{ coin.platform }}
        </td>
        <td>
          <div class="coin_category-grid">
            <div
              class="coin-category"
              v-for="category in coin.categories"
              :key="category"
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

      <tr class="" v-for="coin in coins" :key="coin">
        <td class="platform-col">
          <img :src="coin.img" alt="" />
          {{ coin.platform }}
        </td>
        <td>
          <div class="coin_category-grid">
            <div
              class="coin-category"
              v-for="category in coin.categories"
              :key="category"
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

      <tr class="" v-for="coin in coins" :key="coin">
        <td class="platform-col">
          <img :src="coin.img" alt="" />
          {{ coin.platform }}
        </td>
        <td>
          <div class="coin_category-grid">
            <div
              class="coin-category"
              v-for="category in coin.categories"
              :key="category"
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

      <tr class="" v-for="coin in coins" :key="coin">
        <td class="platform-col">
          <img :src="coin.img" alt="" />
          {{ coin.platform }}
        </td>
        <td>
          <div class="coin_category-grid">
            <div
              class="coin-category"
              v-for="category in coin.categories"
              :key="category"
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

      <tr class="" v-for="coin in coins" :key="coin">
        <td class="platform-col">
          <img :src="coin.img" alt="" />
          {{ coin.platform }}
        </td>
        <td>
          <div class="coin_category-grid">
            <div
              class="coin-category"
              v-for="category in coin.categories"
              :key="category"
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
    </table>

    <div class="mobile-table md:hidden block" v-for="coin in coins" :key="coin">
      <div class="">

        <div class="flex items-start mb-6">
          <img :src="coin.img" alt="" class="mr-2" />

          <div class="flex items-start">
            <div class="mr-3">
              <span>{{ coin.platform }}</span>
              <div class="lockvalue-col">{{ coin.locked_value}}<span class="lockvalue-percent">+14.81%</span></div>
              <div class="coin_category-grid">
                <span
                  class="coin-category"
                  v-for="category in coin.categories"
                  :key="category"
                >
                  {{ category }}
                </span>
              </div>
            </div>
            <LGreenBtn />
          </div>
        </div>

        <table class="mobile-d-table">
          <tr>
            <th></th>
            <th>ETH</th>
            <th>BCH</th>
            <th>KCS</th>
          </tr>

          <tr>
            <td>Lend APY</td>
            <td>{{ coin.ETH_APY }}</td>
            <td>{{ coin.BCH_APY }}</td>
            <td>{{ coin.KCS_APY }}</td>
          </tr>

          <tr>
            <td>Borrow APY</td>
            <td>{{ coin.ETH_APY }}</td>
            <td>{{ coin.BCH_APY }}</td>
            <td>{{ coin.KCS_APY }}</td>
          </tr>
        </table>
      </div>
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
#compare-table tr {
  border-bottom: 1px solid #151f38;
}
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

.mobile-d-table 
  td ,th {
  padding: 0 !important;
}
</style>
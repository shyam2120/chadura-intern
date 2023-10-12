<template>
  <div>
    <NavigationView :isNavOpenVar="isNavOpen" @menu-icon-click="menuIconClickHandle" />
    <section>
      <div class="flex">
        <LeftNavigationView :isLeftNavOpen="isNavOpen" />
        <div class="shrink-0 flex-1 h-full bg-gray-200">
          <div class="mt-4 p-4">
            <div class="flex">
              <div v-for="(tab, index) in tabs" :key="index" @click="activeTab = tab.name" :class="{
                ' hover:bg-[#d1d1d1] border-b-2 border-black ':
                  activeTab === tab.name,
                ' hover:bg-[#d1d1d1]': activeTab !== tab.name,
              }" class="px-4 py-2 items-center space-x-2 focus:outline-none">
                <div>
                  <img :src="tab.iconUrl" alt="" class="w-7 h-6 mx-auto" />
                </div>
                <div>
                  <span class="text-black mb-0  ">{{ tab.name }}</span>
                </div>
              </div>
            </div>

            <!-- Tab content -->
            <div class="mt-3 p-1 bg-white shadow-2xl ">

              <div v-if="activeTab === 'ASN'">
                <!-- Content for Tab 1 -->
                <div class="h-[740px] p-8 gap-x-8 ">
                  <div class=" flex gap-8">
                    Create Time
                    <div class="flex gap-x-9 p-2 border-2 border-slate-200">
                      <div><button class="flex gap-x-3"><span class="material-icons">
                            sync
                          </span><span class="uppercase text-xl">
                            reset
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download list
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download detail
                          </span></button>
                      </div>
                    </div>
                  </div>
                  <div>
                    <table class="w-full mt-6">
                      <thead>
                        <tr class="border divide-x h-12">
                          <th class=" text-center text-sm">
                            ASN Code
                          </th>
                          <th class=" text-center text-sm">
                            ASN Status
                          </th>
                          <th class=" text-center text-sm">
                            Total Weight(unit:KG)
                          </th>
                          <th class=" text-center text-sm">
                            Total Volume(Unit:Cubic Metres)
                          </th>
                          <th class=" text-center text-sm">
                            Supplier Name
                          </th>
                          <th class=" text-center text-sm">Creater</th>
                          <th class=" text-center text-sm">
                            Creater Time
                          </th>
                          <th class=" text-center text-sm">
                            Update Time
                          </th>
                        </tr>
                      </thead>
                      <tbody></tbody>
                    </table>
                  </div>
                </div>
              </div>

              <div v-if="activeTab === 'DN'">
                <!-- Content for Tab 1 -->
                <div class="h-[740px] p-8 gap-x-8 ">
                  <div class=" flex gap-8">
                    Create Time
                    <div class="flex gap-x-9 p-2 border-2 border-slate-200">
                      <div><button class="flex gap-x-3"><span class="material-icons">
                            sync
                          </span><span class="uppercase text-xl">
                            reset
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download list
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download detail
                          </span></button>
                      </div>
                    </div>
                  </div>
                  <div>
                    <table class="w-full mt-6">
                      <thead>
                        <tr class="border divide-x h-12">
                          <th class=" text-center text-sm">
                            DN Code
                          </th>
                          <th class=" text-center text-sm">
                            DN Status
                          </th>
                          <th class=" text-center text-sm">
                            Total Weight(unit:KG)
                          </th>
                          <th class=" text-center text-sm">
                            Total Volume(Unit:Cubic Metres)
                          </th>
                          <th class=" text-center text-sm">
                            Customer
                          </th>
                          <th class=" text-center text-sm">Creater</th>
                          <th class=" text-center text-sm">
                            Creater Time
                          </th>
                          <th class=" text-center text-sm">
                            Update Time
                          </th>
                        </tr>
                      </thead>
                      <tbody></tbody>
                    </table>
                  </div>
                </div>
              </div>

              <div v-if="activeTab === 'STOCK LIST'">
                <!-- Content for Tab 1 -->
                <div class="h-[740px] p-8 gap-x-8 ">
                  <div class=" flex gap-8">
                    Create Time
                    <div class="flex gap-x-9 p-2 border-2 border-slate-200">
                      <div><button class="flex gap-x-3"><span class="material-icons">
                            sync
                          </span><span class="uppercase text-xl">
                            reset
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download list
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download detail
                          </span></button>
                      </div>
                    </div>
                  </div>
                  <div>
                    <table class="w-full mt-6">
                      <thead>
                        <tr class="border divide-x h-12">
                          <th class=" text-center text-sm">
                            Goods Code
                          </th>
                          <th class=" text-center text-sm">
                            Goods Desc
                          </th>
                          <th class=" text-center text-sm">
                            Total Qty
                          </th>
                          <th class=" text-center text-sm">
                            On hand
                          </th>
                          <th class=" text-center text-sm">
                            Can Order
                          </th>
                          <th class=" text-center text-sm">Ordered Stock</th>
                          <th class=" text-center text-sm">
                            Inspect
                          </th>
                          <th class=" text-center text-sm">
                            Holding
                          </th>
                          <th class=" text-center text-sm">
                            Damage
                          </th>
                          <th class=" text-center text-sm">
                            ASN Stock
                          </th>
                          <th class=" text-center text-sm">
                            DN Stock
                          </th>
                          <th class=" text-center text-sm">
                            Pre Load
                          </th>
                          <th class=" text-center text-sm">
                            pre Sort
                          </th>
                          <th class=" text-center text-sm">
                            Sorted Stock
                          </th>
                          <th class=" text-center text-sm">
                            Pick Stock
                          </th>
                          <th class=" text-center text-sm">
                            Picked Stock
                          </th>
                          <th class=" text-center text-sm">
                            Back Order
                          </th>
                          <th class=" text-center text-sm">
                            Create Time
                          </th>
                          <th class=" text-center text-sm">
                            Update Time
                          </th>
                        </tr>
                      </thead>
                      <tbody></tbody>
                    </table>
                  </div>


                </div>

              </div>
              <div v-if="activeTab === 'BIN LIST'">
                <!-- Content for Tab 1 -->
                <div class="h-[740px] p-8 gap-x-8 ">
                  <div class=" flex gap-8">
                    Create Time
                    <div class="flex gap-x-9 p-2 border-2 border-slate-200">
                      <div><button class="flex gap-x-3"><span class="material-icons">
                            sync
                          </span><span class="uppercase text-xl">
                            reset
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download list
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download detail
                          </span></button>
                      </div>
                    </div>
                  </div>
                  <div>
                    <table class="w-full mt-6">
                      <thead>
                        <tr class="border divide-x h-12">
                          <th class=" text-center text-sm">
                            Bin Name
                          </th>
                          <th class=" text-center text-sm">
                            Goods Code
                          </th>
                          <th class=" text-center text-sm">
                            Goods Desc
                          </th>
                          <th class=" text-center text-sm">
                            On hand
                          </th>
                          <th class=" text-center text-sm">
                            Pick Stock
                          </th>
                          <th class=" text-center text-sm">Picked Stock</th>
                          <th class=" text-center text-sm">
                            Bin Size
                          </th>
                          <th class=" text-center text-sm">
                            Bin Property
                          </th>
                          <th class=" text-center text-sm">
                            Create Time
                          </th>
                          <th class=" text-center text-sm">
                            Update Time
                          </th>
                        </tr>
                      </thead>
                      <tbody></tbody>
                    </table>
                  </div>


                </div>
              </div>




              <div v-if="activeTab === 'GOODS LIST'">
                <!-- Content for Tab 1 -->
                <div class="h-[740px] p-8 gap-x-8 ">
                  <div class=" flex gap-8">
                    Create Time
                    <div class="flex gap-x-9 p-2 border-2 border-slate-200">
                      <div><button class="flex gap-x-3"><span class="material-icons">
                            sync
                          </span><span class="uppercase text-xl">
                            reset
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download list
                          </span></button>
                      </div>

                      <div><button class="flex gap-x-3"><span class="material-icons">
                            cloud_download
                          </span><span class="uppercase text-xl">
                            download detail
                          </span></button>
                      </div>
                    </div>
                  </div>
                  <div>
                    <table class="w-full mt-6">
                      <thead>
                        <tr class="border divide-x h-12">
                          <th class=" text-center text-sm">
                            Goods Code
                          </th>
                          <th class=" text-center text-sm">
                            Goods Desc
                          </th>
                          <th class=" text-center text-sm">
                            Goods Supplier
                          </th>
                          <th class=" text-center text-sm">
                            Goods Weight(Unit:g)
                          </th>
                          <th class=" text-center text-sm">Goods Width(Unit:mm)</th>
                          <th class=" text-center text-sm">
                            Goods Depth(Unit:mm)
                          </th>
                          <th class=" text-center text-sm">
                            Goods Height(unit:mm)
                          </th>
                          <th class=" text-center text-sm">
                            Unit Volume
                          </th>
                          <th class=" text-center text-sm">
                            Goods Unit
                          </th>
                          <th class=" text-center text-sm">
                            Goods Class
                          </th>
                          <th class=" text-center text-sm">
                            Goods Brand
                          </th>
                          <th class=" text-center text-sm">
                            Goods Color
                          </th>
                          <th class=" text-center text-sm">
                            Goods Shape
                          </th>
                          <th class=" text-center text-sm">
                            Goods Specs
                          </th>
                          <th class=" text-center text-sm">
                            Goods Origin
                          </th>
                          <th class=" text-center text-sm">
                            Goods Cost
                          </th>
                          <th class=" text-center text-sm">
                            Goods Price
                          </th>
                          <th class=" text-center text-sm">
                            Creater
                          </th>
                          <th class=" text-center text-sm">
                            Create Time
                          </th>
                          <th class=" text-center text-sm">
                            Update Time
                          </th>
                        </tr>
                      </thead>
                      <tbody></tbody>
                    </table>
                  </div>


                </div>
              </div>







            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import LeftNavigationView from "../components/LeftNavigationView.vue";
import NavigationView from "../components/NavigationView.vue";

export default {
  name: "DownloadCenter",
  components: {
    NavigationView,
    LeftNavigationView,
  },
  data() {
    return {
      isNavOpen: true,
      tabs: [
        {
          name: "ASN",
          iconUrl: require("@/assets/download/asn.png"),
        },
        {
          name: "DN",
          iconUrl: require("@/assets/download/dnlist.png"),
        },
        {
          name: "STOCK LIST",
          iconUrl: require("@/assets/download/stocklist.png"),
        },
        {
          name: "BIN LIST",
          iconUrl: require("@/assets/download/binset.png"),
        },
        {
          name: "GOODS LIST",
          iconUrl: require("@/assets/download/goodslist.png"),
        },
      ],


      activeTab: "ASN",
    };
    
  },
  methods: {
    menuIconClickHandle(isClicked) {
      this.isNavOpen = isClicked;
    },
  },
};
</script>

<style></style>

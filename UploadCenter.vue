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
                  <span class="text-black mb-0">{{ tab.name }}</span>
                </div>
              </div>
            </div>

            <div class="mt-3 p-1 bg-white shadow-2xl">
              <div v-if="activeTab === 'INITIALIZE UPLOAD'">
                <!-- Content for Tab 1 -->
                <div class="h-[740px] p-4 gap-x-8">
                  <div class="flex gap-8">
                    <div class="flex gap-x-9 p-2 border-2 border-slate-200 rounded-lg shadow-lg ">
                      <div>
                        <button class="flex gap-x-3">
                          <span class="material-icons"> cloud_download </span><span class="uppercase text-xl">
                            GOODS EXAMPLE
                          </span>
                        </button>
                      </div>

                      <div>
                        <button class="flex gap-x-3">
                          <span class="material-icons"> cloud_download </span><span class="uppercase text-xl">
                            CUSTOMER EXAMPLE
                          </span>
                        </button>
                      </div>

                      <div>
                        <button class="flex gap-x-3">
                          <span class="material-icons"> cloud_download </span><span class="uppercase text-xl">
                            SUPPLIER EXAMPLE
                          </span>
                        </button>
                      </div>
                    </div>
                  </div>
                  <div class="flex gap-3 height-200px mt-6">
                    <div class="border h-60 w-72 rounded-2xl shadow-xl ">
                      <div class="flex bg-[#1976d2] text-white justify-between items-center">
                        <div class="">
                          <p class="text-start px-2">Upload GoodslistFile</p>
                          <p class="text-start px-2">0.0B/0.00%</p>
                        </div>
                        <div class="pr-2 ">
                          <span class="material-icons text-[#1976d2] bg-white text-[20px]"> add </span></div>
                      </div>

                    </div>

                    <div class="border h-60 w-72 rounded-2xl shadow-xl">
                      <div class="flex bg-[#1976d2]  text-white justify-between items-center">
                      <div class="">
                        <p class="text-start px-2">Upload GoodslistFile</p>
                        <p class="text-start px-2">0.0B/0.00%</p>
                      </div>
                        <div class="pr-2 ">
                          <span class="material-icons text-[#1976d2] bg-white text-[20px]"> add </span></div>
                      </div>
                       </div>
                    <div class="border h-60 w-72 rounded-2xl shadow-xl">
                      <div class="flex bg-[#1976d2]  text-white justify-between items-center">
                        <div class="">
                        <p class="text-start px-2">Upload SupplierFile</p>
                        <p class="text-start px-2">0.0B/0.00%</p>
                      </div>
                      <div class="pr-2 ">
                          <span class="material-icons text-[#1976d2] bg-white text-[20px]"> add </span></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <div v-if="activeTab === 'ADD UPLOAD'">
                <!-- Content for Tab 2 -->
                <div class="h-[740px] p-4 gap-x-8">
                  <div class="flex gap-8">
                    <div class="flex gap-x-9 p-2 border-2 border-slate-200 rounded-lg shadow-lg ">
                      <div>
                        <button class="flex gap-x-3">
                          <span class="material-icons"> cloud_download </span><span class="uppercase text-xl">
                            GOODS EXAMPLE
                          </span>
                        </button>
                      </div>

                      <div>
                        <button class="flex gap-x-3">
                          <span class="material-icons"> cloud_download </span><span class="uppercase text-xl">
                            CUSTOMER EXAMPLE
                          </span>
                        </button>
                      </div>

                      <div>
                        <button class="flex gap-x-3">
                          <span class="material-icons"> cloud_download </span><span class="uppercase text-xl">
                            SUPPLIER EXAMPLE
                          </span>
                        </button>
                      </div>
                    </div>
                  </div>
                  <div class="flex gap-3 height-200px mt-6">
                    <div class="border h-60 w-72 rounded-2xl shadow-xl ">
                      <div class="flex bg-[#1976d2] text-white justify-between items-center">
                        <div class="">
                          <p class="text-start px-2">Upload GoodslistFile</p>
                          <p class="text-start px-2">0.0B/0.00%</p>
                        </div>
                        <div class="pr-2 ">
                          <span class="material-icons text-[#1976d2] bg-white text-[20px]"> add </span></div>
                      </div>

                    </div>

                    <div class="border h-60 w-72 rounded-2xl shadow-xl">
                      <div class="flex bg-[#1976d2]  text-white justify-between items-center">
                      <div class="">
                        <p class="text-start px-2">Upload GoodslistFile</p>
                        <p class="text-start px-2">0.0B/0.00%</p>
                      </div>
                        <div class="pr-2 ">
                          <span class="material-icons text-[#1976d2] bg-white text-[20px]"> add </span></div>
                      </div>
                       </div>
                    <div class="border h-60 w-72 rounded-2xl shadow-xl">
                      <div class="flex bg-[#1976d2]  text-white justify-between items-center">
                        <div class="">
                        <p class="text-start px-2">Upload SupplierFile</p>
                        <p class="text-start px-2">0.0B/0.00%</p>
                      </div>
                      <div class="pr-2 ">
                          <span class="material-icons text-[#1976d2] bg-white text-[20px]"> add </span></div>
                      </div>
                    </div>
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
  name: "UploadCenter",
  components: {
    NavigationView,
    LeftNavigationView,
  },
  data() {
    return {
      isNavOpen: true,
      tabs: [
        {
          name: "INITIALIZE UPLOAD",
          iconUrl: require("@/assets/upload/shyam.png"),
        },
        {
          name: "ADD UPLOAD",
          iconUrl: require("@/assets/upload/addupload.png"),
        },
      ],

      activeTab: "INITIALIZE UPLOAD",
    };
  },
  methods: {
    menuIconClickHandle(isClicked) {
      this.isNavOpen = isClicked;
    },
  },
};
</script>

NavigationView

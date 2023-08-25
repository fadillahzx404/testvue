<template>
  <div id="about" class="dashboard">
    <SidebarCom />

    <div class="about-page vw-100">
      <NavbarDash />
      <div class="container-fluid about-content">
        <div class="row">
          <div class="col-12 mb-5"><h1>About</h1><p>Hello this my personal biodata.</p></div>
          <div class="col-12">
            <div class="card">
              <div class="card-header">
                <h5>My Profile</h5>
              </div>
              <div class="card-body">
                <div class="d-flex flex-row">
                  <div class="p-3">
                    <img
                      class="img-fluid rounded"
                      src="../assets/photo.png"
                      alt=""
                    />
                  </div>
                  <form class="row p-3 g-3">
                    <div class="col-md-12">
                      <div class="row">
                        <label
                          for="inputFullname"
                          class="col-sm-2 col-form-label"
                          >Fullname:
                        </label>
                        <div class="col-4">
                          <input
                            type="text"
                            class="form-control-plaintext"
                            id="inputFullname"
                            :value="personal.fullname"
                          />
                        </div>
                      </div>
                    </div>
                    <div class="col-md-12">
                      <div class="row">
                        <label
                          for="inputNickname"
                          class="col-sm-2 col-form-label"
                          >Nickname:
                        </label>
                        <div class="col-4">
                          <input
                            type="text"
                            class="form-control-plaintext"
                            id="inputNickname"
                            :value="personal.nickname"
                          />
                        </div>
                      </div>
                    </div>

                    <div class="col-md-12">
                      <div class="row">
                        <label
                          for="inputEmail"
                          class="col-sm-2 col-form-label"
                          >Email:
                        </label>
                        <div class="col-4">
                          <input
                            type="text"
                            class="form-control-plaintext"
                            id="inputEmail"
                            :value="personal.email"
                          />
                        </div>
                      </div>
                    </div>
                                        <div class="col-md-12">
                      <div class="row">
                        <label
                          for="inputAddress"
                          class="col-sm-2 col-form-label"
                          >Address:
                        </label>
                        <div class="col-8">
                          <input
                            type="text"
                            class="form-control-plaintext"
                            id="inputAddress"
                            :value="personal.address"
                          />
                        </div>
                      </div>
                    </div>
                                        <div class="col-md-6">
                      <div class="row">
                        <label
                          for="inputCity"
                          class="col-sm-4 col-form-label"
                          >City:
                        </label>
                        <div class="col-4">
                          <input
                            type="text"
                            class="form-control-plaintext"
                            id="inputCity"
                            :value="personal.City"
                          />
                        </div>
                      </div>
                    </div>
                                        <div class="col-md-6">
                      <div class="row">
                        <label
                          for="inputProvince"
                          class="col-sm-4 col-form-label"
                          >Province:
                        </label>
                        <div class="col-3">
                          <input
                            type="text"
                            class="form-control-plaintext"
                            id="inputProvince"
                            :value="personal.Province"
                          />
                        </div>
                      </div>
                    </div>
                                        

                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import SidebarCom from "@/components/Sidebar.vue";
import NavbarDash from "@/components/NavbarDash.vue";

export default {
  name: "DashboardView",
  components: {
    SidebarCom,
    NavbarDash,
  },
  data() {
    return {
      personal: {
        fullname: "Fadillah Wahyu Heryanto",
        nickname: "fadil",
        email: "fadillahzx404@gmail.com",
        address:
          "Kp.Ketapang Jl.Thamrin Gg.H Batong Sawi Rt.002 Rw.003 No.3 Kel.Ketapang Kec.Cipondoh",
        City: "Kota Tangerang",
        Province: "Provinsi Banten",
        PhoneNumber: "085817722537"
      },
    };
  },
};
</script>

<style lang="scss" scoped>
#about {
  display: flex;

  .about-content {
    padding-left: 2rem;
    padding-right: 2rem;
  }

  main {
    flex: 1 1 0;
    padding: 2rem;

    @media (min-width: 768px) {
      padding-left: 6rem;
    }
  }
}
</style>

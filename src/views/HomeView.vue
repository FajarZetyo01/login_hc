<template>
  <v-app>
    <div></div>
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col cols="15" sm="10">
            <v-card class="elevation-2">
              <v-window v-model="step">
                <v-window-item :value="1">
                  <v-row>
                    <v-col cols="12" md="5">
                      <v-card-text class="mt-12">
                        <!-- <h1
                          class="text-center display-2 teal--text text--accent-2"
                        >
                          HOME CHARGING
                        </h1> -->

                        <h2 class="text-left mlt-4">LOGIN</h2>
                        <br />
                        <h4 class="text-left mlt-4">
                          Silahkan login terlebih dahulu ke aplikasi
                        </h4>

                        <!-- FORM LOGIN -->
                        <v-form>
                          <v-text-field
                            label="Masukan Email"
                            name="Email"
                            prepend-icon="email"
                            type="text"
                            color="black"
                          />
                          <v-text-field
                            id="Password"
                            label="Kata Sandi"
                            name="Password"
                            prepend-icon="lock"
                            type="password"
                            color="black"
                          />
                          <div class="captcha-wrap"></div>

                          <v-text-field
                            id="captcha-code"
                            label="Enter captcha"
                            name="Password"
                            prepend-icon="refresh"
                            type="input"
                            color="black"
                          />
                        </v-form>

                        <!-- LOGIN BY APPS -->
                        <div class="text-center mt-2">
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-facebook-f</v-icon>
                          </v-btn>
                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-google-plus-g</v-icon>
                          </v-btn>

                          <v-btn class="mx-2" fab color="black" outlined>
                            <v-icon>fab fa-linkedin-in</v-icon>
                          </v-btn>
                        </div>
                        <h3 class="text-center mt-3">Lupa Kata Sandi</h3>
                      </v-card-text>
                      <div class="text-center mt-2">
                        <v-btn rounded color="blue" dark>Login</v-btn>
                      </div>
                    </v-col>
                    <v-col cols="12" md="4" class="teal accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Hello,Friends!</h1>
                        <h5 class="text-center">
                          Enter your personel details and start journay with us
                        </h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined="" dark @click="step++"
                          >SIGN UP</v-btn
                        >
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
                <v-window-item :value="2">
                  <v-row class="fill-height">
                    <v-col cols="12" md="4" class="teal accent-3">
                      <v-card-text class="white--text mt-12">
                        <h1 class="text-center display-1">Welcome Back Buddy!</h1>
                        <h5 class="text-center">
                          To keep connected with us please login with your
                          personal info
                        </h5>
                      </v-card-text>
                      <div class="text-center">
                        <v-btn rounded outlined dark @click="step--"
                          >SIGN UP
                        </v-btn>
                      </div>
                    </v-col>
                  </v-row>
                </v-window-item>
              </v-window>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>
<script>
export default {
  data: () => ({
    step: 1,
  }),
  props: {
    source: String,
  },
};
</script>

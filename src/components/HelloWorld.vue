<template>
  <v-card>
    <!-- https://bootstrapmade.com/demo/MyResume/ -->
    <v-layout>
      <v-flex lg3>
        <v-card >
          <v-navigation-drawer :height="vuetify.height" absolute permanent style="background-color: #040b14" dark width="360">
            <div class="d-flex justify-center mt-2">
              <v-avatar size="140">
                <img class="pa-3" src="@/assets/akash.jpg" alt="John">
              </v-avatar>
            </div>
            <div class="d-flex justify-center mt-3">
              <span class="headline font-weight-bold white--text">Moses Akash J</span>
            </div>
            <div class="d-flex justify-center">
              <span class="subtitle font-weight-thin white--text">WEB DEVELOPER</span>
            </div>
            <div class="d-flex justify-center mt-3">
              <v-list>
                <v-list-item v-for="item in menuItems" :key="item.title" class="py-0 my-0">
                  <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </div>
            <div class="d-flex justify-center align-end">
              <v-layout class="mt-3 mx-1 ml-8">
                <v-flex v-for="(i, index) in socialItems" :key="index">
                  <v-icon dark>{{i.icon}}</v-icon>
                </v-flex>
              </v-layout>
            </div>
          </v-navigation-drawer>
        </v-card>
      </v-flex>
      <v-flex lg9 style="overflow: auto">
        <v-card :height="vuetify.height" elevation="0">
          <section>
            <div>
              <v-layout>
                <v-flex lg6 class="pa-5">
                <v-img src="@/assets/akash.jpg" height="600">
                </v-img>
                </v-flex>
                <v-flex lg6 class="pa-5 my-auto">
                  <div>
                    <h2>I'm Moses Akash J</h2>
                    <p class="mt-5">
                      Aliquam eu nunc. Fusce commodo aliquam arcu. In consectetuer turpis ut velit. Nulla facilisi.. Morbi mollis tellus ac sapien. Fusce vel dui. Praesent ut ligula non mi varius sagittis. Vivamus consectetuer hendrerit lacus. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
                    </p>
                    <p>
                      Aliquam eu nunc. Fusce commodo aliquam arcu. In consectetuer turpis ut velit. Nulla facilisi.. Morbi mollis tellus ac sapien. Fusce vel dui. Praesent ut ligula non mi varius sagittis. Vivamus consectetuer hendrerit lacus. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
                    </p>
                  </div>
                  <div class="mt-7">
                    <v-btn color="teal darken-1" class="mx-2" large>Download My Resume</v-btn>
                    <v-btn color="teal darken-1" large outlined>Hire Me</v-btn>
                  </div>
                </v-flex>
              </v-layout>
            </div>
          </section>
          <section>
            <v-container>
              <div class="section-title">
                <h2>About</h2>
                <p>Magnam dolores commodi suscipit. Necessitatibus eius consequatur ex aliquid fuga eum quidem. Sit sint consectetur velit. Quisquam quos quisquam cupiditate. Et nemo qui impedit suscipit alias ea. Quia fugiat sit in iste officiis commodi quidem hic quas.</p>
              </div>
            </v-container>
          </section>
          <section>
            <v-container>
              <div class="section-title">
                <h2>RESUME</h2>
                <p>Magnam dolores commodi suscipit. Necessitatibus eius consequatur ex aliquid fuga eum quidem. Sit sint consectetur velit. Quisquam quos quisquam cupiditate. Et nemo qui impedit suscipit alias ea. Quia fugiat sit in iste officiis commodi quidem hic quas.</p>
              </div>
              <div>
                <v-row>
                  <v-col cols="6">
                    <v-timeline dense clipped>
                      <v-timeline-item class="mb-1" hide-dot>
                        <span class="resume-title">Education</span>
                      </v-timeline-item>
                      <v-timeline-item class="mb-4" color="grey" icon-color="grey lighten-2" small>
                        <div class="pt-3">
                          Bachelor of Computer Science Engineering
                        </div>
                        <v-chip class="mt-1" label> 2016 - 2021 </v-chip>
                      </v-timeline-item>
                    </v-timeline>
                  </v-col>
                  <v-col cols="6">
                    <v-timeline dense clipped>
                      <v-timeline-item class="mb-1" hide-dot>
                        <span class="resume-title">Professional Experience</span>
                      </v-timeline-item>
                      <v-timeline-item class="mb-4" color="grey" icon-color="grey lighten-2" small>
                        <div class="pt-3">
                          FullStack Developer, ProcessDrive India Pvt. Ltd
                        </div>
                        <v-chip class="mt-1" label> 2020 - Current </v-chip>
                      </v-timeline-item>
                    </v-timeline>
                  </v-col>
                </v-row>
              </div>
            </v-container>
          </section>
          <section>
            <v-container>
              <div class="section-title">
                <h2>Skills</h2>
                <p>Magnam dolores commodi suscipit. Necessitatibus eius consequatur ex aliquid fuga eum quidem. Sit sint consectetur velit. Quisquam quos quisquam cupiditate. Et nemo qui impedit suscipit alias ea. Quia fugiat sit in iste officiis commodi quidem hic quas.</p>
              </div>
              <div>
                <div>
                  <span class="resume-title">FrontEnd</span>
                </div>
                <v-row>
                  <v-col v-for="(i, index) in skills.basics" :key="index">
                    <v-card outlined> 
                      <v-card-text>
                        <v-layout>
                          <v-flex> <v-icon> {{'mdi-codepen'}} </v-icon> </v-flex>
                          <v-flex> {{i.skill}} </v-flex>
                        </v-layout>
                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </div>
              <div class="my-3">
                <div>
                  <span class="resume-title">BackEnd</span>
                </div>
                <v-row>
                  <v-col v-for="(i, index) in skills.frameworks" :key="index">
                    <v-card outlined> 
                      <v-card-text>
                        <v-layout>
                          <v-flex> <v-icon> {{'mdi-view-grid-outline'}} </v-icon> </v-flex>
                          <v-flex> {{i.skill}} </v-flex>
                        </v-layout>
                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </div>
              <div class="mt-5">
                <div>
                  <span class="resume-title">Technologies</span>
                </div>
                <v-row>
                  <v-col v-for="(i, index) in skills.technologies" :key="index">
                    <v-card outlined> 
                      <v-card-text>
                        <v-layout>
                          <v-flex> <v-icon> {{'mdi-gitlab'}} </v-icon></v-flex>
                          <v-flex> {{i.skill}} </v-flex>
                        </v-layout>
                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </div>
            </v-container>
          </section>
          <section id="contact" class="contact">
            <v-container>
              <div class="section-title">
                <h2>Contact</h2>
              </div>
              <v-row class="mt-1">
                <v-col class="col-lg-5">
                  <v-card elevation="0" height="100%" class="d-flex flex-column justify-center">
                    <div>
                      <h4 class="my-2">Location:</h4>
                      <p> <v-icon>mdi-map-marker</v-icon> 7, UKT Malai, Trichy, Tamil Nadu, India.</p>
                    </div>
                    <div>
                      <h4 class="my-2"> Email:</h4>
                      <p> <v-icon>mdi-email</v-icon> mosesakash.j@gmail.com</p>
                    </div>
                    <div>
                      <h4 class="my-2">Call:</h4>
                      <p> <v-icon>mdi-phone</v-icon> +91 9750840534</p>
                    </div>
                  </v-card>
                </v-col>

                <div class="col-lg-7 mt-2 mt-lg-0">
                  <v-form>
                    <v-row>
                      <v-col class="col-md-6 form-group">
                        <v-text-field dense outlined rounded hide-details name="name" class="form-control" id="name" placeholder="Your Name" required=""></v-text-field>
                      </v-col>
                      <v-col class="col-md-6 form-group mt-3 mt-md-0">
                        <v-text-field dense outlined rounded hide-details type="email" class="form-control" name="email" id="email" placeholder="Your Email" required=""></v-text-field>
                      </v-col>
                    </v-row>
                    <div class="form-group mt-3">
                      <v-text-field dense outlined rounded hide-details class="form-control" name="subject" id="subject" placeholder="Subject" required=""></v-text-field>
                    </div>
                    <div class="form-group mt-3">
                      <v-textarea dense outlined class="form-control" name="message" rows="5" placeholder="Message" required=""></v-textarea>
                    </div>
                    <div class="text-center"><v-btn color="primary" rounded >Send Message</v-btn></div>
                  </v-form>
                </div>
              </v-row>
            </v-container>
          </section>
        </v-card>
      </v-flex>
    </v-layout>
    
  </v-card>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      height: window.innerHeight,
      menuItems: [
          { title: 'Home', icon: 'mdi-home-city' },
          { title: 'About', icon: 'mdi-account' },
          { title: 'Resume', icon: 'mdi-account-group-outline' },
          { title: 'Portfolio', icon: 'mdi-account-group-outline' },
          { title: 'Contact', icon: 'mdi-account-group-outline' },
        ],
      skills: {
        basics: [
          {skill: 'Html', level: '', image: '', icon: '' },
          {skill: 'CSS', level: '', image: '', icon: '' },
          {skill: 'JS', level: '', image: '', icon: '' },
          {skill: 'Vue JS', level: '', image: '', icon: '' },
        ],
        frameworks: [
          {skill: 'C#', level: '', image: '', icon: '' },
          {skill: 'Node Js', level: '', image: '', icon: '' },
          {skill: 'Express Js', level: '', image: '', icon: '' },
          {skill: '.Net Core Web API', level: '', image: '', icon: '' },
        ],
        technologies: [
          {skill: 'Github Actions', level: '', image: '', icon: '' },
        ]
      },
      socialItems: [
        { icon: 'mdi-facebook' },
        { icon: 'mdi-twitter' },
        { icon: 'mdi-instagram' },
        { icon: 'mdi-google' },
        { icon: 'mdi-linkedin' },
      ],
    }),
    computed: {
      vuetify () {
        let breakpointKeys = ['name', 'height', 'xs', 'lg', 'lgAndDown', 'lgAndUp', 'lgOnly', 'md',
                              'mdAndDown', 'mdAndUp', 'mdOnly', 'mobile', 'mobileBreakpoint', 'resizeTimeout', 'scrollBarWidth',
                              'sm', 'smAndDown', 'smAndUp', 'smOnly', 'width', 'xl', 'xlOnly', 'xs', 'xsOnly']

        let obj = {}
        breakpointKeys.forEach(x => {
          obj[x] = this.$vuetify.breakpoint[x]
        })
        return obj
      }
    }
  }
</script>
<style scoped>
.resume-title {
    font-size: 23px;
    font-weight: 700;
    margin-top: 20px;
    margin-bottom: 20px;
    color: #45505b;
}
.section-title h2 {
    font-size: 32px;
    font-weight: bold;
    text-transform: uppercase;
    margin-bottom: 20px;
    position: relative;
    color: #45505b;
    font-family: "Raleway", sans-serif;
}
</style>

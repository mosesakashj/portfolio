<template>
  <v-card>
    <!-- https://bootstrapmade.com/demo/MyResume/ -->
    <v-layout>
      <v-flex lg3>
        <v-card :height="height">
          <v-navigation-drawer absolute permanent style="background-color: #040b14" dark width="360">
            <div class="d-flex justify-center mt-3">
              <v-avatar size="190">
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
                <v-list-item v-for="item in menuItems" :key="item.title">
                  <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                  </v-list-item-icon>

                  <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
              </v-list>
            </div>
            <div class="d-flex justify-center">
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
        <v-card :height="height" elevation="0">
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
    padding-bottom: 20px;
    position: relative;
    color: #45505b;
    font-family: "Raleway", sans-serif;
}

</style>

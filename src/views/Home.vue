<template>
  <div class="flex flex-col h-screen overflow-auto space-y-7">
    <personal-component class="sticky top-0 z-10 sm:sticky" :info="info" />
    <div class="flex flex-col w-full p-3 m-auto space-y-10 sm:w-2/3">
      <history-component
        class="pl-3"
        v-for="history in info.histories"
        :key="history.name"
        :history="history"
      />
    </div>
  </div>
</template>

<script>
import HistoryComponent from "../components/HistoryComponent.vue";
import PersonalComponent from "../components/PersonalComponent.vue";

export default {
  components: {
    HistoryComponent,
    PersonalComponent
  },
  data() {
    return {
      info: {
        name: "Karel Díaz Alfonso",
        phone: "+5354653411",
        socialMedias: [
          {
            name: "Telegram",
            icon: "telegram",
            link: "https://t.me/KarelDiazAlfonso"
          },
          {
            name: "Twitter",
            icon: "twitter",
            link: "https://twitter.com/KarelDiazA"
          },
          {
            name: "LinkedIn",
            icon: "linkedin",
            link: "https://linkedin.com/KarelDiaz"
          },
          {
            name: "GitHub",
            icon: "github",
            link: "https://github.com/KarelDiaz"
          }
        ],
        skillsFrontend: [
          { tecName: "Vue", stars: 5 },
          { tecName: "Angular", stars: 4 },
          { tecName: "Tailwind", stars: 5 }
        ],
        skillsBackend: [
          { tecName: "Express", stars: 5 },
          { tecName: "Strapi", stars: 5 }
        ],
        histories: [
          {
            name: "Work",
            contents: [
              {
                name: "Influencer Advisor",
                name2: "Informage Studio",
                dateStart: "01-11-2021",
                dateEnd: "15-11-2021",
                description:
                  "A web site to finde influncer for your bussinnes.",
                events: [],
                role: "Frontend Developer",
                team: "3 Developers",
                tasks: ["Frontend"],
                technologies: ["Laravel", "Vue", "Tailwind"],
                links: []
              },
              {
                name: "Colaboracion Ciudadana",
                name2: "Sadeco",
                dateStart: "01-10-2021",
                dateEnd: "01-11-2021",
                description:
                  "In the application it is possible share information about lost pets or animal with other user and get reward for that.",
                events: [],
                role: "Frontend Developer",
                team: "3 Developers",
                tasks: ["Mockup views"],
                technologies: ["Angular", "Ionic"],
                links: [
                  {
                    title: "Sadeco here",
                    link: "https://www.sadeco.es/"
                  }
                ]
              },
              {
                name: "Caser Starbien",
                name2: "Theinit",
                dateStart: "01-09-2021",
                dateEnd: "01-11-2021",
                description:
                  "Is a private project to help people how are inscribed in Caser Seguros to tracking his exercises.",
                events: [],
                role: "Frontend Developer",
                team: "4 Developers",
                tasks: [],
                technologies: ["Vuejs", "Quasarjs"],
                links: [
                  {
                    title: "Theinit here",
                    link: "https://www.theinit.com"
                  },
                  {
                    title: "Caser Seguros here",
                    link: "https://www.caser.es"
                  }
                ]
              },
              {
                name: "Binary Coffee",
                name2: "Open Source Projects",
                dateStart: "2019",
                dateEnd: "present",
                description:
                  "Binary Coffee is an open-source project, with the idea of unifying the software developers and people who like Informatics in Cuba, in a place where they can interact and share knowledge. This idea born between some friends and currently what started as a blog is a website where people can publish their own articles and share with the community",
                events: [],
                role: "Fullstack Developer",
                team: "The community",
                tasks: [],
                technologies: [
                  "Angular",
                  "Angular Universal",
                  "Strapi",
                  "MongoDB"
                ],
                links: [
                  {
                    title: "You can find it in github here",
                    link: "https://github.com/orgs/dcs-community"
                  },
                  {
                    title: "This is the oficial page of Binary Coffee",
                    link: "https://binary-coffee.dev"
                  }
                ]
              },
              {
                name: "School timetable",
                name2: "University City, Jose Antonio Echeverria",
                dateStart: "2018",
                dateEnd: "2020",
                description:
                  "Organize the class system to the students and professors. ",
                events: [],
                role: "Fullstack Developer",
                team: "1 Developer",
                tasks: [
                  "Implement the timetable module for public information ",
                  "Implement the manage view for professors"
                ],
                technologies: ["Vue", "Tailwind", "Strapi", "MongoDB"],
                links: [
                  {
                    title: "You can look at the university here",
                    link: "https://cuaje.edu.cu"
                  }
                ]
              },
              {
                name:
                  "Post-processing module to illustrative visualization of volumes using GPU",
                name2: "Thesis, Graduation paper",
                dateStart: "2017",
                dateEnd: "2018",
                description:
                  "It is a module to stylize the volumes generated in the software Viscmedic Illustration. Each effect uses an algorithm based in the Graphic Processing Unit (GPU) to achieve the execution in interactive times.",
                events: [],
                role: "Developer",
                team: "1 Developer",
                tasks: [
                  "Implement the plugin to integrate with Vismedic Illutration",
                  "Implement the each of the efects using GPU"
                ],
                technologies: ["Qt", "C++ (CPU)", "GLSL (GPU)"],
                links: [
                  {
                    title: "You can look at the university here",
                    link: "https://uci.cu"
                  }
                ]
              }
            ]
          },
          {
            name: "Education",
            contents: [
              {
                name: "University of Information Sciences",
                name2: "Bachelor of Computer Science",
                dateStart: "2013",
                dateEnd: "2018",
                description: "",
                events: [
                  { name: "ICPC Caribbean Finals", date: "2015/11" },
                  { name: "ICPC Caribbean Finals", date: "2017/11" },
                  { name: "Global Game Jam", date: "2018" }
                ],
                role: "",
                team: "",
                tasks: [],
                technologies: [],
                links: [
                  {
                    title: "You can look at the university site",
                    link: "https://uci.cu"
                  }
                ]
              }
            ]
          }
        ]
      }
    };
  }
};
</script>

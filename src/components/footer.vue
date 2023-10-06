<template>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <div v-for="(column, index) in columns" :class="`col-md-3 col-${index}`" :key="index">
          <h4>{{ column.title }}</h4>
          <ul>
            <li v-for="(link, linkIndex) in column.links" :key="linkIndex">
              <a :href="link.url">{{ link.text }}</a>
            </li>
          </ul>
        </div>
        <div class="col-md-3">
          <h4>MEDIA SOSIAL</h4>
          <ul class="social-icons-list">
            <li v-for="social in socialMediaLinks" :key="social.name">
              <a :href="social.link">
                <i :class="social.iconClass"></i>
                <img :src="social.imageURL" class="social-icon" />
              </a>
            </li>
          </ul>
          <img :src="imageURL" class="kominfo" />
        </div>
      </div>
    </div>
    <p>© 2023 PT Global Inovasi Siber Indonesia - All Rights Reserved</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      socialMediaLinks: [
        {
          name: "Facebook",
          link: "https://www.facebook.com/",
          iconClass: "fab fa-facebook",
          imageURL: require('@/assets/icons8-facebook.png'),
        },
        {
          name: "Instagram",
          link: "https://instagram.com/",
          iconClass: "fab fa-instagram",
          imageURL: require('@/assets/icons8-instagram.png'),
        },
        {
          name: "Linkedin",
          link: "https://linkedin.com/",
          iconClass: "fab fa-linkedin",
          imageURL: require('@/assets/icons8-linkedin.png'),
        },
        {
          name: "Youtube",
          link: "https://youtube.com/",
          iconClass: "fab fa-youtube",
          imageURL: require('@/assets/icons8-youtube.png'),
        },
        {
          name: "Twitter",
          link: "https://twitter.com/",
          iconClass: "fab fa-twitter",
          imageURL: require('@/assets/icons8-twitter.png'),
        },
      ],
      imageURL: require('@/assets/kominfo.png'),
      columns: [
        {
          title: "CYBER ARMY INDONESIA",
          links: [
            { text: "Tentang Kami", url: "#" },
            { text: "Kontak", url: "#" },
            { text: "Karir", url: "#" },
          ],
        },
        {
          title: "LAYANAN PERUSAHAAN",
          links: [
            { text: "Bug Bounty Program", url: "#" },
            { text: "Cyber Security Training", url: "#" },
            { text: "Automated Security Testing", url: "#" },
          ],
        },
        {
          title: "AREA BUGHUNTER",
          links: [
            { text: "Challenge Program", url: "#" },
            { text: "Program List", url: "#" },
            { text: "Leaderboard", url: "#" },
          ],
        },
        {
          title: "LAINNYA",
          links: [
            { text: "FAQ", url: "#" },
            { text: "Syarat & Ketentuan", url: "#" },
            { text: "Kebijakan Privasi", url: "#" },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.footer {
    font-family: 'RobotoBold', sans-serif;
    text-align: center;
    background-color: #161F62;
    color: #fff;
    padding: 20px;
    margin-top: 40px;
  }
  
.container {
    max-width: 1200px;
    margin: 0 auto;
}
  
.container .row {
    display: flex;
    justify-content: space-evenly;

}
  
.col-md-3 {
    display: flex;
    flex-direction: column;
}

h4 {
    font-size: 14px;
    text-align: left;
    margin-bottom: 10px;
}
  
ul {
    list-style: none;
    padding: 0;
}
  
li {
    margin-bottom: 5px;
    text-align: left;
}
  
a {
    color: #fff;
    font-size: 14px;
    text-decoration: none;
  }

  a:hover {
    color: rgb(8, 189, 255);
    text-decoration: none;
  }
.social-icon {
    width: 20px;
    margin-right: 10px;
    display: flex;
  }
  
  .kominfo {
    width: 100px;
    margin-top: 20px;
  }
  
@media (max-width: 768px) {
    .container .row {
      flex-direction: column;
    }
  
    .col-md-3 {
      flex-basis: 100%;
      margin-bottom: 20px;
      margin: 0 10px; 
    }
}

.social-icon {
    width: 25px;
    height: 25px;
    display: flex;;
    align-items: center;
}

.social-icons-list {
  display: flex;
  flex-wrap: wrap; 
  list-style: none;
  padding: 0;
  flex-direction: row;
  align-items: center; 
}

.kominfo-column {
  display: flex;
  align-items: center; 
  justify-content: center;
  margin-top: 20px;
}

.social-icons-list li {
  margin-right: 10px; 
}

.col-md-3 .kominfo {
  display: flex;
  flex-direction: column;
}

.kominfo {
    width: 90px; 
    margin-top: 20px;
}

.footer p {
  font-size: 14.5px;
}

</style>

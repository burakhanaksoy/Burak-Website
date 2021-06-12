<template>
  <div class="about">
    <div class="container">
      <div class="row justify-content-center">
        <h1>Burakhan Aksoy</h1>
      </div>
      <div class="row">
        <div class="col-md-3 col-xs-6">
          <img
            class="my-picture-about-page"
            alt="My Picture"
            src="../../utils/photos/about-page-picture.jpg"
          />
          <div class="row justify-content-center" style="">
            <div class="col-md-3 col-xs-12 mr-4">
              <img
                class="logos"
                src="../../utils/photos/ted-logo.png"
                alt="TED University logo"
              />
            </div>
            <div class="col-md-3 col-xs-12 mr-3">
              <img
                class="east-china-logo"
                src="../../utils/photos/East_China_Normal_University_logo.svg.png"
                alt="East China Normal University logo"
              />
            </div>
            <div class="col-md-3 col-xs-12 mr-3">
              <img
                class="logos"
                src="../../utils/photos/Shanghai-Jiao-Tong-University-01.png"
                alt="TED University logo"
              />
            </div>
          </div>
        </div>
        <div class="col-md-9 col-xs-6">
          <h2 class="background-title">Story</h2>
          <ul>
            <li>
              Graduated from TED University Electrical & Electronics engineering
              department
            </li>
            <li>Been to Shanghai to learn Chinese in my gap year</li>
            <li>Passed HSK 5 exam (274/300)</li>
            <li>Worked as a software test engineer for 1.5 years</li>
            <li>
              <span class="passion"
                >Found a passion in software development and studied</span
              >
            </li>
            <img
              class="logos"
              src="../../utils/photos/Python-Transparent-Background.png"
              alt="TED University logo"
            />
            <img
              class="logos"
              src="../../utils/photos/java_logo.png"
              alt="TED University logo"
            />
            <hr />
            <li>Now, working as a Junior Python developer</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.my-picture-about-page {
  width: 15rem;
  height: 15rem;
  object-fit: contain;
}
.logos {
  width: 83px;
  height: 79px;
  object-fit: cover;
}
.east-china-logo {
  width: 83px;
  height: 85px;
  object-fit: cover;
}
li {
  list-style-type: none;
}
.passion {
  font-weight: bold;
}
</style>
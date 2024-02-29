<template>
  <div class="banner-1">
    <!-- NavBar -->
    <nav
      class="container px-6 mx-auto md:flex md:justify-between md:items-center"
    >
      <div class="flex items-center justify-between">
        <div class="relative w-16 h-16">
          <img
            class="rounded-full border border-gray-100 shadow-sm"
            src="./assets/profile.jpg"
            alt="user image"
          />
        </div>
        <!-- Mobile menu button -->
        <div @click="showMenu = !showMenu" class="flex md:hidden">
          <button
            type="button"
            class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400"
          >
            <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
              <path
                fill-rule="evenodd"
                d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
              ></path>
            </svg>
          </button>
        </div>
      </div>
      <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
      <ul
        :class="showMenu ? 'flex' : 'hidden'"
        class="flex-col items-end mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0"
      >
        <li class="menu-button"><a href="#">Home</a></li>
        <li class="menu-button">
          <a href="#work" v-smooth-scroll>Work Experience</a>
        </li>
        <li class="menu-button">
          <a href="#tools" v-smooth-scroll>Tools & Skills</a>
        </li>
        <li class="menu-button">
          <a href="#About" v-smooth-scroll>About Me</a>
        </li>
        <li class="menu-button">
          <a href="#frameworks" v-smooth-scroll>Frameworks</a>
        </li>
      </ul>
    </nav>
    <!-- End Navbar -->

    <div class="flex items-center mt-6">
      <div class="w-11/12 space-y-5 md:space-y-10">
        <h1
          class="3xl:text-8xl 2xl:text-7xl xl:text-6xl lg:text-4xl md:text-3xl sm:text-3xl text-xl font-Eczar font-bold leading-tight text-gray-700"
        >
          I'm
          <a
            href="https://www.linkedin.com/in/ian-montero-moya-88a180209/"
            target="_blank"
            class="text-black hover:underline"
          >
            Ian Montero</a
          >🧑🏽‍💻<br />Software Engineer & Backend Developer
        </h1>
      </div>

      <div class="w-8/12 flex justify-end">
        <div class="md:flex gap-1 md:gap-10">
          <button
            id="resume"
            @click="downloadPDF"
            class="text-white bg-gray-800 submit-button hidden md:block"
          >
            My Resume
          </button>

          <button
            onclick="window.location.href = 'mailto:djmm171298@gmail.com';"
            class="text-gray-800 border-4 border-gray-800 submit-button mb-5 md:mb-0"
          >
            Contact Me
          </button>
        </div>
      </div>
    </div>
  </div>

  <div class="banner-2 space-y-10 pb-20" id="work">
    <h3 class="heading3 my-5">Work Experience</h3>
  </div>

  <div class="banner-1" id="tools">
    <div class="space-y-4 grid place-items-center mt-5">
      <h3 class="heading3">Tools and Skills</h3>
      <p class="font-work_sans text-gray-600 font-semibold leading-relaxed">
        Some Tools and Skills I've been working with
      </p>
    </div>
    <div class="max-w-6xl mx-auto px-8 py-16">
      <div class="relative">
        <div class="swiper-container">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="https://a.slack-edge.com/80588/marketing/img/meta/slack_hash_256.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del Slack -->
                  <svg
                    class="relative"
                    width="200"
                    height="120"
                    viewBox="0 0 200 120"
                  >
                    <path
                      fill="#fff"
                      fill-rule="evenodd"
                      d="M63.75 75.24l2.5-5.93c2.7 2.05 6.3 3.13 9.85 3.13 2.61 0 4.27-1.03 4.27-2.6-.04-4.37-15.7-.95-15.82-11.9-.04-5.58 4.8-9.86 11.66-9.86 4.08 0 8.16 1.03 11.06 3.38l-2.34 6.05c-2.66-1.73-5.97-2.97-9.12-2.97-2.13 0-3.55 1.03-3.55 2.36.04 4.28 15.82 1.94 15.98 12.4 0 5.7-4.72 9.69-11.5 9.69-4.96 0-9.52-1.2-12.99-3.75zm96.01-8.08a7.16 7.16 0 0 1-8.11 3.5 7.35 7.35 0 0 1-5.38-7.13c0-3.34 2.2-6.27 5.38-7.12 3.16-.85 6.5.58 8.11 3.5l6.9-3.93a15.02 15.02 0 0 0-17.03-7.42 15.42 15.42 0 0 0-11.33 14.97c0 7.04 4.66 13.2 11.33 14.97a15.02 15.02 0 0 0 17.04-7.43l-6.9-3.9zM91.71 35.25h8.64v43.16h-8.64V35.25zm78.34 0v43.16h8.65V65.48l10.25 12.93H200l-13.03-15.37 12.06-14.34h-10.58l-9.76 11.9V35.25h-8.64zm-43.82 31.1a8.14 8.14 0 0 1-6.83 3.56 7.24 7.24 0 0 1-7.33-7.16 7.24 7.24 0 0 1 7.33-7.15 8.1 8.1 0 0 1 6.83 3.67v7.08zm0-18v3.4c-1.43-2.36-5-4-8.72-4-7.7 0-13.76 6.64-13.76 14.96 0 8.33 6.07 15.04 13.76 15.04 3.73 0 7.3-1.63 8.72-4v3.4H135v-28.8h-8.77zM10.53 66.4A5.32 5.32 0 0 1 5.3 71.8 5.32 5.32 0 0 1 .04 66.4a5.32 5.32 0 0 1 5.25-5.38h5.25v5.38zm2.63 0a5.32 5.32 0 0 1 5.25-5.38c2.9 0 5.25 2.4 5.25 5.38v13.46a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39V66.4zm5.26-21.63a5.32 5.32 0 0 1-5.25-5.38A5.32 5.32 0 0 1 18.42 34c2.9 0 5.25 2.41 5.25 5.39v5.38h-5.25zm0 2.74c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38H5.25A5.32 5.32 0 0 1 0 52.9a5.32 5.32 0 0 1 5.25-5.39h13.17zm21.03 5.39a5.32 5.32 0 0 1 5.25-5.39c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38h-5.25V52.9zm-2.62 0a5.32 5.32 0 0 1-5.25 5.38 5.32 5.32 0 0 1-5.25-5.38V39.39A5.32 5.32 0 0 1 31.58 34c2.9 0 5.25 2.41 5.25 5.39v13.5zm-5.25 21.58c2.9 0 5.25 2.41 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39v-5.38h5.25zm0-2.7a5.32 5.32 0 0 1-5.25-5.38 5.32 5.32 0 0 1 5.25-5.38h13.17c2.9 0 5.25 2.4 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39H31.58z"
                    />
                  </svg>
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Slack</strong>
                      as a tool for group communication and manage CI/CD of
                      projects.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://slack.com/intl/es-cr"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Slack
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 2 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/jira.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del jira -->
                  <svg
                    class="relative"
                    width="200"
                    height="120"
                    viewBox="0 0 200 120"
                  >
                    <!-- Imagen de fondo -->
                    <image
                      href="./assets/jiratext.png"
                      width="100%"
                      height="100%"
                    />

                    <!-- Path -->
                    <!-- <path
                      fill="#fff"
                      fill-rule="evenodd"
                      d="M63.75 75.24l2.5-5.93c2.7 2.05 6.3 3.13 9.85 3.13 2.61 0 4.27-1.03 4.27-2.6-.04-4.37-15.7-.95-15.82-11.9-.04-5.58 4.8-9.86 11.66-9.86 4.08 0 8.16 1.03 11.06 3.38l-2.34 6.05c-2.66-1.73-5.97-2.97-9.12-2.97-2.13 0-3.55 1.03-3.55 2.36.04 4.28 15.82 1.94 15.98 12.4 0 5.7-4.72 9.69-11.5 9.69-4.96 0-9.52-1.2-12.99-3.75zm96.01-8.08a7.16 7.16 0 0 1-8.11 3.5 7.35 7.35 0 0 1-5.38-7.13c0-3.34 2.2-6.27 5.38-7.12 3.16-.85 6.5.58 8.11 3.5l6.9-3.93a15.02 15.02 0 0 0-17.03-7.42 15.42 15.42 0 0 0-11.33 14.97c0 7.04 4.66 13.2 11.33 14.97a15.02 15.02 0 0 0 17.04-7.43l-6.9-3.9zM91.71 35.25h8.64v43.16h-8.64V35.25zm78.34 0v43.16h8.65V65.48l10.25 12.93H200l-13.03-15.37 12.06-14.34h-10.58l-9.76 11.9V35.25h-8.64zm-43.82 31.1a8.14 8.14 0 0 1-6.83 3.56 7.24 7.24 0 0 1-7.33-7.16 7.24 7.24 0 0 1 7.33-7.15 8.1 8.1 0 0 1 6.83 3.67v7.08zm0-18v3.4c-1.43-2.36-5-4-8.72-4-7.7 0-13.76 6.64-13.76 14.96 0 8.33 6.07 15.04 13.76 15.04 3.73 0 7.3-1.63 8.72-4v3.4H135v-28.8h-8.77zM10.53 66.4A5.32 5.32 0 0 1 5.3 71.8 5.32 5.32 0 0 1 .04 66.4a5.32 5.32 0 0 1 5.25-5.38h5.25v5.38zm2.63 0a5.32 5.32 0 0 1 5.25-5.38c2.9 0 5.25 2.4 5.25 5.38v13.46a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39V66.4zm5.26-21.63a5.32 5.32 0 0 1-5.25-5.38A5.32 5.32 0 0 1 18.42 34c2.9 0 5.25 2.41 5.25 5.39v5.38h-5.25zm0 2.74c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38H5.25A5.32 5.32 0 0 1 0 52.9a5.32 5.32 0 0 1 5.25-5.39h13.17zm21.03 5.39a5.32 5.32 0 0 1 5.25-5.39c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38h-5.25V52.9zm-2.62 0a5.32 5.32 0 0 1-5.25 5.38 5.32 5.32 0 0 1-5.25-5.38V39.39A5.32 5.32 0 0 1 31.58 34c2.9 0 5.25 2.41 5.25 5.39v13.5zm-5.25 21.58c2.9 0 5.25 2.41 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39v-5.38h5.25zm0-2.7a5.32 5.32 0 0 1-5.25-5.38 5.32 5.32 0 0 1 5.25-5.38h13.17c2.9 0 5.25 2.4 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39H31.58z"
                    /> -->
                  </svg>
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Jira</strong>
                      as a project and task management tool, as well as to
                      manage project progress.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://www.atlassian.com/software/jira?&aceid=&adposition=&adgroup=140479881486&campaign=18442480203&creative=656562805651&device=c&keyword=jira&matchtype=e&network=g&placement=&ds_kids=p73335832032&ds_e=GOOGLE&ds_eid=700000001558501&ds_e1=GOOGLE&gad_source=1&gclid=CjwKCAiArfauBhApEiwAeoB7qCrCy1YHSDsLkdA8x07AlC-lvTcpkK7Cbi4up1q6veyK0o8QWFlGhxoCH60QAvD_BwE&gclsrc=aw.ds"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Jira
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 3 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/docker.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del docker -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Docker</strong>
                      as a project container tool providing greater scalability
                      and ease of project management.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://www.docker.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Docker
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 4 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/github.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del github -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Github</strong>
                      as a central platform to manage and collaborate on
                      projects tracking code changes, facilitating team
                      collaboration.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://github.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about GitHub
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 5 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/figma.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del figma -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Figma</strong>
                      as a collaborative design tool to create, prototype, and
                      share user interfaces and experiences.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://www.figma.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Figma
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>

            <!-- skill 6 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/wordpress.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del  -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium"
                        >Wordpress</strong
                      >
                      as a content management system and website creator to
                      design, build, and manage websites.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://wordpress.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Wordpress
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 7 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/magento.jpg"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del  -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Magento</strong>
                      as a content management system and website creator to
                      design, build, and manage websites.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://magento.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Magento
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- Botones de navegación -->
          <!-- <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div> -->
        </div>
      </div>
    </div>
  </div>

  <div class="banner-2 md:flex items-center md:justify-evenly" id="About">
    <img
      class="md:h-[500px] h-[400px] myimages"
      src="./assets/about.jpg"
      alt="user image"
    />
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
      <h4 class="project-title item">About Me</h4>
      <p class="font-work_sans">
        Passionate Software Engineer. I stand out for my ability to work
        collaboratively, my proactivity, and my self-taught learning skills. I
        am constantly motivated to expand my knowledge and improve my skills,
        preparing myself for a promising future in the field of technology. My
        experience encompasses a wide range of programming languages, including
        PHP, Python, Java , C#, C++, CSS, and JavaScript. Additionally, I am
        familiar with ReactJS, VueJS and have used frameworks such as Node.js,
        Laravel, Django, .NET and WordPress. I also possess strong knowledge in
        backend development with databases like MySQL, SQL, Sqlite, Mongodb and
        PostgreSq, also I used cloud enviroment with GCP and AWS, finally I also
        have expirence with docker.
      </p>
      <button
        onclick="window.open('https://medsimple.ca');"
        target="_blank"
        class="text-white bg-gray-800 submit-button hidden md:block"
      >
        Proudest Work
      </button>
    </div>
  </div>
  <div class="banner-1" id="frameworks">
    <div class="space-y-4 grid place-items-center mt-5">
      <h3 class="heading3">Frameworks and Libraries</h3>
      <p class="font-work_sans text-gray-600 font-semibold leading-relaxed">
        Some Frameworks and Libraries I've been working with
      </p>
    </div>
    <div class="max-w-6xl mx-auto px-8 py-16">
      <div class="relative">
        <div class="swiper-container">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="https://a.slack-edge.com/80588/marketing/img/meta/slack_hash_256.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del Slack -->
                  <svg
                    class="relative"
                    width="200"
                    height="120"
                    viewBox="0 0 200 120"
                  >
                    <path
                      fill="#fff"
                      fill-rule="evenodd"
                      d="M63.75 75.24l2.5-5.93c2.7 2.05 6.3 3.13 9.85 3.13 2.61 0 4.27-1.03 4.27-2.6-.04-4.37-15.7-.95-15.82-11.9-.04-5.58 4.8-9.86 11.66-9.86 4.08 0 8.16 1.03 11.06 3.38l-2.34 6.05c-2.66-1.73-5.97-2.97-9.12-2.97-2.13 0-3.55 1.03-3.55 2.36.04 4.28 15.82 1.94 15.98 12.4 0 5.7-4.72 9.69-11.5 9.69-4.96 0-9.52-1.2-12.99-3.75zm96.01-8.08a7.16 7.16 0 0 1-8.11 3.5 7.35 7.35 0 0 1-5.38-7.13c0-3.34 2.2-6.27 5.38-7.12 3.16-.85 6.5.58 8.11 3.5l6.9-3.93a15.02 15.02 0 0 0-17.03-7.42 15.42 15.42 0 0 0-11.33 14.97c0 7.04 4.66 13.2 11.33 14.97a15.02 15.02 0 0 0 17.04-7.43l-6.9-3.9zM91.71 35.25h8.64v43.16h-8.64V35.25zm78.34 0v43.16h8.65V65.48l10.25 12.93H200l-13.03-15.37 12.06-14.34h-10.58l-9.76 11.9V35.25h-8.64zm-43.82 31.1a8.14 8.14 0 0 1-6.83 3.56 7.24 7.24 0 0 1-7.33-7.16 7.24 7.24 0 0 1 7.33-7.15 8.1 8.1 0 0 1 6.83 3.67v7.08zm0-18v3.4c-1.43-2.36-5-4-8.72-4-7.7 0-13.76 6.64-13.76 14.96 0 8.33 6.07 15.04 13.76 15.04 3.73 0 7.3-1.63 8.72-4v3.4H135v-28.8h-8.77zM10.53 66.4A5.32 5.32 0 0 1 5.3 71.8 5.32 5.32 0 0 1 .04 66.4a5.32 5.32 0 0 1 5.25-5.38h5.25v5.38zm2.63 0a5.32 5.32 0 0 1 5.25-5.38c2.9 0 5.25 2.4 5.25 5.38v13.46a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39V66.4zm5.26-21.63a5.32 5.32 0 0 1-5.25-5.38A5.32 5.32 0 0 1 18.42 34c2.9 0 5.25 2.41 5.25 5.39v5.38h-5.25zm0 2.74c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38H5.25A5.32 5.32 0 0 1 0 52.9a5.32 5.32 0 0 1 5.25-5.39h13.17zm21.03 5.39a5.32 5.32 0 0 1 5.25-5.39c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38h-5.25V52.9zm-2.62 0a5.32 5.32 0 0 1-5.25 5.38 5.32 5.32 0 0 1-5.25-5.38V39.39A5.32 5.32 0 0 1 31.58 34c2.9 0 5.25 2.41 5.25 5.39v13.5zm-5.25 21.58c2.9 0 5.25 2.41 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39v-5.38h5.25zm0-2.7a5.32 5.32 0 0 1-5.25-5.38 5.32 5.32 0 0 1 5.25-5.38h13.17c2.9 0 5.25 2.4 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39H31.58z"
                    />
                  </svg>
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Slack</strong>
                      as a tool for group communication and manage CI/CD of
                      projects.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://slack.com/intl/es-cr"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Slack
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 2 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/jira.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del jira -->
                  <svg
                    class="relative"
                    width="200"
                    height="120"
                    viewBox="0 0 200 120"
                  >
                    <!-- Imagen de fondo -->
                    <image
                      href="./assets/jiratext.png"
                      width="100%"
                      height="100%"
                    />

                    <!-- Path -->
                    <!-- <path
                      fill="#fff"
                      fill-rule="evenodd"
                      d="M63.75 75.24l2.5-5.93c2.7 2.05 6.3 3.13 9.85 3.13 2.61 0 4.27-1.03 4.27-2.6-.04-4.37-15.7-.95-15.82-11.9-.04-5.58 4.8-9.86 11.66-9.86 4.08 0 8.16 1.03 11.06 3.38l-2.34 6.05c-2.66-1.73-5.97-2.97-9.12-2.97-2.13 0-3.55 1.03-3.55 2.36.04 4.28 15.82 1.94 15.98 12.4 0 5.7-4.72 9.69-11.5 9.69-4.96 0-9.52-1.2-12.99-3.75zm96.01-8.08a7.16 7.16 0 0 1-8.11 3.5 7.35 7.35 0 0 1-5.38-7.13c0-3.34 2.2-6.27 5.38-7.12 3.16-.85 6.5.58 8.11 3.5l6.9-3.93a15.02 15.02 0 0 0-17.03-7.42 15.42 15.42 0 0 0-11.33 14.97c0 7.04 4.66 13.2 11.33 14.97a15.02 15.02 0 0 0 17.04-7.43l-6.9-3.9zM91.71 35.25h8.64v43.16h-8.64V35.25zm78.34 0v43.16h8.65V65.48l10.25 12.93H200l-13.03-15.37 12.06-14.34h-10.58l-9.76 11.9V35.25h-8.64zm-43.82 31.1a8.14 8.14 0 0 1-6.83 3.56 7.24 7.24 0 0 1-7.33-7.16 7.24 7.24 0 0 1 7.33-7.15 8.1 8.1 0 0 1 6.83 3.67v7.08zm0-18v3.4c-1.43-2.36-5-4-8.72-4-7.7 0-13.76 6.64-13.76 14.96 0 8.33 6.07 15.04 13.76 15.04 3.73 0 7.3-1.63 8.72-4v3.4H135v-28.8h-8.77zM10.53 66.4A5.32 5.32 0 0 1 5.3 71.8 5.32 5.32 0 0 1 .04 66.4a5.32 5.32 0 0 1 5.25-5.38h5.25v5.38zm2.63 0a5.32 5.32 0 0 1 5.25-5.38c2.9 0 5.25 2.4 5.25 5.38v13.46a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39V66.4zm5.26-21.63a5.32 5.32 0 0 1-5.25-5.38A5.32 5.32 0 0 1 18.42 34c2.9 0 5.25 2.41 5.25 5.39v5.38h-5.25zm0 2.74c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38H5.25A5.32 5.32 0 0 1 0 52.9a5.32 5.32 0 0 1 5.25-5.39h13.17zm21.03 5.39a5.32 5.32 0 0 1 5.25-5.39c2.9 0 5.25 2.41 5.25 5.39a5.32 5.32 0 0 1-5.25 5.38h-5.25V52.9zm-2.62 0a5.32 5.32 0 0 1-5.25 5.38 5.32 5.32 0 0 1-5.25-5.38V39.39A5.32 5.32 0 0 1 31.58 34c2.9 0 5.25 2.41 5.25 5.39v13.5zm-5.25 21.58c2.9 0 5.25 2.41 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39 5.32 5.32 0 0 1-5.25-5.39v-5.38h5.25zm0-2.7a5.32 5.32 0 0 1-5.25-5.38 5.32 5.32 0 0 1 5.25-5.38h13.17c2.9 0 5.25 2.4 5.25 5.38a5.32 5.32 0 0 1-5.25 5.39H31.58z"
                    /> -->
                  </svg>
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Jira</strong>
                      as a project and task management tool, as well as to
                      manage project progress.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://www.atlassian.com/software/jira?&aceid=&adposition=&adgroup=140479881486&campaign=18442480203&creative=656562805651&device=c&keyword=jira&matchtype=e&network=g&placement=&ds_kids=p73335832032&ds_e=GOOGLE&ds_eid=700000001558501&ds_e1=GOOGLE&gad_source=1&gclid=CjwKCAiArfauBhApEiwAeoB7qCrCy1YHSDsLkdA8x07AlC-lvTcpkK7Cbi4up1q6veyK0o8QWFlGhxoCH60QAvD_BwE&gclsrc=aw.ds"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Jira
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 3 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/docker.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del docker -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Docker</strong>
                      as a project container tool providing greater scalability
                      and ease of project management.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://www.docker.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Docker
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 4 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/github.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del github -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Github</strong>
                      as a central platform to manage and collaborate on
                      projects tracking code changes, facilitating team
                      collaboration.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://github.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about GitHub
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 5 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/figma.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del figma -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Figma</strong>
                      as a collaborative design tool to create, prototype, and
                      share user interfaces and experiences.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://www.figma.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Figma
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>

            <!-- skill 6 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/wordpress.png"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del  -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium"
                        >Wordpress</strong
                      >
                      as a content management system and website creator to
                      design, build, and manage websites.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://wordpress.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Wordpress
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <!-- skill 7 -->
            <div class="swiper-slide">
              <div
                class="relative lg:flex rounded-lg shadow-2xl overflow-hidden"
              >
                <div
                  class="h-56 lg:h-auto lg:w-5/12 relative flex items-center justify-center"
                >
                  <img
                    class="absolute h-full w-full object-cover"
                    src="./assets/magento.jpg"
                    alt=""
                  />
                  <div class="absolute inset-0 bg-gray-700 opacity-75"></div>
                  <!-- SVG del  -->
                </div>
                <div class="relative lg:w-7/12 bg-white">
                  <svg
                    class="absolute h-full text-white w-24 -ml-12"
                    fill="currentColor"
                    viewBox="0 0 100 100"
                    preserveAspectRatio="none"
                  >
                    <polygon points="50,0 100,0 50,100 0,100" />
                  </svg>
                  <div
                    class="relative py-12 lg:py-24 px-8 lg:px-16 text-gray-700 leading-relaxed"
                  >
                    <p>
                      I have used
                      <strong class="text-gray-900 font-medium">Magento</strong>
                      as a content management system and website creator to
                      design, build, and manage websites.
                    </p>
                    <p class="mt-6">
                      <a
                        href="https://magento.com"
                        target="_blank"
                        class="font-medium text-indigo-600 hover:text-indigo-900"
                        >&rarr; Learn more about Magento
                      </a>
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- Botones de navegación -->
          <!-- <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div> -->
        </div>
      </div>
    </div>
  </div>

  <div class="banner-1 flex h-full items-center" style="padding-top: 15%">
    <div class="w-7/12 p-12">
      <h2 class="text-gray-700 md:text-6xl text-2xl font-Eczar mb-5 font-bold">
        Let's build a path to success together: innovation and exceptional
        results.
      </h2>
      <a class="underline text-2xl text-blue-600 font-work_sans"
        >📧 djmm171298@gmail.com</a
      >
    </div>
    <div class="w-5/12 pr-28">
      <div class="flex flex-wrap justify-end gap-2">
        <button
          onclick="window.location.href = 'mailto:djmm171298@gmail.com';"
          class="text-white bg-gray-800 submit-button hidden md:block"
        >
          Contact Me
        </button>

        <button
          onclick="window.open('https://www.linkedin.com/in/ian-montero-moya-88a180209/', '_blank')"
          class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded"
        >
          <svg
            class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current"
            role="img"
            viewBox="0 0 256 256"
            xmlns="http://www.w3.org/2000/svg"
          >
            <g>
              <path
                d="M218.123122,218.127392 L180.191928,218.127392 L180.191928,158.724263 C180.191928,144.559023 179.939053,126.323993 160.463756,126.323993 C140.707926,126.323993 137.685284,141.757585 137.685284,157.692986 L137.685284,218.123441 L99.7540894,218.123441 L99.7540894,95.9665207 L136.168036,95.9665207 L136.168036,112.660562 L136.677736,112.660562 C144.102746,99.9650027 157.908637,92.3824528 172.605689,92.9280076 C211.050535,92.9280076 218.138927,118.216023 218.138927,151.114151 L218.123122,218.127392 Z M56.9550587,79.2685282 C44.7981969,79.2707099 34.9413443,69.4171797 34.9391618,57.260052 C34.93698,45.1029244 44.7902948,35.2458562 56.9471566,35.2436736 C69.1040185,35.2414916 78.9608713,45.0950217 78.963054,57.2521493 C78.9641017,63.090208 76.6459976,68.6895714 72.5186979,72.8184433 C68.3913982,76.9473153 62.7929898,79.26748 56.9550587,79.2685282 M75.9206558,218.127392 L37.94995,218.127392 L37.94995,95.9665207 L75.9206558,95.9665207 L75.9206558,218.127392 Z M237.033403,0.0182577091 L18.8895249,0.0182577091 C8.57959469,-0.0980923971 0.124827038,8.16056231 -0.001,18.4706066 L-0.001,237.524091 C0.120519052,247.839103 8.57460631,256.105934 18.8895249,255.9977 L237.033403,255.9977 C247.368728,256.125818 255.855922,247.859464 255.999,237.524091 L255.999,18.4548016 C255.851624,8.12438979 247.363742,-0.133792868 237.033403,0.000790807055"
              ></path>
            </g>
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>
<script>
import Swiper from "swiper";
import "swiper/swiper-bundle.css";
export default {
  data() {
    return {
      showMenu: false,
    };
  },
  mounted() {
    this.call_work();
    this.initSwiper();
  },
  methods: {
    print_Work(title, jobDesc, imageName, company, siteURL) {
      const htmlString = `
      <div class="card">
        <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
          <h4 class="project-title item">${title}</h4>
          <p class="font-work_sans pr-12">${jobDesc}</p>
          <button onclick="window.open('${siteURL}');" target="_blank" class="text-sky-800 font-bold text-2xl tracking-wider">${company}</button>
        </div>
        <div class="card-image bg-green-100">
          <img class="object-cover w-full h-72 md:h-96 " src="src/assets/${imageName}" />
        </div>
      </div>
    `;
      const printDiv = document.querySelector("#work");
      if (printDiv) {
        // Agregar la nueva tarjeta al contenido existente
        printDiv.innerHTML += htmlString;
      } else {
        console.error("Elemento #work no encontrado en el DOM");
      }
    },
    call_work() {
      this.print_Work(
        "Software Engineer",
        "Work with team of developers in the development of backend and frontend solutions for the system that belongs to the company. I had to work with the docker tool to manage the Mysql database images and the main site image, also Github was used as version control. And the site is deployed on AWS . Develop bug fixes and create new backend and frontend feautures, using reactjs and php with Yii frame work. I managed to meet the sprint dates by demonstrating my progress using the scrum methodology.",
        "commandlink.jpg",
        "Commandlink",
        "https://www.commandlink.com"
      );
      this.print_Work(
        "Software Developer",
        "Work with the team of software engineers in the development from scratch of Web applications for clients, using different stacks and different tools. For the development from scratch I used the Docker tool for database and site management, I also got experience in Google Cloud Platform and AWS. Among the stacks that I worked mainly on was Php with its framework Laravel and Mysql as a database, I also managed Python in the backend with Django, withs Sqlite and ReacJS,  finally the last stack I worked on was Java using SpringBoot, with mongo DB, creating an API’s  for a clients. Use CI/CD for each of the projects we work on, creating continuous iterations to manage and meet client deadlines, using tools such as Jira and Slack. I managed to increase the amount of projects that the company could handle since I was able to be in two projects simultaneously as well as meet the expectations of the clients due to the process that is carried out with them in the development of the website. ",
        "dsprocr.jpg",
        "DSpro",
        "https://dspro.tech"
      );
      this.print_Work(
        "Team Lead / Full Stack Developer",
        " As a lead I have been responsible for planning, executing and testing the projects and leading a team of 5 Software Developers. Also I have to develop Web applications in blockchain with javascript, web3 and reactjs. I had a direct relationship with customers and accompany them in the process of creating the Web Application. As a Full Stack developer I had to create resposive sites with diferents stacks as C# with framwork .NET, SQL and bootstrap, also Full stack aplications with php, Mysql, and in the Frontend with VueJS. I Develop  Smarts contracts with solidity to web3 Applications, Also I work and payment API’s as Paypal API or Binance API, among others... I had experience in CRM as a Magento and Wordpress, creating templates and made bug fixes",
        "studios23.jpg",
        "Studios23",
        "https://www.codester.com/studios23"
      );
    },
    initSwiper() {
      new Swiper(".swiper-container", {
        loop: true,
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      });
    },
    async downloadPDF() {
      try {
        const response = await fetch("/assets/resume/resume.pdf");
        const blob = await response.blob();
        const url = window.URL.createObjectURL(blob);

        const link = document.createElement("a");
        link.href = url;
        link.download = "resume.pdf";
        link.click();

        window.URL.revokeObjectURL(url);
      } catch (error) {
        console.error("Error al descargar el PDF:", error);
      }
    },
  },
};
</script>


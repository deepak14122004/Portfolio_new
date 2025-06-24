<script lang="ts">
  import BlurFade from "$lib/components/magic/BlurFade/BlurFade.svelte";
  import InteractiveHover from "$lib/components/magic/InteractiveHover/InteractiveHover.svelte";
  import ShineBorder from "$lib/components/magic/ShineBorder/ShineBorder.svelte";
  import ShimmerButton from "$lib/components/magic/ShimmerButton/ShimmerButton.svelte";
  import RetroGrid from "$lib/components/magic/RetroGrid/RetroGrid.svelte";
  import FeatureCard from "$lib/components/magic/FeatureCard/FeatureCard.svelte";
  import { GraduationCap, BackpackIcon } from "lucide-svelte";
  import Marquee from "$lib/components/magic/Marquee/Marquee.svelte";
  import MagicCard from "$lib/components/magic/MagicCard/MagicCard.svelte";
  import Reviewcard from "$lib/components/magic/Reviewcard/Reviewcard.svelte";
  import { cn } from "$lib/utils";
  import BoxReveal from "$lib/components/magic/BoxReveal/BoxReveal.svelte";
  import OrbitingCircles from "$lib/components/magic/OrbitingCircles";
  import Separator from "$lib/components/ui/separator/separator.svelte";
  const year = new Date().getFullYear();

  let className: any = "";
  export { className as class };

  const projects = [
    {
      name: "CareerSync",
      username: "Project : Under Development",
      body: "A web-based job portal that streamlines hiring through job posting, application tracking, and notifications.",
      stack:
        "Tech Stack : SvelteKit, TypeScript, Tailwind CSS, Shadcn, Firebase",
      link: "https://github.com/deepak14122004/Career_Sync",
      img: "/sveltekit.png",
    },
    {
      name: "Patent",
      username: "Idea and prototype : Published",
      body: "A system designed to detect and prevent alcohol-impaired driving using onboard sensors and smart vehicle integration.",
      stack:
        "Tech Stack : Arduino IDE, C++, Sensors, Smart Vehicle Integration, OBD-II",
      link: "https://github.com/deepak14122004/Patent---202341032600",
      img: "/patent.jpg",
    },
    {
      name: "WeBlog",
      username: "Project : Completed",
      body: "WeBlog is a modern SvelteKit-based blogging platform for creating, managing, and sharing posts with a clean, minimal UI.",
      stack:
        "Tech Stack : SvelteKit, TypeScript, Tailwind CSS, Shadcn, Firebase",
      link: "https://github.com/deepak14122004/WeBlog",
      img: "/sveltekit.png",
    },
    {
      name: "Stock Price Prediction",
      username: "Project : Completed",
      body: "A machine learning model using Bidirectional LSTM to predict stock prices from historical",
      stack:
        "Tech Stack : Python, Jupyter Notebook, Pandas, NumPy, Scikit-learn, Keras",
      link: "https://github.com/deepak14122004/Stock-Price-Prediction",
      img: "/python.jpg",
    },
    {
      name: "QR-Textualize",
      username: "Project : Completed",
      body: "A Java Swing app to generate and decode QR codes for fast, offline text sharing.",
      stack: "Tech Stack : Java, Java Swing, Zxing Library",
      link: "https://github.com/deepak14122004/QRTextualize",
      img: "/java.jpg",
    },
    {
      name: "FinaTips",
      username: "Project : Completed",
      body: "FinaTips is a web-based finance management tool that helps users track budgets, view summaries, and receive personalized financial tips.",
      stack: "Tech Stack : HTML, CSS, JavaScript",
      link: "https://github.com/deepak14122004/FinaTips",
      img: "/html.jpg",
    },
    {
      name: "Construction Management System",
      username: "Idea : Completed",
      body: "A smart Construction Site Management System that uses ARIMA, vibration monitoring, and real-time tracking to optimize asset usage, analyze productivity, and automate infrastructure maintenance.",
      stack: "Tech Stack : Nil (Idea only, no code available)",
      link: "https://github.com/deepak14122004/L-T_Ideathon",
      img: "/idea.jpg",
    },
    {
      name: "Student Database Management System",
      username: "Project : Completed",
      body: "Student Semester Academic Record Manager is a Java-based system for managing student records, grades, and course enrollments across semesters using a relational database.",
      stack: "Tech Stack : Java, JDBC, MySQL",
      link: "https://github.com/deepak14122004/Student-Database-System",
      img: "/java.jpg",
    },
  ];

  let firstRow = projects.slice(0, projects.length / 2);
  let secondRow = projects.slice(projects.length / 2);

  let data = [
    {
      id: 1,
      title: "S R M Institute of Science and Technology",
      content: [
        "B.Tech in Computer Science and Engineering",
        "2022 - 2026",
        "CGPA: 8.5",
      ],

      image: "/srm.jpg",
      icon: GraduationCap,
    },
    {
      id: 2,
      title: "K R M Public School",
      content: ["Higher Secondary Certificate", "2022", "85.2 %"],
      image: "/krm.jpg",
      icon: BackpackIcon,
    },
    {
      id: 3,
      title: "K R M Public School",
      content: ["Secondary School Certificate", "2020", "77.7 %"],
      image: "/krm.jpg",
      icon: BackpackIcon,
    },
  ];
</script>

<div class="bg-[#0f172a] overflow-hidden">
  <div
    class="fixed top-0 left-0 z-50 flex w-full h-20 flex-row items-center justify-center gap-x-8 text-gray-200 backdrop-blur-2xl"
    style="
  mask-image: linear-gradient(to bottom, transparent 0%, black 10%, black 85%, transparent 100%);
  -webkit-mask-image: linear-gradient(to bottom, transparent 0%, black 10%, black 85%, transparent 100%);
"
  >
    <div class="z-10 flex min-h-[16rem] items-center justify-center">
      <ShimmerButton class="shadow-2xl rounded-m" href="#aboutme">
        <span
          class="whitespace-pre-wrap text-center text-sm font-medium leading-none tracking-tight text-white dark:from-white dark:to-slate-900/10 lg:text-lg"
        >
          About Me
        </span>
      </ShimmerButton>
    </div>
    <div class="z-10 flex min-h-[16rem] items-center justify-center">
      <ShimmerButton class="shadow-2xl" href="#education">
        <span
          class="whitespace-pre-wrap text-center text-sm font-medium leading-none tracking-tight text-white dark:from-white dark:to-slate-900/10 lg:text-lg"
        >
          <a href="www.google.com">Education</a>
        </span>
      </ShimmerButton>
    </div>
    <div class="z-10 flex min-h-[16rem] items-center justify-center">
      <ShimmerButton class="shadow-2xl" href="#projects">
        <span
          class="whitespace-pre-wrap text-center text-sm font-medium leading-none tracking-tight text-white dark:from-white dark:to-slate-900/10 lg:text-lg"
        >
          Projects
        </span>
      </ShimmerButton>
    </div>
    <div class="z-10 flex min-h-[16rem] items-center justify-center">
      <ShimmerButton class="shadow-2xl" href="#skills">
        <span
          class="whitespace-pre-wrap text-center text-sm font-medium leading-none tracking-tight text-white dark:from-white dark:to-slate-900/10 lg:text-lg"
        >
          Skills
        </span>
      </ShimmerButton>
    </div>
    <div class="z-10 flex min-h-[16rem] items-center justify-center">
      <ShimmerButton class="shadow-2xl" href="#achievements">
        <span
          class="whitespace-pre-wrap text-center text-sm font-medium leading-none tracking-tight text-white dark:from-white dark:to-slate-900/10 lg:text-lg"
        >
          Achievements
        </span>
      </ShimmerButton>
    </div>
    <div class="z-10 flex min-h-[16rem] items-center justify-center">
      <ShimmerButton class="shadow-2xl" href="#contactme">
        <span
          class="whitespace-pre-wrap text-center text-sm font-medium leading-none tracking-tight text-white dark:from-white dark:to-slate-900/10 lg:text-lg"
        >
          Contact Me
        </span>
      </ShimmerButton>
    </div>
  </div>
  <div class="flex flex-col items-center justify-center gap-20">
    <div class="flex items-center justify-center h-screen w-screen">
      <ShineBorder
        class="max-w-3xl rounded-4xl"
        borderRadius={32}
        duration={12}
        color={["#6366F1", "#94A3B8"]}
      >
        <div class="relative p-4 flex items-center gap-x-5">
          <img
            src="/deepak.jpeg"
            alt="Deepak"
            class="h-80 w-64 bg-gray-50 rounded-3xl"
          />
          <div class="text-sm leading-5">
            <div>
              <BlurFade delay={0.25}>
                <h3
                  class="mt-3 text-lg font-semibold leading-6 text-gray-200 group-hover:text-gray-50"
                >
                  <span class="absolute inset-0"></span>
                  <div class="text-4xl">Yalavarthi Venkata Sai Deepak</div>
                </h3>
              </BlurFade>
              <br />
              <BlurFade delay={2 * 0.25}>
                <p class="text-sm text-gray-400"></p>
                <p class="text-l">Turning ideas into impactful solutions.</p>

                <br />
                <p class="text-m text-gray-400">
                  Developer • Engineer • Patent Holder
                </p>
              </BlurFade>
              <br />
              <br />
              <BlurFade delay={4 * 0.25}>
                <div class="flex items-center gap-20 justify-center">
                  <InteractiveHover
                    text="Resume"
                    class="w-[170px]"
                    href="https://drive.google.com/file/d/1A-J5zCNdaxGb2tcNo75Zqy-wBZe73NRZ/view?usp=sharing"
                  ></InteractiveHover>
                  <InteractiveHover
                    text="Contact me"
                    class="w-[170px]"
                    href="mailto:yvsdeepak@gmail.com"
                  ></InteractiveHover>
                </div>
              </BlurFade>
            </div>
          </div>
        </div>
      </ShineBorder>
    </div>

    <div class="flex items-center justify-center w-screen">
      <div
        id="aboutme"
        class="relative flex flex-col max-w-6xl items-center justify-center overflow-hidden rounded-lg border bg-background p-20 md:shadow-xl"
      >
        <div>
          <h1 class="text-4xl">About Me</h1>

          <br />
          <p class="text-justify">
            A passionate Computer Science undergraduate with a strong foundation
            in software development, full-stack web technologies, and machine
            learning. Known for building practical, user-focused solutions and
            exploring innovative ideas — including filing a patent for an
            automotive safety system. Continuously learning, experimenting, and
            contributing to meaningful tech projects.
          </p>
        </div>

        <RetroGrid />
      </div>
    </div>

    <div
      class="flex flex-col items-center justify-center w-screen pt-16"
      id="education"
    >
      <h1 class="text-4xl">Education</h1>
      <FeatureCard {data} />
    </div>

    <div
      class="flex flex-col items-center justify-center w-screen pt-16"
      id="projects"
    >
      <h1 class="text-4xl">Projects</h1>
      <br />
      <h1>Click on the cards to to view the github repo</h1>
      <br />
      <br />
      <div
        class="relative flex h-full w-full flex-col items-center justify-center overflow-hidden rounded-lg border bg-background py-10 md:shadow-xl"
      >
        <Marquee pauseOnHover class="[--duration:20s]">
          {#each firstRow as item}
            <Reviewcard {...item} />
          {/each}
        </Marquee>
        <br />
        <Marquee reverse pauseOnHover class="[--duration:20s]">
          {#each secondRow as item}
            <Reviewcard {...item} />
          {/each}
        </Marquee>
        <div
          class="pointer-events-none absolute inset-y-0 left-0 w-1/3 bg-gradient-to-r from-white dark:from-background"
        ></div>
        <div
          class="pointer-events-none absolute inset-y-0 right-0 w-1/3 bg-gradient-to-l from-white dark:from-background"
        ></div>
      </div>
    </div>
    <div
      class="flex flex-col items-center justify-center w-full pt-16"
      id="skills"
    >
      <h1 class="text-4xl">Tech Stack</h1>
      <br />
      <div class="flex flex-row items-center justify-center w-full max-w-6xl">
        <div
          class={cn(
            "relative flex h-[400px] w-full max-w-[26rem] items-center justify-center overflow-hidden rounded-tl-4xl border bg-background md:shadow-xl",
            className
          )}
        >
          <span
            class="pointer-events-none whitespace-pre-wrap bg-gradient-to-b from-black to-gray-300/80 bg-clip-text text-center text-6xl font-semibold leading-none text-transparent dark:from-white dark:to-slate-900/10"
          >
            Languages
          </span>

          <!--  Inner Circles  -->
          <OrbitingCircles
            class="h-[40px] w-[40px] border-none bg-transparent"
            duration={20}
            radius={80}
          >
            <img
              src="/python-svg.svg"
              alt="python"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[40px] w-[40px] border-none bg-transparent"
            duration={20}
            radius={80}
            delay={-14}
          >
            <img src="/java-svg.svg" alt="java" class="h-8 w-8 rounded-full" />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[40px] w-[40px] border-none bg-transparent"
            duration={20}
            radius={80}
            delay={-7}
          >
            <img
              src="/js-svg.svg"
              alt="js"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>

          <!-- Outer Circles (reverse)  -->
          <OrbitingCircles
            class="h-[50px] w-[50px] border-none bg-transparent"
            radius={160}
            duration={20}
            reverse
          >
            <img
              src="/ts-svg.svg"
              alt="ts"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[50px] w-[50px] border-none bg-transparent"
            radius={160}
            duration={20}
            delay={-7}
            reverse
          >
            <img
              src="/c-svg.svg"
              alt="c"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[50px] w-[50px] border-none bg-transparent"
            radius={160}
            duration={20}
            delay={-14}
            reverse
          >
            <img
              src="/cpp-svg.svg"
              alt="cpp"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
        </div>
        <div
          class={cn(
            "relative flex h-[400px] w-full max-w-[26rem] items-center justify-center overflow-hidden rounded-tr-4xl border bg-background md:shadow-xl",
            className
          )}
        >
          <span
            class="pointer-events-none whitespace-pre-wrap bg-gradient-to-b from-black to-gray-300/80 bg-clip-text text-center text-7xl font-semibold leading-none text-transparent dark:from-white dark:to-slate-900/10"
          >
            WebDev
          </span>

          <!--  Inner Circles  -->
          <OrbitingCircles
            class="h-[40px] w-[40px] border-none bg-transparent"
            duration={20}
            radius={80}
          >
            <img
              src="/svelte-svg.svg"
              alt="svelte"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[40px] w-[40px] border-none bg-transparent"
            duration={20}
            radius={80}
            delay={-14}
          >
            <img
              src="/html-svg.svg"
              alt="html"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[40px] w-[40px] border-none bg-transparent"
            duration={20}
            radius={80}
            delay={-7}
          >
            <img
              src="/css-svg.svg"
              alt="css"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>

          <!-- Outer Circles (reverse)  -->
          <OrbitingCircles
            class="h-[50px] w-[50px] border-none bg-transparent"
            radius={160}
            duration={20}
            reverse
          >
            <img
              src="/bootstrap-svg.svg"
              alt="bootstrap"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[50px] w-[50px] border-none bg-transparent"
            radius={160}
            duration={20}
            delay={-7}
            reverse
          >
            <img
              src="/tailwind-svg.svg"
              alt="tailwind"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[50px] w-[50px] border-none bg-transparent"
            radius={160}
            duration={20}
            delay={-14}
            reverse
          >
            <img
              src="/firebase-svg.svg"
              alt="firebase"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
        </div>
      </div>
      <div class="flex flex-row items-center justify-center w-full max-w-6xl">
        <div
          class={cn(
            "relative flex h-[400px] w-full max-w-[26rem] items-center justify-center overflow-hidden border bg-background md:shadow-xl rounded-bl-4xl",
            className
          )}
        >
          <span
            class="pointer-events-none whitespace-pre-wrap bg-gradient-to-b from-black to-gray-300/80 bg-clip-text text-center text-8xl font-semibold leading-none text-transparent dark:from-white dark:to-slate-900/10"
          >
            ML/DS
          </span>

          <!--  Inner Circles  -->
          <OrbitingCircles
            class="h-[30px] w-[30px] border-none"
            duration={20}
            radius={80}
          >
            <!-- Open AI -->
            <img
              src="/numpy-svg.svg"
              alt="numpy"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[30px] w-[30px] border-none bg-transparent"
            duration={20}
            radius={80}
            delay={-10}
          >
            <img
              src="/pandas-svg.svg"
              alt="pandas"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>

          <!-- Outer Circles (reverse)  -->
          <OrbitingCircles
            class="h-[45px] w-[45px] border-none bg-transparent"
            radius={160}
            duration={20}
            reverse
          >
            <img
              src="/keras-svg.svg"
              alt="keras"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[45px] w-[45px] border-none bg-transparent"
            radius={160}
            duration={20}
            delay={-10}
            reverse
          >
            <img
              src="/matplotlib-svg.png"
              alt="matplotlib"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
        </div>
        <div
          class={cn(
            "relative flex h-[400px] w-full max-w-[26rem] items-center justify-center overflow-hidden rounded-br-4xl border bg-background md:shadow-xl",
            className
          )}
        >
          <span
            class="pointer-events-none whitespace-pre-wrap bg-gradient-to-b from-black to-gray-300/80 bg-clip-text text-center text-8xl font-semibold leading-none text-transparent dark:from-white dark:to-slate-900/10"
          >
            Tools
          </span>

          <!--  Inner Circles  -->
          <OrbitingCircles
            class="h-[30px] w-[30px] border-none bg-transparent"
            duration={20}
            radius={80}
          >
            <img
              src="/github-svg.svg"
              alt="github"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[30px] w-[30px] border-none bg-transparent"
            duration={20}
            radius={80}
            delay={-10}
          >
            <img
              src="/jupyter-svg.svg"
              alt="jupyter"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>

          <!-- Outer Circles (reverse)  -->
          <OrbitingCircles
            class="h-[45px] w-[45px] border-none bg-transparent"
            radius={160}
            duration={20}
            reverse
          >
            <img
              src="/vscode-svg.svg"
              alt="vscode"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
          <OrbitingCircles
            class="h-[45px] w-[45px] border-none bg-transparent"
            radius={160}
            duration={20}
            delay={-10}
            reverse
          >
            <img
              src="/arduino-svg.svg"
              alt="arduino"
              class="h-8 w-8 rounded-full bg-white"
            />
          </OrbitingCircles>
        </div>
      </div>
    </div>
    <div class="flex flex-col items-center justify-center w-screen pt-16">
      <div>
        <h1 class="text-4xl">SoftSkills</h1>
      </div>
      <div
        class="flex flex-wrap justify-center items-center w-full pt-8 text-xl gap-4 text-center"
      >
        <BoxReveal boxColor={"#5046e6"} duration={0.5}>
          <div>Problem Solving</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#f59e0b"} duration={0.5}>
          <div>Teamwork</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#ec4899"} duration={0.5}>
          <div>Communication</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#14b8a6"} duration={0.5}>
          <div>Adaptability</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#8b5cf6"} duration={0.5}>
          <div>Time Management</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#f97316"} duration={0.5}>
          <div>Critical Thinking</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#0ea5e9"} duration={0.5}>
          <div>Leadership</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#eab308"} duration={0.5}>
          <div>Creativity</div>
        </BoxReveal>
        <p>|</p>
        <BoxReveal boxColor={"#f43f5e"} duration={0.5}>
          <div>Attention to Detail</div>
        </BoxReveal>
      </div>
    </div>
    <div
      class="flex flex-col items-center justify-center w-screen pt-16 gap-10"
      id="achievements"
    >
      <div>
        <h1 class="text-4xl">Achievements and Certifications</h1>
        <br />
        <h1 class="text-center">Click on the card for details</h1>
      </div>
      <div
        class="flex flex-col items-center justify-center w-full gap-4 max-w-5xl"
      >
        <!-- 🌿 Mint Green (Soft) -->
        <MagicCard
          class="cursor-pointer flex-col items-center justify-center shadow-2xl whitespace-nowrap text-xl group hover:border-[#7FFFD4] transition-all duration-300"
          gradientColor="#7FFFD4"
          gradientSize={300}
        >
          <div
            class="group-hover:text-[#7FFFD4] transition-all duration-500 flex gap-1.5 justify-center items-center font-semibold h-5"
          >
            <img
              src="/patent-svg.svg"
              alt="patent_logo"
              class="size-10 mt-1.5"
            />
            <a
              href="https://github.com/deepak14122004/Patent---202341032600"
              target="_blank">Patent - GitHub</a
            >
          </div>
        </MagicCard>

        <!-- 🍊 Soft Orange -->
        <MagicCard
          class="cursor-pointer flex-col items-center justify-center shadow-2xl whitespace-nowrap text-xl group hover:border-[#F4A261] transition-all duration-300"
          gradientColor="#F4A261"
          gradientSize={300}
        >
          <div
            class="group-hover:text-[#F4A261] transition-all duration-500 flex gap-1.5 justify-center items-center font-semibold h-5"
          >
            <img src="/edge-svg.png" alt="edge_logo" class="size-10 mt-1.5" />
            <a
              href="https://drive.google.com/file/d/1IkrS4nbJPhnbGwQA_2hOL7zVbGBf5e1U/view?usp=sharing"
              target="_blank"
            >
              Edge Computing (NPTEL) (Silver Badge) - Certificate
            </a>
          </div>
        </MagicCard>

        <!-- ☀️ Soft Yellow -->
        <MagicCard
          class="cursor-pointer flex-col items-center justify-center shadow-2xl whitespace-nowrap text-xl group hover:border-[#F6E05E] transition-all duration-300"
          gradientColor="#F6E05E"
          gradientSize={300}
        >
          <div
            class="group-hover:text-[#F6E05E] transition-all duration-500 flex gap-1.5 justify-center items-center font-semibold h-5"
          >
            <img src="/os-svg.png" alt="os_logo" class="size-10 mt-1.5" />
            <a
              href="https://drive.google.com/file/d/13-PLexiJf4IrWYs-Yaa0YxEo2rCQ0Cjw/view?usp=sharing"
              target="_blank"
            >
              Introduction to Operating Systems (NPTEL) (Top 5%) - Certificate
            </a>
          </div>
        </MagicCard>

        <!-- 🟣 Soft Magenta -->
        <MagicCard
          class="cursor-pointer flex-col items-center justify-center shadow-2xl whitespace-nowrap text-xl group hover:border-[#D8B4FE] transition-all duration-300"
          gradientColor="#D8B4FE"
          gradientSize={300}
        >
          <div
            class="group-hover:text-[#D8B4FE] transition-all duration-500 flex gap-1.5 justify-center items-center font-semibold h-5"
          >
            <img src="/algo-svg.png" alt="algo_logo" class="size-10 mt-1.5" />
            <a
              href="https://drive.google.com/file/d/19LECDo2_DXt2HmN92POZ5z5uRz-5doTg/view?usp=sharing"
              target="_blank"
            >
              Fundamental Algorithms : Design and Analysis (NPTEL) - Certificate
            </a>
          </div>
        </MagicCard>

        <!-- 🔵 Soft Indigo -->
        <MagicCard
          class="cursor-pointer flex-col items-center justify-center shadow-2xl whitespace-nowrap text-xl group hover:border-[#A5B4FC] transition-all duration-300"
          gradientColor="#A5B4FC"
          gradientSize={300}
        >
          <div
            class="group-hover:text-[#A5B4FC] transition-all duration-500 flex gap-1.5 justify-center items-center font-semibold h-5"
          >
            <img
              src="/python-svg.svg"
              alt="python_logo"
              class="size-10 mt-1.5"
            />
            <a
              href="https://drive.google.com/file/d/1AFb3XVQdl6HA5GGon4wV-DFNrvEQoAp8/view?usp=sharing"
              target="_blank"
            >
              Programming Data Structures and Algorithms in Python (NPTEL) -
              Certificate
            </a>
          </div>
        </MagicCard>

        <!-- 💗 Soft Pink -->
        <MagicCard
          class="cursor-pointer flex-col items-center justify-center shadow-2xl whitespace-nowrap text-xl group hover:border-[#F9A8D4] transition-all duration-300"
          gradientColor="#F9A8D4"
          gradientSize={300}
        >
          <div
            class="group-hover:text-[#F9A8D4] transition-all duration-500 flex gap-1.5 justify-center items-center font-semibold h-5"
          >
            <img
              src="/networks-svg.png"
              alt="networks_logo"
              class="size-10 mt-1.5"
            />
            <a
              href="https://drive.google.com/file/d/1mB0ehYjPFJuA_S3VPQJQFOyIBtmGiOdW/view?usp=sharing"
              target="_blank"
            >
              Demystifying Networking (NPTEL) - Certificate
            </a>
          </div>
        </MagicCard>

        <!-- 🌱 Soft Lime -->
        <MagicCard
          class="cursor-pointer flex-col items-center justify-center shadow-2xl whitespace-nowrap text-xl group hover:border-[#BBF7D0] transition-all duration-300"
          gradientColor="#BBF7D0"
          gradientSize={300}
        >
          <div
            class="group-hover:text-[#BBF7D0] transition-all duration-500 flex gap-1.5 justify-center items-center font-semibold h-5"
          >
            <img src="/ml-svg.png" alt="ml_logo" class="size-10 mt-1.5" />
            <a
              href="https://drive.google.com/file/d/1LVu375hmFfBAjtMXr7nO1Tnk-Af1m-qJ/view?usp=sharing"
              target="_blank"
            >
              Introduction to Machine Learning (NPTEL) - Certificate
            </a>
          </div>
        </MagicCard>
      </div>
    </div>

    <div
      class="flex flex-col items-center w-screen justify-between"
      id="contactme"
    >
      <footer
        class="w-screen bg-background text-muted-foreground border-t justify-between"
      >
        <div
          class="flex flex-col md:flex-row items-center justify-between mx-auto p-8 max-w-7xl"
        >
          <div>
            <h1 class="font-semibold text-3xl text-foreground mb-3">
              Y V S Deepak
            </h1>

            <p>
              <img
                src="/phone-clr.webp"
                alt="Phone"
                class="h-5 w-5 inline-block"
              /> +91 8778307453
            </p>
            <p>
              <img
                src="/location-clr.png"
                alt="location"
                class="h-5 w-5 inline-block"
              /> Chennai
            </p>
          </div>
          <div class="top-0">
            <h1 class="font-semibold text-3xl text-foreground mb-3">Socials</h1>
            <div class="flex flex-row gap-4">
              <div>
                <a
                  href="mailto:yvsdeepak@gmail.com"
                  target="_blank"
                  class="hover:text-foreground transition"
                >
                  <img
                    src="/gmail-clr.webp"
                    alt="gmail"
                    class="h-10 w-12 inline-block transition-transform duration-300 hover:scale-150"
                  />
                </a>
              </div>
              <div>
                <a
                  href="https://www.linkedin.com/in/venkata-sai-deepak-yalavarthi-925ab9327/e"
                  target="_blank"
                  class="hover:text-foreground transition"
                >
                  <img
                    src="/linedin-clr.webp"
                    alt="linkedin"
                    class="h-10 w-10 inline-block transition-transform duration-300 hover:scale-150"
                  />
                </a>
              </div>
              <div>
                <a
                  href="https://github.com/deepak14122004"
                  target="_blank"
                  class="hover:text-foreground transition"
                >
                  <img
                    src="/github-clr.webp"
                    alt="github"
                    class="h-10 w-10 inline-block transition-transform duration-300 hover:scale-150"
                  />
                </a>
              </div>
              <div>
                <a
                  href="https://leetcode.com/u/Deepak141204/"
                  target="_blank"
                  class="hover:text-foreground transition"
                >
                  <img
                    src="/leetcode-clr.png"
                    alt="leetcode"
                    class="h-10 w-10 inline-block transition-transform duration-300 hover:scale-150"
                  />
                </a>
              </div>
              <div>
                <a
                  href="https://codeforces.com/profile/Deepak141204"
                  target="_blank"
                  class="hover:text-foreground transition"
                >
                  <img
                    src="/cf-clr.webp"
                    alt="cf"
                    class="h-10 w-10 inline-block transition-transform duration-300 hover:scale-150"
                  />
                </a>
              </div>
              <div>
                <a
                  href="https://www.instagram.com/_.deepak1412._/"
                  target="_blank"
                  class="hover:text-foreground transition"
                >
                  <img
                    src="/insta-clr.png"
                    alt="insta"
                    class="h-10 w-10 inline-block transition-transform duration-300 hover:scale-150"
                  />
                </a>
              </div>
            </div>
          </div>
        </div>
      </footer>
    </div>
  </div>
</div>

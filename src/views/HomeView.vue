<script setup>
import ExperienceItem from "../components/ExperienceItem.vue";
import EducationItem from "../components/EducationItem.vue";
import TechItem from "../components/TechItem.vue";
import InterestItem from "../components/InterestItem.vue";
import ProfileItem from "@/components/ProfileItem.vue";
import TrophyItem from "@/components/TrophyItem.vue";
import CertificateItem from "@/components/CertificateItem.vue";
import LanguageItem from "@/components/LanguageItem.vue";

//import DocumentationIcon from "./icons/IconDocumentation.vue";
//import ToolingIcon from "./icons/IconTooling.vue";
//import EcosystemIcon from "./icons/IconEcosystem.vue";
//import CommunityIcon from "./icons/IconCommunity.vue";
//import SupportIcon from "./icons/IconSupport.vue";
</script>

<template>
	<main class="container mx-auto my-8 font-sans text-gray-700 [&>hr]:border-slate-600/50 [&>hr]:my-8">
		<section class="resume-section" id="profile">
			<ProfileItem
				first_name="José"
				last_name="Romão"
				email="jscromao@gmail.com"
				:phonecountry="351"
				:phonenumber="913856080"
				location="Lisbon, Portugal"
			>
				<template #socials>
					<div class="social-icons flex flex-row gap-x-2 h-8 [&_*]:h-full">
						<!--<a class="social-icon" href="#!"><i class="fab fa-linkedin-in"></i></a>-->
						<a class="social-icon" target="_blank" href="https://github.com/jscromao"><i class="fab fa-github"></i></a>
						<a class="social-icon" target="_blank" href="https://x.com/majoreon"><i class="fab fa-twitter"></i></a>
						<a class="social-icon" target="_blank" href="https://instagram.com/majoreontv"><i class="fab fa-instagram"></i></a>
						<a class="social-icon" target="_blank" href="https://twitch.tv/majoreon"><i class="fab fa-twitch"></i></a>
					</div>
				</template>

				<h3 class="font-semibold text-xl">Web Developer &amp; Streamer</h3>
				<p class="lead mb-5">
					💻 Grew up Tech Curious in the 90s <br />
					💜 Passionate Coder & Gamer <br />
					🔨 Into building things
				</p>
			</ProfileItem>
		</section>

		<hr class="border-red-400" />

		<section class="resume-section [&_ul]:list-disc" id="traits">
			<h2 class="mb-5 text-5xl text-green-900/90 uppercase font-[700]">Traits &amp; Summary</h2>

			<ul class="fa-ul mb-0 !list-none text-lg">
				<li>
					<span class="fa-li"><i class="fas fa-person-running"></i></span>
					<span>Entrepreneurial spirit, with experience in self-motivation and project management.</span><br />
					<span>Enjoys a good challenge.</span>
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-bars-progress"></i></span>
					<span class=""
						>Practically experienced in collaboration within Agile and Scrum environments and iterative cycle approaches.</span
					><br />
					<span> Capable of adapting to a project's needs. </span>
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-laptop-code"></i></span>
					<span class=""> Proven ability to transition between various programming languages, paradigms and environments. </span
					><br />
					<span class="">
						Decent background in Web Development, with some full-stack experience in and a focus on backend dev. </span
					><br />
					<span class=""
						>Extensive experience in PHP, JavaScript and TypeScript, and several versions of well-known frameworks.
					</span>
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-gear"></i></span>
					<span class=""> Developed & sold, both native & third-party integrated custom widgets for Twitch streams. </span>
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-hammer"></i></span>
					<span class="">
						Created a sizeable project in a Node.js environment for a Streaming-adjacent platform with distinctive features and
						third-party API integrations.
					</span>
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-flask"></i></span>
					<span class=""
						>Experimenting in Python with Unsupervised Machine Learning models for clustering & recommendations.</span
					>
				</li>
			</ul>
		</section>

		<hr class="border-red-400" />

		<section class="resume-section [&_ul]:list-disc" id="experience">
			<h2 class="mb-5 text-5xl text-green-900/90 uppercase font-[700]">Work Experience</h2>

			<div
				class="flex flex-col gap-y-5 [&>*]:pb-5 [&>*]:border-dashed [&>*]:border-b [&>*]:border-slate-400/40 [&>*:last-child]:pb-0 [&>*:last-child]:border-none pt-1"
			>
				<ExperienceItem>
					<template #position>Academic Internship ➡ Junior Dev (Java)</template>
					<template #company>Novabase Engineering Solutions</template>
					<template #timeline>2010-2012</template>

					<ul>
						<li>Worked on planning and coding portions of Novabase's Governmental bid for a TGV infotainment system.</li>
						<li>Viability study to feature Contactless NFC for the train's infotainment systems.</li>
						<li>
							Primarily focused on intranet infrastructure aboard the train, some low-level communications in Java and
							participated in client projects helping establish custom API's.
						</li>
						<li>Achieved the highest grade that year, amongst any students in said academic internship.</li>
					</ul>
				</ExperienceItem>

				<ExperienceItem>
					<template #position>Full-stack Web Dev (PHP + JS)</template>
					<template #company>Personal Business, Self-Employed</template>
					<template #timeline>2013-2016</template>

					<ul>
						<li>Worked on various freelance web development projects, in PHP (2+ years)</li>
						<li>
							Used custom (6mo.) & several other PHP frameworks: Symfony (6mo.), Yii (1.5yr.) & a very early version of
							Laravel (~3mo.).
						</li>
						<li>Used both MySQL and PostgreSQL, with and without ORM.</li>
						<li>
							Experience in full-stack development (with a backend focus in PHP) and mild experience in front-end development,
							both with Native JS and React.
						</li>
					</ul>
				</ExperienceItem>

				<ExperienceItem>
					<template #position>Partnered Streamer, Content Creator</template>
					<template #company>@Majoreon, Twitch - Amazon</template>
					<template #timeline>2016-2022</template>

					<ul>
						<li>
							Early Twitch consumer (2014), turned Streamer (Jan 2016), Partnered soon after (Nov.), Full-time Content Creator
							through 2016 to later 2022.
						</li>
						<li>
							Relevance: Also designed various custom widgets for Stream engagement (using JS & optimal solutions for the
							problems - SVG, CSS, Canvas & Web Components, Also experimented with React and Vue.js for this).
						</li>
						<li>Experienced with streaming-related tools & their basic scripting in Python.</li>
					</ul>
				</ExperienceItem>

				<ExperienceItem>
					<template #position>Full-stack Web Dev (TS, Node.js, Solid.js)</template>
					<template #company>N/A (TBD - MVP in the near-future)</template>
					<template #timeline>2022-2024</template>

					<ul>
						<li>
							Working on a big Full-stack project: Content Creation Assistance & Management platform with various
							tools/features (for the Stream ecosystem - currently Twitch, YT soon to follow) like CMS, CRM, Event Planning &
							Calendar, Content Management, Socials Management, Monetization Assistance and more.
						</li>
						<li>
							Full-stack development using TypeScript within Node.js (Express, Passport, Socket.io) and MongoDB, with a focus
							on performant code & queries, no ORM or overly abstracted libraries.
						</li>
						<li>
							Frontend development with TypeScript and Solid.js for enhanced reactivity. Solid was chosen for simple and
							performant reactive primitives.
						</li>
						<li>
							Large amount of Third-party API development & other tech choices: offloading heavier computations with threads
							and to other Microservices, using message queueing and realtime communication through Socket.io for some
							aspects.
						</li>
						<li>Game Recommendation tool has prompted some Machine Learning Python work as well.</li>
					</ul>
				</ExperienceItem>
			</div>
		</section>

		<hr class="m-0" />

		<section class="resume-section [&_ul]:list-disc" id="education">
			<h2 class="mb-5 text-5xl text-green-900/90 uppercase font-[700]">Education</h2>

			<div>
				<EducationItem>
					<template #school>Faculdade de Ciências e Tecnologia</template>
					<template #degree>Bachelor of Computer Science (BSc in CS)</template>
					<template #graduation>2010</template>

					<ul>
						<li>
							Several MSc-level classes finished: Database Systems, Distributed Systems, Development of Web Applications,
							Concurrent Programming, Artificial Intelligence
						</li>
						<li>Developed custom MVC framework in PHP for college project in DAW, receiving the highest grade.</li>
						<li>
							Several classes in Databases, Distributed Systems as well as the above project all used sanitized performant SQL
							queries, no ORM.
						</li>
						<li>Used Java, C++, C, JavaScript & SQL heavily as well as Python, PHP, Pascal & OCaml on occasion</li>
					</ul>
				</EducationItem>
			</div>
		</section>

		<hr class="m-0" />

		<section class="resume-section" id="skills">
			<h2 class="mb-5 text-5xl text-green-900/90 uppercase font-[700]">Skills</h2>

			<div class="flex flex-col gap-y-10">
				<div class="grid grid-cols-3 gap-3 lg:grid-cols-6 lg:gap-6">
					<TechItem tech="Laravel" icon="fa-laravel" :recency="40" :proficiency="75" />
					<TechItem tech="React" icon="fa-react" :recency="60" :proficiency="90" />
					<TechItem tech="Vue.js" icon="fa-vuejs" :recency="80" :proficiency="80" />
					<TechItem tech="Angular" icon="fa-angular" :recency="15" :proficiency="66" />
					<TechItem tech="Svelte" :recency="90" :proficiency="95" />
					<TechItem tech="Solid" :recency="100" :proficiency="99" />
				</div>

				<div class="grid grid-cols-3 gap-3 lg:grid-cols-6 lg:gap-6">
					<TechItem tech="JavaScript" icon="fa-js-square" :recency="99" :proficiency="99" />
					<TechItem tech="PHP" icon="fa-php" :recency="45" :proficiency="90" />
					<TechItem tech="Java" icon="fa-java" :recency="38" :proficiency="80" />
					<TechItem tech="Python" icon="fa-python" :recency="80" :proficiency="80" />
					<TechItem tech="Rust" icon="fa-rust" :recency="70" :proficiency="75" />
					<TechItem tech="C#" :recency="15" :proficiency="66" />
				</div>

				<div class="grid grid-cols-3 gap-3 lg:grid-cols-6 lg:gap-6">
					<TechItem tech="HTML5" icon="fa-html5" :recency="99" :proficiency="99" />
					<TechItem tech="CSS3" icon="fa-css3-alt" :recency="95" :proficiency="90" />
					<TechItem tech="NPM" icon="fa-npm" :recency="99" :proficiency="95" />
					<TechItem tech="Node.js" icon="fa-node-js" :recency="99" :proficiency="90" />
				</div>
			</div>

			<div class="subheading mb-3">Workflow</div>
			<ul class="fa-ul mb-0">
				<li>
					<span class="fa-li"><i class="fas fa-check"></i></span>
					Mobile-First, Responsive Design
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-check"></i></span>
					Cross Browser Testing & Debugging
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-check"></i></span>
					Cross Functional Teams
				</li>
				<li>
					<span class="fa-li"><i class="fas fa-check"></i></span>
					Agile Development & Scrum
				</li>
			</ul>
		</section>

		<hr class="m-0" />

		<section class="resume-section" id="languages">
			<h2 class="mb-5 text-5xl text-green-900/90 uppercase font-[700]">Languages</h2>

			<ul class="fa-ul mb-0 flex !flex-row gap-x-10">
				<LanguageItem lang="Portuguese" :level="100" extrainfo="Native" :inList="true" />
				<LanguageItem lang="English" :level="99" extrainfo="Near Native" :inList="true" />
				<LanguageItem lang="Spanish" :level="40" :inList="true" />
				<LanguageItem lang="French" :level="25" :inList="true" class="hidden" />
			</ul>
		</section>
		<hr class="m-0" />

		<section class="resume-section" id="interests">
			<h2 class="mb-5 text-5xl text-green-900/90 uppercase font-[700]">Interests</h2>

			<div class="flex flex-col gap-y-2">
				<InterestItem>
					<template #interest>Gaming</template>
					<template #icon><i class="fas fa-gamepad"></i></template>
					<template #description>
						<span
							>Fell in love with gaming from the very first moment I pressed a key and a character moved on-screen, back when
							I was 5yo.</span
						>
					</template>
				</InterestItem>
				<InterestItem>
					<template #interest>Programming</template>
					<template #icon><i class="fas fa-laptop-code"></i></template>
					<template #description>
						<span>A programmer who actually loves to code? 🤓 NERD!</span>
						<br />
						<span>I know, but I've kinda loved it ever since I was a kid due to my interest in...</span>
					</template>
				</InterestItem>
				<InterestItem>
					<template #interest>Game Development&nbsp;<i class="fas fa-laptop-code"></i></template>
					<template #icon><i class="fas fa-gamepad"></i></template>
					<template #description>
						<span
							>I've been into game development on &amp; off, ever since I started learning programming back when I was 9, so I
							could try and make my own games.</span
						>
					</template>
				</InterestItem>
				<InterestItem>
					<template #interest>Streaming</template>
					<template #icon><i class="fab fa-twitch"></i></template>
					<template #description>
						<span
							>Early bird Youtube user from 2006, and early to Twitch watching from 2014 - stumbled into a Streamer in Jan.
							2016 and Partnered soon after in Nov.</span
						><br />
						<span
							>Having always had <em>the bug</em> for Creating, Content Creation was no exception. Went Full-time as a Creator
							through 2016 to later 2022 and I still very much like to hang out with a community and hopefully make people's
							day a bit better for it, if I can.</span
						>
					</template>
				</InterestItem>
				<InterestItem>
					<template #interest>Nature</template>
					<template #icon><i class="fas fa-tree"></i></template>
					<template #description>
						<span
							>When you spend as much time lost in code and tech as I do, it just feels good to take some of it offline to
							appreciate being surrounded by Nature and help keep it pure.</span
						>
					</template>
				</InterestItem>
			</div>
		</section>

		<hr class="m-0" />

		<section class="resume-section" id="merits">
			<h2 class="mb-5 text-5xl text-green-900/90 uppercase font-[700]">Merits</h2>

			<ul class="fa-ul mb-0 text-lg">
				<TrophyItem
					place="1st Place (Solo)"
					entity="Colégio Manuel Bernardes (High School)"
					subject="IIT Java Programming Competition"
					timeline="2001 & 2002"
					:inList="true"
				/>
				<TrophyItem
					place="3rd Place (Team)"
					entity="FCT - Universidade Nova de Lisboa"
					subject="Hackathon"
					timeline="2005"
					:inList="true"
				/>
				<TrophyItem
					place="2nd Place (Team of 2)"
					entity="FCT - Universidade Nova de Lisboa"
					subject="Introductory Robotics Jam"
					timeline="2005"
					:inList="true"
				/>
				<CertificateItem
					subject="Analytics Developer & UX Design Certificates Enrollee"
					entity="Google"
					timeline="Ongoing"
					:inList="true"
				/>
			</ul>
		</section>
	</main>
</template>

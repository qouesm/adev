<script>
	import Header from '../components/Header.svelte';
	import Footer from '../components/Footer.svelte';

	import Portrait from '../assets/portraits/6.jpg';
	import Icon from '../components/Icon.svelte';
	import Button from '../components/Button.svelte';
</script>

<div class="flex h-auto flex-col justify-between gap-y-4 bg-svelte-50 md:h-screen">
	<Header />
	<main class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
		<div class="flex flex-col justify-between gap-8 py-8 md:flex-row md:gap-0 md:py-0">
			<div class="flex w-full flex-col gap-10 md:w-2/4">
				<div class="flex flex-col items-start gap-4">
					<h1>ANDREW AVELLA</h1>
					<div
						class="inline-block rounded-full bg-fuchsia-200 px-4 py-1 text-sm font-semibold uppercase leading-6 text-fuchsia-800"
					>
						For Hire
					</div>
					<p class="text-2xl text-slate-700">
						Senior at SUNY New Paltz graduating this May with a B.S. in Computer Science on the job
						hunt. Hire me?
					</p>
				</div>
				<div class="flex gap-4 flex-wrap">
					<Button left href="/resume.pdf"><Icon symbol="user" />Resume</Button>
					<Button left type="secondary" href="https://linkedin.com/andrew-avella/"
						><Icon symbol="linkedin" strokeWidth="1" />LinkedIn</Button
					>
					<Button left type="secondary" href="https://github.com/qouesm/"
						><Icon symbol="github" />Github</Button
					>
					<Button left type="secondary" href="https://gitlab.com/qouesm/"
						><Icon symbol="gitlab" strokeWidth="0.1" />Gitlab</Button
					>
				</div>

				<div class="text-xl text-slate-700 flex flex-col gap-y-2">
					<p>
						I've been a technology hobbyist since I knew what computers were, playing computer
						games, building my own computer, and installing Linux as my primary operating system. I
						first took two AP high school courses on Javascript and Java before diving head deep
						into the program at SUNY New Paltz.
					</p>
					<p>
						At university, I founded an online community for students of the school to chat and
						converse about coursework which has since grown to more than 250 members. I created a
						bot to help manage it and have several of my friends help out to moderate the
						discussion, such that we maintain a welcoming environment for everyone. At our school's
						computer science club, I have been a regular presenter, where I have given workshops on
						the basics of Git with Github, creating sketches with p5.js, getting people with a Java
						background into Python, exploring the many features of Visual Studio Code, and Raspberry
						Pi project deployment using Docker.
					</p>
					<p>
						This website was created by me with Svelte+TailwindCSS and is being served via a Docker
						container my own Raspberry Pi. See <a
							href="https://github.com/qouesm/"
							target="_blank"
							rel="noreferrer">Github</a
						> for more details. Please consider me for employment opportunities pending my graduation
						this May.
					</p>
				</div>
			</div>
			<a href="src/assets/resume.pdf" target="_blank" rel="noreferrer">
				<img class="relative object-cover w-[500px]" src={Portrait} alt="Portrait" />
			</a>
		</div>
	</main>
	<Footer />
</div>

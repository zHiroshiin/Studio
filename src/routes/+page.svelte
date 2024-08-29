<script>
	import moment from 'moment';

	moment.locale('en');

	var viewingPage = 'aboutme';
	var currentYear = new Date().getFullYear();
	var currentMonth = new Date().getMonth();
	var currentDay = new Date().getDate();
	var age = moment([currentYear, currentMonth, currentDay]).diff(moment([2004, 10, 16]), 'years');
</script>

<div
	class="fixed flex h-12 w-full items-center justify-center bg-slate-800 text-white transition-all hover:h-16 hover:text-xl"
>
	<h1>Hiroshi's Studio</h1>
</div>
<div class="top-0 min-h-screen bg-slate-900 p-4 px-20 pb-0 pt-16 text-white">
	<div class="flex space-x-2">
		<!-- Navigation -->
		<div class="w-48">
			<h1 class="text-2xl">Navigation</h1>
			<br />
			<hr class="mb-5" />
			<ul class=" text-xl">
				<li>
					<!-- About me Button -->
					<button
						on:click={() => {
							viewingPage = 'aboutme';
						}}
						class="flex w-full items-center py-2 transition-all hover:translate-x-2 hover:text-gray-300"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="size-6"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="m11.25 11.25.041-.02a.75.75 0 0 1 1.063.852l-.708 2.836a.75.75 0 0 0 1.063.853l.041-.021M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Zm-9-3.75h.008v.008H12V8.25Z"
							/>
						</svg>
						&nbsp;About me
					</button>
				</li>
				<li>
					<!-- Music Button -->
					<button
						on:click={() => {
							viewingPage = 'music';
						}}
						class="flex w-full items-center py-2 transition-all hover:translate-x-2 hover:text-gray-300"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="size-6"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="m9 9 10.5-3m0 6.553v3.75a2.25 2.25 0 0 1-1.632 2.163l-1.32.377a1.803 1.803 0 1 1-.99-3.467l2.31-.66a2.25 2.25 0 0 0 1.632-2.163Zm0 0V2.25L9 5.25v10.303m0 0v3.75a2.25 2.25 0 0 1-1.632 2.163l-1.32.377a1.803 1.803 0 0 1-.99-3.467l2.31-.66A2.25 2.25 0 0 0 9 15.553Z"
							/>
						</svg>

						&nbsp;Music
					</button>
				</li>
				<li>
					<!-- Portfolio Button -->
					<button
						on:click={() => {
							viewingPage = 'portfolio';
						}}
						class="flex w-full items-center py-2 transition-all hover:translate-x-2 hover:text-gray-300"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="size-6"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M19.5 14.25v-2.625a3.375 3.375 0 0 0-3.375-3.375h-1.5A1.125 1.125 0 0 1 13.5 7.125v-1.5a3.375 3.375 0 0 0-3.375-3.375H8.25m2.25 0H5.625c-.621 0-1.125.504-1.125 1.125v17.25c0 .621.504 1.125 1.125 1.125h12.75c.621 0 1.125-.504 1.125-1.125V11.25a9 9 0 0 0-9-9Z"
							/>
						</svg>

						&nbsp;Portfolio
					</button>
				</li>
				<li>
					<!-- Contact Button -->
					<button
						on:click={() => {
							viewingPage = 'contact';
						}}
						class="flex w-full items-center py-2 transition-all hover:translate-x-2 hover:text-gray-300"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="size-6"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 0 0 2.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 0 1-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 0 0-1.091-.852H4.5A2.25 2.25 0 0 0 2.25 4.5v2.25Z"
							/>
						</svg>

						&nbsp;Contact
					</button>
				</li>
				<li>
					<!-- Thanks Button -->
					<button
						on:click={() => {
							viewingPage = 'thanks';
						}}
						class="flex w-full items-center py-2 transition-all hover:translate-x-2 hover:text-gray-300"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
							class="size-6"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M7.5 8.25h9m-9 3H12m-9.75 1.51c0 1.6 1.123 2.994 2.707 3.227 1.129.166 2.27.293 3.423.379.35.026.67.21.865.501L12 21l2.755-4.133a1.14 1.14 0 0 1 .865-.501 48.172 48.172 0 0 0 3.423-.379c1.584-.233 2.707-1.626 2.707-3.228V6.741c0-1.602-1.123-2.995-2.707-3.228A48.394 48.394 0 0 0 12 3c-2.392 0-4.744.175-7.043.513C3.373 3.746 2.25 5.14 2.25 6.741v6.018Z"
							/>
						</svg>

						&nbsp;Thanks
					</button>
				</li>
			</ul>
			<br />
			<hr />
			<!-- Language Select -->
			<h1 class="justify-center p-2 text-lg">Linguagem/Language</h1>
			<div class=" flex justify-between p-2">
				<a class="flex h-full w-full items-center justify-center" href="/ptbr">
					<img
						class="size-16 origin-center object-contain transition-all hover:size-14 hover:translate-x-1"
						src="https://flagemoji.net/img/flags/brazil-flag.png"
						alt="Língua Portuguesa do Brasil"
					/>
				</a>
				<a class="flex h-full w-full items-center justify-center" href="/">
					<img
						class="size-16 origin-center object-contain transition-all hover:size-14 hover:-translate-x-1"
						src="https://em-content.zobj.net/source/skype/289/flag-united-kingdom_1f1ec-1f1e7.png"
						alt="English Language"
					/>
				</a>
			</div>
		</div>
		<!-- Page -->
		<div class="flex w-full border-l border-r px-2">
			<!-- About me -->
			{#if viewingPage == 'aboutme'}
				<div class="space-y-2">
					<h1 class="mb-5 text-2xl">About me</h1>
					<p class="text-justify text-lg">
						Hi! I'm Hiroshi, some times known as Rick. I'm a brazillian {age} year old musician and programmer.
						I made this site you're looking at right now!
						<br />
						<br />
						My passions and my hobbies walk hand in hand. I love doing my things my way, but also enjoy
						woking as a team to bring things far beyond me to fruition.
						<br />
						<br />
						My hobbies include, but are not limited to:
						<br />
						🎸 • Playing and Creating music.
						<br />
						🎚 &nbsp;• Mixing and Mastering music.
						<br />
						🖥 • Programming - Web and Game development.
						<br />
						🎮 • Gaming, of course, as all game developers should!
						<br />
						<br />
						And here are some of my inspirations:
						<br />
						• Favourite bands
						<br />
						- Periphery - My favourite band of all time. The most fun guys making the most amazing music,
						exploring the baoundaries of metal.
						<br />
						- Veil of Maya - Incredibly skilled musicians, with a similar flavour to Periphery.
						<br />
						- Meshuggah - Who in their right minds have ever made metal and not been enamoured with Meshuggah's
						technical prowess?
						<br />
						<br />
						• Favourite games
						<br />
						- Mafia (2002) (PC) - Incredible attention to detail paired with an amazing story and a love
						for the medium. Absolute perfection.
						<br />
						- Minecraft - One of the all time best selling games, and for a reason. I love creativity
						in the games i play, and here i can express it all.
						<br />
						- Undertale - Even if not so much today, it was integral to my childhood and brought me into
						my passion for music. I owe much to this game.
						<br />
						<br />
						I hope this can give you a little insight into the little chest of wonders i am. Thanks for
						the visit! 🙏
					</p>
				</div>
			{/if}
			<!-- Music -->
			{#if viewingPage == 'music'}
				<div class="space-y-2">
					<h1 class="mb-5 text-2xl">Music</h1>
					<p class="text-justify text-lg">
						A musician's main source of expression is his music. So here's a bit of mine!
						<br />
						You can listen to this while you read through the other pages, so don't worry about clicking
						off.
					</p>
				</div>
			{/if}
		</div>
		<div class="w-64">
			<h1 class="text-2xl">Music Player</h1>
			<br />
			<hr class="mb-5" />
			<div>
				<!-- Title -->
				<h1>Song Title</h1>
			</div>
			<div>progress bar goes here</div>
			<div class="flex items-center justify-center space-x-2">
				<button
					class="transition- flex size-8 items-center justify-center rounded-full bg-white text-slate-900 hover:bg-gray-400"
				>
					<!-- Stop -->
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="size-6"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M5.25 7.5A2.25 2.25 0 0 1 7.5 5.25h9a2.25 2.25 0 0 1 2.25 2.25v9a2.25 2.25 0 0 1-2.25 2.25h-9a2.25 2.25 0 0 1-2.25-2.25v-9Z"
						/>
					</svg>
				</button>
				<button
					class="flex size-8 items-center justify-center rounded-full bg-white text-slate-900 transition-all hover:bg-gray-400"
				>
					<!-- Play/Pause -->
					<svg
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						class="size-6"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M21 7.5V18M15 7.5V18M3 16.811V8.69c0-.864.933-1.406 1.683-.977l7.108 4.061a1.125 1.125 0 0 1 0 1.954l-7.108 4.061A1.125 1.125 0 0 1 3 16.811Z"
						/>
					</svg>
				</button>
			</div>
			<br />
			<div>Song description</div>
		</div>
	</div>
</div>

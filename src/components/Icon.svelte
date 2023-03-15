<script lang="ts">
	export let symbol: string;
	export let size: string = '1rem';
	export let color: string = 'currentColor';
	export let strokeWidth: number = 2;

	const symbols = {
		edit: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-linecap="round" stroke-linejoin="round"><polygon points="14 2 18 6 7 17 3 17 3 13 14 2"></polygon><line x1="3" y1="22" x2="21" y2="22"></line></svg>`,
		grid: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-linecap="square" stroke-linejoin="round"><rect x="3" y="3" width="7" height="7"></rect><rect x="14" y="3" width="7" height="7"></rect><rect x="14" y="14" width="7" height="7"></rect><rect x="3" y="14" width="7" height="7"></rect></svg>`,
		options: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-linecap="round" stroke-linejoin="round"><line x1="4" y1="21" x2="4" y2="14"></line><line x1="4" y1="10" x2="4" y2="3"></line><line x1="12" y1="21" x2="12" y2="12"></line><line x1="12" y1="8" x2="12" y2="3"></line><line x1="20" y1="21" x2="20" y2="16"></line><line x1="20" y1="12" x2="20" y2="3"></line><line x1="1" y1="14" x2="7" y2="14"></line><line x1="9" y1="8" x2="15" y2="8"></line><line x1="17" y1="16" x2="23" y2="16"></line></svg>`,
		search: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"></circle><line x1="21" y1="21" x2="16.65" y2="16.65"></line></svg>`,
		x: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="18" y1="6" x2="6" y2="18"></line><line x1="6" y1="6" x2="18" y2="18"></line></svg>`,
		mail: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path><polyline points="22,6 12,13 2,6"></polyline></svg>`,
		user: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-linecap="round" stroke-linejoin="round"><path d="M5.52 19c.64-2.2 1.84-3 3.22-3h6.52c1.38 0 2.58.8 3.22 3"/><circle cx="12" cy="10" r="3"/><circle cx="12" cy="12" r="10"/></svg>`,
		github: `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"> <g clip-path="url(#a)"> <path stroke-linecap="round" stroke-linejoin="round" d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22" /> </g> <defs> <clipPath id="a"> <path d="M0 0h24v24H0z" /> </clipPath> </defs> </svg>`,
		gitlab: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16"><path fill="currentColor" fill-rule="evenodd" d="m14.329 6.922l-.02-.053l-1.239-3.232l-.668 2.044l-.337 1.035H3.936L3.598 5.68l-.667-2.043l-1.24 3.237l-.005.01l-.004.01l-.018.045a2.543 2.543 0 0 0 .848 2.93l.005.004l.01.008l.01.008l.009.006l3.302 2.474l.004.004l1.644 1.242l.5.379l.501-.379l1.644-1.242l.006-.004l3.325-2.489l.007-.005l.009-.007a2.543 2.543 0 0 0 .844-2.939l-.003-.008Zm.053 4.152l-3.337 2.497l-1.643 1.242l-.999.755a.675.675 0 0 1-.813 0l-.999-.755l-1.643-1.242l-3.313-2.483l-.018-.014l-.008-.006A4.043 4.043 0 0 1 .267 6.395l.023-.057l1.9-4.963l.013-.033l.081-.212l.023-.06l.158-.413A.565.565 0 0 1 2.941.3a.576.576 0 0 1 .613.415l.134.41l.005.017l.078.239l.011.033l1.242 3.802h5.953l1.241-3.802l.011-.033l.078-.24l.006-.016l.133-.41a.575.575 0 0 1 1.088-.058l.157.409l.025.064l.08.211l.013.033l1.903 4.963l.022.058a4.043 4.043 0 0 1-1.343 4.671l-.01.008Z" clip-rule="evenodd"/></svg>`,
		linkedin: `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"><path d="M22.23 0H1.77C.8 0 0 .77 0 1.72v20.56C0 23.23.8 24 1.77 24h20.46c.98 0 1.77-.77 1.77-1.72V1.72C24 .77 23.2 0 22.23 0zM7.27 20.1H3.65V9.24h3.62V20.1zM5.47 7.76h-.03c-1.22 0-2-.83-2-1.87 0-1.06.8-1.87 2.05-1.87 1.24 0 2 .8 2.02 1.87 0 1.04-.78 1.87-2.05 1.87zM20.34 20.1h-3.63v-5.8c0-1.45-.52-2.45-1.83-2.45-1 0-1.6.67-1.87 1.32-.1.23-.11.55-.11.88v6.05H9.28s.05-9.82 0-10.84h3.63v1.54a3.6 3.6 0 0 1 3.26-1.8c2.39 0 4.18 1.56 4.18 4.89v6.21z"/></svg>`
	};
</script>

<svg height={size} width={size} stroke={color} stroke-width={strokeWidth}>
	{@html symbols[symbol]}
</svg>

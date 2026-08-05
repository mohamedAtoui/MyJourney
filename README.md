# mohamedatoui.uk

My personal site — portfolio, project write-ups, and blog. Built with Next.js 16 (App Router), TypeScript, Tailwind CSS, and next-intl for English/French.

**Live:** [mohamedatoui.uk](https://mohamedatoui.uk)

## Development

```bash
npm install
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000).

| Command         | Description                |
| --------------- | -------------------------- |
| `npm run dev`   | Start the dev server       |
| `npm run build` | Production build           |
| `npm run start` | Serve the production build |
| `npm run lint`  | Lint with ESLint           |

## Content

Nearly all site content is data, not code. It lives in three JSON files per locale under `src/i18n/messages/{en,fr}/`:

- `personal.json` — name, headline, bio, location, meta description
- `collections.json` — news, projects, work experience, education, skills, social links
- `common.json` — section headings, navbar, footer

Blog posts are MDX under `content/blog/<locale>/`. Site-wide config (URL, avatar, last-updated) is in `src/data/site.ts`.

The CV is built from LaTeX. Edit `mycvs/Mohamed_Atoui_CV.tex`, then:

```bash
cd mycvs && xelatex Mohamed_Atoui_CV.tex
```

Copy the resulting PDF to `public/Mohamed_Atoui_CV.pdf` — that is the file the site serves.

## Credits

Built on [nextjs-portfolio-blog-research](https://github.com/zhengzangw/nextjs-portfolio-blog-research) by Zangwei Zheng (MIT), which in turn draws on [dillionverma/portfolio](https://github.com/dillionverma/portfolio). See [LICENSE](./LICENSE) and [THIRD_PARTY_NOTICES.md](./THIRD_PARTY_NOTICES.md).

## License

MIT — see [LICENSE](./LICENSE).

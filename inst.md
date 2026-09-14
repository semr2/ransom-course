4. Branding & Theme Injection
Edit `theme.css` in the new folder to enforce the user's Shadcn primary color schema.
Inject the Shadcn CSS Variables: Prepend the user's `:root` and `.default-dark` blocks (containing their `--primary`, `--background`, `--card`, etc.) to the absolute top of the file.
Map Global Backgrounds: Replace hardcoded hex values for variables like `--bg-void`, `--bg-deep`, and `--bg-base` with `hsl(var(--background))`.
Map Global Surfaces/Text: Replace `--bg-surface` and `--bg-card` with `hsl(var(--card))`. Replace `--text-primary` with `hsl(var(--foreground))`.
Flatten Accent Colors: The template relies on module-specific colors. Map ALL of the following variables to `hsl(var(--primary))`:
`--red`, `--red-bright`, `--red-glow`
`--blue`, `--blue-bright`, `--blue-glow`
`--orange`, `--orange-bright`, `--orange-glow`
`--purple`, `--purple-bright`, `--purple-glow`
`--cyan`, `--cyan-bright`, `--cyan-glow`
(Do not modify `--green` or `--amber`, as they are used semantically for Success and Warning states).

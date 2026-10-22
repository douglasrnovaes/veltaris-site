# veltarisit.com.br

Static institutional site for Veltaris IT Consultoria em TI Ltda.
Single file (`index.html`), no build step. PT/EN toggle built in (`?lang=en` forces English).

## Publish on GitHub Pages

1. Create a repository (e.g. `veltaris-site`) and push `index.html`, `CNAME` and this README to `main`.
2. Repository → Settings → Pages → Source: *Deploy from a branch* → `main` / root.
3. Custom domain: `veltarisit.com.br` (the `CNAME` file already sets it). Enable **Enforce HTTPS** once the certificate is issued.

## DNS at Registro.br

In the domain panel, use Registro.br DNS ("Editar zona") and add:

| Type  | Name | Value |
|-------|------|-------|
| A     | (blank / @) | 185.199.108.153 |
| A     | (blank / @) | 185.199.109.153 |
| A     | (blank / @) | 185.199.110.153 |
| A     | (blank / @) | 185.199.111.153 |
| CNAME | www  | `<your-github-user>.github.io` |

Propagation usually takes from a few minutes up to a few hours.

## Alternative: Netlify

Connect the repository in Netlify (no build command, publish directory `/`), add the custom domain, and follow the DNS records Netlify shows in the domain settings.

## Before going live

- Confirm the mailbox `contato@veltarisit.com.br` exists (or change the address in `index.html`).
- Replace the LinkedIn link (`https://www.linkedin.com/`) with the real profile URL.

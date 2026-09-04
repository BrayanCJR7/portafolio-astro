# Portafolio personal

Portafolio personal construido con Astro y preparado para desplegarse en Cloudflare Pages.

## Desarrollo local

Requisitos:

- Node.js `22.12.0` o superior
- pnpm `11.25.0`

```sh
pnpm install
pnpm dev
```

El sitio estara disponible en `http://localhost:4321`.

## Build de produccion

```sh
pnpm build
pnpm preview
```

El build estatico se genera en `dist/`.

## Despliegue en Cloudflare Pages

En Cloudflare Pages, conecta el repositorio y configura:

| Configuracion | Valor |
| --- | --- |
| Framework preset | Astro |
| Build command | `pnpm build` |
| Build output directory | `dist` |
| Node.js version | `22.12.0` o superior |
| pnpm version | `11.25.0` |

El archivo `wrangler.toml` tambien declara `dist` como salida para despliegues mediante Wrangler. Para desplegar desde la CLI:

```sh
pnpm dlx wrangler pages deploy dist --project-name portafolio-astro
```

El nombre del proyecto debe coincidir con el creado en Cloudflare Pages.

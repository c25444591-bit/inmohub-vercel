```markdown
# my-v0-project — Cómo ejecutar y desplegar

Este repositorio es una aplicación Next.js (Next 14). Aquí tienes instrucciones rápidas en español para:
- ejecutar el proyecto localmente,
- prepararlo para producción,
- y desplegarlo en la web con Vercel.

Requisitos recomendados
- Node.js 18.x o 20.x
- pnpm (recomendado porque hay `pnpm-lock.yaml`) — opcionalmente puedes usar `npm` o `yarn`.

Instalar pnpm (si no lo tienes):
```bash
npm install -g pnpm
```

1) Ejecutar localmente (modo desarrollo)
```bash
git clone <tu-repo-url>
cd <tu-repo-folder>
pnpm install
pnpm dev
# abre http://localhost:3000
```

2) Probar la versión de producción localmente
```bash
pnpm build
pnpm start
```

3) Desplegar en Vercel (pasos rápidos)
- Crea cuenta en https://vercel.com (puedes usar GitHub).
- Pulsa "New Project" → "Import Git Repository" → conecta tu GitHub.
- Selecciona tu repositorio.
- Ajustes recomendados:
  - Framework: Next.js (debería detectarlo)
  - Package Manager: pnpm (si aparece)
  - Build Command: next build (o pnpm build)
- Pulsa Deploy y Vercel te dará una URL pública.

4) Uso de GitHub Actions (opcional, CI/CD)
Si agregas el workflow y configuras un secret VERCEL_TOKEN en GitHub, cada push a main desplegará automáticamente.

5) Notas
- Si tu rama principal no es main (ej. master), cambia el nombre en el workflow.
- Si quieres, te guío paso a paso mientras creas los archivos.
```

# React + Vite + Docker

Este template visa ter um projeto padrão para iniciar um aplicativo react com vite para rodar em um container docker previamente configurado no dockerfile.

Para configurar a porta vá no arquivo vite.config.js :



```
// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  server: {
    watch: {
      usePolling: true,
    },
    host: true, // Mapeia o host
    strictPort: true,
    port: 5173 // troque a porta favorita
}})


```

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

Podés probar esta app visitando esta página: [vue3-pinia-login-example.vercel.app](vue3-pinia-login-example.vercel.app)

## 🔵 Vue 3 + Pinia Login Example

Esta app contene una página de inicio de sesión y una pantalla sucursales.
La pantalla sucursales hace una llamada a una api externa.


## Características
- Se utiliza Pinia para manejar el estado.
- Obtuve información de esta [API](https://apis.datos.gob.ar/georef/api/provincias/)
- Con flexbox me aseguré de que la app sea adaptable a diferentes tipos de dispositivos: grandes pantallas🖥️, celulares📱 y laptops💻.
- Utilizó CSS puro (sin frameworks como styled component ni sass).
- Los elementos visuales se probaron en varios navegadores.
- Se ejecutó prettier para que el código fuera consistente en toda la aplicación.

## 🏃‍♂️ Cómo correr esta aplicación?

🚀 Primero, lanza el servidor de desarrollo:

```bash
npm install
npm run dev
```

💻 Luego, puedes abrir [localhost:3000](http://localhost:3000) con tu navegador para ver el resultado.


## Estructura de carpetas

- /public: donde se almacenan los logos e iconos de la app.
- /components: Acá van todos los componentes, cuando aumente la cantidad de componentes van a estar organizados en subcarpetas según los principios del Atomic Design.
- /stores: En esta carpeta van los stores de pinia.
- /router: Archivos para el enrutamiento de la app. 
- /views: Se guardan las vistas. En este caso solo se utiliza la vista Sucursales.




# FleetProof Mock Platform

Fake RESTful API del curso Aplicaciones Web. Reutiliza el JSON Server del frontend y los datos ficticios de demostracion; no sustituye al backend real.

## Ejecucion

Node.js 24.21.0. Ejecutar `npm ci` y `npm start`.
Base local: `http://127.0.0.1:3000/api/v1`.
Health check: `/api/v1/health`.

## Render

Web Service, plan Free. Build: `npm ci`. Start: `npm start`.
Variables: `HOST=0.0.0.0`, `NODE_VERSION=24.21.0`.
Render proporciona `PORT`. Health check: `/api/v1/health`.
En Netlify configurar `VITE_FLEETPROOF_API_URL` con la URL HTTPS del servicio seguida de `/api/v1`.

Los registros se filtran por usuario en el servidor. Las cuentas nuevas comienzan vacias; los registros de ejemplo sin propietario se asignan al administrador de demostracion `etepepe`. El registro publico siempre crea un usuario normal. La cuenta administradora conserva exclusivamente sus propios datos, no los de otros usuarios.

Los tokens aleatorios vencen en 24 horas y se invalidan al reiniciar el servidor. La API sigue siendo una simulacion academica: contrasenas en texto plano y sin controles de produccion. No ingresar informacion personal ni reutilizar contrasenas reales. El almacenamiento gratuito es efimero: cambios pueden perderse al reiniciar o desplegar.

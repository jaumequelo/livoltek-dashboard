# ☀️ Livoltek Solar Dashboard

Panel web **autocontenido en un solo `index.html`** (sin dependencias ni build) para monitorizar
una planta fotovoltaica con inversor **Livoltek** mediante la API oficial del cloud (HESS · servidor EMEA).

🌐 **Demo en vivo:** [https://jaumequelo.github.io/livoltek-dashboard/](https://jaumequelo.github.io/livoltek-dashboard/)

![HTML](https://img.shields.io/badge/HTML5-single--file-orange) ![API](https://img.shields.io/badge/API-Livoltek%20HESS-blue) ![Meteo](https://img.shields.io/badge/Meteo-Open--Meteo-brightgreen) ![License](https://img.shields.io/badge/Licencia-MIT-green)

## ✨ Características

- 🔐 Login automático contra la API Livoltek (`secuid` + `key` → JWT) + token de usuario.
- ⚡ Diagrama de flujo en vivo estilo app oficial: paneles → inversor → casa / baterías / red,
  con **flechas animadas y colores por estado** (generando, cargando, descargando, batería baja, red desconectada…).
- 📊 Potencias instantáneas, SOC, estado de subsistemas, energías diaria/mensual/anual/total y CO₂ evitado.
- 📈 Gráfico de generación de los últimos días (informe diario del inversor + fallbacks).
- 🌦️ Meteo en directo con **Open-Meteo** (sin clave): temperatura, tiempo, amanecer/atardecer,
  ciudad por geolocalización y **previsión a 3 días**.
- 🔄 Auto-refresco cada 5 min + botón manual con ventana de carga.
- 📱 Diseño responsive (móvil, tablet y escritorio).
- 🧪 Modo **Demo** integrado para probar sin credenciales.

## 🚀 Uso

```bash
git clone https://github.com/jaumequelo/livoltek-dashboard.git
cd livoltek-dashboard
# abre index.html en tu navegador
```

1. Pulsa **⚙ Configuración** y elige **Modo Real**.
2. Obtén tus credenciales en **www.livoltek-portal.com → My Profile**:
   - **Generate Token** → token de usuario
   - **Secure ID** → `Security ID` (secuid) y `API Key`
3. Pega los 3 valores, pulsa **🔎 Cargar plantas**, selecciona la tuya y **💾 Guardar y conectar**.

> Las credenciales se guardan **únicamente en tu navegador** (localStorage).
> Este proyecto no está afiliado a Livoltek/Hexing.

## 🌍 Despliegue con GitHub Pages

`Settings → Pages → Branch: main → Save` → listo en `https://TU_USUARIO.github.io/livoltek-dashboard/`.

## 🤝 Contribuir

Pull requests y issues bienvenidos. Si tu instalación reporta signos de potencia distintos,
prueba los checkboxes *«Invertir sentido de red/batería»* en Configuración.

## 📜 Licencia

[MIT](LICENSE) — úsalo, modifícalo y compártelo libremente.

---
Hecho en Peñíscola con ❤ por [Jaumequelo.online](https://jaumequelo.online)
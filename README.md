# Kazeji

風路 · «camino del viento». Páginas públicas del estudio y de sus juegos.

Aquí no hay código de juego: solo las páginas que las tiendas exigen tener en una
URL pública y la presentación del estudio. El código de cada título vive en su
propio repositorio.

## Qué hay

```
kazeji/
├── index.html              El estudio y la lista de juegos
└── flowzy/
    ├── index.html          Presentación de Flowzy
    └── privacidad.html     Política de privacidad de Flowzy
```

Cada juego cuelga de su propia carpeta. El siguiente se añade al lado sin tocar
lo que ya está.

## Publicar

Las dos tiendas exigen una **URL pública** de política de privacidad, y la
comprueban sin sesión iniciada. El sitio lo sirve **Cloudflare Pages** desde este
repositorio: cada empujón a `main` despliega. La configuración es la de un sitio
estático sin construir —sin comando de compilación y con la raíz del repositorio
como carpeta de salida—, porque aquí solo hay HTML.

El dominio `kazeji.com` está apuntado en **Workers & Pages → el proyecto → Custom
domains**, con el apex y `www` resolviendo los dos. GitHub Pages quedó apagado
(`Settings → Pages → Source → None`) para que el sitio no viva en dos sitios a la
vez y los buscadores no tengan que elegir.

Las direcciones quedan así:

| Página | Dirección |
|---|---|
| Estudio | `kazeji.com` |
| Flowzy | `kazeji.com/flowzy/` |
| Privacidad | `kazeji.com/flowzy/privacidad.html` |

La tercera es la que se pega en la ficha de Google Play y de App Store.

Los enlaces internos son relativos —`flowzy/`, `../`—, así que las mismas páginas
funcionan con el dominio, en la vista previa de despliegue de Cloudflare y
abiertas desde un servidor local, sin tocar nada.

## Estado

- [x] Repositorio público.
- [x] Servido por Cloudflare Pages en `kazeji.com`.
- [x] Enlaces internos relativos: funcionan con dominio, en vista previa y en local.
- [x] Política de privacidad con responsable y fecha. Publicable.
- [x] GitHub Pages desactivado: el sitio ya no se duplica en `igisgoce.github.io/Kazeji/`.
- [ ] Domicilio del responsable, pendiente de resolver dónde se fija.
- [ ] Abrir las tres páginas en un móvil de verdad, no solo en el escritorio.

### Sobre el domicilio

El RGPD pide identidad y datos de contacto del responsable, y un correo que se
atiende cumple esa parte: por eso la política ya es publicable sin dirección
postal. Dos cosas que conviene resolver antes del lanzamiento, y que van por
caminos distintos:

- **Google Play** no acepta apartados de correos ni oficinas virtuales en la
  verificación de una cuenta personal, y **publica la dirección completa** en la
  ficha si la aplicación monetiza. Separar el domicilio particular de la ficha
  pasa por registrar una cuenta de organización, no por un apartado.
- **La LSSI** (Ley 34/2002, art. 10) exige a los prestadores de servicios
  publicar su domicilio. Si aplica a este caso, la dirección tendrá que estar en
  la política de todas formas. Merece una consulta antes de publicar.

## Mantener

La política de privacidad tiene que decir la verdad sobre lo que el binario hace,
no sobre lo que se pretendía que hiciera. Cada vez que un juego añada publicidad,
analítica, cuentas o cualquier otra recogida de datos:

1. Se actualiza la política **antes** de publicar esa versión.
2. Se cambia la fecha de «Última actualización».
3. Se revisa el formulario de seguridad de datos de Play y el manifiesto de
   privacidad de Apple para que digan lo mismo.

Una ficha que declara algo distinto de lo que hace el binario es motivo de
retirada, y se detecta automáticamente.

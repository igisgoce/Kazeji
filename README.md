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
comprueban sin sesión iniciada. Con GitHub Pages:

1. **Settings → Pages**, origen `Deploy from a branch`, rama `main`, carpeta `/`.
2. El repositorio tiene que ser **público**, o hacer falta un plan de pago: Pages
   sobre un repositorio privado no sirve en el plan gratuito.
3. Con dominio propio, el fichero `CNAME` va en la raíz y el dominio se apunta en
   la misma pantalla de Pages.

Las direcciones quedan así:

| Página | Sin dominio propio | Con dominio propio |
|---|---|---|
| Estudio | `kazeji.github.io/` | `kazeji.com` |
| Flowzy | `kazeji.github.io/flowzy/` | `kazeji.com/flowzy/` |
| Privacidad | `kazeji.github.io/flowzy/privacidad.html` | `kazeji.com/flowzy/privacidad.html` |

La tercera es la que se pega en la ficha de Google Play y de App Store.

## Estado

- [x] Repositorio público.
- [x] Servido por Cloudflare Pages en `kazeji.com`.
- [x] Enlaces internos relativos: funcionan con dominio, en vista previa y en local.
- [x] Política de privacidad con responsable y fecha. Publicable.
- [ ] Domicilio del responsable, pendiente de resolver dónde se fija.
- [ ] Desactivar GitHub Pages, que quedó activo y duplica el sitio en
      `igisgoce.github.io/Kazeji/` (Settings → Pages → Source → None).
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

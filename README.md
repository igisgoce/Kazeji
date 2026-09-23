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

## Antes de publicar

- [ ] Rellenar los marcadores de `flowzy/privacidad.html`: fecha de publicación,
      nombre y apellidos del responsable, y dirección postal.
- [ ] Decidir si el repositorio pasa a público o se contrata Pages de pago.
- [ ] Comprobar que los enlaces entre páginas funcionan con el dominio elegido.
- [ ] Abrir las tres páginas en un móvil de verdad, no solo en el navegador de
      escritorio.

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

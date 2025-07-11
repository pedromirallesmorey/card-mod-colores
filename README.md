# 🎨 Personalización de Colores en Home Assistant con Card-Mod

Autor: Pedro Miralles

Última versión: Julio 2025   

## 1. 🧩 ¿Qué es Card-Mod?

Card-Mod permite aplicar estilos CSS directamente a las tarjetas de Home Assistant. Es ideal para cambiar colores, márgenes, opacidad y más.

## 2. 🔤 Cambiar el color del texto en tarjetas entities

![](assets/Cambiar%20el%20color%20del%20texto%20en%20tarjetas.PNG)

```yaml
type: entities
entities:
  - entity: light.cine
    card_mod:
      style: |
        :host {
          color: red;
        }
  - entity: light.extended_color_light_1
    card_mod:
      style: |
        :host {
          color: green;
        }
```

Esto cambia el color del texto de cada entidad. Puedes ver ejemplos similares en Modifica temas para crearlos a tu gusto. Cambia el color de ..., especialmente desde el minuto 20:27.

## 3. ⚠️ Alertas con colores personalizados

![](assets/Alertas%20con%20colores%20personalizados.PNG)

```html
<ha-alert alert-type="error">This is an error alert — check it out!</ha-alert>
<ha-alert alert-type="warning">This is a warning alert — check it out!</ha-alert>
<ha-alert alert-type="info">This is an info alert — check it out!</ha-alert>
<ha-alert alert-type="success">This is a success alert — check it out!</ha-alert>
<ha-alert title="Test alert">This is an alert with a title</ha-alert>
Estas alertas son útiles para mostrar mensajes destacados con colores según el tipo de alerta.
```

## 4. 🟪 Tarjeta personalizada con colores de fondo y texto

![](assets/colores%20de%20fondo%20y%20texto.PNG)

```yaml
type: custom:button-text-card
title: Warning!
subtitle: Draw attention with custom colors
icon: mdi:comment-alert
large: true
font_color: "#fff"
background_color: "#A81419"
Ideal para destacar información importante.
```

## 5. 🖌️ Personalización del fondo de tarjetas entity

Fondo sólido

![](assets/Establecer%20un%20color%20como%20fondo.PNG)

```yaml
card_mod:
  style: |
    ha-card {
      background-color: black;
    }
```

Fondo con opacidad

![](assets/Establecer%20color%20como%20fondo%20y%20opacidad.PNG)

```yaml
card_mod:
  style: |
    ha-card {
      background-color: green;
      opacity: 0.4;
    }
```

Fondo con degradado RGB

![](assets/degradado%20de%20colores%20como%20fondo.PNG)

```yaml
card_mod:
  style: |
    ha-card {
      background: linear-gradient( rgba(67, 150, 206), rgba(59, 190, 188) );
    }
```

Fondo transparente

![](assets/fondo%20transparente.PNG)

```yaml
card_mod:
  style: |
    ha-card {
      background: transparent;
      box-shadow: none;
    }
```

## 6. 📐 Ajuste de márgenes

Margen derecho

![](assets/Margen%20derecho.PNG)

```yaml
card_mod:
  style: |
    ha-card {
      margin-right: 40px;
    }
```

Margen izquierdo

![](assets/Margen%20izquierdo.PNG)

```yaml
card_mod:
  style: |
    ha-card {
      margin-left: 50px;
    }
```

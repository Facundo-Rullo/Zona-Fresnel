# 📡 Calculadora de Zona de Fresnel

Software desarrollado para calcular la **Primera Zona de Fresnel (F1)** de forma rápida, sencilla e intuitiva, utilizando la fórmula proporcionada en la consigna de la materia.

---

## 👨‍💻 Autor

**Facundo Rullo**

---

## 📖 Descripción

La aplicación permite calcular la **Primera Zona de Fresnel (F1)** ingresando:

- Distancia (D) en kilómetros.
- Frecuencia (f) en GHz.

El sistema realiza el cálculo utilizando la siguiente fórmula:

\[
F1 = 8.656 \times \sqrt{\frac{D}{f}}
\]

El resultado se muestra en **metros**, truncado a **dos decimales** (sin redondear), tal como solicita la consigna.

---

## ✨ Funcionalidades

- ✅ Cálculo automático de la Primera Zona de Fresnel.
- ✅ Acepta números con **coma (,)** o **punto (.)** como separador decimal.
- ✅ Validación de caracteres inválidos.
- ✅ Validación de valores negativos o iguales a cero.
- ✅ Resultado truncado a dos decimales.
- ✅ Interfaz simple y fácil de utilizar.

---

## 🛠️ Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript

---

## 📷 Capturas de pantalla

### Pantalla principal

> ![Inicial](imagenes/inicial.png)

```md
![Pantalla Principal](imagenes/principal.png)
```

---

## 🚀 Cómo ejecutar el proyecto

1. Descargar o clonar el repositorio.

```bash
git clone https://github.com/USUARIO/calculadora-zona-fresnel.git
```

2. Abrir el archivo:

```
index.html
```

No requiere instalación ni servidor.

---

## 🧮 Ejemplo de cálculo

| Distancia | Frecuencia | Resultado |
|-----------:|-----------:|-----------:|
| 1 km | 2.4 GHz | 5.58 m |
| 5.5 km | 2.4 GHz | 13.10 m |
| 10 km | 5 GHz | 12.24 m |

---

## ✔️ Validaciones implementadas

El sistema controla:

- Campos vacíos.
- Caracteres no numéricos.
- Valores negativos.
- Valores iguales a cero.
- Uso de coma o punto decimal.

---

## 📌 Observaciones

El resultado mostrado se encuentra **truncado a dos decimales**, evitando el redondeo para cumplir con los requisitos establecidos en la consigna.

---

## 📄 Licencia

Proyecto desarrollado con fines académicos.

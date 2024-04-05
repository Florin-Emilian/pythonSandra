# Introducción a XML, DOM y Python

## XML (Extensible Markup Language)

![XML](https://www.manualweb.net/img/logos/xml.png)


XML es un lenguaje de marcado que se utiliza para almacenar y transportar datos de manera legible tanto para humanos como para máquinas. Algunas características importantes de XML son:

- Es extensible y flexible.
- Permite definir estructuras de datos personalizadas.
- Es independiente del lenguaje y la plataforma.

Para obtener más información sobre XML, puedes consultar la [documentación oficial de XML](https://www.w3.org/XML/).

## DOM (Document Object Model)

![DOM](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/1200px-DOM-model.svg.png)

El DOM es una interfaz de programación para documentos HTML y XML. Proporciona una representación estructurada del documento, lo que permite a los programas acceder y manipular el contenido, la estructura y el estilo de un documento. Algunos puntos clave sobre DOM son:

- Representa el documento como un árbol de nodos.
- Permite la manipulación dinámica de la estructura del documento.
- Es una API independiente del lenguaje.

Para obtener más información sobre DOM, puedes consultar la [especificación DOM de la W3C](https://www.w3.org/TR/dom/).

## Python y XML

![Python](https://www.python.org/static/community_logos/python-logo-master-v3-TM.png)


Python ofrece varias bibliotecas para trabajar con XML. Una de las más utilizadas es `xml.dom`, que proporciona una implementación del DOM para Python. Aquí hay un ejemplo básico de cómo usar `xml.dom` en Python:

```python
import xml.dom.minidom

# Crear un nuevo documento XML
doc = xml.dom.minidom.Document()

# Crear un elemento raíz
root = doc.createElement("bookstore")
doc.appendChild(root)

# Añadir un elemento hijo
book = doc.createElement("book")
root.appendChild(book)

# Añadir atributos al elemento
book.setAttribute("category", "cooking")

# Añadir elementos hijos al libro
title = doc.createElement("title")
title.appendChild(doc.createTextNode("Everyday Italian"))
book.appendChild(title)

author = doc.createElement("author")
author.appendChild(doc.createTextNode("Giada De Laurentiis"))
book.appendChild(author)

# Imprimir el documento XML
print(doc.toprettyxml())
```
## Recursos adicionales:

[Documentación oficial de Python sobre xml.dom](https://docs.python.org/3/library/xml.dom.html)

[Tutorial de W3Schools sobre XML](https://www.w3schools.com/xml/)

[Tutorial de MDN Web Docs sobre DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)
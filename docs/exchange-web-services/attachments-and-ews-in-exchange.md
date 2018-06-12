---
title: Los datos adjuntos y EWS en Exchange
manager: sethgros
ms.date: 7/11/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e4289a4-ec9d-4502-9854-c593c95d5f98
description: Obtenga información sobre cómo la API administrada de EWS o EWS en Exchange cliente representa ellos y datos adjuntos.
ms.openlocfilehash: e4a97873798b8252e6fc14003519ce8a0eab7ec8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19762995"
---
# <a name="attachments-and-ews-in-exchange"></a>Los datos adjuntos y EWS en Exchange

Obtenga información sobre cómo la API administrada de EWS o EWS en Exchange cliente representa ellos y datos adjuntos.
  
Normalmente, los datos adjuntos están asociados con elementos de correo, pero en realidad, todos los elementos EWS: correo electrónico de los mensajes, elementos de calendario, contactos, tareas, puede incluir datos adjuntos.
  
## <a name="types-of-attachments"></a>Tipos de datos adjuntos

EWS categoriza los datos adjuntos en dos grupos: los datos adjuntos y los datos adjuntos de elemento de archivo.
  
- **Los datos adjuntos de elemento:** Establecimiento inflexible de tipos de [elementos EWS](folders-and-items-in-ews-in-exchange.md), como mensajes de correo electrónico y elementos de calendario, que se adjuntan a otro elemento de EWS fuertemente tipado. Cualquier elemento de establecimiento inflexible de tipos que puede crearse mediante el uso de la API administrada de EWS o EWS puede usarse como datos adjuntos del elemento. El contenido de datos adjuntos del elemento es el elemento establecimiento inflexible de tipos, que proporciona acceso fácil a todas sus propiedades. Datos adjuntos de elemento pueden tener sus propio elemento de los datos adjuntos, por lo que es posible una jerarquía de los datos adjuntos de elemento (o el anidamiento de los datos adjuntos).
    
- **Los datos adjuntos del archivo:** Cualquier archivo, como .txt, .jpg, .zip, .pdf, o incluso un archivo .msg. Un archivo adjunto sólo tiene algunas propiedades, uno de los cuales es el contenido codificado de base-64 del archivo. 
    
- **Hacer referencia a los datos adjuntos:** Los datos adjuntos que se hace referencia por un proveedor de archivo, como un archivo que se encuentra en la nube. Puede ser un archivo adjunto de varios proveedores. 
    
Al agregar o recuperar los datos adjuntos de un elemento, podrá hacerlo diferente dependiendo de si es un archivo adjunto o un elemento de datos adjuntos. Por ejemplo, para agregar un archivo adjunto a un elemento, sólo puede pasar en la ubicación del archivo. Para agregar un elemento existente como datos adjuntos de elemento, realmente tener que copiar las propiedades o el contenido MIME del elemento existente a un nuevo elemento de datos adjuntos; simplemente no se puede enlazar el elemento existente. Por lo que distinguir entre los dos tipos de datos adjuntos es importante. Para obtener más detalles acerca de las diferencias entre los datos adjuntos de elemento y datos adjuntos de archivo se tratan en los artículos [de esta sección](#bk_inthissection).
  
## <a name="how-are-attachments-represented-programmatically"></a>¿Cómo se se representan mediante programación los datos adjuntos?

Los datos adjuntos se almacenan en una colección en el elemento EWS. La colección de datos adjuntos se compone de datos adjuntos de archivos o datos adjuntos de elemento. Metadatos acerca de la colección de datos adjuntos están disponible al obtener un elemento mediante el método de la API administrada de EWS [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) o la operación de EWS [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) , pero las llamadas adicionales necesarios para recuperar el contenido de los datos adjuntos. 
  
**La tabla 1. Elemento de metadatos sobre los datos adjuntos**

|**Entidad de metadatos**|**Propiedad de la API administrada de EWS**|**Elemento EWS**|
|:-----|:-----|:-----|
|Indicador de datos adjuntos (no marca los datos adjuntos en línea)  <br/> |[Item.HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](http://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |
|Colección de datos adjuntos  <br/> |[Item.Attachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[Datos adjuntos](http://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |
|Identificador de datos adjuntos  <br/> |[Attachment.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.id%28v=exchg.80%29.aspx) <br/> |[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |
   
**Tabla 2. Entidades de datos adjuntos**

|**Tipo de datos adjuntos**|**Clase de la API administrada de EWS**|**Elemento EWS**|
|:-----|:-----|:-----|
|Datos adjuntos del archivo  <br/> |[FileAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.fileattachment%28v=exchg.80%29.aspx) <br/> |[FileAttachment](http://msdn.microsoft.com/library/3ecea174-73d1-47fd-8917-6065cef1d565%28Office.15%29.aspx) <br/> |
|Datos adjuntos del elemento  <br/> |[ItemAttachment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemattachment%28v=exchg.80%29.aspx) <br/> [ItemAttachment\<TItem\>](http://msdn.microsoft.com/en-us/library/dd635165%28v=exchg.80%29.aspx) <br/> |[ItemAttachment](http://msdn.microsoft.com/library/089ee599-f45e-46f5-a18a-5cfb3d2851ff%28Office.15%29.aspx) <br/> |
|Datos adjuntos de referencia  <br/> |[ReferenceAttachmentType complexType (EWS)](http://msdn.microsoft.com/library/18bfa012-e903-d7f3-528a-31ccceb65463%28Office.15%29.aspx) <br/> |[ReferenceAttachment](http://msdn.microsoft.com/library/b9bde862-6b75-4a81-8033-00a47be4dc2f%28Office.15%29.aspx) <br/> |
   
## <a name="inline-attachments"></a>Datos adjuntos en línea

Incorporar datos adjuntos son un tipo especial de datos adjuntos. Ambos archivos adjuntos y los datos adjuntos de elemento pueden ser datos adjuntos en línea. Datos adjuntos en línea aparecen como parte del contenido del cuerpo y mantiene su posición en relación con el resto del contenido en el elemento. 
  
Datos adjuntos son datos adjuntos en línea si se establece la propiedad de la API administrada de EWS [IsInline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) o el elemento EWS [IsInline](http://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) en true. Datos adjuntos en línea usar las siguientes propiedades opcionales y elementos para identificar la ubicación de los datos adjuntos en línea: 
  
- API administrada de EWS: [ContentId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.contentid%28v=exchg.80%29.aspx) o [ContentLocation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.contentlocation%28v=exchg.80%29.aspx) propiedades. 
    
- EWS: Elemento [ContentId](http://msdn.microsoft.com/library/bc59100d-6079-414b-a6e0-7c15feaa3184%28Office.15%29.aspx) o [ContentLocation](http://msdn.microsoft.com/library/d91cf587-24e3-4c13-8784-5ca29787cca7%28Office.15%29.aspx) . 
    
Tenga en cuenta que la propiedad de la API administrada de EWS [HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) y el elemento EWS [HasAttachments](http://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) no reflejan la existencia de datos adjuntos en línea y que ha ¿por qué también se conocen como datos adjuntos en línea oculta los datos adjuntos. Por lo que si se establece la propiedad de la API administrada de EWS [IsInline](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) o el elemento EWS [IsInline](http://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) en true, y el elemento no tiene otros datos adjuntos, **HasAttachments** se establecerá en false. Si el cliente utiliza **HasAttachments** para rellenar un icono en un correo electrónico o un indicador de datos adjuntos, tenga en cuenta que el icono no aparecerá para los correos electrónicos con datos adjuntos en línea. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Agregar datos adjuntos mediante el uso de EWS en Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Obtener datos adjuntos mediante el uso de EWS en Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [Eliminar los datos adjuntos mediante el uso de EWS en Exchange](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Ver también
<a name="bk_additionalresources"> </a>

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Las carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Correo electrónico y EWS en Exchange](email-and-ews-in-exchange.md)
    


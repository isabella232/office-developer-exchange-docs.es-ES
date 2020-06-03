---
title: Datos adjuntos y EWS en Exchange
manager: sethgros
ms.date: 7/11/2016
ms.audience: Developer
ms.assetid: 8e4289a4-ec9d-4502-9854-c593c95d5f98
description: Obtenga información sobre los datos adjuntos y cómo la API administrada de EWS o EWS en el cliente de Exchange los representa.
localization_priority: Priority
ms.openlocfilehash: d37fef9ea14a3b42a0eed0240724fe69c8531c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528492"
---
# <a name="attachments-and-ews-in-exchange"></a>Datos adjuntos y EWS en Exchange

Obtenga información sobre los datos adjuntos y cómo la API administrada de EWS o EWS en el cliente de Exchange los representa.
  
Normalmente, los datos adjuntos están asociados a los elementos de correo electrónico, pero, de hecho, todos los elementos de EWS (mensajes de correo electrónico, elementos de calendario, contactos y tareas) pueden incluir datos adjuntos.
  
## <a name="types-of-attachments"></a>Tipos de datos adjuntos

EWS clasifica los datos adjuntos en dos grupos: archivos adjuntos y elementos adjuntos.
  
- **Datos adjuntos de elemento:** [Elementos EWS](folders-and-items-in-ews-in-exchange.md)con establecimiento inflexible de tipos, como mensajes de correo electrónico y elementos de calendario, que están asociados a otro elemento EWS con establecimiento inflexible de tipos. Cualquier elemento con establecimiento inflexible de tipos que se pueda crear mediante la API administrada de EWS o EWS puede usarse como datos adjuntos de un elemento. El contenido de los datos adjuntos de un elemento es el elemento con establecimiento inflexible de tipos, que proporciona acceso sencillo a todas sus propiedades. Los datos adjuntos de elemento pueden tener sus propios datos adjuntos, por lo que es posible que haya una jerarquía de elementos adjuntos (o anidación de datos adjuntos).
    
- **Archivos adjuntos:** Cualquier archivo, como un archivo. txt,. jpg,. zip,. pdf o incluso un archivo. msg. Los datos adjuntos de un archivo solo tienen algunas propiedades, uno de los cuales es el contenido codificado en base 64 del archivo. 
    
- **Datos adjuntos de referencia:** Cualquier dato adjunto al que haga referencia un proveedor de archivos, como un archivo ubicado en la nube. Los datos adjuntos pueden ser de varios proveedores. 
    
Cuando se agregan o se recuperan datos adjuntos de un elemento, se realiza de forma diferente en función de si se trata de un archivo adjunto o de un elemento adjunto. Por ejemplo, para agregar un archivo adjunto a un elemento, puede pasar solo la ubicación del archivo. Para agregar un elemento existente como datos adjuntos de elemento, en realidad tiene que copiar las propiedades o el contenido MIME del elemento existente a un nuevo adjunto de elemento; no se puede enlazar simplemente al elemento existente. Por lo tanto, es importante distinguir entre los dos tipos de datos adjuntos. En los artículos [de esta sección](#bk_inthissection)se describen más detalles sobre las diferencias entre los datos adjuntos de elementos y los archivos adjuntos.
  
## <a name="how-are-attachments-represented-programmatically"></a>¿Cómo se representan los datos adjuntos mediante programación?

Los datos adjuntos se almacenan en una colección en el elemento EWS. La colección Attachments está formada por datos adjuntos de archivo o elementos adjuntos. Los metadatos sobre la colección Attachments están disponibles cuando obtiene un elemento mediante el método [Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) de la API administrada de EWS o la operación de [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) de EWS, pero se requieren llamadas adicionales para recuperar realmente el contenido de los datos adjuntos. 
  
**Tabla 1. Metadatos de elemento sobre datos adjuntos**

|**Entidad de metadatos**|**Propiedad de la API administrada EWS**|**Elemento EWS**|
|:-----|:-----|:-----|
|Indicador de datos adjuntos (no marca datos adjuntos en línea)  <br/> |[Item. HasAttachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) <br/> |[HasAttachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) <br/> |
|Colección Attachment  <br/> |[Item. Attachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) <br/> |[Datos adjuntos](https://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx) <br/> |
|Identificador de datos adjuntos  <br/> |[Attachment.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.id%28v=exchg.80%29.aspx) <br/> |[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |
   
**Tabla 2. Entidades de datos adjuntos**

|**Tipo de datos adjuntos**|**Clase de API administrada de EWS**|**Elemento EWS**|
|:-----|:-----|:-----|
|Archivo adjunto  <br/> |[FileAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.fileattachment%28v=exchg.80%29.aspx) <br/> |[FileAttachment](https://msdn.microsoft.com/library/3ecea174-73d1-47fd-8917-6065cef1d565%28Office.15%29.aspx) <br/> |
|Datos adjuntos del elemento  <br/> |[ItemAttachment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemattachment%28v=exchg.80%29.aspx) <br/> [ItemAttachment\<TItem\>](https://msdn.microsoft.com/library/dd635165%28v=exchg.80%29.aspx) <br/> |[ItemAttachment](https://msdn.microsoft.com/library/089ee599-f45e-46f5-a18a-5cfb3d2851ff%28Office.15%29.aspx) <br/> |
|Datos adjuntos de referencia  <br/> |[ReferenceAttachmentType complexType (EWS)](https://msdn.microsoft.com/library/18bfa012-e903-d7f3-528a-31ccceb65463%28Office.15%29.aspx) <br/> |[ReferenceAttachment](https://msdn.microsoft.com/library/b9bde862-6b75-4a81-8033-00a47be4dc2f%28Office.15%29.aspx) <br/> |
   
## <a name="inline-attachments"></a>Datos adjuntos en línea

Los datos adjuntos en línea son una raza especial de datos adjuntos. Tanto los archivos adjuntos como los elementos adjuntos pueden ser datos adjuntos en línea. Los datos adjuntos en línea aparecen como parte del contenido del cuerpo y conservan su posición en relación con el resto del contenido del elemento. 
  
Los datos adjuntos son datos adjuntos en línea si la propiedad [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) de la API administrada de EWS o el elemento de la EWS [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) están establecidos en true. Los datos adjuntos en línea usan las siguientes propiedades y elementos opcionales para identificar la ubicación de los datos adjuntos en línea: 
  
- API administrada de EWS: propiedades de [contentid](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentid%28v=exchg.80%29.aspx) o [ContentLocation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.contentlocation%28v=exchg.80%29.aspx) . 
    
- EWS: elemento [contentid](https://msdn.microsoft.com/library/bc59100d-6079-414b-a6e0-7c15feaa3184%28Office.15%29.aspx) o [ContentLocation](https://msdn.microsoft.com/library/d91cf587-24e3-4c13-8784-5ca29787cca7%28Office.15%29.aspx) . 
    
Tenga en cuenta que la propiedad [HasAttachments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) de la API administrada de EWS y el elemento [HasAttachments](https://msdn.microsoft.com/library/538b7a85-11d7-4daa-8458-09b540760e8b%28Office.15%29.aspx) de EWS no reflejan la existencia de datos adjuntos en línea, por lo que los datos adjuntos en línea también se denominan datos adjuntos ocultos. Por lo tanto, si se establece la propiedad [IsInline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachment.isinline%28v=exchg.80%29.aspx) de la API administrada de EWS o el elemento de [IsInline](https://msdn.microsoft.com/library/5e7712c8-372a-4a16-be64-360c5ff3961a%28Office.15%29.aspx) de EWS en true, y el elemento no tiene otros datos adjuntos, **HasAttachments** se establecerá en false. Si el cliente usa **HasAttachments** para rellenar un indicador o icono de datos adjuntos en un correo electrónico, tenga en cuenta que el icono no aparecerá para los correos electrónicos con datos adjuntos en línea. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Adición de datos adjuntos mediante EWS en Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Obtener datos adjuntos mediante EWS en Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    
- [Eliminar datos adjuntos mediante EWS en Exchange](how-to-delete-attachments-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también
<a name="bk_additionalresources"> </a>

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Correo electrónico y EWS en Exchange](email-and-ews-in-exchange.md)
    


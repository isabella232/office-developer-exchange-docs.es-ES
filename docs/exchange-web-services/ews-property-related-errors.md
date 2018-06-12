---
title: Errores relacionados con la propiedad EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c4c5969-7bdd-4021-be0e-cae99e86cf2c
description: Descubra cómo tratar los errores relacionados con la propiedad en la aplicación de EWS.
ms.openlocfilehash: f214ab40c3717178c6957a9da93bdf89999fc1d3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763008"
---
# <a name="ews-property-related-errors"></a>Errores relacionados con la propiedad EWS

Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Descubra cómo tratar los errores relacionados con la propiedad en la aplicación de EWS.
  
La mayoría de las aplicaciones de cliente EWS se usan propiedades, lo que significa que debe tratar los errores relacionados con la propiedad. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS.
  
**Tabla 1: Errores relacionados con la propiedad y cómo controlarlos**

|**Error**|**Debido a un intento...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorDataSizeLimitExceeded  <br/> |Establecer una propiedad con un valor que supere el tamaño máximo de la propiedad o la propiedad no es compatible con la transmisión por secuencias, como las propiedades de la carpeta.  <br/> |Limitar el tamaño de datos se establece en la propiedad.  <br/> |
|ErrorFolderPropertRequestFailed  <br/> |Obtener una propiedad que no se pudieron recuperar.  <br/> |Que indica que no se puede recuperar la propiedad.  <br/> |
|ErrorInvalidExtendedProperty  <br/> |Establecer una combinación de valores de propiedad extendida o resultados no válida en el identificador uniforme de recursos (URI) de la propiedad extendida no es válida.  <br/> |Comprobar el valor de la propiedad extendida.  <br/> |
|ErrorInvalidExtendedPropertyValue  <br/> |Establecer un valor de propiedad extendida que no coincide con el tipo especificado  <br/> |Actualizar el código para comprobar tipos coincidentes.  <br/> |
|ErrorInvalidFolderId  <br/> |Establecer la estructura de un identificador de la carpeta en un formulario no válido.  <br/> |Sólo mediante identificadores devueltos por EWS.  <br/> |
|ErrorInvalidId  <br/> |Establecer la estructura de un identificador o cambiar la clave a un formulario no válido.  <br/> |Sólo mediante identificadores devueltos por EWS.  <br/> |
|ErrorInvalidIdEmpty  <br/> |Un identificador de conjunto vacío.  <br/> |Si se establece el identificador con un identificador de elemento o carpeta válido.  <br/> |
|ErrorInvalidIdMalformed  <br/> |Establecer la estructura de un identificador o cambiar la clave a un formulario no válido.  <br/> |Sólo mediante identificadores devueltos por EWS.  <br/> |
|ErrorInvalidPropertyAppend  <br/> |Anexar una propiedad que no es compatible con la anexión.  <br/> |Actualizar el código para que solo intenta anexar valores a las propiedades de la colección de destinatarios (para, Cc, CCO), las propiedades de la colección de Attendee (obligatorio, opcional, recursos), propiedad Body y la propiedad de origen.  <br/> |
|ErrorInvalidPropertyDelete  <br/> |Eliminar una propiedad que no es compatible con la eliminación.  <br/> |Actualizar el código para que no se intenta eliminar la propiedad. Por ejemplo, los identificadores de elemento y la carpeta no se puede eliminar.  <br/> |
|ErrorInvalidPropertyForExists  <br/> |Establecer una restricción de la búsqueda según existencialista en una propiedad basada en la marca.  <br/> |Actualizar el código para que no utilice propiedades de marca en una restricción de búsqueda según existencialista. Propiedades de marca son IsDraft, IsSubmitted, IsUnmodified, IsResend y IsFromMe.  <br/> |
|ErrorInvalidPropertyForOperation  <br/> |Actuar en una propiedad de un elemento o carpeta que no es compatible con la operación.  <br/> |Actualizar el código para no tener acceso a la propiedad con la operación que provocó el error.  <br/> |
|ErrorInvalidPropertyRequest  <br/> |Especifica una propiedad en la solicitud que no es compatible con el tipo de elemento.  <br/> |Actualizar el código para que no intente obtener acceso a la propiedad con la operación.  <br/> |
|ErrorInvalidPropertySet  <br/> |Establecer una propiedad de solo lectura.  <br/> |Actualizar el código para no intenta establecer la propiedad.  <br/> |
|ErrorInvalidValueForProperty  <br/> |Compare el valor de una propiedad en una restricción de búsqueda donde el valor de comparación no coincide con el tipo de propiedad.  <br/> |Actualizar el código para comprobar el error de coincidencia de tipo de propiedad.  <br/> |
|ErrorItemSavePropertyError  <br/> |Guardar un elemento o carpeta con los valores de propiedad no válido.  <br/> |Comprobación de los tipos y valores de propiedad antes de enviarlos en una solicitud.  <br/> |
|ErrorNoFolderClassOverride  <br/> |Establezca la clase de carpeta en una nueva carpeta que no es el tipo de carpeta base.  <br/> |Uso de un tipo de carpeta genérico para establecer la clase de la carpeta.  <br/> |
|ErrorNoPropertyTagForCustomProperties  <br/> |Hacer referencia a una propiedad extendida personalizada por su etiqueta de propiedad.  <br/> |Actualizar el código para hacer referencia a personalizados ampliado el identificador del conjunto de propiedad por propiedad y el nombre de la propiedad o el identificador de envío de la propiedad.  <br/> |
|ErrorObjectTypeChanged  <br/> |Establecer o actualizar la clase de elemento en un elemento que no coincide con su tipo de esquema.  <br/> |Actualizar el código para que la clase de elemento coincide con el tipo de elemento de esquema.  <br/> |
|ErrorPropertyUpdate  <br/> |Actualizar una propiedad con un valor de propiedad no válido.  <br/> |Comprobando el valor de la propiedad antes de enviarla en una solicitud de [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) .  <br/> |
|ErrorRequiredPropertyMissing  <br/> |Enviar una solicitud de CreateAttachment que falta una propiedad necesaria.  <br/> |Actualizar el código para establecer la propiedad falta según lo especificado por la ruta de acceso de la propiedad devuelto en la respuesta.  <br/> |
|ErrorUnsupportedMapiPropertyType  <br/> |Utilice la propiedad extendida de tipos de objeto de tipo, matriz de objetos, error o null.  <br/> |Actualizar el código para no usar los tipos de propiedad extendida restringidos.  <br/> |
|ErrorUnsupportedPathForQuery  <br/> |Use una ruta de acceso de propiedad no admitido en una restricción de búsqueda.  <br/> |Cambio de la restricción de la búsqueda para excluir la ruta de acceso de propiedad no admitido.  <br/> |
|ErrorUnsupportedPathForSortGroup  <br/> |Usar una ruta de acceso de propiedad no admitido en una solicitud de búsqueda ordenados o agrupados.  <br/> |Cambio de la restricción de la búsqueda para excluir la ruta de acceso de propiedad no admitido.  <br/> |
|ErrorUnsupportedTypeForConversion  <br/> |Solicitar un tipo de propiedad que no puede convertirse en XML de EWS devolver en una respuesta.  <br/> |Actualizar el código para no solicitar la propiedad no compatible.  <br/> |
|ErrorUpdatePropertyMismatch  <br/> |Actualizar un elemento o carpeta la descripción del cambio para que no coincide con la propiedad que se especifica para actualizarse.  <br/> |Cambiar el código para que la descripción del cambio coincide con el tipo de elemento o carpeta que se está actualizando.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Propiedades y propiedades extendidas de EWS en Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    


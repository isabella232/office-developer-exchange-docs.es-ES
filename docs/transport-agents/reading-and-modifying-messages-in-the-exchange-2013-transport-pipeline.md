---
title: Leer y modificar mensajes en la canalización de transporte de Exchange 2013
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b53ed47a-3d01-4c4e-ad32-fb0532872aad
description: Obtenga información sobre las clases de .NET Framework que puede usar en los agentes de transporte de Exchange 2013 para leer, escribir y modificar mensajes.
ms.openlocfilehash: 42d9dc7f05dce495b7695a2862af244313caffcb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527582"
---
# <a name="reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline"></a>Leer y modificar mensajes en la canalización de transporte de Exchange 2013

Obtenga información sobre las clases de .NET Framework que puede usar en los agentes de transporte de Exchange 2013 para leer, escribir y modificar mensajes.
  
**Se aplica a:** Exchange Server 2013
  
- Clases usadas para leer, escribir o modificar mensajes
- Espacio de nombres de los codificadores
- espacio de nombres iCalendar
- Espacio de nombres MIME
- Espacio de nombres TextConverters
- Espacio de nombres TNEF
- espacio de nombres vCard
  
A medida que los mensajes pasan por la canalización de transporte, el agente de transporte puede leer, escribir y convertir el contenido de los mensajes entre diferentes formatos de datos. Por ejemplo, puede leer y escribir datos MIME, identificar los mensajes entrantes que están en formato UUEncoded o entrecomillado imprimible (QP) y, a continuación, convertirlos a un estándar usado por su organización, o leer y, a continuación, guardar la información de contacto o de contacto asociada con los mensajes entrantes. 
  
También puede identificar el contenido que supone una amenaza para la seguridad y mover o eliminar el contenido o los mensajes que los contienen; por ejemplo, quitando los vínculos de un mensaje HTML.
  
En este artículo se proporciona información acerca de las clases de .NET Framework que puede usar para leer, escribir y modificar mensajes.
  
> [!CAUTION]
> Muchas de las propiedades y parámetros de las API de conversión de contenido permiten que los valores sean lo suficientemente grandes como para causar problemas de rendimiento, incluida la denegación de servicio. Cuando se usan las API de conversión de contenido en un agente de transporte, se deben implementar límites en los tamaños de valor de propiedad y parámetro admitidos al leer o escribir para limitar el consumo de recursos del agente. 

<a name="Namespaces"> </a>

## <a name="classes-used-to-read-write-or-modify-messages"></a>Clases usadas para leer, escribir o modificar mensajes

En la siguiente tabla se enumeran las clases de .NET Framework que puede usar para leer, escribir y modificar mensajes de correo electrónico.
  
**Espacios de nombres de procesamiento de mensajes de .NET Framework**

|**Espacio de nombres de .NET Framework**|**Clases**|
|:-----|:-----|
|[Microsoft. Exchange. Data. MIME. codificadores](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Contiene clases para codificar y descodificar la memoria, una clase de secuencia de codificador que acepta una de las clases de codificador o descodificador incluidas en una enumeración asociada, y la clase base [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) y la clase de excepción [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) para los codificadores y descodificadores.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Contiene tipos que permiten leer y escribir secuencias de datos que contienen información del calendario. Incluye un lector y un escritor de calendario, un objeto de excepción, un objeto de periodicidad y estructuras y enumeraciones que ayudan a devolver información sobre las propiedades de los elementos del calendario.  <br/> |
|[Microsoft. Exchange. Data. MIME](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Contiene clases, estructuras, enumeraciones y delegados que se pueden usar para crear, leer, escribir, recorrer, codificar y descodificar datos MIME. Incluye un lector y un escritor basados en secuencias que le proporciona acceso de lectura y escritura únicamente a secuencias de datos MIME, así como métodos y clases basados en DOM que puede usar en documentos MIME.  <br/> |
|[Microsoft. Exchange. Data. TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Contiene clases, estructuras, enumeraciones y delegados que permiten leer y escribir una secuencia de datos y realizar conversiones entre tipos de datos específicos; por ejemplo, HTML para el formato de texto enriquecido (RTF). Los convertidores de texto permiten cambiar el formato de una secuencia de documentos de un formulario a otro, así como quitar selectivamente los elementos de un documento que puedan representar un riesgo para la seguridad.  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. TNEF](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Contiene un lector y escritor de secuencias de solo avance, una clase de excepción y estructuras y enumeraciones que facilitan la lectura y escritura de datos de formato de encapsulación neutro para el transporte (TNEF).  <br/> |
|[Microsoft. Exchange. Data. ContentTypes. vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Contiene un lector y un escritor de secuencias de solo avance, una clase de excepción y estructuras y enumeraciones que facilitan la lectura y escritura de datos de contacto con formato vCard.  <br/> |
   
## <a name="encoders-namespace"></a>Espacio de nombres de los codificadores
<a name="Encoders"> </a>

El espacio de nombres de los codificadores contiene clases para la codificación y descodificación en memoria. Estos se heredan de la clase base [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) . Clases que se codifican y descodifican para Base64, BinHex, Entrecomilladoes imprimibles (QP) y UNIX a Unix (UU). Las siguientes clases se usan para la codificación y descodificación en memoria: 
  
- [Base64Encoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Encoder.aspx)
    
- [Base64Decoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Decoder.aspx)
    
- [BinHexEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexEncoder.aspx)
    
- [BinHexDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexDecoder.aspx)
    
- [QPEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPEncoder.aspx)
    
- [QPDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPDecoder.aspx)
    
- [UUEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUEncoder.aspx)
    
- [UUDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUDecoder.aspx)
    
Los codificadores y descodificadores heredan de la clase base [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) y usan la clase de excepción [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) para controlar los errores. 
  
Además, el espacio de nombres contiene la clase [MacBinaryHeader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.MacBinaryHeader.aspx) , que identifica los archivos codificados MacBinary y lee su encabezado de archivo asociado. 
  
Por último, la clase [EncoderStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStream.aspx) realiza una conversión en una secuencia de datos en lugar de un objeto en memoria. Esta clase acepta una de las clases de codificador o descodificador, y lee o escribe según la enumeración [EncoderStreamAccess](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStreamAccess.aspx) asociada. 
  
## <a name="icalendar-namespace"></a>espacio de nombres iCalendar
<a name="iCalendar"> </a>

El espacio de nombres iCalendar proporciona un lector y un escritor de sólo avance para los datos de iCalendar, además de admitir estructuras y clases para crear, obtener acceso y modificar secuencias de iCalendar.
  
Las clases [CalendarReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.aspx) y [CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) se usan para leer y escribir datos de secuencia iCalendar. 
  
El CalendarReader toma una [secuencia](https://msdn.microsoft.com/library/System.IO.Stream.aspx) legible como argumento de sus constructores. A continuación, puede usar los métodos [ReadFirstChildComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadFirstChildComponent.aspx), [ReadNextSiblingComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextSiblingComponent.aspx)y [ReadNextComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextComponent.aspx) para obtener acceso secuencialmente a los componentes de iCalendar en la secuencia de datos. Según el valor que haya establecido para la propiedad [ComplianceMode](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceMode.aspx) , los errores en la secuencia de iCalendar harán que se produzca una excepción o que la propiedad [ComplianceStatus](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceStatus.aspx) se establezca en un valor que no sea [compatible](https://msdn.microsoft.com/library/microsoft.exchange.data.contenttypes.icalendar.calendarcompliancestatus.aspx). Puede comprobar esta propiedad para descubrir cualquier problema con los datos de iCalendar entrantes. 
  
La clase [CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) toma una [secuencia](https://msdn.microsoft.com/library/System.IO.Stream.aspx) modificable como argumento a sus constructores. 
  
## <a name="mime-namespace"></a>Espacio de nombres MIME
<a name="MIME"> </a>

El espacio de nombres MIME proporciona clases que permiten crear, tener acceso y modificar documentos MIME. Puede trabajar con documentos MIME mediante un método basado en secuencias o en DOM.
  
### <a name="mimedocument-class-and-the-mime-dom"></a>Clase MimeDocument y DOM MIME

La clase [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) habilita el acceso de Dom a un documento MIME. Use los objetos de este tipo si tiene la memoria disponible para cargar un DOM completo y debe tener acceso aleatorio a los encabezados y al contenido del mensaje. 
  
Los datos se cargan en un objeto [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) mediante los métodos [GetLoadStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.GetLoadStream.aspx) o [Load](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.Load.aspx) . A continuación, puede recorrer la jerarquía DOM y crear, modificar o quitar datos MIME. Después de modificar los datos MIME, puede escribirlos en un objeto Stream mediante uno de los métodos [writeTo](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeNode.WriteTo.aspx) . 
  
En la siguiente figura se muestra la estructura de los datos dentro de un objeto [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) . 
  
**Figura 1. Estructura de objetos MimeDocument**

![Arquitectura DOM MIME](media/MimeDomArchitecture.gif)
  
### <a name="mimereader-and-mimewriter-classes-and-stream-based-mime-parsing"></a>Clases MimeReader y MimeWriter y análisis de MIME basado en secuencias

Las clases [MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) y [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) habilitan el acceso de solo avance a las secuencias MIME. Use estas clases cuando no tenga que cambiar los datos MIME que requieran datos que ya se hayan leído o escrito. Por ejemplo, si desea imprimir mensajes que se ajustan a un formato predefinido, la clase [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) podría ser ideal. 
  
La clase [MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) ENCAPSULA un Dom. Las clases [MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) y [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) representan equipos de estado. Sus Estados cambian en función de la entrada recibida y de los métodos a los que se llama. Las figuras 2 a 5 son diagramas de transición de estado simplificados que muestran, para el objeto [MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) , los métodos que son válidos para llamar desde cada Estado y el estado que se producirá. 
  
Para usar estos diagramas, siga las flechas de un estado a la siguiente, anotando las llamadas al método o los valores devueltos que hacen que cambie el estado. Por ejemplo, en el primer diagrama, supongamos que se encuentra al principio de la secuencia que pertenece a la MimeReader que ha creado. Para obtener el estado de los encabezados de parte, llame a uno de los [ReadNextPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadNextPart.aspx) o [ReadFirstChildPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadFirstChildPart.aspx), en ese orden. Si hay encabezados (es decir, si el MIME está bien formado), deberá especificar el estado de los encabezados de partes. De lo contrario, se producirá una excepción. 
  
**Figura 2. Diagrama de transición de estado simplificado para objetos MimeReader**

![Diagrama de estado de MimeReader](media/MimeReader_StateDiagram_01.gif)
  
> [!NOTE]
> Las figuras 3, 4 y 5 expanden los Estados que se muestran en cada uno de los diagramas anteriores. 
  
**Figura 3. Expansión del estado de los encabezados de parte de la figura 2**

![Expansión del estado 'Encabezados de partes'](media/MimeReader_StateDiagram_02.gif)
  
**Figura 4. Expansión del estado de encabezado de la figura 3 cuando se ha encontrado un parámetro en un encabezado**

![Expansión del estado 'Encabezados de partes'](media/MimeReader_StateDiagram_03.gif)
  
> [!NOTE]
> El estado representado en la figura 5 es recurrente en ese caso, si se encuentra un grupo de direcciones, puede usar la propiedad [GroupRecipientReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeAddressReader.GroupRecipientReader.aspx) para leer las direcciones del grupo. 
  
**Figura 5. Expansión del estado de encabezado de la figura 3 cuando se encuentra una dirección o un grupo de direcciones**

![Expansión del estado 'Encabezado' para dirección o grupo](media/MimeReader_StateDiagram_04.gif)
  
Las figuras 6 y 7 muestran diagramas de transición de estado simplificados para el objeto [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) . 
  
> [!NOTE]
> La figura 7 amplía el estado de los encabezados de partes que se muestran en la figura 6. 
  
**Figura 6. Diagrama de transición de estado simplificado para objetos MimeWriter**

![Diagrama de transición de estado para MimeWriter](media/MimeWriter_TopLevel.gif)
  
**Figura 7. Expansión del estado de los encabezados de parte en la figura 6**

![Expansión de diagrama de transición de estado para MimeWriter](media/MimeWriter_Diagram_Expansion.gif)
  
## <a name="textconverters-namespace"></a>Espacio de nombres TextConverters
<a name="TextConverters"> </a>

El espacio de nombres TextConverters contiene tipos que admiten la conversión del contenido de los mensajes de correo electrónico. Estos tipos pueden realizar la conversión de la página de códigos, quitar HTML que no es seguro y realizar otras transformaciones en los cuerpos de los mensajes de correo electrónico. El espacio de nombres [Microsoft. Exchange. Data. TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) incluye las siguientes clases que derivan de la clase abstracta [TextConverter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) : 
  
- [EnrichedToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToHtml.aspx)
    
- [EnrichedToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.EnrichedToText.aspx)
    
- [HtmlToEnriched](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToEnriched.aspx)
    
- [HtmlToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToHtml.aspx)
    
- [HtmlToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToRtf.aspx)
    
- [HtmlToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.HtmlToText.aspx)
    
- [RtfCompressedToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfCompressedToRtf.aspx)
    
- [RtfToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToHtml.aspx)
    
- [RtfToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtf.aspx)
    
- [RtfToRtfCompressed](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToRtfCompressed.aspx)
    
- [RtfToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.RtfToText.aspx)
    
- [TextToHtml](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToHtml.aspx)
    
- [TextToRtf](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToRtf.aspx)
    
- [TextToText](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextToText.aspx)
    
Estos convertidores de texto permiten cambiar el formato de una secuencia de documentos o quitar elementos que no son seguros de un documento HTML. Estas clases pueden usarse por sí mismas para realizar una conversión mediante una única llamada a uno de los métodos Convert de la clase base [TextConverter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) , o se pueden pasar a un constructor del convertidor, que la usa para realizar lecturas o escrituras convertidas. 
  
La funcionalidad heredada de la clase base es útil para realizar conversiones cuando hay suficiente espacio para almacenar el documento original y su resultado convertido, o cuando se desea almacenar los resultados de la conversión. El método **Convert** toma secuencias de entrada y salida, lectores de texto o escritores de texto y convierte el contenido de la entrada en el resultado asociado. 
  
En el espacio de nombres también se incluyen las siguientes clases de lector, escritor y secuencia de texto:
  
- [ConverterReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterReader.aspx) : derivada de **System. IO. TextReader**. 
    
- [ConverterWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterWriter.aspx) : derivada de **System. IO. TextWriter**. 
    
- [ConverterStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterStream.aspx) : derivada de **System. IO. Stream**. 
    
Estos se usan para realizar conversiones cuando no tiene espacio para almacenar el original o su salida convertido, cuando recibe la entrada del resultado o la envía a una secuencia, o cuando desea obtener el resultado solo para la indización o la búsqueda, por lo que no desea almacenar el resultado de una conversión.
  
## <a name="tnef-namespace"></a>Espacio de nombres TNEF
<a name="TNEF"> </a>

El espacio de nombres TNEF contiene clases y tipos que permiten la lectura y escritura de datos TNEF basados en secuencias de sólo avance. TNEF es un formato de datos que se usa para encapsular propiedades MAPI para clientes que no pueden interpretar MAPI.
  
Las clases [TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) y [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) proporcionan la funcionalidad principal del espacio de nombres [Microsoft. Exchange. Data. contentTypes. TNEF](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) . 
  
La clase [TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) toma una secuencia legible como argumento de sus constructores. A continuación, se usa el método [ReadNextAttribute](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadNextAttribute.aspx) para leer secuencialmente los atributos de la secuencia TNEF. Una vez que haya leído un atributo, puede obtener acceso a la información sobre el atributo mediante cualquiera de las propiedades de solo lectura en el objeto [TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) , además de obtener una [TnefPropertyReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefPropertyReader.aspx) para leer la propiedad actual. También puede tener acceso directamente al atributo actual mediante el método [ReadAttributeRawValue](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadAttributeRawValue.aspx) . 
  
La clase [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) toma una [secuencia](https://msdn.microsoft.com/library/System.IO.Stream.aspx) modificable como argumento a sus constructores. La clase [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) proporciona varias maneras de escribir datos en esta secuencia. 
  
## <a name="vcard-namespace"></a>espacio de nombres vCard
<a name="vCard"> </a>

El espacio de nombres vCard contiene clases, estructuras y enumeraciones que se usan para leer y escribir información de contacto en un mensaje de correo electrónico que se encuentra en el formato de datos vCard. El espacio de nombres contiene un lector y un escritor de contactos, una clase Exception, un lector de propiedades, un lector de parámetros y enumeraciones auxiliares que permiten leer datos vCard asociados a un mensaje de correo electrónico.
  
## <a name="see-also"></a>Vea también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)  
- [Conceptos del agente de transporte en Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- [Referencia del agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Tipos de medios MIME](http://www.iana.org/assignments/media-types)
    


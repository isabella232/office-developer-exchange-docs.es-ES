---
title: Lectura y modificación de mensajes en la canalización Exchange transporte de 2013
manager: sethgros
ms.date: 09/17/2021
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b53ed47a-3d01-4c4e-ad32-fb0532872aad
description: Obtenga información sobre las .NET Framework que puede usar en los agentes de transporte de Exchange 2013 para leer, escribir y modificar mensajes.
ms.openlocfilehash: 5bf4406f7ca82512bb55388e0865e0d343cae66e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537239"
---
# <a name="reading-and-modifying-messages-in-the-exchange-2013-transport-pipeline"></a>Lectura y modificación de mensajes en la canalización Exchange transporte de 2013

Obtenga información sobre las .NET Framework que puede usar en los agentes de transporte de Exchange 2013 para leer, escribir y modificar mensajes.
  
**Se aplica a:** Exchange Server 2013
  
- Clases usadas para leer, escribir o modificar mensajes
- Espacio de nombres de codificadores
- Espacio de nombres iCalendar
- Espacio de nombres MIME
- Espacio de nombres TextConverters
- Espacio de nombres Tnef
- Espacio de nombres vCard
  
A medida que los mensajes pasan por la canalización de transporte, el agente de transporte puede leer, escribir y convertir el contenido del mensaje entre diferentes formatos de datos. Por ejemplo, puede leer y escribir datos MIME, identificar los mensajes entrantes que están en formato Uuencoded o Quoted-printable (qp) y, a continuación, convertirlos a un estándar usado por su organización, o leer y guardar la información de calendario o contacto asociada con los mensajes entrantes. 
  
También puede identificar el contenido que representa una amenaza de seguridad y mover o eliminar el contenido o los mensajes que los contienen; por ejemplo, quitando vínculos en un mensaje HTML.
  
En este artículo se proporciona información sobre las .NET Framework que puede usar para leer, escribir y modificar mensajes.
  
> [!CAUTION]
> Muchas de las propiedades y parámetros de las API de conversión de contenido permiten valores lo suficientemente grandes como para causar problemas de rendimiento, incluida la denegación de servicio. Al usar las API de conversión de contenido en un agente de transporte, debe implementar límites en los tamaños de valor de propiedad y parámetro que admite al leer o escribir para limitar el consumo de recursos por parte del agente. 

<a name="Namespaces"> </a>

## <a name="classes-used-to-read-write-or-modify-messages"></a>Clases usadas para leer, escribir o modificar mensajes

En la tabla siguiente se enumeran las .NET Framework que puede usar para leer, escribir y modificar mensajes de correo electrónico.
  
**.NET Framework de procesamiento de mensajes**

|**.NET Framework espacio de nombres**|**Clases**|
|:-----|:-----|
|[Microsoft. Exchange. Data.Mime.Encoders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.aspx) <br/> |Contiene clases para codificación y descodificación en memoria, una clase de secuencia de codificador que acepta una de las clases de codificador o descodificador contenidas en una enumeración asociada, y la clase base [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) y la clase de excepción [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) para los codificadores y descodificadores.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.iCalendar](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.aspx) <br/> |Contiene tipos que permiten leer y escribir secuencias de datos que contienen información de calendario. Incluye un lector y un escritor de calendario, un objeto de excepción, un objeto de periodicidad y estructuras y enumeraciones que le ayudan a devolver información de propiedades acerca de los elementos del calendario.  <br/> |
|[Microsoft. Exchange. Data.Mime](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.aspx) <br/> |Contiene clases, estructuras, enumeraciones y delegados que puede usar para crear, leer, escribir, atravesar, codificar y descodificar datos MIME. Incluye un lector y un escritor basados en secuencias que le proporciona acceso de lectura y escritura de solo avance a secuencias de datos MIME, así como métodos y clases basados en DOM que puede usar en documentos MIME.  <br/> |
|[Microsoft. Exchange. Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) <br/> |Contiene clases, estructuras, enumeraciones y delegados que permiten leer y escribir un flujo de datos y realizar conversiones entre tipos de datos específicos; por ejemplo, HTML a formato de texto enriquecido (RTF). Los convertidores de texto permiten cambiar el formato de una secuencia de documentos de un formulario a otro, así como quitar selectivamente elementos de un documento que pueden suponer un riesgo para la seguridad.  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.Tnef](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) <br/> |Contiene un lector de secuencias y un escritor de solo avance, una clase de excepción y estructuras y enumeraciones que facilitan la lectura y escritura de datos de formato de encapsulación neutro de transporte (TNEF).  <br/> |
|[Microsoft. Exchange. Data.ContentTypes.vCard](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.vCard.aspx) <br/> |Contiene un lector de secuencias y un escritor de solo avance, una clase de excepción y estructuras y enumeraciones que facilitan la lectura y escritura de datos de contacto con formato vCard.  <br/> |
   
## <a name="encoders-namespace"></a>Espacio de nombres de codificadores
<a name="Encoders"> </a>

El espacio de nombres Encoders contiene clases para codificación y decodificación en memoria. Estos heredan de la clase base [ByteEncoder.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) Las clases codifican y descodifican para Base64, BinHex, Quoted-printable (qp) y Unix-to-Unix (Uu). Las siguientes clases se usan para codificar y decodificar en memoria: 
  
- [Base64Encoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Encoder.aspx)
    
- [Base64Decoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.Base64Decoder.aspx)
    
- [BinHexEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexEncoder.aspx)
    
- [BinHexDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.BinHexDecoder.aspx)
    
- [QPEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPEncoder.aspx)
    
- [QPDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.QPDecoder.aspx)
    
- [UUEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUEncoder.aspx)
    
- [UUDecoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.UUDecoder.aspx)
    
Los codificadores y descodificadores heredan de la clase base [ByteEncoder](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoder.aspx) y usan la clase de excepción [ByteEncoderException](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.ByteEncoderException.aspx) para el control de errores. 
  
Además, el espacio de nombres contiene la [clase MacBinaryHeader,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.MacBinaryHeader.aspx) que identifica los archivos codificados de MacBinary y lee su encabezado de archivo asociado. 
  
Por último, [la clase EncoderStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStream.aspx) realiza una conversión en una secuencia de datos en lugar de un objeto en memoria. Esta clase acepta una de las clases de codificador o descodificador y lee o escribe según la enumeración [EncoderStreamAccess](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.Encoders.EncoderStreamAccess.aspx) asociada. 
  
## <a name="icalendar-namespace"></a>Espacio de nombres iCalendar
<a name="iCalendar"> </a>

El espacio de nombres iCalendar proporciona un lector y un escritor de solo avance para los datos de iCalendar, además de admitir estructuras y clases para crear, acceder y modificar secuencias de iCalendar.
  
Las [clases CalendarReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.aspx) y [CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) se usan para leer y escribir datos de secuencia de iCalendar. 
  
CalendarReader toma un [stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx) legible como argumento para sus constructores. A continuación, puede usar los métodos [ReadFirstChildComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadFirstChildComponent.aspx), [ReadNextSiblingComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextSiblingComponent.aspx)y [ReadNextComponent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ReadNextComponent.aspx) para obtener acceso secuencialmente a los componentes de iCalendar en el flujo de datos. En función del valor que haya establecido para la propiedad [ComplianceMode,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceMode.aspx) los errores de la secuencia iCalendar provocarán una excepción o provocarán que la propiedad [ComplianceStatus](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarReader.ComplianceStatus.aspx) se establezca en un valor distinto de [Compliant](https://msdn.microsoft.com/library/microsoft.exchange.data.contenttypes.icalendar.calendarcompliancestatus.aspx). Puede comprobar esta propiedad para detectar cualquier problema con los datos iCalendar entrantes. 
  
La [clase CalendarWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.iCalendar.CalendarWriter.aspx) toma un [objeto Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx) grabable como argumento para sus constructores. 
  
## <a name="mime-namespace"></a>Espacio de nombres MIME
<a name="MIME"> </a>

El espacio de nombres MIME proporciona clases que permiten crear, acceder y modificar documentos MIME. Puede trabajar con documentos MIME mediante un método basado en secuencias o basado en DOM.
  
### <a name="mimedocument-class-and-the-mime-dom"></a>Clase MimeDocument y DOM MIME

La [clase MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) habilita el acceso DOM a un documento MIME. Use objetos de este tipo cuando tenga la memoria disponible para cargar un DOM completo y tenga acceso aleatorio a los encabezados y el contenido del mensaje. 
  
Los datos se cargan en [un objeto MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) mediante los [métodos GetLoadStream](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.GetLoadStream.aspx) [o Load.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.Load.aspx) A continuación, puede recorrer la jerarquía DOM y crear, modificar o quitar datos MIME. Después de modificar los datos MIME, puede escribir en una secuencia mediante uno de los [métodos WriteTo.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeNode.WriteTo.aspx) 
  
En la siguiente figura se muestra la estructura de los datos dentro de un [objeto MimeDocument.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) 
  
**Figura 1. Estructura de objetos MimeDocument**

![Arquitectura DOM MIME](media/MimeDomArchitecture.gif)
  
### <a name="mimereader-and-mimewriter-classes-and-stream-based-mime-parsing"></a>Clases MimeReader y MimeWriter y análisis MIME basado en secuencias

Las [clases MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) y [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) permiten el acceso de solo avance a secuencias MIME. Use estas clases cuando no tenga que cambiar los datos MIME que requieren datos que ya se han leído o escrito. Por ejemplo, si desea imprimir mensajes que se ajustan a un formato predefinido, la clase [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) puede ser ideal. 
  
La [clase MimeDocument](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeDocument.aspx) encapsula un DOM. Las [clases MimeReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) y [MimeWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) representan equipos de estado. Sus estados cambian en función de la entrada recibida y los métodos llamados. Las figuras 2 a 5 son diagramas simplificados de transición de estado que muestran, para el objeto [MimeReader,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.aspx) qué métodos son válidos para llamar desde cada estado y el estado que se dará como resultado. 
  
Para usar estos diagramas, siga las flechas de un estado al siguiente, notando las llamadas al método o valores devueltos que hacen que el estado cambie. Por ejemplo, en el primer diagrama, suponga que está al principio de la secuencia que pertenece al MimeReader que ha creado. Para obtener el estado encabezados de elemento, llame a uno de [ReadNextPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadNextPart.aspx) o [ReadFirstChildPart](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeReader.ReadFirstChildPart.aspx), en ese orden. Si hay encabezados (es decir, si el MIME está bien formado), entrará en el estado Encabezados de elemento. De lo contrario, se producirá una excepción. 
  
**Figura 2. Diagrama de transición de estado simplificado para objetos MimeReader**

![Diagrama de estado de MimeReader](media/MimeReader_StateDiagram_01.gif)
  
> [!NOTE]
> Las figuras 3, 4 y 5 se expanden en los estados que se muestran en cada uno de los diagramas anteriores. 
  
**Figura 3. Expansión del estado de encabezados de parte de la figura 2**

![Expansión del estado 'Encabezados de partes'](media/MimeReader_StateDiagram_02.gif)
  
**Figura 4. Expansión del estado de encabezado de la figura 3 cuando se ha encontrado un parámetro en un encabezado**

![Expansión del estado 'Encabezados de parte' cuando se ha encontrado un parámetro en un encabezado](media/MimeReader_StateDiagram_03.gif)
  
> [!NOTE]
> El estado representado por la figura 5 es recursivo en que, si se encuentra un grupo de direcciones, puede usar la propiedad [GroupRecipientReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeAddressReader.GroupRecipientReader.aspx) para leer las direcciones del grupo. 
  
**Figura 5. Expansión del estado de encabezado de la figura 3 cuando se encuentra una dirección o un grupo de direcciones**

![Expansión del estado 'Encabezado' para dirección o grupo](media/MimeReader_StateDiagram_04.gif)
  
Las figuras 6 y 7 muestran diagramas de transición de estado simplificados para el [objeto MimeWriter.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mime.MimeWriter.aspx) 
  
> [!NOTE]
> La figura 7 se expande en el estado de encabezados de elemento que se muestra en la figura 6. 
  
**Figura 6. Diagrama de transición de estado simplificado para objetos MimeWriter**

![Diagrama de transición de estado para MimeWriter](media/MimeWriter_TopLevel.gif)
  
**Figura 7. Expansión del estado de encabezados de parte de la figura 6**

![Expansión de diagrama de transición de estado para MimeWriter](media/MimeWriter_Diagram_Expansion.gif)
  
## <a name="textconverters-namespace"></a>Espacio de nombres TextConverters
<a name="TextConverters"> </a>

El espacio de nombres TextConverters contiene tipos que admiten la conversión del contenido de los mensajes de correo electrónico. Estos tipos pueden realizar la conversión de páginas de código, quitar HTML que no es seguro y realizar otras transformaciones en los cuerpos de mensajes de correo electrónico. [Microsoft.Exchange. El espacio de nombres Data.TextConverters](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.aspx) incluye las siguientes clases que derivan de la clase abstracta [TextConverter:](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) 
  
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
    
Estos convertidores de texto permiten cambiar el formato de una secuencia de documentos o quitar elementos que no son seguros de un documento HTML. Estas clases se pueden usar por sí mismas para realizar una conversión mediante una sola llamada a uno de los métodos Convert de la clase base [TextConverter,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.TextConverter.aspx) o se pueden pasar a un constructor del convertidor, que lo usa para realizar lecturas o escrituras convertida. 
  
La funcionalidad heredada de la clase base es útil para realizar conversiones cuando tiene suficiente espacio para almacenar el documento original y su resultado convertido, o cuando desea almacenar los resultados de la conversión. El **método Convert** toma secuencias de entrada y salida, lectores de texto o escritores de texto y convierte el contenido de la entrada en el resultado asociado. 
  
También se incluyen en el espacio de nombres las siguientes clases de lector de texto, escritor y secuencia:
  
- [ConverterReader:](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterReader.aspx) derivado de **System.IO.TextReader**. 
    
- [ConverterWriter:](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterWriter.aspx) derivado de **System.IO.TextWriter**. 
    
- [ConverterStream:](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.TextConverters.ConverterStream.aspx) derivado de **System.IO.Stream**. 
    
Se usan para realizar conversiones cuando no tiene espacio para almacenar el resultado original o convertido, cuando recibe la entrada de o envía el resultado a una secuencia, o cuando desea que el resultado solo se almacene con fines de indización o búsqueda y, por lo tanto, no desea almacenar el resultado de una conversión.
  
## <a name="tnef-namespace"></a>Espacio de nombres Tnef
<a name="TNEF"> </a>

El espacio de nombres Tnef contiene clases y tipos que permiten leer y escribir datos TNEF basados en secuencias de solo avance. TNEF es un formato de datos que se usa para encapsular propiedades MAPI para clientes que no pueden interpretar MAPI.
  
Las [clases TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) y [TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) proporcionan la funcionalidad principal en [microsoft.Exchange. Espacio de nombres Data.ContentTypes.Tnef.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.aspx) 
  
La [clase TnefReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) toma una secuencia legible como argumento para sus constructores. A continuación, use [el método ReadNextAttribute](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadNextAttribute.aspx) para leer secuencialmente los atributos de la secuencia TNEF. Después de leer un atributo, puede obtener acceso a información sobre el atributo mediante cualquiera de las propiedades de solo lectura del objeto [TnefReader,](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.aspx) además de obtener un [TnefPropertyReader](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefPropertyReader.aspx) para leer la propiedad actual. También puede obtener acceso directamente al atributo actual mediante el [método ReadAttributeRawValue.](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefReader.ReadAttributeRawValue.aspx) 
  
La [clase TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) toma un [objeto Stream](https://msdn.microsoft.com/library/System.IO.Stream.aspx) grabable como argumento para sus constructores. La [clase TnefWriter](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.ContentTypes.Tnef.TnefWriter.aspx) proporciona varias formas de escribir datos en esta secuencia. 
  
## <a name="vcard-namespace"></a>Espacio de nombres vCard
<a name="vCard"> </a>

El espacio de nombres vCard contiene clases, estructuras y enumeraciones que se usan para leer y escribir información de contacto contenida en un mensaje de correo electrónico con el formato de datos vCard. El espacio de nombres contiene un lector de contactos y un escritor, una clase de excepción, un lector de propiedades, un lector de parámetros y enumeraciones compatibles que permiten leer los datos de vCard asociados a un mensaje de correo electrónico.
  
## <a name="see-also"></a>Ver también

- [Agentes de transporte en Exchange](transport-agents-in-exchange-2013.md)  
- [Conceptos de agente de transporte Exchange 2013](transport-agent-concepts-in-exchange-2013.md) 
- [Referencia de agente de transporte para Exchange 2013](transport-agent-reference-for-exchange-2013.md)
- [Tipos de medios MIME](http://www.iana.org/assignments/media-types)
    


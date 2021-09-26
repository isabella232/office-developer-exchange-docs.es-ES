---
title: ExtendedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExtendedFieldURI
api_type:
- schema
ms.assetid: b3c6ea3a-9ead-44b9-9d99-64ecf12bde23
description: El elemento ExtendedFieldURI identifica una propiedad MAPI extendida.
ms.openlocfilehash: 0cf3926c900e1b1f35018c6706cfe99ebefbe76f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542319"
---
# <a name="extendedfielduri"></a>ExtendedFieldURI

El **elemento ExtendedFieldURI** identifica una propiedad MAPI extendida. 
  
```xml
<ExtendedFieldURI DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" />
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**DistinguishedPropertySetId** <br/> |Define los nombres de conjunto de propiedades conocidos para las propiedades MAPI extendidas.<br/><br/>Si se usa este atributo, no se pueden usar los atributos **PropertySetId** y **PropertyTag.** Este atributo debe usarse con el **atributo PropertyId** o **PropertyName** y el **atributo PropertyType.**<br/><br/>La **tabla atributo DistinguishedPropertySetId** más adelante en este tema enumera los valores posibles para este atributo.<br/><br/>Este atributo es opcional.  <br/> |
|**PropertySetId** <br/> |Identifica un espacio de nombres o un conjunto de propiedades extendidas MAPI por su GUID de identificación.<br/><br/>Si se usa este atributo, no se pueden usar los atributos **DistinguishedPropertySetId** y **PropertyTag.** Este atributo debe usarse con el **atributo PropertyId** o **PropertyName** y el **atributo PropertyType.**<br/><br/>Este atributo es opcional.  <br/> |
|**PropertyTag** <br/> |Identifica la etiqueta de propiedad sin la parte de tipo de la etiqueta. **PropertyTag** se puede representar como un número entero hexadecimal o corto.<br/><br/>El intervalo entre 0x8000 y 0xFFFE representa el intervalo personalizado de propiedades. Cuando una base de datos de buzones de correo encuentra una propiedad personalizada por primera vez, asigna a esa propiedad personalizada una etiqueta de propiedad dentro del intervalo de propiedades personalizadas de 0x8000-0xFFFE. Es muy probable que una etiqueta de propiedad personalizada determinada sea diferente entre las bases de datos. Por lo tanto, una solicitud de propiedad personalizada por etiqueta de propiedad puede devolver distintas propiedades en bases de datos diferentes. El uso del atributo **PropertyTag** está prohibido para las propiedades personalizadas. En su lugar, use el **atributo PropertySetId** y el **atributo PropertyName** **o PropertyId.**<br/><br/>**IMPORTANTE:** Obtenga acceso a cualquier propiedad personalizada entre 0x8000 y 0xFFFE mediante el GUID + nombre/identificador. Si se **usa el atributo PropertyTag,** no se pueden usar los atributos **DistinguishedPropertySetId**, **PropertySetId**, **PropertyName** y **PropertyId.**<br/><br/>Este atributo es opcional.<br/><br/>**NOTA:** No puede usar un atributo de etiqueta de propiedad para las propiedades dentro del intervalo personalizado 0x8000-0xFFFE. En este caso, debe usar una propiedad con nombre.           |
|**PropertyName** <br/> |Identifica una propiedad extendida por su nombre. Esta propiedad debe combinarse con **DistinguishedPropertySetId** o **PropertySetId**.<br/><br/>Si se usa este atributo, no se pueden usar los atributos **PropertyId** y **PropertyTag.**<br/><br/>Este atributo es opcional.  <br/> |
|**PropertyId** <br/> |Identifica una propiedad extendida por su identificador de envío. El identificador de envío se puede identificar en formatos decimales o hexadecimales. Esta propiedad debe combinarse con **DistinguishedPropertySetId** o **PropertySetId**.<br/><br/>Si se usa este atributo, no se pueden usar los atributos **PropertyName** y **PropertyTag.**<br/><br/>Este atributo es opcional.  <br/> |
|**PropertyType** <br/> |Representa el tipo de propiedad de una etiqueta de propiedad. Esto corresponde a la palabra menos significativa de una etiqueta de propiedad.<br/><br/>La tabla Atributo PropertyType más adelante en este tema contiene los valores posibles para este atributo.<br/><br/>Este atributo es obligatorio.  <br/> |
   
#### <a name="distinguishedpropertysetid-attribute"></a>Atributo DistinguishedPropertySetId

|**Valor**|**Descripción**|
|:-----|:-----|
|Dirección  <br/> |Identifica el identificador del conjunto de propiedades de dirección por su nombre.  <br/> |
|Cita  <br/> |Identifica el identificador del conjunto de propiedades de cita por su nombre.  <br/> |
|CalendarAssistant  <br/> |Identifica el identificador del conjunto de propiedades del asistente de calendario por su nombre.  <br/> |
|Común  <br/> |Identifica el identificador del conjunto de propiedades común por su nombre.  <br/> |
|InternetHeaders  <br/> |Identifica el identificador del conjunto de propiedades de encabezados de Internet por su nombre.  <br/> |
|Reunión  <br/> |Identifica el identificador del conjunto de propiedades de reunión por su nombre.  <br/> |
|Compartir  <br/> | <br/> |
|PublicStrings  <br/> |Identifica el identificador del conjunto de propiedades de cadenas públicas por su nombre.  <br/> |
|Tarea  <br/> |Identifica el identificador del conjunto de propiedades de tarea por su nombre.  <br/> |
|UnifiedMessaging  <br/> |Identifica el identificador del conjunto de propiedades de mensajería unificada por su nombre.  <br/> |
   
#### <a name="propertytype-attribute"></a>Atributo PropertyType

|**Valor**|**Descripción**|
|:-----|:-----|
|ApplicationTime  <br/> |Valor doble que se interpreta como fecha y hora. La parte entera es la fecha y la parte de fracción es la hora.  <br/> |
|ApplicationTimeArray  <br/> |Una matriz de valores dobles que se interpretan como una fecha y hora.  <br/> |
|Binario  <br/> |Un valor binario codificado en Base64.  <br/> |
|BinaryArray  <br/> |Matriz de valores binarios codificados en Base64.  <br/> |
|Booleano  <br/> |Un valor **booleano true** o **false**.  <br/> |
|CLSID  <br/> |Una cadena GUID.  <br/> |
|CLSIDArray  <br/> |Una matriz de cadenas GUID.  <br/> |
|Divisa  <br/> |Entero de 64 bits que se interpreta como el número de céntimos.  <br/> |
|CurrencyArray  <br/> |Una matriz de enteros de 64 bits que se interpretan como el número de céntimos.  <br/> |
|Doble  <br/> |Un valor de punto flotante de 64 bits.  <br/> |
|DoubleArray  <br/> |Una matriz de valores de punto flotante de 64 bits.  <br/> |
|Error  <br/> |Valor SCODE; Entero sin signo de 32 bits.  <br/> No se usa para restricciones ni para obtener o establecer valores. Esto solo existe para los informes.  <br/> |
|Float  <br/> |Un valor de punto flotante de 32 bits.  <br/> |
|FloatArray  <br/> |Matriz de valores de punto flotante de 32 bits.  <br/> |
|Entero  <br/> |Entero de 32 bits (Int32) firmado.  <br/> |
|IntegerArray  <br/> |Matriz de enteros de 32 bits (Int32) firmados.  <br/> |
|Long  <br/> |Entero de 64 bits (Int64) firmado o sin firmar.  <br/> |
|LongArray  <br/> |Una matriz de enteros de 64 bits (Int64) firmados o sin firmar.  <br/> |
|Null  <br/> |Indica que no hay ningún valor de propiedad.  <br/> No se usa para restricciones ni para obtener o establecer valores. Esto solo existe para los informes.  <br/> |
|Objeto  <br/> |Puntero a un objeto que implementa la interfaz IUnknown.  <br/> No se usa para restricciones ni para obtener o establecer valores. Esto solo existe para los informes.  <br/> |
|ObjectArray  <br/> |Una matriz de punteros a objetos que implementan la interfaz IUnknown.  <br/> No se usa para restricciones ni para obtener o establecer valores. Esto solo existe para los informes.  <br/> |
|Corta  <br/> |Entero de 16 bits firmado.  <br/> |
|ShortArray  <br/> |Una matriz de enteros de 16 bits firmados.  <br/> |
|SystemTime  <br/> |Un valor de tiempo y datos enteros de 64 bits en forma de una estructura FILETIME.  <br/> |
|SystemTimeArray  <br/> |Una matriz de datos enteros de 64 bits y valores de tiempo en forma de una estructura FILETIME.  <br/> |
|Cadena  <br/> |Una cadena Unicode.  <br/> |
|StringArray  <br/> |Una matriz de cadenas Unicode.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica propiedades extendidas en carpetas y elementos.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> | Identifica propiedades adicionales.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización de una sola propiedad de un elemento en una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Representa una actualización de una sola propiedad de una carpeta en una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Representa una operación de eliminación para eliminar una propiedad determinada de un elemento durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Representa una operación de eliminación para eliminar una propiedad determinada de una carpeta durante una llamada a UpdateFolder.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se anexarán a una sola propiedad de un elemento durante una [operación UpdateItem](updateitem-operation.md).  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |Especifica los datos que se anexarán a una propiedad folder durante una [operación UpdateFolder](updatefolder-operation.md).  <br/> |
|[Exists](exists.md) <br/> |Representa una expresión de búsqueda que devuelve **true** si la propiedad proporcionada existe en un elemento.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Representa una propiedad o un valor constante que se usará al comparar con otra propiedad.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y se evalúa como **true** si son iguales.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es mayor o igual que la segunda.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor que la segunda.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor que la segunda.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si los valores no son los mismos.  <br/> |
|[Excluye](excludes.md) <br/> |Realiza una máscara bit a bit de las propiedades.  <br/> |
|[Contains](contains.md) <br/> |Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionado.  <br/> |
|[FieldOrder](fieldorder.md) <br/> |Representa un único campo por el que se ordenan los resultados e indica la dirección de la ordenación.  <br/> |
   
## <a name="remarks"></a>Comentarios

Algunos atributos no se pueden usar en combinación con otros atributos. Cualquier solicitud que se incluye con una combinación no válida de atributos de propiedad extendida generará un mensaje de error.
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
> [!NOTE]
> En Microsoft .NET, un long es un entero con signo de 64 bits, mientras que en MAPI y COM, un long es un entero de 32 bits. La mayoría de los desarrolladores usarán Microsoft.NET Framework para desarrollar Exchange cliente de servicios web. Por lo tanto, se usa la nomenclatura .NET en lugar de la nomenclatura MAPI.
> 
> Por ejemplo, la PR_MESSAGE_FLAGS MAPI, 0x0E07, es un tipo PT \_ LONG. En .NET, esto se considera un entero. Una propiedad extendida para PR_MESSAGE_FLAGS se define como `<t:ExtendedFieldURI PropertyTag="0x0E07" PropertyType="Integer"/>` . 
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de una solicitud se crea un elemento que tiene dos propiedades personalizadas. La primera propiedad personalizada se denomina **IsMyHouse con** un valor booleano establecido en **true**. La segunda propiedad extendida personalizada se denomina **HousePrices**. Contiene una matriz de valores Currency. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
    MessageDisposition="SaveOnly">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </SavedItemFolderId>
      <Items>
        <t:Item>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Create an extended property</t:Subject>
          <t:Body BodyType="Text">Added info to extended props</t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="IsMyHouse" 
                                PropertyType="Boolean"/>
            <t:Value>true</t:Value>
          </t:ExtendedProperty>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI DistinguishedPropertySetId="PublicStrings" 
                                PropertyName="HousePrices" 
                                PropertyType="CurrencyArray"/>
            <t:Values>
              <t:Value>30000000</t:Value>
              <t:Value>40000000</t:Value>
              <t:Value>50000000</t:Value>
            </t:Values>
          </t:ExtendedProperty>
        </t:Item>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [FieldURI](fielduri.md)
- [IndexedFieldURI](indexedfielduri.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


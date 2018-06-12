---
title: ExtendedFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExtendedFieldURI
api_type:
- schema
ms.assetid: b3c6ea3a-9ead-44b9-9d99-64ecf12bde23
description: El elemento ExtendedFieldURI identifica una propiedad MAPI extendida.
ms.openlocfilehash: 8d946aec8ae2c5e6bb4ca3f1d8ee74250262d373
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764519"
---
# <a name="extendedfielduri"></a>ExtendedFieldURI

El elemento **ExtendedFieldURI** identifica una propiedad MAPI extendida. 
  
```xml
<ExtendedFieldURI DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" />
```

 **PathToExtendedFieldType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**DistinguishedPropertySetId** <br/> |Define la conocida (propiedad) establece los identificadores de las propiedades extendidas de MAPI.  <br/> Si se usa este atributo, no se puede usar los atributos **PropertySetId** y **PropertyTag** . Este atributo se debe usar con la **PropertyId** o **PropertyName** atributos y **PropertyType** .  <br/> La tabla de atributos **DistinguishedPropertySetId** más adelante en este tema enumera los valores posibles para este atributo.  <br/> Este atributo es opcional.  <br/> |
|**PropertySetId** <br/> |Identifica una MAPI extendida de la propiedad set o espacio de nombres por su GUID que identifica.  <br/> Si se usa este atributo, no se puede usar el atributo **DistinguishedPropertySetId** y **PropertyTag** . Este atributo se debe usar con la **PropertyId** o **PropertyName** atributos y **PropertyType** .  <br/> Este atributo es opcional.  <br/> |
|**PropertyTag** <br/> |Identifica a la etiqueta de la propiedad sin el elemento de tipo de la etiqueta. El **PropertyTag** se puede representar como valor hexadecimal o entero corto.  <br/> El intervalo entre 0 x 8000 y 0xFFFE representa el intervalo de propiedades personalizado. Cuando una base de datos de buzón de correo encuentra una propiedad personalizada por primera vez, asigna esa propiedad personalizada una etiqueta de propiedad dentro del intervalo de propiedad personalizada de 0 x 8000 0xFFFE. Es muy probable que será diferentes en una etiqueta de propiedad personalizada especificada a través de las bases de datos. Por lo tanto, una solicitud de propiedad personalizada mediante la etiqueta de la propiedad puede devolver distintas propiedades en las bases de datos diferentes. Se prohíbe el uso del atributo **PropertyTag** para las propiedades personalizadas. En su lugar, use el atributo **PropertySetId** y el atributo **PropertyName** o **PropertyId** .  <br/> > [!IMPORTANT]> Tener acceso a cualquier propiedad personalizada entre 0 x 8000 y 0xFFFE mediante el GUID + nombre o identificador.           Si se usa el atributo **PropertyTag** , no se puede usar los atributos **DistinguishedPropertySetId**, **PropertySetId**, **PropertyName**y **PropertyId** .  <br/> Este atributo es opcional.  <br/> > [!NOTE]> No puede usar un atributo de etiqueta de propiedad para las propiedades dentro del intervalo personalizado 0 x 8000 0xFFFE. En este caso debe utilizar una propiedad con nombre.           |
|**PropertyName** <br/> |Identifica una propiedad extendida por su nombre. Esta propiedad debe ser junto con **DistinguishedPropertySetId** o **PropertySetId**.  <br/> Si se usa este atributo, no se puede usar los atributos **PropertyId** y **PropertyTag** .  <br/> Este atributo es opcional.  <br/> |
|**PropertyId** <br/> |Identifica una propiedad extendida por su identificador de envío. El identificador de envío se puede identificar en formatos de decimales o hexadecimales. Esta propiedad debe ser junto con **DistinguishedPropertySetId** o **PropertySetId**.  <br/> Si se usa este atributo, no se puede usar los atributos **PropertyName** y **PropertyTag** .  <br/> Este atributo es opcional.  <br/> |
|**PropertyType** <br/> |Representa el tipo de propiedad de una etiqueta de propiedad. Esto corresponde a la palabra menos significativa en una etiqueta de propiedad.  <br/> La tabla de atributos de PropertyType más adelante en este tema contiene los valores posibles para este atributo.  <br/> Este atributo es necesario.  <br/> |
   
#### <a name="distinguishedpropertysetid-attribute"></a>Atributo DistinguishedPropertySetId

|**Valor**|**Descripción**|
|:-----|:-----|
|Reunión  <br/> |Identifica la reunión (propiedad) establece identificador por su nombre.  <br/> |
|Cita  <br/> |Identifica el identificador de conjunto de propiedades de cita por su nombre.  <br/> |
|Common  <br/> |Identifica el identificador de conjunto común de propiedad por su nombre.  <br/> |
|PublicStrings  <br/> |Identifica el identificador de conjunto de cadenas públicas propiedad por su nombre.  <br/> |
|Address  <br/> |Identifica el identificador de conjunto de propiedades de dirección por su nombre.  <br/> |
|InternetHeaders  <br/> |Identifica el identificador de conjunto de propiedad de los encabezados de Internet por su nombre.  <br/> |
|CalendarAssistant  <br/> |Identifica el identificador de conjunto de calendario Ayudante propiedad por su nombre.  <br/> |
|Ésta  <br/> |Identifica el identificador de conjunto de propiedad de mensajería unificada por su nombre.  <br/> |
   
#### <a name="propertytype-attribute"></a>Atributo PropertyType

|**Valor**|**Descripción**|
|:-----|:-----|
|ApplicationTime  <br/> |Un valor de tipo double que se interpreta como una fecha y hora. La parte entera es la fecha y la parte fraccionaria es la hora.  <br/> |
|ApplicationTimeArray  <br/> |Una matriz de valores de tipo dos que se interpreta como una fecha y hora.  <br/> |
|Binario  <br/> |Un valor binario con codificación Base64.  <br/> |
|BinaryArray  <br/> |Una matriz de valores binarios con codificación Base64.  <br/> |
|Boolean  <br/> |Un valor booleano **true** o **false**.  <br/> |
|CLSID  <br/> |Una cadena GUID.  <br/> |
|CLSIDArray  <br/> |Una matriz de cadenas GUID.  <br/> |
|Moneda  <br/> |Un entero de 64 bits que se interpreta como el número de céntimos.  <br/> |
|CurrencyArray  <br/> |Una matriz de enteros de 64 bits que se interpreta como el número de céntimos.  <br/> |
|Doble  <br/> |Un valor de punto flotante de 64 bits.  <br/> |
|DoubleArray  <br/> |Una matriz de valores de punto flotante de 64 bits.  <br/> |
|Error  <br/> |Valor SCODE; entero sin signo de 32 bits.  <br/> No se usa para las restricciones o para obtener o establecer valores. Esto sólo existe para informes.  <br/> |
|Flotante  <br/> |Un valor de punto flotante de 32 bits.  <br/> |
|FloatArray  <br/> |Una matriz de valores de punto flotante de 32 bits.  <br/> |
|Entero  <br/> |Un número entero con signo (Int32) de 32 bits.  <br/> |
|IntegerArray  <br/> |Una matriz de enteros (Int32) de 32 bits con signo.  <br/> |
|Long  <br/> |Un entero con o sin signo 64-bit (Int64).  <br/> |
|LongArray  <br/> |Una matriz de enteros (Int64) de 64 bits con o sin signo.  <br/> |
|Null  <br/> |No indica ningún valor de la propiedad.  <br/> No se usa para las restricciones o para obtener o establecer valores. Esto sólo existe para informes.  <br/> |
|Objeto  <br/> |Un puntero a un objeto que implementa la interfaz IUnknown.  <br/> No se usa para las restricciones o para obtener o establecer valores. Esto sólo existe para informes.  <br/> |
|ObjectArray  <br/> |Una matriz de punteros a objetos que implementan la interfaz IUnknown.  <br/> No se usa para las restricciones o para obtener o establecer valores. Esto sólo existe para informes.  <br/> |
|Corta  <br/> |Un entero de 16 bits.  <br/> |
|ShortArray  <br/> |Una matriz de enteros de 16 bits con signo.  <br/> |
|SystemTime  <br/> |Un entero de 64 bits datos valor y hora con el formato de una estructura FILETIME.  <br/> |
|SystemTimeArray  <br/> |Una matriz de valores de fecha y hora de entero de 64 bits con el formato de una estructura FILETIME.  <br/> |
|Cadena  <br/> |Una cadena Unicode.  <br/> |
|StringArray  <br/> |Una matriz de cadenas Unicode.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ExtendedProperty](extendedproperty.md) <br/> |Identifica las propiedades extendidas en carpetas y elementos.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> | Identifica las propiedades adicionales.  <br/>  Los siguientes son las expresiones de XPath para este elemento:  <br/>  `/FindFolder/FolderShape/AdditionalProperties` <br/>  `/GetFolder/FolderShape/AdditionalProperties` <br/>  `/SyncFolderHierarchy/FolderShape/AdditionalProperties` <br/>  `/GetItem/ItemShape/AdditionalProperties` <br/>  `/FindItem/ItemShape/AdditionalProperties` <br/>  `/SyncFolderItems/ItemShape/AdditionalProperties` <br/>  `/GetAttachment/AttachmentShape/AdditionalProperties` <br/> |
|[SetItemField](setitemfield.md) <br/> |Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Representa una actualización a una propiedad única en una carpeta en una [operación de UpdateFolder](updatefolder-operation.md).  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Representa una operación de eliminación para eliminar una propiedad determinada de un elemento durante una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[DeleteFolderField](deletefolderfield.md) <br/> |Representa una operación de eliminación para eliminar una propiedad determinada de una carpeta durante una llamada UpdateFolder.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifica los datos que se anexará a una sola propiedad de un elemento durante una [operación de UpdateItem](updateitem-operation.md).  <br/> |
|[AppendToFolderField](appendtofolderfield.md) <br/> |Especifica los datos que se anexará a una propiedad de la carpeta durante una [operación de UpdateFolder](updatefolder-operation.md).  <br/> |
|[Existe](exists.md) <br/> |Representa una expresión de búsqueda que devuelve **true** si existe la propiedad proporcionada en un elemento.  <br/> |
|[FieldURIOrConstant](fielduriorconstant.md) <br/> |Representa una propiedad o un valor constante que se usará cuando se comparan con otra propiedad.  <br/> |
|[IsEqualTo](isequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y se evalúa como **true** si son iguales.  <br/> |
|[IsGreaterThan](isgreaterthan.md) <br/> |Representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor.  <br/> |
|[IsGreaterThanOrEqualTo](isgreaterthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si la primera propiedad es mayor o igual que el segundo.  <br/> |
|[IsLessThan](islessthan.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor que el segundo.  <br/> |
|[IsLessThanOrEqualTo](islessthanorequalto.md) <br/> |Representa una expresión de búsqueda que compara una propiedad con un valor constante u otra propiedad y devuelve **true** si la primera propiedad es menor que el segundo.  <br/> |
|[IsNotEqualTo](isnotequalto.md) <br/> |Representa una expresión de búsqueda que se compara una propiedad con un valor constante o de otra propiedad y devuelve **true** si los valores no son los mismos.  <br/> |
|[Excluye](excludes.md) <br/> |Realiza una máscara de bit a bit de las propiedades.  <br/> |
|[Incluye](contains.md) <br/> |Representa una expresión de búsqueda que determina si una propiedad determinada contiene el valor de cadena constante proporcionada.  <br/> |
|[FieldOrder](fieldorder.md) <br/> |Representa un solo campo por el que se va a ordenar los resultados y se indica la dirección para la ordenación.  <br/> |
   
## <a name="remarks"></a>Notas

Algunos atributos no se puede usar en combinación con otros atributos. Cualquier solicitud que viene con una combinación no válida de atributos de la propiedad extendida generará un mensaje de error.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
> [!NOTE]
> En Microsoft. NET, un valor Long es un entero de 64 bits, mientras que en MAPI y COM, un valor Long es un entero de 32 bits. La mayoría de los desarrolladores usará Microsoft.NET Framework para desarrollar aplicaciones de cliente de servicios Web de Exchange. Por lo tanto, la nomenclatura de .NET se usa en lugar de la MAPI de nomenclatura. Por ejemplo, la propiedad MAPI PR_MESSAGE_FLAGS, 0x0E07, es un tipo PT_LONG. En. NET, esto se considera un número entero. Una propiedad extendida para PR_MESSAGE_FLAGS se define como \<t:ExtendedFieldURI PropertyTag = "0x0E07" PropertyType = "Entero" /\>. 
  
## <a name="example"></a>Ejemplo

El ejemplo siguiente de una solicitud, crea un elemento que tiene dos propiedades personalizadas. La primera propiedad personalizada se denomina **IsMyHouse** con un valor Boolean establecido en **true**. La segunda propiedad extendida personalizada se denomina **HousePrices**. Contiene una matriz de valores de moneda. 
  
```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[FieldURI](fielduri.md)
  
[IndexedFieldURI](indexedfielduri.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


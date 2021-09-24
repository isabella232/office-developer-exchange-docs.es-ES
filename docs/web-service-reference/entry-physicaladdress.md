---
title: Entry (PhysicalAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Entry
api_type:
- schema
ms.assetid: 9e5b6515-453e-4f4c-b55e-6ffefe23c31b
description: El elemento Entry describe una única dirección física para un elemento de contacto.
ms.openlocfilehash: b951c8c099a9653635e8fa95fe06204659b7d1fd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517108"
---
# <a name="entry-physicaladdress"></a>Entry (PhysicalAddress)

El **elemento Entry** describe una única dirección física para un elemento de contacto. 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 **PhysicalAddressDictionaryEntryType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Clave** <br/> | Identifica una dirección física.<br/><br/> Estos son los valores posibles para este atributo:<br/>  <br/>- Empresa  <br/>- Inicio  <br/>- Otros  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Calle](street.md) <br/> |Representa una dirección de calle de un elemento de contacto.  <br/> |
|[Ciudad](city.md) <br/> |Representa el nombre de la ciudad asociado a un contacto.  <br/> |
|[Estado](state-ex15websvcsotherref.md) <br/> |Representa el estado de residencia de un elemento de contacto.  <br/> |
|[CountryOrRegion](countryorregion.md) <br/> |Representa el país o la región de una dirección física determinada.  <br/> |
|[PostalCode](postalcode.md) <br/> |Representa el código postal de un elemento de contacto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PhysicalAddresses](physicaladdresses.md) <br/> |Contiene una colección de direcciones físicas asociadas a un contacto.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de contactos (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [Actualizar contactos](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Eliminación de contactos](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)


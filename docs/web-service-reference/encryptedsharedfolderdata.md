---
title: EncryptedSharedFolderData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EncryptedSharedFolderData
api_type:
- schema
ms.assetid: c1d4ca18-c5ce-41ff-bab4-f75e358c8b9f
description: El elemento EncryptedSharedFolderData contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de su calendario o datos de contacto con otros clientes.
ms.openlocfilehash: c86f615e8936a379f465afab337a264d27238537
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546626"
---
# <a name="encryptedsharedfolderdata"></a>EncryptedSharedFolderData

El **elemento EncryptedSharedFolderData** contiene los datos cifrados que un cliente puede usar para autorizar el uso compartido de su calendario o datos de contacto con otros clientes. 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 **EncryptedSharedFolderDataType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Token](token.md) <br/> |Contiene datos cifrados que representa el token de identificación de los datos compartidos.  <br/> |
|[Datos](data.md) <br/> |Contiene datos cifrados que representan los datos compartidos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[EncryptedSharedFolderDataCollection](encryptedsharedfolderdatacollection.md) <br/> |Representa una colección de estructuras de datos que un cliente puede usar para autorizar el uso compartido de su calendario o datos de contacto con otros clientes.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Servicios web del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación GetSharingMetadata](getsharingmetadata-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


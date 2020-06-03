---
title: Acceso a carpetas públicas con EWS en Exchange
manager: sethgros
ms.date: 7/17/2015
ms.audience: Developer
ms.assetid: d9372057-1deb-45de-8f98-b9149604429a
description: Obtenga información sobre cómo usar EWS y la API administrada de EWS para acceder a carpetas públicas y redirigir solicitudes de carpetas públicas en Exchange.
localization_priority: Priority
ms.openlocfilehash: e921a77b250e11e974b0c47b1d28a8e020837d44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460214"
---
# <a name="public-folder-access-with-ews-in-exchange"></a>Acceso a carpetas públicas con EWS en Exchange

Obtenga información sobre cómo usar EWS y la API administrada de EWS para acceder a carpetas públicas y redirigir solicitudes de carpetas públicas en Exchange.
  
Las carpetas públicas proporcionan un repositorio compartido de los elementos a los que pueden tener acceso los usuarios de su organización. Office 365, Exchange Online y las versiones locales de Exchange a partir de Exchange 2013 introducen una nueva arquitectura para las carpetas públicas. Las carpetas públicas de Exchange usan un diseño de buzón de correo especializado (en lugar de una base de datos de carpetas públicas) para almacenar la jerarquía de carpetas públicas y el contenido de las carpetas públicas. Los permisos de carpetas públicas se administran mediante el control de acceso basado en roles (RBAC).
  
Las tecnologías de acceso de cliente, como los servicios web Exchange (EWS) y la API administrada de EWS, proporcionan acceso mediante programación tanto a la jerarquía de carpetas públicas como a los elementos de contenido de una base de datos de carpetas públicas. En este artículo se proporciona información sobre cómo usar EWS y la API administrada de EWS para tener acceso a las carpetas públicas y a los datos de carpetas públicas y carpetas públicas. 
  
## <a name="ews-operations-and-ews-managed-api-methods-for-public-folder-access"></a>Operaciones de EWS y métodos de API administrada EWS para el acceso a carpetas públicas
<a name="bk_functionality"> </a>

La mayoría de las operaciones principales de EWS admiten el acceso a carpetas públicas. Puede usar las operaciones de carpeta y elemento y los métodos de API administrada de EWS que se enumeran en la tabla siguiente para trabajar con carpetas públicas.
  
Para obtener información sobre los métodos de la API administrada de EWS, vea los espacios de nombres de la [API administrada EWS](https://msdn.microsoft.com/library/jj220535%28v=exchg.80%29.aspx).
  
|**Operación de EWS**|**Método de la API administrada de EWS**|
|:-----|:-----|
|[Operación CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |**Folder. Save ()** <br/> |
|[Operación UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |**Folder. Update ()** <br/> |
|[Operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |**Folder. Delete ()** <br/> |
|[Operación](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx)<sup>1</sup> de MoveFolder <br/> |**Folder. Move ()** <br/> |
|[Operación CopyFolder](https://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx)<sup>2</sup> <br/> |**Folder. Copy ()** <br/> |
|[Operación GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |**Folder. BIND ()** <br/> |
|[EmptyFolder Operation](https://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx)<sup>3</sup> <br/> |**Folder. Empty ()** <br/> |
|[Operación FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |**ExchangeService. FindFolders ()** <br/> **Folder. FindFolders ()** <br/> |
|[Operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |**Item. Save ()** <br/> |
|[Operación MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |**Item. Move ()** <br/> |
|[Operación CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |**Item. Copy ()** <br/> |
|[Operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |**Item. Update ()** <br/> |
|[Operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |**Item. Delete ()** <br/> |
|[FindItem Operation](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)<sup>4</sup> <br/> |**ExchangeService. FindItems ()** <br/> **Folder. FindItems ()** <br/> |
|[Operación GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |**Item. BIND ()** <br/> |
|[Operación ConvertId](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)<sup>5</sup> <br/> |**ExchangeService. ConvertId ()** <br/> **ExchangeService. ConvertIds ()** <br/> |
   
<sup>1</sup> las carpetas que se mueven entre una carpeta pública y una carpeta privada no están disponibles en las versiones de Exchange a partir de Exchange 2013. 
  
<sup>2</sup> esta operación solo se aplica a las carpetas públicas de exchange Server 2007 y exchange Server 2010. 
  
<sup>3</sup> esta operación solo se aplica a las carpetas públicas de Exchange 2010. 
  
<sup>4</sup> la búsqueda de texto completo indizada dentro de una sola carpeta pública por medio de la opción de búsqueda QueryString se admite en las versiones de Exchange a partir de Exchange 2013. 
  
<sup>5</sup> la operación ConvertId no convierte correctamente los identificadores de carpeta pública del identificador EWS al identificador del almacén. Puede actualizar manualmente el identificador que se devuelve como [solución alternativa](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx#bk_usingConvertId).
  
Las siguientes operaciones no se admiten, o son parcialmente compatibles, en las carpetas públicas de las versiones de Exchange a partir de Exchange 2013:
  
- **CopyFolder** (no admitido). Puede usar **CreateFolder** con la operación **CopyItems** para implementar la funcionalidad de la operación de **CopyFolder** . 
    
- **EmptyFolder** (no admitido). Puede usar **FindItem** con la operación **DeleteItem** para implementar la funcionalidad de la operación **EmptyFolder** . 
    
- **MoveFolder** (compatible parcialmente). No se pueden mover carpetas entre carpetas privadas y públicas. Puede mover carpetas entre carpetas privadas y públicas en Exchange 2007 y Exchange 2010. Puede mover carpetas dentro de una carpeta pública en todas las versiones de Exchange. 
    
EWS y la API administrada de EWS no admiten las siguientes funciones para las carpetas públicas:
  
- Con **SyncFolderHierarchy**. Use las operaciones **FindFolder**, **GetFolder** y **SyncFolderItems** para sincronizar elementos y carpetas en un buzón de carpetas públicas. 
    
- Búsquedas de recorrido profundo de una jerarquía de carpetas públicas. Use llamadas de operación **FindFolder** recursivas para atravesar la jerarquía de carpetas públicas. 
    
- Uso de la operación **CreateFolderPath** para crear una jerarquía de carpetas para las carpetas públicas. Tendrá que usar la operación **CreateFolder** para cada nivel de carpeta en una jerarquía de carpetas distinta cuando se destina a un buzón de carpetas públicas. 
    
- Uso de la operación **CreateItem** para guardar copias de mensajes de correo electrónico enviados. En su lugar, use la operación **MoveItem** para mover una copia del mensaje a una carpeta pública. 
    
## <a name="scenarios-for-using-ews-and-the-ews-managed-api-to-work-with-public-folders"></a>Escenarios para usar EWS y la API administrada de EWS para trabajar con carpetas públicas
<a name="bk_scenarios"> </a>

Las carpetas públicas permiten muchos escenarios importantes para los usuarios de buzones de correo de Exchange. Puede proporcionar a los usuarios el uso de EWS y la API administrada de EWS para implementar soluciones personalizadas de acceso y uso de carpetas públicas y su contenido. 
  
### <a name="programmatically-access-email-messages-that-have-been-sent-to-distribution-lists"></a>Acceso mediante programación a los mensajes de correo electrónico enviados a listas de distribución

Los usuarios de buzones de Exchange pueden usar carpetas públicas para almacenar los mensajes de correo electrónico que se envían a listas de distribución. Esta es una forma cómoda de guardar el historial de la lista de distribución. Puede usar la [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) en EWS o los métodos **ExchangeService. FindItems ()** y **Folder. FINDITEMS ()** en la API administrada de EWS para tener acceso a los mensajes de correo electrónico de la lista de distribución almacenada. 
  
### <a name="share-important-email-messages-and-other-mailbox-items"></a>Compartir mensajes de correo electrónico importantes y otros elementos del buzón

Los usuarios de buzones de correo pueden usar las carpetas públicas como repositorio compartido para los elementos del buzón. Los distintos usuarios de una organización pueden compartir mensajes de correo electrónico importantes o contactos mediante carpetas públicas. EWS puede proporcionar el acceso a estos elementos de buzón compartidos. Puede usar la [operación MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) en EWS o el método **Item. Move ()** en la API administrada de EWS para mover mensajes de correo electrónico, contactos y otros elementos de buzón de correo a una carpeta pública. 
  
### <a name="public-discussions-with-post-items"></a>Discusiones públicas con elementos expuestos

Las carpetas públicas son un contenedor conveniente para los elementos post. Los elementos post proporcionan una forma de usar conversaciones encadenadas sin tener que enviar mensajes de correo electrónico entre usuarios. Los usuarios pueden usar carpetas públicas y elementos de publicación para hospedar y mantener conversaciones encadenadas entre diferentes usuarios de buzones de una organización. De esta forma, los usuarios de buzones de correo pueden tener acceso al historial compartido de una conversación que usa elementos post incluso si no formaban parte de la conversación. Puede usar la [operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) en EWS o el método **Item. Save ()** en la API administrada EWS para crear y responder a elementos almacenados en una carpeta pública. 
  
## <a name="routing-public-folder-requests"></a>Enrutamiento de solicitudes de carpetas públicas
<a name="bk_routing"> </a>

El contenido de las carpetas públicas se puede almacenar en varios servidores de buzones. La jerarquía de carpetas públicas se puede almacenar en un buzón de correo, mientras que el contenido de la carpeta pública se almacena en otro. Cada uno de estos servidores puede ser diferente del servidor de buzones de correo para el usuario que solicita la información. En estas situaciones, es importante incluir los encabezados X-AnchorMailbox y X-PublicFolderMailbox adicionales en las solicitudes de carpetas públicas para recibir información precisa sobre las carpetas públicas.
  
El valor de X-AnchorMailbox y X-PublicFolderMailbox puede variar en función de si está realizando una solicitud relacionada con la jerarquía de carpetas o con el contenido de la carpeta. En la siguiente tabla se identifica el procedimiento que se debe seguir para cada método de la API administrada de EWS o la operación de EWS.
  
**Métodos de API administrada de EWS y operaciones EWS para el enrutamiento de solicitudes de carpetas públicas**

|**Al llamar a estos métodos**|**Al llamar a estas operaciones**|**Use este procedimiento**|
|:-----|:-----|:-----|
|[Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder. Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |Enrutamiento de solicitudes de jerarquía de carpetas públicas  <br/> |
|[Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item. Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item. Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Enrutamiento de solicitudes de contenido de carpetas públicas  <br/> |
   
## <a name="version-differences"></a>Diferencias de versión
<a name="VersionDifferences"> </a>

En Exchange 2007 y Exchange 2010, la operación **ConvertId** funciona según lo esperado al convertir los identificadores de carpeta pública del identificador EWS al identificador del almacén. 
  
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Límites de carpetas públicas](https://technet.microsoft.com/library/dn594582%28v=exchg.150%29.aspx)
    
- [Preguntas frecuentes: carpetas públicas](https://technet.microsoft.com/library/jj552408.aspx)
    
- [Procedimientos de carpetas públicas](https://technet.microsoft.com/library/jj657481.aspx)
    


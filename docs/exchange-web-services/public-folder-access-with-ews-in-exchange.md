---
title: Carpetas públicas en Exchange obtener acceso con EWS
manager: sethgros
ms.date: 7/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d9372057-1deb-45de-8f98-b9149604429a
description: Obtenga información sobre cómo usar EWS y la API administrada de EWS para obtener acceso a las carpetas públicas y enrutar las solicitudes de carpetas públicas en Exchange.
ms.openlocfilehash: cfa089ba617dc760ed12883590e141debb5ecd9b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763300"
---
# <a name="public-folder-access-with-ews-in-exchange"></a>Carpetas públicas en Exchange obtener acceso con EWS

Obtenga información sobre cómo usar EWS y la API administrada de EWS para obtener acceso a las carpetas públicas y enrutar las solicitudes de carpetas públicas en Exchange.
  
Las carpetas públicas proporcionan un repositorio compartido de elementos que pueden tener acceso los usuarios de su organización. Office 365, Exchange Online y versiones locales de Exchange a partir de Exchange 2013 presentan una nueva arquitectura para las carpetas públicas. Las carpetas públicas en Exchange utilizan un diseño de buzón especializados (en lugar de una base de datos de carpetas públicas) para almacenar la jerarquía de carpetas públicas y el contenido de carpetas públicas. Permisos de carpetas públicas se administran a través de Control de acceso de en función de rol (RBAC).
  
Tecnologías de acceso de cliente, al igual que Exchange Web Services (EWS) y la API administrada de EWS, proporcionan acceso mediante programación a la jerarquía de carpetas públicas y los elementos de contenido en una base de datos de carpetas públicas. En este artículo se proporciona información acerca de cómo puede usar EWS y la API administrada de EWS para obtener acceso a las carpetas públicas y las carpetas públicas y datos de carpetas públicas. 
  
## <a name="ews-operations-and-ews-managed-api-methods-for-public-folder-access"></a>Las operaciones de EWS y métodos de la API administrada de EWS para acceso a carpetas públicas
<a name="bk_functionality"> </a>

La mayoría de las operaciones de EWS principales admite el acceso de carpeta pública. Puede usar las operaciones de carpetas y elementos y los métodos de la API administrada de EWS enumerados en la siguiente tabla para trabajar con carpetas públicas.
  
Para obtener información acerca de los métodos de la API administrada de EWS, vea [los espacios de nombres de la API administrada de EWS](http://msdn.microsoft.com/en-us/library/jj220535%28v=exchg.80%29.aspx).
  
|**Operación de EWS**|**Método de la API administrada de EWS**|
|:-----|:-----|
|[Operación CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |**Folder.Save()** <br/> |
|[Operación UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |**Folder.Update()** <br/> |
|[Operación DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |**Folder.Delete()** <br/> |
|[Operación MoveFolder](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <sup>1</sup> <br/> |**Folder.Move()** <br/> |
|[Operación CopyFolder](http://msdn.microsoft.com/library/c7ea0d68-9793-4144-b378-d99536776db9%28Office.15%29.aspx) <sup>2</sup> <br/> |**Folder.Copy()** <br/> |
|[Operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |**Folder.Bind()** <br/> |
|[Operación EmptyFolder](http://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx) <sup>3</sup> <br/> |**Folder.Empty()** <br/> |
|[Operación FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |**ExchangeService.FindFolders()** <br/> **Folder.FindFolders()** <br/> |
|[Operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |**Item.Save()** <br/> |
|[Operación MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |**Item.Move()** <br/> |
|[Operación CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |**Item.Copy()** <br/> |
|[Operación UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |**Item.Update()** <br/> |
|[Operación DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |**Item.Delete()** <br/> |
|[Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <sup>4</sup> <br/> |**ExchangeService.FindItems()** <br/> **Folder.FindItems()** <br/> |
|[Operación GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |**Item.Bind()** <br/> |
|[Operación ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) <sup>5</sup> <br/> |**ExchangeService.ConvertId()** <br/> **ExchangeService.ConvertIds()** <br/> |
   
<sup>1</sup> no está disponible en las versiones de Exchange a partir de Exchange 2013 mover carpetas entre una carpeta pública y la carpeta privada. 
  
<sup>2</sup> esta operación sólo es aplicable a las carpetas públicas en Exchange Server 2007 y Exchange Server 2010. 
  
<sup>3</sup> esta operación sólo es aplicable a las carpetas públicas en Exchange 2010. 
  
<sup>4</sup> indizado búsqueda de texto completo dentro de una única carpeta pública mediante la opción de búsqueda de la cadena de consulta se admite en las versiones de Exchange a partir de Exchange 2013. 
  
<sup>5</sup> ConvertId la operación no convierte correctamente los identificadores de carpetas públicas desde el identificador de EWS para el identificador de almacén. Puede actualizar manualmente el identificador que se devuelve como una [solución alternativa](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx#bk_usingConvertId).
  
Las siguientes operaciones no son compatibles o parcialmente compatibles, para las carpetas públicas en las versiones de Exchange 2013 a partir de Exchange:
  
- **CopyFolder** (no compatible). Puede usar **CreateFolder** con la operación de **CopyItems** para implementar la funcionalidad de operación **CopyFolder** . 
    
- **EmptyFolder** (no compatible). Puede usar **FindItem** con la operación **DeleteItem** para implementar la funcionalidad de operación **EmptyFolder** . 
    
- **MoveFolder** (parcialmente compatible). No se puede mover carpetas entre carpetas públicas y privadas. Puede mover carpetas entre carpetas privadas y públicas en Exchange 2007 y Exchange 2010. Puede mover carpetas dentro de una carpeta pública en todas las versiones de Exchange. 
    
EWS y la API administrada de EWS no admiten la siguiente funcionalidad para las carpetas públicas:
  
- Uso de **SyncFolderHierarchy**. Usar las operaciones **FindFolder**, **GetFolder** y **SyncFolderItems** para sincronizar los elementos y carpetas en un buzón de correo de carpetas públicas. 
    
- Búsquedas de recorrido de análisis de una jerarquía de carpetas públicas. Utilizar recursiva **FindFolder** operación llamadas para atravesar la jerarquía de carpetas públicas. 
    
- Uso de la operación de **CreateFolderPath** para crear una jerarquía de carpeta para carpetas públicas. Debe usar la operación de **CreateFolder** para cada nivel de carpeta en una jerarquía de carpetas distintos cuando el destino de un buzón de correo de carpetas públicas. 
    
- Mediante la operación **CreateItem** para guardar copias de mensajes de correo electrónico enviado. En su lugar, use la operación **MoveItem** para mover una copia del mensaje a una carpeta pública. 
    
## <a name="scenarios-for-using-ews-and-the-ews-managed-api-to-work-with-public-folders"></a>Escenarios de uso de EWS y la API administrada de EWS para trabajar con carpetas públicas
<a name="bk_scenarios"> </a>

Las carpetas públicas permiten muchos escenarios importantes para los usuarios del buzón de Exchange. Puede ofrecer a los usuarios mediante el uso de EWS y la API administrada de EWS para la implementación de soluciones personalizadas de acceso y uso de las carpetas públicas y su contenido. 
  
### <a name="programmatically-access-email-messages-that-have-been-sent-to-distribution-lists"></a>Mediante programación mensajes de correo electrónico de acceso que se han enviado a listas de distribución

Los usuarios del buzón de Exchange pueden utilizar las carpetas públicas para almacenar mensajes de correo electrónico que se envían a las listas de distribución. Esto es una forma cómoda para guardar el historial de la lista de distribución. Puede usar la [operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) en EWS o los métodos **ExchangeService.FindItems()** y **Folder.FindItems()** en la API administrada de EWS para obtener acceso a mensajes de correo electrónico de lista de distribución almacenado. 
  
### <a name="share-important-email-messages-and-other-mailbox-items"></a>Compartir mensajes de correo electrónico importantes y otros elementos del buzón de correo

Los usuarios del buzón pueden utilizar las carpetas públicas como un repositorio compartido para los elementos del buzón. Los usuarios diferentes en una organización pueden compartir mensajes de correo electrónico importantes o contactos mediante el uso de las carpetas públicas. EWS puede proporcionar el acceso a estos elementos de buzón compartido. Puede usar la [operación MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) en EWS o el método **Item.Move()** en la API administrada de EWS para mover mensajes de correo electrónico, contactos y otros elementos del buzón de correo y desconectarse de una carpeta pública. 
  
### <a name="public-discussions-with-post-items"></a>Discusiones públicas con los elementos de entrada

Las carpetas públicas son un contenedor adecuado para los elementos de entrada. Elementos para exponer proporcionan una forma de usar conversaciones encadenadas sin tener que enviar mensajes de correo electrónico entre los usuarios. Los usuarios pueden utilizar las carpetas públicas y publicar elementos para hospedar y mantener conversaciones encadenadas entre los usuarios de buzones diferentes en una organización. De este modo, los usuarios del buzón pueden tener acceso al historial compartido de una conversación que usa registra elementos incluso si no formaran parte de la conversación. Puede usar la [operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) en EWS o el método **Item.Save()** en la API administrada de EWS para crear y responder para registrar elementos almacenados en una carpeta pública. 
  
## <a name="routing-public-folder-requests"></a>Enrutamiento de las solicitudes de carpetas públicas
<a name="bk_routing"> </a>

Contenido de carpetas públicas se puede almacenar en varios servidores de buzón de correo. La jerarquía de carpetas públicas puede almacenarse en un buzón de correo, mientras que el contenido de la carpeta pública se almacena en otro. Y cada uno de estos servidores puede ser diferente que el servidor de buzón de correo del usuario que solicita la información. En estas situaciones, es importante incluir los encabezados X-AnchorMailbox y X-PublicFolderMailbox adicionales en sus solicitudes de carpeta pública para recibir información precisa sobre las carpetas públicas.
  
El valor de X-AnchorMailbox y X-PublicFolderMailbox puede variar dependiendo de si está realizando una solicitud relacionados con la jerarquía de carpetas o el contenido de la carpeta. En la siguiente tabla identifica qué procedimiento que se deben seguir para cada método de la API administrada de EWS o la operación de EWS.
  
**Métodos de la API administrada de EWS y las operaciones de EWS para enrutar solicitudes de carpetas públicas**

|**Cuando se llama a estos métodos**|**Cuando se llama a estas operaciones**|**Use este procedimiento**|
|:-----|:-----|:-----|
|[Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |Enrutamiento de las solicitudes de jerarquía de carpetas públicas  <br/> |
|[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Enrutamiento de las solicitudes de contenido de carpetas públicas  <br/> |
   
## <a name="version-differences"></a>Diferencias de versión
<a name="VersionDifferences"> </a>

En Exchange 2007 y Exchange 2010, la operación de **ConvertId** funciona según lo esperado cuando se convierte identificadores de carpetas públicas desde el identificador de EWS para el identificador de almacén. 
  
## <a name="see-also"></a>Ver también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Límites de carpetas públicas](http://technet.microsoft.com/en-us/library/dn594582%28v=exchg.150%29.aspx)
    
- [P+F: Carpetas públicas](http://technet.microsoft.com/en-us/library/jj552408.aspx)
    
- [Procedimientos de carpeta pública](http://technet.microsoft.com/en-us/library/jj657481.aspx)
    


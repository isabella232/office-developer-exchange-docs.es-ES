---
title: Configuración de aplicación persistente en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: Obtenga información sobre las diferentes opciones que puede usar la API administrada de EWS o la aplicación de EWS para crear configuraciones de aplicaciones personalizadas persistentes en Exchange.
ms.openlocfilehash: b1faa057e5a0c1a96498efcc23738c83d25ae986
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457406"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>Configuración de aplicación persistente en EWS en Exchange

Obtenga información sobre las diferentes opciones que puede usar la API administrada de EWS o la aplicación de EWS para crear configuraciones de aplicaciones personalizadas persistentes en Exchange.
  

  
La forma más sencilla de mantener la configuración de cliente personalizada en sincronización para un buzón, o carpetas y elementos en un buzón de correo, es almacenar la configuración de la aplicación en un servidor de Exchange. Puede asegurarse de que la configuración persiste para un buzón con una de las siguientes opciones: 
  
- Objetos de configuración de usuario
    
- Propiedades extendidas
    
- Elementos personalizados
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>¿Cuáles son mis opciones para crear una configuración de aplicación persistente?
<a name="Options"> </a>

Los objetos de configuración de usuario son la mejor opción para almacenar las opciones de configuración de las aplicaciones cliente de EWS. También puede usar las propiedades extendidas o los elementos personalizados, o bien una combinación de los tres. Elija su opción según el ámbito de la configuración y si la configuración debe estar disponible para otras aplicaciones.
  
**Tabla 1. Opciones recomendadas para crear una configuración de aplicación persistente basada en el ámbito**

|**Ámbito de configuración**|**Use…**|**Al que tiene acceso**|
|:-----|:-----|:-----|
|Elemento  <br/> |Una propiedad extendida de un elemento existente.  <br/> |Cualquier aplicación de EWS. Solo los clientes EWS que conocen el identificador de propiedad pueden tener acceso a una propiedad extendida.  <br/> |
|Folder  <br/> |Un objeto de configuración de usuario en la carpeta de destino. Esta es una buena forma de guardar la configuración de vista de una carpeta.  <br/> |Cualquier aplicación de EWS.  <br/> |
|Buzón de correo  <br/> |Un objeto de configuración de usuario en la carpeta msgrootfolder predeterminada.  <br/> |Cualquier aplicación de EWS.  <br/> |
   
### <a name="user-configuration-objects"></a>Objetos de configuración de usuario
<a name="UserConfig"> </a>

Los objetos de configuración de usuario son elementos especiales que están asociados a carpetas en un buzón. Los objetos de configuración de usuario, también conocidos como elementos asociados de carpeta, suelen ser la mejor opción para conservar la configuración de la aplicación, sobre todo si la información de configuración está asociada a una carpeta o a un buzón. Por lo general, no se exponen a los usuarios finales. Dado que pueden almacenar de forma nativa secuencias de datos y diccionarios de datos, son ideales para almacenar información de configuración. La mejor manera de usar los objetos de configuración de usuario es almacenar un conjunto de configuraciones en un documento XML y, a continuación, guardar la información en una de las propiedades de la secuencia de configuración del usuario.
  
Se obtiene acceso a los objetos de configuración de usuario de forma diferente a la de los demás tipos de elemento almacenados en un buzón. Puede usar el método de la API administrada de EWS [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) o la operación de EWS de [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar todos los elementos, pero debe usar la opción de recorrido de búsqueda **asociado** para buscar objetos de configuración de usuario. El recorrido de búsqueda **asociado** indica que los resultados de la búsqueda solo deben contener objetos de configuración de usuario. EWS incluye un conjunto de operaciones que son específicas de los objetos de configuración de usuario. 
  
**Tabla 1. Operaciones de EWS y métodos de API administrada de EWS para trabajar con objetos de configuración de usuario**

|**Para**|**Usar esta operación de EWS**|**Usar este método de API administrada de EWS**|
|:-----|:-----|:-----|
|Crear un objeto de configuración de usuario  <br/> |[Operación CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|Obtener un objeto de configuración de usuario  <br/> |[Operación GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration. Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|Actualizar un objeto de configuración de usuario  <br/> |[Operación UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|Eliminación de un objeto de configuración de usuario  <br/> |[Operación DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> Los objetos de configuración de usuario creados mediante EWS tienen un prefijo [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) que empieza con "IPM. Configuración. ". El **ItemClass** de un objeto de configuración de usuario es el prefijo del objeto de configuración de usuario y su nombre de objeto de configuración de usuario. Puede usar la propiedad [Item. ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) de la API administrada de EWS o el elemento EWS **ItemClass** para buscar los objetos de configuración de usuario que haya definido. 
  
### <a name="extended-properties"></a>Propiedades extendidas
<a name="ExtendedProperties"> </a>

Utilice [propiedades extendidas](properties-and-extended-properties-in-ews-in-exchange.md) si desea almacenar información de configuración en elementos. EWS, a diferencia de MAPI, no devuelve un contenedor de propiedades para los elementos. Esto significa que un cliente de EWS debe conocer el identificador de propiedad extendida para buscar y obtener acceso a la propiedad extendida. Si necesita almacenar información de configuración en elementos distintos de los objetos de configuración de usuario, el uso de propiedades extendidas para crear propiedades personalizadas podría ser la solución. Las propiedades extendidas le permiten tener acceso y almacenar información sobre las propiedades que no forman parte del conjunto de propiedades estándar de un elemento. 
  
> [!IMPORTANT]
> El esquema de base de datos de Exchange tiene un número finito de propiedades. El número máximo de identificadores de propiedad para una base de datos de Exchange es de 32.767. Si está usando propiedades extendidas para almacenar muchas opciones de configuración, le sugerimos que use una única propiedad extendida para almacenar dicha configuración de modo que no supere este máximo. 
  
Puede usar el método [Item. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) de la API administrada de EWS o la operación de EWS [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para establecer propiedades extendidas en objetos de configuración de usuario. 
  
### <a name="custom-items"></a>Elementos personalizados
<a name="CustomItems"> </a>

Los elementos personalizados también pueden usarse para almacenar información. Las propiedades de elemento existentes pueden reasignarse para que contengan información de configuración. O bien, puede usar las propiedades extendidas para definir sus propias propiedades para la aplicación. El uso de elementos personalizados para almacenar la configuración proporciona las siguientes ventajas: 
  
- Funcionan en todas las versiones de Exchange que admiten EWS.
    
- Si no usa propiedades extendidas en el elemento, no se cargará el presupuesto de las propiedades de Exchange.
    
## <a name="where-should-i-store-my-application-settings"></a>¿Dónde se debe almacenar la configuración de la aplicación?
<a name="ApplicationSettingsLocation"> </a>

Las carpetas de buzones de correo y los elementos que contiene se encuentran en la carpeta raíz del mensaje. Esta carpeta se identifica mediante el valor [WellKnownFolderName. msgfolderroot](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) en la API administrada de EWS. En términos de MAPI, este es el equivalente del subárbol IPM de un buzón de correo. Los objetos de configuración de usuario suelen usarse para crear configuraciones basadas en la interfaz de usuario, de modo que una aplicación pueda representar la configuración de la vista basada en la carpeta a la que tiene acceso un usuario. La configuración de la vista basada en carpetas suele establecerse en un objeto de configuración de usuario que está asociado a la carpeta. Pero, a veces, es posible que desee que la configuración sea global para la aplicación. En este caso, puede almacenar la configuración en la carpeta raíz del mensaje. 
  
La mayoría de los usuarios no saben y normalmente no tienen acceso a la carpeta raíz del buzón de correo. Esta carpeta se identifica mediante el valor [WellKnownFolderName. root](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) en la API administrada de EWS. En términos de MAPI, este es el equivalente del subárbol no IPM de un buzón de correo. La información a la que los usuarios finales no tienen acceso directo se almacena en la carpeta raíz del buzón de correo. Es posible que desee almacenar la configuración de la aplicación en esta carpeta porque las aplicaciones cliente no suelen tener acceso a ella. 
  
## <a name="version-differences"></a>Diferencias de versión
<a name="VersionDifferences"> </a>

Los objetos de configuración de usuario están disponibles en Exchange Online, Exchange online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2010.
  
## <a name="see-also"></a>Vea también


- [Administración de la configuración de aplicaciones persistentes mediante EWS en Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    
- [Propiedades y propiedades extendidas de EWS en Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Trabajar con carpetas mediante EWS en Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Trabajar con elementos de buzón de Exchange mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    


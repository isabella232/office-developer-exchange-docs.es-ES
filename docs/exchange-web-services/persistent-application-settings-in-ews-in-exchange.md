---
title: Configuración de aplicación persistente en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: Obtenga información sobre las diferentes opciones que la API administrada ews o la aplicación EWS pueden usar para crear la configuración de la aplicación personalizada persistente en Exchange.
ms.openlocfilehash: 3fdc7ad3d5acabf6b498743afe8d93f0eff048c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516143"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>Configuración de aplicación persistente en EWS en Exchange

Obtenga información sobre las diferentes opciones que la API administrada ews o la aplicación EWS pueden usar para crear la configuración de la aplicación personalizada persistente en Exchange.
  

  
La forma más sencilla de mantener sincronizadas las configuraciones de cliente personalizadas para un buzón de correo, o las carpetas y los elementos de un buzón, es almacenar la configuración de la aplicación en un Exchange servidor. Puede asegurarse de que esa configuración persiste para un buzón mediante uno de los siguientes procedimientos: 
  
- Objetos de configuración de usuario
    
- Propiedades extendidas
    
- Elementos personalizados
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>¿Cuáles son mis opciones para crear la configuración de la aplicación persistente?
<a name="Options"> </a>

Los objetos de configuración de usuario son la mejor opción para almacenar las opciones de configuración de las aplicaciones cliente de EWS. También puede usar propiedades de extensión o elementos personalizados, o una combinación de los tres. Elija la opción según el ámbito de la configuración y si la configuración debe estar disponible para otras aplicaciones.
  
**Tabla 1. Opciones recomendadas para crear opciones de aplicación persistentes basadas en el ámbito**

|**Establecer ámbito**|**Use…**|**A la que se accede por**|
|:-----|:-----|:-----|
|Item  <br/> |Una propiedad extendida en un elemento existente.  <br/> |Cualquier aplicación EWS. Solo los clientes EWS que conocen el identificador de la propiedad pueden tener acceso a una propiedad extendida.  <br/> |
|Folder  <br/> |Un objeto de configuración de usuario en la carpeta de destino. Esta es una buena forma de guardar la configuración de vista de una carpeta.  <br/> |Cualquier aplicación EWS.  <br/> |
|Buzón de correo  <br/> |Un objeto de configuración de usuario en la carpeta msgrootfolder predeterminada.  <br/> |Cualquier aplicación EWS.  <br/> |
   
### <a name="user-configuration-objects"></a>Objetos de configuración de usuario
<a name="UserConfig"> </a>

Los objetos de configuración de usuario son elementos especiales asociados con carpetas de un buzón. Los objetos de configuración de usuario, también conocidos como elementos asociados a carpetas, suelen ser la mejor opción para conservar la configuración de la aplicación, especialmente si la información de configuración está asociada a una carpeta o un buzón. Por lo general, no se hacen llegar a los usuarios finales. Dado que pueden almacenar de forma nativa secuencias de datos y diccionarios de datos, son ideales para almacenar información de configuración. La mejor manera de usar objetos de configuración de usuario es almacenar un conjunto de configuraciones en un documento XML y, a continuación, guardar esa información en una de las propiedades de secuencia de configuración de usuario.
  
Se tiene acceso a los objetos de configuración de usuario de forma diferente a los demás tipos de elementos almacenados en un buzón. Puede usar el método de API administrada EWS [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) o la operación EWS  [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar todos los elementos, pero debe usar la opción Recorrido de búsqueda asociado para buscar objetos de configuración de usuario. El **recorrido** de búsqueda asociado indica que los resultados de la búsqueda deben contener solo objetos de configuración de usuario. EWS incluye un conjunto de operaciones específicas de los objetos de configuración de usuario. 
  
**Tabla 1. Operaciones ews y métodos de API administrada ews para trabajar con objetos de configuración de usuario**

|**Para**|**Usar esta operación EWS**|**Usar este método de API administrada ews**|
|:-----|:-----|:-----|
|Crear un objeto de configuración de usuario  <br/> |[Operación CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|Obtener un objeto de configuración de usuario  <br/> |[Operación GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|Actualizar un objeto de configuración de usuario  <br/> |[Operación UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|Eliminar un objeto de configuración de usuario  <br/> |[Operación DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> Los objetos de configuración de usuario creados mediante EWS tienen un [prefijo ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) que comienza por "IPM. Configuración.". ItemClass **de** un objeto de configuración de usuario es el prefijo del objeto de configuración de usuario y el nombre del objeto de configuración de usuario. Puede usar la propiedad de LA API administrada ews [Item.ItemClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) o el **elemento EWS ItemClass** para buscar objetos de configuración de usuario que haya definido. 
  
### <a name="extended-properties"></a>Propiedades extendidas
<a name="ExtendedProperties"> </a>

Usa [propiedades extendidas](properties-and-extended-properties-in-ews-in-exchange.md) si quieres almacenar información de configuración en los elementos. EWS, a diferencia de MAPI, no devuelve un paquete de propiedades para los elementos. Esto significa que un cliente EWS debe conocer el identificador de propiedad extendida para buscar y obtener acceso a la propiedad extendida. Si necesita almacenar información de configuración en elementos que no sean objetos de configuración de usuario, el uso de propiedades extendidas para crear propiedades personalizadas puede ser la solución adecuada. Las propiedades extendidas permiten obtener acceso y almacenar información sobre propiedades que no forman parte del conjunto de propiedades estándar de un elemento. 
  
> [!IMPORTANT]
> El Exchange de base de datos tiene un número finito de propiedades. El número máximo de identificadores de propiedad para una Exchange base de datos es 32.767. Si usa propiedades extendidas para almacenar muchas opciones de configuración, le recomendamos que use una sola propiedad extendida para almacenar dicha configuración de modo que no supere este máximo. 
  
Puede usar el método de LA API administrada de EWS [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) o la operación [EWS UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para establecer propiedades extendidas en objetos de configuración de usuario. 
  
### <a name="custom-items"></a>Elementos personalizados
<a name="CustomItems"> </a>

Los elementos personalizados también se pueden usar para almacenar información. Las propiedades de elemento existentes se pueden reutilizar para contener información de configuración. O bien, puede usar propiedades extendidas para definir sus propias propiedades para la aplicación. El uso de elementos personalizados para almacenar la configuración proporciona las siguientes ventajas: 
  
- Funcionan para todas las versiones de Exchange que admiten EWS.
    
- Si no usa propiedades extendidas en el elemento, no se cobrará el presupuesto de Exchange propiedades.
    
## <a name="where-should-i-store-my-application-settings"></a>¿Dónde debo almacenar la configuración de la aplicación?
<a name="ApplicationSettingsLocation"> </a>

Las carpetas de buzones de correo y los elementos dentro de ellos se encuentran en la carpeta de mensajes raíz. Esta carpeta se identifica mediante el valor [WellKnownFolderName.msgfolderroot](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) en la API administrada ews. En términos mapi, esto es el equivalente del subárbol IPM de un buzón. Los objetos de configuración de usuario suelen usarse para crear configuraciones basadas en la interfaz de usuario, de modo que una aplicación pueda representar la configuración de vista en función de la carpeta a la que tiene acceso un usuario. La configuración de vista basada en carpetas suele establecerse en un objeto de configuración de usuario asociado a la carpeta. Pero a veces, es posible que quieras convertir la configuración global en la aplicación. En este caso, puede almacenar la configuración en la carpeta de mensajes raíz. 
  
La mayoría de los usuarios no conocen y normalmente no tienen acceso a la carpeta del buzón raíz. Esta carpeta se identifica mediante el [valor WellKnownFolderName.root](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) en la API administrada ews. En términos mapi, esto es el equivalente del subárbol que no es IPM de un buzón. La información a la que los usuarios finales no tienen acceso directamente se almacena en la carpeta del buzón raíz. Es posible que desee almacenar la configuración de la aplicación en esta carpeta porque las aplicaciones cliente normalmente no tienen acceso a ella. 
  
## <a name="version-differences"></a>Diferencias de versión
<a name="VersionDifferences"> </a>

Los objetos de configuración de usuario están disponibles en Exchange Online, Exchange Online como parte de Office 365 y versiones de Exchange a partir de Exchange 2010.
  
## <a name="see-also"></a>Ver también


- [Administrar la configuración de la aplicación persistente mediante EWS en Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    
- [Propiedades y propiedades extendidas de EWS en Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Trabajar con carpetas mediante EWS en Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Trabajar con Exchange buzón de correo mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    


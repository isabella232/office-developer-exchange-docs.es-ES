---
title: Configuración de aplicación persistente EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394d4e70-8517-4073-809a-5b61780ff923
description: Obtenga información sobre las diferentes opciones que puede usar la API administrada de EWS o la aplicación de EWS para crear una configuración de aplicación personalizada persistente en Exchange.
ms.openlocfilehash: b384fd5608dc647950d7cd31e861e24c12e3316f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763295"
---
# <a name="persistent-application-settings-in-ews-in-exchange"></a>Configuración de aplicación persistente EWS en Exchange

Obtenga información sobre las diferentes opciones que puede usar la API administrada de EWS o la aplicación de EWS para crear una configuración de aplicación personalizada persistente en Exchange.
  

  
Es la manera más fácil de mantener las configuraciones de cliente personalizado sincronizados para un buzón de correo, o carpetas y elementos en un buzón de correo almacenar la configuración de la aplicación en un servidor de Exchange. Asegúrese de que conservan esas opciones de configuración para un buzón de correo mediante el uso de uno de estos procedimientos: 
  
- Objetos de configuración de usuario
    
- Propiedades extendidas
    
- Elementos personalizados
    
## <a name="what-are-my-options-for-creating-persistent-application-settings"></a>¿Qué son las opciones para la creación de la configuración de la aplicación persistentes?
<a name="Options"> </a>

Objetos de configuración de usuario son la mejor opción para almacenar la configuración para las aplicaciones de cliente EWS. También puede utilizar extender propiedades o elementos personalizados o una combinación de las tres. Elija la opción en función del ámbito de la configuración y si debe estar disponibles para otras aplicaciones de la configuración.
  
**La tabla 1. Opciones recomendadas para la creación de configuración de aplicación persistente en función de ámbito**

|**Establecer el ámbito**|**Use…**|**Para obtener acceso a**|
|:-----|:-----|:-----|
|Elemento  <br/> |Una propiedad extendida en un elemento existente.  <br/> |Cualquier aplicación EWS. Sólo los clientes EWS que conocer el identificador de la propiedad pueden tener acceso a una propiedad extendida.  <br/> |
|Carpeta  <br/> |Un objeto de configuración de usuario en la carpeta de destino. Esto es una buena forma de guardar la configuración de la vista de una carpeta.  <br/> |Cualquier aplicación EWS.  <br/> |
|Buz?n de correo  <br/> |Un objeto de configuración de usuario en la carpeta msgrootfolder de forma predeterminada.  <br/> |Cualquier aplicación EWS.  <br/> |
   
### <a name="user-configuration-objects"></a>Objetos de configuración de usuario
<a name="UserConfig"> </a>

Objetos de configuración de usuario son elementos especiales que están asociados con las carpetas de un buzón de correo. Objetos de configuración de usuario, también conocido como elementos de una carpeta asociada, suelen ser la mejor opción para conservar la configuración de aplicación, especialmente si la información de configuración está asociada con una carpeta o un buzón de correo. Normalmente no se exponen a los usuarios finales. Debido a que forma nativa pueden almacenar las secuencias de datos y diccionarios de datos, que son ideales para almacenar información de configuración. Es la mejor manera de utilizar los objetos de configuración de usuario almacenar un conjunto de configuraciones en un documento XML y, a continuación, guardar la información en una de las propiedades de secuencia de configuración de usuario.
  
Se obtiene acceso a los objetos de configuración de usuario distinto de los otros tipos de elementos almacenados en un buzón de correo. Puede usar el método de la API administrada de EWS [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=EXCHG.80%29.aspx) o la operación de EWS [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) para buscar todos los elementos, pero debe usar la opción de recorrido de búsqueda **asociado** para buscar objetos de configuración de usuario. El recorrido de búsqueda **asociada** indica que los resultados de búsqueda deben contener sólo los objetos de configuración de usuario. EWS incluye un conjunto de operaciones que son específicos de objetos de configuración de usuario. 
  
**La tabla 1. Las operaciones de EWS y métodos de la API administrada de EWS para trabajar con objetos de configuración de usuario**

|**Con el fin...**|**Use esta operación de EWS**|**Use este método de la API administrada de EWS**|
|:-----|:-----|:-----|
|Crear un objeto de configuración de usuario  <br/> |[Operación CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) <br/> |[UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) <br/> |
|Obtener un objeto de configuración de usuario  <br/> |[Operación GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) <br/> |[UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> [UserConfiguration.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.load%28v=exchg.80%29.aspx) <br/> |
|Actualizar un objeto de configuración de usuario  <br/> |[Operación UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) <br/> |[UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) <br/> |
|Eliminar un objeto de configuración de usuario  <br/> |[Operación DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |
   
> [!NOTE]
> Objetos de configuración de usuario creados mediante el uso de EWS tienen un prefijo de [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) que comienza por "IPM. Configuración. ". El **ItemClass** de un objeto de configuración de usuario es el prefijo de objeto de configuración de usuario y el nombre de objeto de configuración de usuario. Puede usar la propiedad de la API administrada de EWS [Item.ItemClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) o el elemento **ItemClass** EWS para buscar objetos de configuración de usuario que ha definido. 
  
### <a name="extended-properties"></a>Propiedades extendidas
<a name="ExtendedProperties"> </a>

Usar [Propiedades extendidas](properties-and-extended-properties-in-ews-in-exchange.md) si desea almacenar la información de configuración en los elementos. Dirección URL de EWS, a diferencia de MAPI, no devuelve un contenedor de propiedades para los elementos. Esto significa que un cliente de EWS debe conocer el identificador de la propiedad extendida con el fin de buscar y obtener acceso a la propiedad extendida. Si necesita almacenar información de configuración en los elementos que no sean objetos de configuración de usuario, el uso de las propiedades extendidas para crear propiedades personalizadas puede ser la solución para usted. Las propiedades extendidas permiten obtener acceso y almacenar información sobre las propiedades que no forman parte de la propiedad standard establecido para un elemento. 
  
> [!IMPORTANT]
> El esquema de base de datos de Exchange tiene un número limitado de propiedades. El número máximo de identificadores de las propiedades de una base de datos de Exchange es 32.767. Si está utilizando las propiedades extendidas para almacenar muchos valores de configuración, es recomendable que usar una sola propiedad extendida para almacenar esa configuración para que no supere este máximo. 
  
Puede usar el método de la API administrada de EWS [Item.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=EXCHG.80%29.aspx) o la operación de EWS [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) para establecer las propiedades extendidas en objetos de configuración de usuario. 
  
### <a name="custom-items"></a>Elementos personalizados
<a name="CustomItems"> </a>

Los elementos personalizados también pueden utilizarse para almacenar información. Las propiedades de elemento existentes pueden utilizarse para incluir información de configuración. O bien, puede usar las propiedades extendidas para definir sus propias propiedades para la aplicación. Uso de elementos personalizados para almacenar la configuración ofrece las siguientes ventajas: 
  
- Funcionan para todas las versiones de Exchange que admiten EWS.
    
- Si no utiliza las propiedades extendidas en el elemento, no se carga el presupuesto de las propiedades de Exchange.
    
## <a name="where-should-i-store-my-application-settings"></a>¿Dónde debería almacenar la configuración de mi aplicación?
<a name="ApplicationSettingsLocation"> </a>

Las carpetas de buzón de correo y los elementos dentro de ellos se encuentran en la carpeta raíz del mensaje. Esta carpeta se identifica mediante el valor de [WellKnownFolderName.msgfolderroot](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) en la API administrada de EWS. En términos MAPI, esto es el equivalente del subárbol IPM de un buzón de correo. Objetos de configuración de usuario a menudo se usan para crear opciones basadas en la interfaz de usuario, por lo que una aplicación puede representar la configuración de la vista en función de la carpeta que tiene acceso un usuario. Configuración de la vista de carpeta-based normalmente se establece en un objeto de configuración de usuario que está asociado a la carpeta. Pero, en ocasiones, es posible que desee realizar la configuración global para la aplicación. En este caso, puede almacenar la configuración en la carpeta raíz del mensaje. 
  
La mayoría de los usuarios no son conscientes de y normalmente no tengan acceso a la carpeta raíz del buzón de correo. Esta carpeta se identifica mediante el valor de [WellKnownFolderName.root](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) en la API administrada de EWS. En términos MAPI, esto es el equivalente del subárbol no IPM de un buzón de correo. Información que no tengan acceso directamente los usuarios finales se almacena en la carpeta raíz del buzón de correo. Es posible que desee almacenar la configuración de la aplicación en esta carpeta debido a que las aplicaciones cliente no suelen tener acceso a él. 
  
## <a name="version-differences"></a>Diferencias de versión
<a name="VersionDifferences"> </a>

Objetos de configuración de usuario están disponibles en Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2010.
  
## <a name="see-also"></a>Vea también


- [Administrar la configuración de aplicación persistente mediante el uso de EWS en Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    
- [Propiedades y propiedades extendidas de EWS en Exchange](properties-and-extended-properties-in-ews-in-exchange.md)
    
- [Trabajar con carpetas mediante EWS en Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Trabajar con los elementos del buzón de Exchange mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    


---
title: Acceso delegado y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 240d1776-7adc-46cd-9099-88ffeba0a8aa
description: Descubra cómo usar la API administrada de EWS y EWS en Exchange para proporcionar acceso de delegado a buzones de los usuarios.
ms.openlocfilehash: 344255d86a51e13b21f1eda5113d292395d7cb8f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354053"
---
# <a name="delegate-access-and-ews-in-exchange"></a>Acceso delegado y EWS en Exchange

Descubra cómo usar la API administrada de EWS y EWS en Exchange para proporcionar acceso de delegado a buzones de los usuarios.
  
Puede habilitar a los usuarios tener acceso a los buzones de otros usuarios en uno de tres maneras: 
  
- Adición de delegados y especificando los permisos para cada delegado.
    
- Mediante la modificación de permisos de carpeta directamente.
    
- Mediante el uso de suplantación.
    
Permisos de delegación y carpeta están mejor cuando solo va a conceder acceso a unos pocos usuarios, debido a que se debe agregar permisos individualmente a cada buzón de correo. Suplantación de es la mejor opción cuando usted está tratando con cantidades de buzones de correo, debido a que se puede habilitar fácilmente una cuenta de servicio tener acceso a todos los buzones de una base de datos. La figura 1 muestra algunas de las diferencias entre cada tipo de acceso.
  
**En la figura 1. Formas de acceso a los buzones de otros usuarios**

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
Cuando se trata de enviar correo o programar reuniones, los delegados se le pueden asignar permisos "enviar en nombre de", por lo que el destinatario de un correo electrónico o una convocatoria de reunión que se ha enviado por un delegado verá " *delegar* en nombre *del propietario del buzón* " cuando se cob d inv fin e la convocatoria de reunión o de correo electrónico en Outlook. Incluido el texto "enviar en nombre de" es un detalle de implementación de cliente - y se pueden crear mediante el uso de "de" y "sender" valores. El valor "desde" indica el propietario del buzón y el valor de "sender" indica al delegado que envía el correo. Si una cuenta de servicio de suplantación de un usuario envía un correo electrónico o programa una reunión para el propietario del buzón de correo, el mensaje se "envía como" propietario del buzón. No hay ninguna forma para el destinatario que debe conocer que el correo se ha enviado por la cuenta de servicio. Los usuarios que se conceden permisos de carpetas y acceso de delegado no no son capaces de "Enviar como" o "enviar en nombre de" de un propietario del buzón. Cuando tengan acceso a las carpetas de buzón de correo y es posible que pueda crear elementos en las carpetas, pero no pueden enviar los elementos. 
  
¿Cuándo es apropiado modificar los permisos de carpeta directamente? Por lo general, cuando se desea proporcionar un acceso de usuario a una carpeta, pero no desea conceder al usuario permisos "enviar en nombre de", cuando los requisitos de permisos no se asignan a los valores de enumeración de la API administrada de EWS de [DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) o la [PermissionLevel](http://msdn.microsoft.com/library/87978600-3523-451e-a725-ef092c543e2a%28Office.15%29.aspx) Los valores del elemento EWS, o cuando desee proporcionar un acceso de usuario a una sola carpeta personalizada. 
  
Si sólo necesita modificar los permisos de carpeta para lograr su objetivo y no es necesario agregar un delegado (es decir, no necesita permisos "enviar en nombre de"), vea [establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md). 
  
Tenga en cuenta que también puede usar [Outlook](http://office.microsoft.com/en-us/outlook-help/allow-someone-else-to-manage-your-mail-and-calendar-HA102749417.aspx) o el [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) para configurar el acceso de delegado. 
  
## <a name="how-does-delegate-access-work"></a>¿Cómo delegar el trabajo de acceso?

Acceso delegado permite a los usuarios tener acceso a algunas o todas las carpetas del propietario del buzón y actuar en nombre del propietario del buzón de correo. El propietario del buzón puede ser un usuario o un recurso, como una sala de conferencias. Por ejemplo, un recepcionista puede tener permisos de delegado a la carpeta del calendario de una sala de conferencias, para administrar las solicitudes de reserva. Puede usar la API administrada de EWS o EWS para habilitar el propietario del buzón o un administrador agregar un delegado, para especificar qué carpetas, el delegado puede tener acceso y, a continuación, especifique los permisos para esa carpeta. Los delegados se pueden conceder acceso a las siguientes carpetas: 
  
- Calendario
    
- Tareas
    
- Bandeja de entrada
    
- Contactos
    
- Notas
    
- Journal
    
Cuando un usuario tiene acceso de delegado a una o varias de estas carpetas, puede crear, obtener, actualizar, eliminar, copiar y búsqueda para los elementos de esa carpeta y todas las carpetas secundarias, dependiendo de los [permisos](#bk_delegateperms) establecidos en la carpeta. La forma en que la aplicación realiza estas acciones depende de si se requiere acceso [explícita](#bk_explicit) o [implícita](#bk_implicit) . 
  
## <a name="delegate-permissions"></a>Permisos de delegado
<a name="bk_delegateperms"> </a>

Cuando un administrador o propietario del buzón agrega un delegado a un buzón de correo, también puede establecer el nivel de permisos para una o varias carpetas. Si no se establece un nivel de permisos para una carpeta, el valor de permiso predeterminado en ninguno. Varios usuarios pueden tener el mismo nivel de permisos en una carpeta y los usuarios pueden tener diferentes niveles de permisos para carpetas diferentes. Si se usa la API administrada de EWS, utilice la propiedad [DelegateUser.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser.permissions%28v=exchg.80%29.aspx) , que contiene uno de los valores de enumeración de [DelegateFolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) para cada carpeta, para establecer los permisos de delegación en las carpetas. Si está usando EWS, use el elemento [DelegatePermissions](http://msdn.microsoft.com/library/292badc7-bab3-4368-9d7c-9a8b7edb279b%28Office.15%29.aspx) para establecer permisos de delegado y el elemento [PermissionLevel](http://msdn.microsoft.com/library/87978600-3523-451e-a725-ef092c543e2a%28Office.15%29.aspx) para definir el nivel de permisos. 
  
**Tabla 2. Niveles de permisos de delegado**

|**Nivel de permisos**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Esto es el valor predeterminado para todas las carpetas.  <br/> |
|Autor  <br/> |Un delegado puede leer y crear elementos y modificar y eliminar los elementos que se crean. Por ejemplo, un delegado puede crear solicitudes de tareas y convocatorias de reunión directamente en la carpeta de tareas o el calendario del propietario del buzón y, a continuación, enviar un elemento en el nombre del propietario del buzón.  <br/> |
|Editor  <br/> |Un delegado puede hacer todo lo que un autor puede hacer y también modificar y eliminar los elementos creado por el propietario del buzón.  <br/> |
|Reviewer  <br/> |Un delegado puede leer elementos. Por ejemplo, un delegado con el permiso de revisor puede leer los mensajes en la Bandeja de entrada de la otra persona.  <br/> |
|Personalizado  <br/> |El propietario del buzón le haya asignado un conjunto de permisos personalizados para el delegado.  <br/> |
   
La propiedad de la API administrada de EWS [DelgateUser.ViewPrivateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.delegateuser.viewprivateitems%28v=exchg.80%29.aspx) y el elemento EWS [ViewPrivateItems](http://msdn.microsoft.com/library/80b949ac-440c-4a01-b428-ebafb5b1b802%28Office.15%29.aspx) es una configuración global que afecta a las carpetas de todos los buzones de correo del propietario, incluidos todos los correo, contactos, calendario, tareas, notas y carpetas de diario. No se puede permitir el acceso a los elementos privados sólo en una carpeta. 
  
## <a name="explicit-access"></a>Acceso explícito
<a name="bk_explicit"> </a>

Acceso explícito, simplemente put es la manera de entrada para los delegados para llevar a cabo acciones en las carpetas o elementos de un propietario de buzón de correo. Se concede acceso explícito a un delegado cuando incluye el nombre de la carpeta conocida de carpeta del propietario del buzón junto con la dirección de SMTP del propietario del buzón en una solicitud al servidor. El acceso es explícito debido a que la solicitud del delegado explícitamente indica que el contexto para el método o la operación es buzón el buzón del propietario del y no el buzón del delegado.
  
Acceso explícito define el contexto para todos los métodos ni las operaciones realizadas en las carpetas o elementos en el futuro. Todos los identificadores de elemento y carpeta devueltos cuando se establece el acceso explícito de forma exclusiva se identifiquen como pertenecientes al propietario del buzón (aunque no en cualquier formato legible). De este modo, no necesita la aplicación especificar la dirección de SMTP del propietario del buzón y otra vez; el contexto está oculto en los identificadores. Después de identifica un elemento o carpeta, un delegado utiliza realmente [acceso implícito](#bk_implicit) para modificar el elemento. En la siguiente figura se muestra el proceso de obtener acceso implícito y explícito. 
  
**La figura 2. Solicitar acceso implícito y explícito a una carpeta o elemento**

![Un diagrama que muestra la aplicación enviando una solicitud para el acceso explícito, una respuesta del servidor, una solicitud para el acceso implícito y una respuesta del servidor.](media/Ex15_Delegate_ExplictImplicit.png)
  
Puede establecer acceso explícito en muchos escenarios diferentes. Básicamente, cada vez que se va a enviar un identificador de la carpeta en un método o una operación, puede establecer acceso explícito. Esto puede incluir buscar carpetas, buscar citas, obtener elementos, buscar conversaciones y así sucesivamente.
  
### <a name="explicit-access-and-the-ews-managed-api"></a>Acceso explícito y la API administrada de EWS
<a name="bk_explicitewsma"> </a>

Puede iniciar el acceso delegado explícitas mediante cualquiera de los siguientes métodos sobrecargados que toman un parámetro de entrada [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) para identificar la carpeta de destino: 
  
- [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- Y mucho más.
    
Puede usar el parámetro **FolderId** en cada uno de estos métodos para identificar la carpeta de destino del propietario del buzón, como se indica a continuación. 
  
```cs
new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com");
```

Por ejemplo, para enlazar a la carpeta del calendario, el **FolderId** en este método **enlazar** especifica el nombre de la carpeta conocida y la dirección de SMTP del propietario del buzón. 
  
```cs
CalendarFolder calendar = CalendarFolder.Bind(service, new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com"), new PropertySet());
```

Mediante la especificación de nombre de la carpeta conocida y la dirección SMTP, puede enlazar el delegado a la carpeta del calendario del propietario del buzón, convirtiéndose en acceso explícito a la carpeta. Todas las solicitudes posteriores para el [acceso implícito](#bk_implicit) a elementos de la carpeta, a continuación, se basan en el contexto que se devuelven en el elemento de identificadores e identificadores de carpeta. Básicamente, los identificadores contienen el contexto de las llamadas de acceso de delegado implícita. O bien, para recuperar el identificador de elemento de un elemento que cumpla los criterios específicos, utilice la siguiente. 
  
```cs
FindItemsResults<Item> results = service.FindItems(new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com"), filter, view);
```

En este caso se devuelve el identificador de elemento y, a continuación, el delegado, a continuación, puede usar acceso implícito para realizar cambios en el elemento utilizando el identificador del elemento.
  
No es necesario iniciar de nuevo acceso explícito hasta que requieren un identificador de elemento o un identificador de carpeta que no tienen acceso a mediante el acceso explícito existente. 
  
### <a name="explicit-access-and-ews"></a>Acceso explícito y EWS
<a name="bk_explicitewsma"> </a>

Puede iniciar el acceso explícito mediante el uso de las operaciones [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx), [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)o [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) . Estas operaciones proporcionan la opción para usar el elemento [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) para identificar la carpeta de destino. El elemento **DistinguishedFolderId** tiene un elemento secundario opcional, el elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) . El elemento de **buzón de correo** , cuando se usa como un elemento secundario del elemento **DistinguishedFolderId** , especifica el buzón de correo para el delegado para obtener acceso a. Si el usuario que realiza la llamada tiene permiso para tener acceso a la carpeta del propietario del buzón de correo, la respuesta contendrá una colección de identificadores de los elementos o las carpetas de ese buzón. Los identificadores de elemento y carpeta que se devuelven en la respuesta se pueden usar para el acceso de delegado implícitas. 
  
## <a name="implicit-access"></a>Acceso implícito
<a name="bk_implicit"> </a>

Acceso implícito se usa después de un delegado ha recuperado el identificador para un elemento o carpeta en buzón el buzón del propietario del y el delegado que desea actualizar, eliminar o copiar el elemento. Cuando el delegado usa ese identificador de elemento o carpeta en una solicitud, se realizan los cambios en el elemento en buzón el buzón del propietario del. El delegado no tiene que incluir la dirección de SMTP del propietario del buzón. 
  
Por ejemplo, cuando un delegado tiene el identificador de una de las carpetas del propietario del buzón, el delegado puede realizar una operación **FindItem** en esa carpeta con el identificador de la carpeta, sin identificar explícitamente buzón el buzón del propietario del. En ese momento, el delegado puede realizar acciones en la carpeta del propietario del buzón de correo mediante el uso de los identificadores que se devuelven en las respuestas. 
  
### <a name="implicit-access-and-the-ews-managed-api"></a>Acceso implícito y la API administrada de EWS

Si un identificador de elemento se ha recuperado por el método [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , se puede usar ese identificador de elemento en una llamada al método [Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) posterior a la que para enlazar el elemento. A continuación, puede llamar al método [Item.Update](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx), [Item.Delete](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)o [Item.Copy](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) , o cualquier llamada al método que requiere un identificador de elemento, según sea necesario para completar la tarea. Siempre y cuando el delegado tiene los permisos adecuados a la carpeta que contiene el elemento (y, si procede, la carpeta el elemento se traslada al), el delegado puede realizar cambios según sus niveles de permisos. 
  
### <a name="implicit-access-and-ews"></a>Acceso implícito y EWS

Si el identificador de un elemento se ha recuperado por la operación [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , ese identificador de elemento puede utilizarse en las siguientes operaciones [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para enlazar al elemento. A continuación, puede llamar a la operación [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx), [DeleteItem](../web-service-reference/deleteitem-operation.md)o [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) — o cualquier operación que requiera un identificador de elemento, según sea necesario para completar la tarea. Siempre y cuando el delegado tiene los permisos adecuados a la carpeta que contiene el elemento (y, si procede, la carpeta el elemento se traslada al), el delegado puede realizar cambios según sus niveles de permisos. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_implicit"> </a>

- [Agregar y quitar delegados mediante EWS en Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
    
- [Obtener acceso a un calendario como delegado mediante el uso de EWS en Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Contactos de acceso como delegado mediante el uso de EWS en Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Correo electrónico de acceso como delegado mediante el uso de EWS en Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Establecer permisos de carpeta de otro usuario mediante el uso de EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la delegación en EWS en Exchange](handling-delegation-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Permitir que otra persona administre su correo y calendario](http://office.microsoft.com/en-us/outlook-help/allow-someone-else-to-manage-your-mail-and-calendar-HA102749417.aspx)
    
- [Agregar permiso de buzón](http://technet.microsoft.com/en-us/library/bb124097%28v=exchg.150%29.aspx)
    


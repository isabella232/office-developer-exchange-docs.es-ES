---
title: Acceso delegado y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 240d1776-7adc-46cd-9099-88ffeba0a8aa
description: Descubra cómo usar la API administrada de EWS y EWS en Exchange para proporcionar acceso de delegado a los buzones de los usuarios.
localization_priority: Priority
ms.openlocfilehash: 4223d625213a3f71726ec5b8d3f09f9e2e7e7e51
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528457"
---
# <a name="delegate-access-and-ews-in-exchange"></a>Acceso delegado y EWS en Exchange

Descubra cómo usar la API administrada de EWS y EWS en Exchange para proporcionar acceso de delegado a los buzones de los usuarios.
  
Puede habilitar a los usuarios para que tengan acceso a los buzones de otros usuarios de una de estas tres maneras: 
  
- Mediante la adición de delegados y la especificación de permisos para cada delegado.
    
- Modificando los permisos de carpeta directamente.
    
- Mediante la suplantación.
    
La delegación y los permisos de carpeta son los mejores cuando solo concede acceso a algunos usuarios, porque tiene que agregar permisos individualmente a cada buzón. La suplantación es la mejor opción cuando se trabaja con cantidades de buzones de correo, ya que es posible habilitar fácilmente una cuenta de servicio para el acceso a todos los buzones de una base de datos. La figura 1 muestra algunas de las diferencias entre cada tipo de acceso.
  
**Figura 1. Formas de tener acceso a los buzones de otros usuarios**

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
Cuando se trata de enviar reuniones de correo o de programación, se puede proporcionar a los delegados los permisos "enviar en nombre de", por lo que el destinatario de un correo electrónico o una convocatoria de reunión enviada por un delegado verá " *delegar* en nombre de *buzón propietario* " cuando reciban el correo electrónico o la solicitud de reunión en Outlook. Incluir el texto "enviar en nombre de" es un detalle de la implementación del cliente y se puede crear mediante los valores "desde" y "remitente". El valor "de" indica el propietario del buzón y el valor "Sender" indica el delegado que envió el correo. Si una cuenta de servicio que suplanta a un usuario envía un correo electrónico o programa una reunión para el propietario del buzón, el mensaje se "envía como" el propietario del buzón. No hay forma de que el destinatario sepa que el correo se envió mediante la cuenta de servicio. Los usuarios a los que se conceden permisos de carpeta y no acceso delegado no pueden "enviar como" ni "enviar en nombre de" de un propietario de buzón. Tienen acceso a las carpetas del buzón y pueden crear elementos en las carpetas, pero no pueden enviar los elementos. 
  
¿Cuándo es apropiado modificar los permisos de carpeta directamente? Por lo general, cuando desea proporcionar a un usuario acceso a una carpeta, pero no desea conceder al usuario los permisos "enviar en nombre de", cuando sus requisitos de permisos no se asignan a los valores de enumeración de la API administrada de EWS de [DelegateFolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) o a los valores de los elementos EWS [PermissionLevel](https://msdn.microsoft.com/library/87978600-3523-451e-a725-ef092c543e2a%28Office.15%29.aspx) o cuando desea proporcionar a un usuario acceso a una sola carpeta personalizada. 
  
Si solo necesita modificar los permisos de carpeta para lograr su objetivo y no necesita agregar un delegado (es decir, no necesita "enviar en nombre de"), vea [establecer permisos de carpeta para otro usuario mediante EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md). 

Tenga en cuenta que también puede usar [Outlook](https://office.microsoft.com/outlook-help/allow-someone-else-to-manage-your-mail-and-calendar-HA102749417.aspx) o [Exchange Server PowerShell (Shell de administración de Exchange)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) para configurar el acceso delegado. 

  
## <a name="how-does-delegate-access-work"></a>¿Cómo funciona el acceso delegado?

Acceso delegado permite a los usuarios acceder a algunas o a todas las carpetas del propietario del buzón y actuar en nombre del propietario del buzón. El propietario del buzón puede ser un usuario o un recurso, como una sala de conferencias. Por ejemplo, un recepcionista puede tener permisos de delegado en la carpeta Calendario de una sala de conferencias para controlar las solicitudes de reserva. Puede usar la API administrada de EWS o EWS para habilitar al propietario del buzón o a un administrador para que agregue un delegado, especifique a qué carpetas puede tener acceso el delegado y, a continuación, especifique los permisos para esa carpeta. Se puede conceder acceso a los delegados a las siguientes carpetas: 
  
- Calendario
    
- Tareas
    
- Bandeja de entrada
    
- Contactos
    
- Notas
    
- Diario
    
Cuando un usuario tiene acceso delegado a una o varias de estas carpetas, puede crear, obtener, actualizar, eliminar, copiar y buscar elementos en esa carpeta y en cualquier carpeta secundaria, según los [permisos](#bk_delegateperms) establecidos en la carpeta. La forma en que la aplicación realiza estas acciones depende de si se requiere acceso [explícito](#bk_explicit) o [implícito](#bk_implicit) . 
  
## <a name="delegate-permissions"></a>Delegar permisos
<a name="bk_delegateperms"> </a>

Cuando un administrador o el propietario del buzón agrega un delegado a un buzón de correo, también puede establecer el nivel de permisos para una o más carpetas. Si no se establece un nivel de permisos para una carpeta, el valor de permiso predeterminado es None. Varios usuarios pueden tener el mismo nivel de permisos en una carpeta y los usuarios pueden tener distintos niveles de permisos para distintas carpetas. Si está usando la API administrada de EWS, use la propiedad [DelegateUser. Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegateuser.permissions%28v=exchg.80%29.aspx) , que contiene uno de los valores de enumeración [DelegateFolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegatefolderpermissionlevel%28v=exchg.80%29.aspx) para cada carpeta, para establecer permisos de delegado en las carpetas. Si está usando EWS, use el elemento [DelegatePermissions](https://msdn.microsoft.com/library/292badc7-bab3-4368-9d7c-9a8b7edb279b%28Office.15%29.aspx) para establecer permisos de delegado y el elemento [PermissionLevel](https://msdn.microsoft.com/library/87978600-3523-451e-a725-ef092c543e2a%28Office.15%29.aspx) para definir el nivel de permisos. 
  
**Tabla 2. Delegación de niveles de permisos**

|**Nivel de permisos**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Este es el valor predeterminado de todas las carpetas.  <br/> |
|Autor  <br/> |Un delegado puede leer y crear elementos, y modificar y eliminar los elementos que crean. Por ejemplo, un delegado puede crear solicitudes de tareas y convocatorias de reunión directamente en la carpeta de calendario o de tareas del propietario del buzón y, a continuación, enviar cualquier elemento en nombre del propietario del buzón.  <br/> |
|Editor  <br/> |Un delegado puede hacer todo lo que puede hacer un autor, además de modificar y eliminar los elementos creados por el propietario del buzón.  <br/> |
|Reviewer  <br/> |Un delegado puede leer elementos; por ejemplo, un delegado con el permiso de revisor puede leer los mensajes de la bandeja de entrada de otra persona.  <br/> |
|Personalizado  <br/> |El propietario del buzón ha concedido un conjunto personalizado de permisos para el delegado.  <br/> |
   
La propiedad de la API administrada de EWS [DelgateUser. ViewPrivateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.delegateuser.viewprivateitems%28v=exchg.80%29.aspx) y el elemento de EWS [ViewPrivateItems](https://msdn.microsoft.com/library/80b949ac-440c-4a01-b428-ebafb5b1b802%28Office.15%29.aspx) es una configuración global que afecta a todas las carpetas del propietario del buzón, incluidas todas las carpetas correo, contactos, calendario, tareas, notas y diario. No se puede permitir el acceso a elementos privados en una sola carpeta. 
  
## <a name="explicit-access"></a>Acceso explícito
<a name="bk_explicit"> </a>

En pocas palabras, el acceso explícito es la forma en que los delegados realizan acciones en los elementos o carpetas de un propietario del buzón. El acceso explícito se concede a un delegado cuando incluye el nombre de carpeta conocido para la carpeta de un propietario del buzón junto con la dirección SMTP del propietario del buzón de correo en una solicitud al servidor. El acceso es explícito porque la solicitud del delegado indica explícitamente que el contexto para el método o la operación es el buzón de correo del propietario del buzón y no el buzón de correo del delegado.
  
Acceso explícito define el contexto para todos los métodos u operaciones que se realizan en las carpetas o elementos que se mueven hacia delante. Todos los identificadores de elemento y carpeta que se devuelven cuando se establece el acceso explícito se identifican de manera única como pertenecientes al propietario del buzón (aunque no en ningún formato legible para el ojo humano). De este modo, la aplicación no tiene que especificar la dirección SMTP del propietario del buzón de nuevo y de nuevo; el contexto se oculta en los identificadores. Una vez identificado un elemento o carpeta, un delegado realmente usa el [acceso implícito](#bk_implicit) para modificar el elemento. La siguiente figura muestra el proceso de obtener acceso explícito e implícito. 
  
**Figura 2. Solicitar acceso explícito e implícito a un elemento o una carpeta**

![Un diagrama que muestra la aplicación enviando una solicitud para el acceso explícito, una respuesta del servidor, una solicitud para el acceso implícito y una respuesta del servidor.](media/Ex15_Delegate_ExplictImplicit.png)
  
Puede establecer el acceso explícito en muchos escenarios diferentes. Básicamente, cada vez que envía un identificador de carpeta en un método u operación, puede establecer el acceso explícito. Esto puede incluir buscar carpetas, buscar citas, obtener elementos, buscar conversaciones, etc.
  
### <a name="explicit-access-and-the-ews-managed-api"></a>Acceso explícito y API administrada de EWS
<a name="bk_explicitewsma"> </a>

Puede iniciar el acceso delegado explícito mediante cualquiera de los siguientes métodos sobrecargados que toman un parámetro de entrada [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) para identificar la carpeta de destino: 
  
- [Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)
    
- [ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [ExchangeService. FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx)
    
- [ExchangeService. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- Y mucho más.
    
Puede usar el parámetro **FolderId** en cada uno de estos métodos para identificar la carpeta de destino del propietario del buzón, como se indica a continuación. 
  
```cs
new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com");
```

Por ejemplo, para enlazar con la carpeta calendario, el **FolderId** en este método **BIND** especifica el nombre de carpeta conocido y la dirección SMTP del propietario del buzón. 
  
```cs
CalendarFolder calendar = CalendarFolder.Bind(service, new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com"), new PropertySet());
```

Al especificar el nombre de carpeta conocido y la dirección SMTP, el delegado puede enlazarse a la carpeta de calendario del propietario del buzón de correo, con lo que se obtiene acceso explícito a la carpeta. Todas las solicitudes posteriores para el [acceso implícito](#bk_implicit) a los elementos de la carpeta se basan en el contexto devuelto en los identificadores de elemento y los identificadores de carpeta. Básicamente, los identificadores contienen el contexto de las llamadas de acceso delegado implícitas. O bien, para recuperar el identificador de elemento de un elemento que cumpla los criterios especificados, use lo siguiente. 
  
```cs
FindItemsResults<Item> results = service.FindItems(new FolderId(WellKnownFolderName.Calendar, "primary@contoso.com"), filter, view);
```

En este caso, se devuelve el identificador de elemento y, a continuación, el delegado puede usar el acceso implícito para realizar cambios en el elemento mediante el identificador de elemento.
  
No es necesario iniciar de nuevo el acceso explícito hasta que se requiera un identificador de elemento o un identificador de carpeta al que no se haya tenido acceso a través del acceso explícito existente. 
  
### <a name="explicit-access-and-ews"></a>Acceso explícito y EWS
<a name="bk_explicitewsma"> </a>

Puede iniciar acceso explícito mediante las operaciones [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx), [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)o [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) . Estas operaciones proporcionan la opción de usar el elemento [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) para identificar la carpeta de destino. El elemento **DistinguishedFolderId** tiene un solo elemento secundario opcional, el elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) . El elemento **Mailbox** , cuando se usa como elemento secundario del elemento **DistinguishedFolderId** , especifica el buzón de correo al que tiene acceso el delegado. Si el usuario que llama tiene permiso para obtener acceso a la carpeta del propietario del buzón, la respuesta contendrá una colección de identificadores a los elementos o carpetas de ese buzón. Los identificadores de elemento y carpeta que se devuelven en la respuesta pueden usarse para el acceso de delegado implícito. 
  
## <a name="implicit-access"></a>Acceso implícito
<a name="bk_implicit"> </a>

El acceso implícito se usa después de que un delegado haya recuperado el identificador de un elemento o una carpeta en el buzón de correo del propietario del buzón y el delegado quiera actualizar, eliminar o copiar el elemento. Cuando el delegado usa ese identificador de elemento o carpeta en una solicitud, los cambios se realizan en el elemento en el buzón del propietario del buzón. El delegado no tiene que incluir la dirección SMTP del propietario del buzón. 
  
Por ejemplo, cuando un delegado tiene el identificador de una de las carpetas del propietario del buzón, el delegado puede realizar una operación **FindItem** en dicha carpeta mediante el identificador de la carpeta, sin identificar explícitamente el buzón del propietario del buzón. En ese momento, el delegado puede realizar acciones en la carpeta del propietario del buzón con los identificadores que se devuelven en las respuestas. 
  
### <a name="implicit-access-and-the-ews-managed-api"></a>Acceso implícito y la API administrada EWS

Si se ha recuperado un identificador de elemento mediante el método [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , dicho identificador de elemento se puede usar en una llamada al método [Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) subsiguiente para enlazar con el elemento. A continuación, puede llamar al método [Item. Update](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx), [Item. Delete](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)o [Item. Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) , o a cualquier llamada de método que requiera un identificador de elemento, según sea necesario para completar la tarea. Siempre que el delegado tenga los permisos adecuados para la carpeta que contiene el elemento (y, si procede, la carpeta a la que se va a mover el elemento), el delegado puede realizar cambios según sus niveles de permisos. 
  
### <a name="implicit-access-and-ews"></a>Acceso implícito y EWS

Si se ha recuperado un identificador de elemento mediante la operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , dicho identificador de elemento se puede usar en las siguientes operaciones [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) para enlazarse al elemento. A continuación, puede llamar a la operación [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx), [DeleteItem](../web-service-reference/deleteitem-operation.md)o [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) , o a cualquier operación que requiera un identificador de elemento, según sea necesario para completar la tarea. Siempre que el delegado tenga los permisos adecuados para la carpeta que contiene el elemento (y, si procede, la carpeta a la que se va a mover el elemento), el delegado puede realizar cambios según sus niveles de permisos. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_implicit"> </a>

- [Agregar y quitar delegados mediante EWS en Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
    
- [Obtener acceso a un calendario como delegado mediante EWS en Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Obtener acceso a los contactos como un delegado mediante EWS en Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Obtener acceso al correo electrónico como delegado mediante EWS en Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Establecer los permisos de carpeta para otro usuario mediante EWS en Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
    
- [Control de errores relacionados con la delegación en EWS en Exchange](handling-delegation-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)

- [Permitir que otra persona administre su correo y su calendario](https://office.microsoft.com/outlook-help/allow-someone-else-to-manage-your-mail-and-calendar-HA102749417.aspx)  

- [Add-MailboxPermission](https://technet.microsoft.com/library/bb124097%28v=exchg.150%29.aspx)
    
---
title: Complementos de Outlook y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 821c8eb9-bb58-42e8-9a3a-61ca635cba59
description: Obtenga información acerca de los complementos de Outlook y cómo funcionan con EWS en Exchange.
ms.openlocfilehash: 7eae834fe0bb93e2e94f094e811ab6cf002fc71b
ms.sourcegitcommit: 42eecc78e7aed7e95f73370d6c39ab8f4e96bf68
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/12/2018
ms.locfileid: "25541641"
---
# <a name="outlook-add-ins-and-ews-in-exchange"></a>Complementos de Outlook y EWS en Exchange

Obtenga información acerca de los complementos de Outlook y cómo funcionan con EWS en Exchange.

Complementos de Outlook proporcionan una interfaz única y un modelo de programación que usa los estándares de web para que pueda crear una experiencia personalizada para los usuarios de correo electrónico. Puede crear aplicaciones de correo que muestran información contextual o útil en un marco de HTML5 alojado en Outlook; Por ejemplo, una aplicación de correo puede mostrar un mapa de Bing con una dirección de resaltado cuando un mensaje de correo electrónico contiene una dirección. O bien, cuando un usuario redacta un mensaje, una aplicación de correo puede mostrar información adicional sobre el destinatario e insertar un saludo estándar en el correo electrónico con sólo pulsar un botón.

> [!NOTE]
> En este artículo, "Outlook" hace referencia al cliente enriquecido de Outlook, Outlook RT, Outlook Web App y OWA para dispositivos.

La interfaz de aplicaciones de correo es parte de la API de JavaScript para Office. Puede usar la API para tener acceso a información de Exchange para habilitar la aplicación de correo:

- [Reconocer entidades](http://msdn.microsoft.com/library/a6b0904b-afe9-4882-9136-3d8cfd57fcf8%28Office.15%29.aspx), como direcciones, números de teléfono, sugerencias de tarea o sugerencias de reunión en un correo electrónico.

- Abrir y mostrar existente de [mensajes](http://msdn.microsoft.com/library/d0bca550-70c3-457c-85f8-e19b39e3b892%28Office.15%29.aspx) y [citas](http://msdn.microsoft.com/library/6cfbc29d-8581-474e-9a8b-510471e4bf8b%28Office.15%29.aspx) en una vista independiente para que los usuarios pueden aplicar una referencia cruzada información en uno o más mensajes.

- [EWS realizar solicitudes](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx) al servidor de Exchange que hospeda el buzón del usuario. Una aplicación de correo por ejemplo, puede obtener una lista de carpetas para que el usuario puede elegir uno para almacenar el mensaje, o mostrar todos los elementos en una conversación o marcar un mensaje de correo electrónico como correo no deseado.

- [Obtener un token](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx) para identificar de forma única una cuenta de correo electrónico para habilitar un único inicio de sesión en un servicio de terceros.

- [Obtener un token](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx) que permite a un servicio de terceros para hacer solicitudes EWS en nombre del usuario, por ejemplo, para extraer los datos adjuntos de un elemento o para obtener un elemento desde el servidor de Exchange para continuar el procesamiento.

Puede usar las aplicaciones de correo para personalizar la experiencia de Outlook Web App para los usuarios; Si desea personalizar la "apariencia" de Outlook Web App, vea estos artículos de TechNet:

- [Crear un tema de Outlook Web App](http://technet.microsoft.com/en-us/library/bb201700%28v=exchg.150%29.aspx)

- [Personalizar la Outlook Web App inicio de sesión, selección de idioma y las páginas de error](http://technet.microsoft.com/en-us/library/ee633483%28v=exchg.150%29.aspx)

Su organización puede instalar las aplicaciones de correo en un servidor interno para limitar el acceso a los usuarios autorizados, u otros desarrolladores de aplicaciones de correo y se pueden colocar las aplicaciones de correo en la [Tienda de Office](http://office.microsoft.com/store/) para la venta al público en general. Cualquier persona que se está ejecutando Outlook puede descargar, instalar y usar aplicaciones de correo desde el catálogo de soluciones.

Si desea obtener más información sobre la creación de aplicaciones de correo, consulte la [documentación de complementos de Outlook](/outlook/add-ins) o en el ejemplo [para realizar una solicitud EWS](http://code.msdn.microsoft.com/exchange/Mail-apps-for-Outlook-Make-770b2528) .

## <a name="ews-and-outlook-add-ins"></a>Complementos EWS y Outlook

Puede usar un subconjunto de las operaciones de EWS en el servidor de Exchange que hospeda la cuenta que ejecuta una aplicación de correo.

La función [mailbox.makeEwsRequestAsync](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx) le permite realizar solicitudes EWS desde su aplicación de correo en el servidor que hospeda el buzón del usuario. Crear el elemento envelope de SOAP y solicitud XML y las llamadas de función **makeEwsRequestAsync** EWS con un token de autenticación que identifica el buzón de correo y la aplicación que realiza la solicitud de correo. Para ayudar a proteger el buzón del usuario, el servidor de Exchange rechazará las solicitudes que no se incluyen desde la aplicación de correo o desde un buzón que no esté hospedado en el servidor.

Al igual que cualquier otra aplicación, una aplicación de correo necesita permisos para trabajar. El administrador debe:

- [Acceso a EWS conceder](controlling-client-application-access-to-ews-in-exchange.md) al usuario de aplicaciones de correo.

- [Establecer "oauthauthentication" como true](http://technet.microsoft.com/en-us/library/aa997233%28v=exchg.150%29.aspx) en el directorio EWS del servidor de acceso de cliente.

También debe asegurarse de que la aplicación solicita el permiso de buzón de lectura y escritura en las aplicaciones para Office [modelo de permisos](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md).

Una vez completados estos pasos, están disponibles para la aplicación de correo para utilizar un subconjunto de operaciones de EWS de elemento y carpeta.

**La tabla 1. Pueden usar la carpeta y elemento de las operaciones de EWS que aplicaciones de correo**

|**Operaciones de carpeta**|**Operaciones de elemento**|
|:-----|:-----|
|[Operación CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [Operación FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [Operación GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [Operación UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |[Operación CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [Operación CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [Operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> [Operación FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> [Operación GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> [Operación GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [Operación MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) <br/> [Operación MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [Operación SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> [Operación UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |

### <a name="service-callback-tokens"></a>Tokens de devolución de llamada de servicio

Los tokens de devolución de llamada de servicio permiten a las aplicaciones de correo pasar un token de acceso a un servicio de terceros para que el servicio puede realizar solicitudes EWS en el servidor de Exchange que hospeda el buzón de correo. Por ejemplo, una aplicación de correo puede pasar un token de devolución de llamada de servicio a un servicio de terceros junto con una lista de identificadores de datos adjuntos de imágenes adjunto a un correo electrónico. A continuación, puede usar el servicio de los datos adjuntos de los identificadores y el token de devolución de llamada para realizar una solicitud EWS al servidor de Exchange del usuario para obtener las imágenes adjuntas. Las aplicaciones de correo también pueden usar el token de devolución de llamada de servicio con una lista de los identificadores de elementos para obtener los elementos de correo electrónico y cita desde el servidor de Exchange.

El token de devolución de llamada de servicio es un token de opaco que el servicio de terceros que se adjunta a la solicitud EWS en un encabezado de autenticación de portador. El token identifica la aplicación de correo y el buzón de correo para ayudar a proteger la solicitud EWS. Para obtener información sobre cómo usar tokens de devolución de llamada de servicio, vea la [los complementos de Outlook: obtener datos adjuntos de un servidor de Exchange](http://code.msdn.microsoft.com/exchange/Mail-apps-for-Office-Get-38babdc9) ejemplo.

## <a name="see-also"></a>Vea también


- [Controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md)

- [Método Mailbox.makeEwsRequestAsync (API de JavaScript para Office)](http://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)

- [Complementos de Outlook](https://docs.microsoft.com/outlook/add-ins)

- [Método Mailbox.getUserIdentityTokenAsync (API de JavaScript para Office)](http://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)

- [Autenticar un complemento de Outlook con tokens de identidad de Exchange](http://msdn.microsoft.com/library/c0520a1e-d9ba-495a-a99f-6816d7d2a23e%28Office.15%29.aspx)

- [Uso del modelo de permisos para aplicaciones de correo en Outlook 2013 Preview](https://docs.microsoft.com/en-us/outlook/add-ins/understanding-outlook-add-in-permissions)

- [Set-WebServicesVirtualDirectory](http://technet.microsoft.com/en-us/library/aa997233%28v=exchg.150%29.aspx)

- [Complementos de Outlook: para realizar una solicitud EWS](http://code.msdn.microsoft.com/office/Mail-apps-for-Outlook-Make-770b2528)

- [Complementos de Outlook: usar un token de identidad de cliente](http://code.msdn.microsoft.com/Mail-apps-for-Outlook-Use-b20a66b6)

- [Complementos de Outlook: obtener datos adjuntos de un servidor de Exchange](http://code.msdn.microsoft.com/office/Mail-apps-for-Office-Get-38babdc9)

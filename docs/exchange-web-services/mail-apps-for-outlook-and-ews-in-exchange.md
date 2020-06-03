---
title: Complementos de Outlook y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 821c8eb9-bb58-42e8-9a3a-61ca635cba59
description: Encuentre información sobre los complementos de Outlook y cómo funcionan con EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 2b0cee2017c24d714fa444c094ab1797be1fbe99
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456279"
---
# <a name="outlook-add-ins-and-ews-in-exchange"></a>Complementos de Outlook y EWS en Exchange

Encuentre información sobre los complementos de Outlook y cómo funcionan con EWS en Exchange.

Los complementos de Outlook proporcionan una interfaz única y un modelo de programación que usa estándares web para permitirle crear una experiencia personalizada para los usuarios de correo electrónico. Puede crear aplicaciones de correo que muestren información contextual o útil en un marco de HTML5 hospedado en Outlook; por ejemplo, una aplicación de correo puede mostrar un mapa de Bing con una dirección resaltada cuando un mensaje de correo electrónico contiene una dirección. O bien, cuando un usuario redacta un mensaje, una aplicación de correo puede mostrar información adicional sobre el destinatario e insertar un saludo estándar en el correo electrónico con sólo pulsar un botón.

> [!NOTE]
> En este artículo, "Outlook" hace referencia al cliente enriquecido de Outlook, Outlook RT, Outlook Web App y OWA para dispositivos.

La interfaz de aplicaciones de correo forma parte de la API de JavaScript para Office. Puede usar la API para obtener acceso a la información de Exchange para habilitar su aplicación de correo para:

- [Reconocer entidades](https://msdn.microsoft.com/library/a6b0904b-afe9-4882-9136-3d8cfd57fcf8%28Office.15%29.aspx), como direcciones, números de teléfono, sugerencias de tareas o sugerencias de reunión en un correo electrónico.

- Abrir y mostrar [mensajes](https://msdn.microsoft.com/library/d0bca550-70c3-457c-85f8-e19b39e3b892%28Office.15%29.aspx) y [citas](https://msdn.microsoft.com/library/6cfbc29d-8581-474e-9a8b-510471e4bf8b%28Office.15%29.aspx) existentes en una vista independiente para que los usuarios puedan hacer referencias cruzadas de la información en uno o más mensajes.

- [Realizar solicitudes EWS](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx) al servidor Exchange que hospeda el buzón del usuario. Una aplicación de correo puede, por ejemplo, obtener una lista de carpetas para que el usuario pueda elegir una para almacenar el mensaje o Mostrar todos los elementos de una conversación, o marcar un mensaje de correo electrónico como correo no deseado.

- [Obtenga un token](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx) para identificar de forma única una cuenta de correo electrónico para habilitar el inicio de sesión único en un servicio de terceros.

- [Obtenga un token](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx) que habilita a un servicio de terceros para realizar solicitudes EWS en nombre del usuario, por ejemplo, para extraer los datos adjuntos de un elemento o para obtener un elemento del servidor Exchange para su procesamiento posterior.

Puede usar aplicaciones de correo para personalizar la experiencia de Outlook Web App para los usuarios; sin embargo, si desea personalizar la "apariencia" de Outlook Web App, consulte estos artículos en TechNet:

- [Crear un tema para Outlook Web App](https://technet.microsoft.com/library/bb201700%28v=exchg.150%29.aspx)

- [Personalización de las páginas de inicio de sesión, selección de idioma y error de Outlook Web App](https://technet.microsoft.com/library/ee633483%28v=exchg.150%29.aspx)

Su organización puede instalar aplicaciones de correo en un servidor interno para limitar el acceso a los usuarios autorizados, o usted y otros desarrolladores de aplicaciones de correo pueden poner aplicaciones de correo en la [tienda Office](https://office.microsoft.com/store/) para su venta al público en general. Cualquier usuario que ejecute Outlook puede descargar, instalar y usar aplicaciones de correo desde el catálogo de soluciones.

Si desea obtener más información sobre la creación de aplicaciones de correo, consulte la [documentación de complementos de Outlook](/outlook/add-ins) o el ejemplo [realizar una solicitud EWS](https://code.msdn.microsoft.com/exchange/Mail-apps-for-Outlook-Make-770b2528) .

## <a name="ews-and-outlook-add-ins"></a>EWS y complementos de Outlook

Puede usar un subconjunto de operaciones de EWS en el servidor de Exchange que hospeda la cuenta que ejecuta una aplicación de correo.

La función [Mailbox. makeEwsRequestAsync](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx) permite realizar solicitudes EWS desde la aplicación de correo de vuelta al servidor que hospeda el buzón del usuario. Cree el envoltorio SOAP y la solicitud XML, y la función **makeEwsRequestAsync** llama a EWS con un token de autenticación que identifica el buzón y la aplicación de correo que realiza la solicitud. Para ayudar a proteger el buzón del usuario, el servidor Exchange rechazará todas las solicitudes que no provengan de la aplicación de correo o de un buzón que no esté hospedado en el servidor.

Como cualquier otra aplicación, una aplicación de correo necesita permisos para funcionar. El administrador debe:

- [Conceder acceso a EWS](controlling-client-application-access-to-ews-in-exchange.md) al usuario de las aplicaciones de correo.

- [Establezca "OAuthAuthentication" en true](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) en el directorio EWS del servidor de acceso de cliente.

También debe asegurarse de que la aplicación solicita el permiso buzón de lectura y escritura en el [modelo de permisos](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)de aplicaciones para Office.

Una vez completados estos pasos, se puede usar un subconjunto de las operaciones de EWS de elementos y carpetas para que la aplicación de correo la use.

**Tabla 1. Operaciones de elementos y carpetas de EWS que las aplicaciones de correo pueden usar**

|**Operaciones de carpeta**|**Operaciones de elementos**|
|:-----|:-----|
|[Operación CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [Operación FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [Operación GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [Operación UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |[Operación CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [Operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [Operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> [Operación FindConversation](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> [Operación GetConversationItems](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> [Operación GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [Operación MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) <br/> [Operación MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [Operación SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> [Operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |

### <a name="service-callback-tokens"></a>Tokens de devolución de llamada de servicio

Los tokens de devolución de llamada de servicio permiten a las aplicaciones de correo pasar un token de acceso a un servicio de terceros para que el servicio pueda realizar solicitudes EWS al servidor Exchange que hospeda el buzón. Por ejemplo, una aplicación de correo puede pasar un token de devolución de llamada de servicio a un servicio de terceros junto con una lista de identificadores de datos adjuntos para imágenes adjuntas a un correo electrónico. A continuación, el servicio puede usar los identificadores de datos adjuntos y el token de devolución de llamada para realizar una solicitud de EWS al servidor de Exchange del usuario para obtener las imágenes adjuntas. Las aplicaciones de correo también pueden usar el token de devolución de llamada de servicio con una lista de identificadores de elemento para obtener los elementos de correo electrónico y citas del servidor Exchange.

El token de devolución de llamada de servicio es un token opaco que el servicio de terceros se adjunta a la solicitud de EWS en un encabezado de autenticación de portador. El token identifica la aplicación de correo y el buzón para ayudar a proteger la solicitud de EWS. Para obtener información sobre cómo usar los tokens de devolución de llamada de servicio, vea la muestra de [Complementos de Outlook: obtener datos adjuntos de un servidor de Exchange](https://code.msdn.microsoft.com/exchange/Mail-apps-for-Office-Get-38babdc9) .

## <a name="see-also"></a>Vea también


- [Controlar el acceso de la aplicación cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md)

- [Método Mailbox.makeEwsRequestAsync (API de JavaScript para Office)](https://msdn.microsoft.com/library/2ec380e0-4a67-4146-92a6-6a39f65dc6f2%28Office.15%29.aspx)

- [Complementos de Outlook](https://docs.microsoft.com/outlook/add-ins)

- [Método Mailbox.getUserIdentityTokenAsync (API de JavaScript para Office)](https://msdn.microsoft.com/library/c658518b-6867-41a0-99cf-810303e4c539%28Office.15%29.aspx)

- [Autenticar un complemento de Outlook con tokens de identidad de Exchange](https://msdn.microsoft.com/library/c0520a1e-d9ba-495a-a99f-6816d7d2a23e%28Office.15%29.aspx)

- [Información sobre los permisos de los complementos de Outlook](https://docs.microsoft.com/outlook/add-ins/understanding-outlook-add-in-permissions)

- [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx)

- [Complementos de Outlook: realizar una solicitud de EWS](https://code.msdn.microsoft.com/office/Mail-apps-for-Outlook-Make-770b2528)

- [Complementos de Outlook: usar un token de identidad de cliente](https://code.msdn.microsoft.com/Mail-apps-for-Outlook-Use-b20a66b6)

- [Complementos de Outlook: obtener datos adjuntos de un servidor de Exchange](https://code.msdn.microsoft.com/office/Mail-apps-for-Office-Get-38babdc9)

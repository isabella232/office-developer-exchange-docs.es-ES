---
title: Personas y contactos de EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 043c33be-a0d1-4bad-a840-85715eda4813
description: Obtenga información sobre los roles, el almacén de contactos unificado y cómo trabajar con los contactos mediante la API administrada de EWS o EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: f0590a0d8a99b8320cc1b316829177e05e443de6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457677"
---
# <a name="people-and-contacts-in-ews-in-exchange"></a>Personas y contactos de EWS en Exchange

Obtenga información sobre los roles, el almacén de contactos unificado y cómo trabajar con los contactos mediante la API administrada de EWS o EWS en Exchange. 
  
Los contactos son elementos de Exchange que almacenan información sobre una persona, un grupo o una organización. Los contactos pueden incluir nombres y direcciones de correo electrónico, y otra información, como direcciones de mensajería instantánea, direcciones físicas, cumpleaños, información de la familia y una foto o imagen que representa al contacto.
  
La información de contacto se almacena en uno de estos dos lugares:
  
- Servicios de dominio de Active Directory (AD DS), si el contacto está dentro de la organización.
    
- La carpeta contactos u otra carpeta en el buzón de un usuario, si el contacto está fuera de la organización.
    
Varios elementos de contacto pueden representar una sola persona. Exchange usa personas para ayudar a reunir estos distintos elementos de contacto. Un *rol* es una agregación de información de contacto para la misma persona desde diferentes orígenes. Además de la información de contacto en Exchange, los roles también se pueden agregar desde la información de la caché de destinatarios para el buzón de correo, una carpeta oculta para los contactos de mensajería instantánea denominado QuickContacts y de los orígenes de datos de terceros. El almacén de contactos unificados de Exchange permite a los clientes de mensajería instantánea usar esta agregación; la única diferencia es que el almacén de contactos unificado no agrega información de AD DS, como se muestra en la figura 1. 
  
**Figura 1. Orígenes de información de contacto para roles y para el almacén de contactos unificados**

![Una imagen que muestra los orígenes que se agregan en los roles frente a los orígenes que están incluidos en el almacén de contactos unificado. El almacén de contactos unificado no agrega información de contacto del servicio de directorios.](media/EX15_PersonaOverview.png)
  
**Tabla 1. Métodos de API administrada de EWS y operaciones de EWS para trabajar con contactos**

|**Si quiere...**|**Usar este método de API administrada de EWS**|**Usar esta operación de EWS**|
|:-----|:-----|:-----|
|Crear un contacto nuevo  <br/> |Cree una instancia de un nuevo objeto de [contacto](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) y use [Contact. Save](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.save%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/417e994b-0a17-4c24-9527-04796b80b029%28Office.15%29.aspx) <br/> |
|Copiar un contacto  <br/> |[Contact. Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.copy%28v=exchg.80%29.aspx) <br/> |[CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|Mover un contacto  <br/> |[Contact. Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.move%28v=exchg.80%29.aspx) <br/> |[MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|Actualizar un contacto existente  <br/> |[Contact. bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) y [Contact. Update](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.update%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/298fdd71-a83d-4407-9728-4f0a8e2d857c%28Office.15%29.aspx) <br/> |
|Eliminar un contacto  <br/> |[Contact. bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) y [Contact. Delete](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.delete%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
|Buscar un contacto  <br/> |[ExchangeService. FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
|Busque personas  <br/> |N/D  <br/> |[FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |
|Expandir un grupo de distribución  <br/> |[ExchangeService. ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |
|Resolver un nombre ambiguo  <br/> |[ExchangeService. ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |
|Obtener un rol  <br/> |N/D  <br/> |[GetPersona](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |
|Trabajar con fotos de contactos  <br/> |[Contact. SetContactPicture](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.setcontactpicture%28v=exchg.80%29.aspx), [Contact. GetContactPictureAttachment](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.getcontactpictureattachment%28v=exchg.80%29.aspx)o [Contact. RemoveContactPicture](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.setcontactpicture%28v=exchg.80%29.aspx) <br/> |[GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx) o [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) <br/> |
   
## <a name="personas"></a>Roles
<a name="PEOPLESEARCH"> </a>

Hasta hace poco, los contactos se almacenaban normalmente en una sola ubicación, normalmente, en un cliente de correo electrónico. Actualmente, es cada vez más común almacenar contactos en muchas ubicaciones diferentes, como en un teléfono, en un sitio de redes sociales, en una carpeta de contactos en un buzón de Exchange o en el servicio de directorio de una organización. Con la proliferación de información de contactos, es posible que varios contactos que representan a la misma persona contengan distinta información; por ejemplo, un contacto puede incluir un número de teléfono de la empresa y otro número de teléfono personal, o un contacto almacenado en una carpeta de contactos puede tener un nombre distinto al de la misma persona que está almacenada en el teléfono.
  
En Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange a partir de Exchange 2013, los contactos de orígenes diferentes que representan a la misma persona están asociados entre sí, de manera similar a como se agregan los mensajes de correo electrónico en conversaciones, por medio de un identificador de vínculo común. Cuando un servidor de Exchange devuelve información de contacto agregada, incluye un conjunto de atributos para cada contacto, como una carpeta de origen, un nombre para mostrar, un identificador y un identificador de origen. La suma de las propiedades y atributos devueltos se conoce como rol y el conjunto de propiedades devueltas se conoce como la [forma del rol](https://msdn.microsoft.com/library/61d87cd5-3270-40d1-bab7-d0d5bf938607%28Office.15%29.aspx).
  
Debido a que la información que conforma un rol no se almacena en una sola ubicación y dado que la información puede cambiar en cualquier momento, se crea un rol solo cuando se realiza una solicitud a un servidor de Exchange. Use la operación de EWS de [FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) para realizar una solicitud de búsqueda de un rol. La solicitud puede incluir un criterio de ordenación y se puede filtrar según una cadena de consulta para ayudarle a encontrar el rol correcto mediante la ordenación y el filtrado de los resultados. Por ejemplo, puede recuperar el nombre para mostrar y un conjunto de todas las direcciones de correo electrónico que están asociadas a un contacto específico de la carpeta contactos, una cuenta de hotmail, una cuenta de LinkedIn y el servicio de directorio de una compañía, o puede recuperar un conjunto de todos los roles que tienen direcciones de mensajería instantánea. La vinculación de contactos en roles se basa automáticamente en un algoritmo que reconoce una relación entre los contactos almacenados en varios dispositivos. 
  
> [!NOTE]
> La API administrada de EWS no implementa esta funcionalidad. 
  
**Tabla 2. Operaciones de EWS para trabajar con roles**

|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Devuelve todos los roles disponibles de una carpeta de contactos especificada o recupera contactos que coinciden con una cadena de consulta especificada.  <br/> |
|[GetPersona](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |Devuelve un conjunto de propiedades asociadas a un rol específico, como todas las direcciones de mensajería instantánea o los nombres para mostrar de un identificador de rol especificado.  <br/> |
   
Puede usar las operaciones **GetPersona** y **FindPeople** para recuperar eficazmente la información de contacto de varios orígenes. Como todos los elementos relacionados con un rol están asociados con un identificador de vínculo, puede usar estas operaciones en una amplia variedad de aplicaciones que usan datos de contacto. A continuación se proporcionan ejemplos: 
  
- Una aplicación de teléfono móvil que usa la operación **GetPersona** cuando un usuario llama a un contacto y, a continuación, ofrece números de teléfono adicionales para llamar si no hay una sola respuesta. 
    
- Una aplicación que usa la operación **FindPeople** para analizar los mensajes de la bandeja de entrada en busca de direcciones de correo electrónico para determinar si se encuentran en un rol existente. Las direcciones que aún no están asociadas a un rol se pueden usar para crear clientes potenciales de ventas o para enumerar todas las comunicaciones recientes con la persona representada por ese rol. 
    
- [Una aplicación de correo para Outlook](mail-apps-for-outlook-and-ews-in-exchange.md) que ofrece distintos saludos en función de si la correspondencia es formal o informal. Los saludos formales se proporcionan mediante los nombres para mostrar del servicio de directorio y los saludos informales provienen del nombre para mostrar que se origina en los contactos de la red social. 
    
## <a name="unified-contact-store"></a>Almacén de contactos unificado
<a name="PEOPLESEARCH"> </a>

Los roles no se limitan solo a un cliente de correo electrónico. Si está desarrollando un cliente de mensajería instantánea, es posible que se plantee alguna o todas las opciones siguientes:
  
- ¿Cómo puedo aprovisionar aplicaciones cliente de Lync con un conjunto predeterminado de elementos de contacto de mensajería instantánea?
    
- ¿Cómo se administran las listas de contactos y grupos de mensajería instantánea?
    
- ¿Cómo puedo administrar el acceso de clientes de Lync personalizado a los contactos de mensajería instantánea y los grupos de mensajería instantánea?
    
El almacén de contactos unificado funciona en segundo plano en Exchange para agregar datos de contactos de Exchange y otros orígenes a una única entidad o rol. Aunque las operaciones de EWS que se usan para tener acceso al almacén de contactos unificado son específicas de los contactos de mensajería instantánea, puede usar el almacén de contactos unificados de Exchange para trabajar con roles en todos los tipos de aplicaciones. Tenga en cuenta que el almacén de contactos unificados no puede tener acceso a los datos de contacto de AD DS.
  
Los contactos de mensajería instantánea se almacenan en una carpeta oculta denominada QuickContacts. Puede usar las operaciones **AddNewImContactToGroup** y **AddImContactToGroup** para agregar contactos a grupos que se almacenan en esta carpeta oculta. Y, dado que puede usar el almacén de contactos unificados para agrupar contactos de mensajería instantánea, puede tener acceso a los grupos de contactos y actualizarlos más fácilmente. 
  
> [!NOTE]
> La API administrada de EWS no implementa esta funcionalidad. 
  
**Tabla 3. Operaciones de EWS para tener acceso al almacén de contactos unificado**

|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[AddNewImContactToGroup](https://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |Agrega un nuevo contacto de mensajería instantánea a un grupo de mensajería instantánea, hasta un máximo de 1000 contactos.  <br/> |
|[AddImContactToGroup](https://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |Agrega un contacto de mi existente a un grupo de mensajería instantánea, hasta un máximo de 1000 contactos.  <br/> |
|[AddImGroup](https://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |Agrega un nuevo grupo de mensajería instantánea, hasta un máximo de 64 grupos.  <br/> |
|[AddDistributionGroupToImList](https://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |Agrega un nuevo grupo de distribución a un grupo de mensajería instantánea, hasta un máximo de 64 grupos.  <br/> |
|[GetImItemList](https://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |Recupera una lista de grupos de mensajería instantánea y los roles de contactos de mensajería instantánea.  <br/> |
|[GetImItems](https://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |Recupera información sobre grupos de mensajería instantánea específicos y roles de contactos de mensajería instantánea.  <br/> |
|[RemoveContactFromImList](https://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |Quita un contacto de un grupo de mensajería instantánea.  <br/> |
|[RemoveImContactFromGroup](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |Quita un contacto de mensajería instantánea de un grupo de mensajería instantánea.  <br/> |
|[RemoveDistributionGroupFromImList](https://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |Quita un grupo de distribución de un grupo de mensajería instantánea.  <br/> |
|[RemoveImGroup](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |Quita un grupo de mensajería instantánea.  <br/> |
|[SetImGroup](https://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |Cambia el nombre para mostrar de un grupo de mensajería instantánea.  <br/> |
   
## <a name="in-this-section"></a>En esta sección
<a name="PEOPLESEARCH"> </a>

- [Procesar contactos en lotes mediante EWS en Exchange](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    
- [Resolver nombres ambiguos mediante EWS en Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    
- [Obtener fotos de usuario mediante EWS en Exchange](how-to-get-user-photos-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también
<a name="PEOPLESEARCH"> </a>

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    


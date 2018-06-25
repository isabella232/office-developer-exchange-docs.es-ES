---
title: Grupos de distribución y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: Obtenga información sobre los diferentes tipos de grupos de distribución que están disponibles en Exchange y cómo se pueden administrar en la API administrada de EWS o aplicación de EWS.
ms.openlocfilehash: 9b54bfd75f7d68f08c767171d99251b5ce86b7c4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763009"
---
# <a name="distribution-groups-and-ews-in-exchange"></a>Grupos de distribución y EWS en Exchange

Obtenga información sobre los diferentes tipos de grupos de distribución que están disponibles en Exchange y cómo se pueden administrar en la API administrada de EWS o aplicación de EWS.
  
Un grupo de distribución es una colección de direcciones de correo electrónico que están asociadas con una sola dirección de correo electrónico o alias. Grupos de distribución (también denominados listas de distribución) habilitar a un usuario enviar correo electrónico a varias personas mediante el uso de una sola dirección del destinatario. Debido a que la pertenencia a grupos de distribución y, por lo tanto, los destinatarios del mensaje, se pueden administrar fuera de subprocesos de correo electrónico individual, grupos de distribución proporcionan una forma excelente para habilitar la distribución de correo a un grupo de usuarios. Puede crear y administrar grupos de distribución mediante el uso de la API administrada de EWS, EWS y el Shell de administración de Exchange mediante programación. Antes de empezar a programar, vamos a explorar los diferentes tipos de grupos de distribución que están disponibles y las opciones para trabajar con ellos.
  
## <a name="types-of-distribution-groups"></a>Tipos de grupos de distribución

Exchange admite tres tipos de grupos de distribución:
  
- [Grupos de distribución universal](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup) : objetos de grupo de distribución universal de Active Directory que están habilitados para correo. Grupos de distribución universal se utilizan para distribuir mensajes a un grupo de destinatarios. 
    
- [Grupos de seguridad](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup) : objetos de Active Directory que están habilitados para correo; también conocido como grupos de seguridad universal. Grupos de seguridad se utilizan para asignar permisos de acceso a recursos en los servicios de dominio de Active Directory (AD DS), así como para distribuir mensajes. 
    
- [Grupos de contactos](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup) , grupos de distribución privada que se encuentran en el buzón del usuario. 
    
El tipo de grupo de distribución que elija dependerá donde va a almacenar el grupo de distribución, que lo utilizará, y qué se va a usar.
  
### <a name="universal-distribution-groups"></a>Grupos de distribución universal
<a name="bk_DistributionGroup"> </a>

Puede usar grupos de distribución universal para consolidar los grupos de destinatarios en una sola dirección de correo electrónico o alias. Debido a que los grupos de distribución universal se almacenan en AD DS, cualquiera puede usar para enviar correo electrónico, incluidos los usuarios fuera de la organización. Puede usar la API administrada de EWS o EWS para expandir un grupo de distribución, pero para crear y administrar grupos de distribución, necesita usar [los cmdlets del Shell de administración de Exchange](#bk_UsingEMS).
  
También puede usar grupos de distribución universal para que contenga una colección de las salas de; Por ejemplo, para facilitar a los usuarios encontrar una sala de conferencias para una reunión. Los usuarios pueden agregar una lista de salas: un grupo de distribución universal que contiene los buzones de recursos de sala, a una convocatoria de reunión para buscar una sala disponible sin tener que agregar individualmente cada sala.
  
Puede crear un grupo de distribución universal estática que sigue siendo la misma hasta que se va a actualizar la pertenencia, o puede crear un grupo de distribución universal dinámico. Un grupo de distribución universal dinámico consulta objetos habilitados para correo de Active Directory y basa la pertenencia a grupos en función de los resultados. La pertenencia al grupo se vuelve a calcular cada vez que se envía un mensaje de correo electrónico para el grupo. 
  
### <a name="security-groups"></a>Grupos de seguridad
<a name="bk_SecurityGroup"> </a>

Grupos de distribución universal y grupos de seguridad son idénticos en la mayoría de los aspectos. Sin embargo, a diferencia de los grupos de distribución universal, puede usar grupos de seguridad para asignar permisos a recursos de red en AD DS. No se puede usar la API administrada de EWS o EWS para crear y administrar grupos de seguridad; en su lugar, use [los cmdlets del Shell de administración de Exchange](#bk_UsingEMS). Pero, al igual que los grupos de distribución universal, puede usar la API administrada de EWS o EWS para expandir los grupos de seguridad.
  
### <a name="contact-groups"></a>Grupos de contactos
<a name="bk_ContactGroup"> </a>

Si no desea dar a cada acceso administrativo del usuario en el servidor para crear grupos de distribución, pero desea que puedan enviar un solo mensaje a una colección grande de personas, puede hacerlo mediante el uso de grupos de contactos. Un grupo de contactos no tiene una dirección de correo electrónico asociada con él y existe únicamente en el buzón de un usuario; otros usuarios no tienen acceso a ella. Puede [utilizar la API administrada de EWS o EWS para crear grupos de contactos](how-to-create-contact-groups-by-using-ews-in-exchange.md).
  
## <a name="managing-distribution-groups-by-using-the-ews-managed-api-or-ews"></a>Administrar grupos de distribución mediante el uso de la API administrada de EWS o EWS

Puede usar la API administrada de EWS o EWS para expandir un grupo de distribución universal o un grupo de seguridad y para controlar la creación y administración de un grupo de contactos; Sin embargo, no puede usar estas tecnologías para crear o editar a los miembros de esos grupos. 
  
**La tabla 1. Métodos de la API administrada de EWS y las operaciones de EWS para administrar grupos de distribución**

|**Método de la API administrada de EWS**|**Operación de EWS**|**Usar para...**|
|:-----|:-----|:-----|
|Métodos de la [clase ContactGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx)  <br/> |[CreatItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |Crear un grupo de contactos en el almacén de Exchange.  <br/> > [!NOTE]> No puede crear un grupo de distribución universal o un grupo de seguridad mediante el uso de API administrada de EWS o EWS.           |
|[ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |Expanda un grupo de distribución universal, un grupo de seguridad o un grupo de contactos, se recupera una lista de sus miembros.  <br/> |
|[FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Búsqueda de grupos de contactos en el buzón de correo.  <br/> |
|[GetRooms](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](http://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |Recuperar una colección de todas las salas de una lista de salas especificado en una organización. Una lista de salas es un grupo de distribución que sólo contenga buzones de recursos de sala.  <br/> |
|[ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |Buscar y devolver posibles candidatos para que coincida con un nombre ambiguo. Los candidatos pueden ser grupos de distribución.  <br/> |
   
Puede usar la información devuelta por el método [ExpandGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) o la operación de [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) para determinar cuáles son los tipos de miembros en el grupo. Los tipos de miembro se definen mediante la enumeración de la API administrada de EWS [MailboxType](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) y el elemento EWS [MailboxType](http://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) . 
  
**Tabla 2. Tipos de miembro del grupo de distribución**

|**Valor de MailboxType (enumeración)**|**Valor del elemento MailboxType**|**Descripción**|
|:-----|:-----|:-----|
|Buz?n de correo  <br/> |Buz?n de correo  <br/> |Un objeto de Active Directory habilitados para correo.  <br/> |
|PublicGroup  <br/> |PublicDL  <br/> |Un grupo de distribución contenido en el grupo que acaba de expandir. Para obtener una lista completa de miembros, expanda así como para este grupo.  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |Un grupo de contactos que se encuentra en el buzón de correo y sólo está disponible para los usuarios de ese buzón.  <br/> |
|Contacto  <br/> |Contacto  <br/> |Un contacto de la base de datos de Exchange o un contacto de correo de Active Directory.  <br/> |
   
## <a name="managing-distribution-groups-by-using-the-exchange-management-shell"></a>Administración de grupos de distribución mediante el Shell de administración de Exchange
<a name="bk_UsingEMS"> </a>

Puede [usar los cmdlets del Shell de administración de Exchange](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx) para crear y administrar grupos de distribución universal y grupos de seguridad en el código. 
  
> [!NOTE]
> No puede usar los cmdlets del Shell de administración de Exchange para administrar grupos de contactos. 
  
**Tabla 3. Cmdlets del Shell de administración de Exchange para trabajar con grupos de distribución**

|**Cmdlet**|**Usar para...**|
|:-----|:-----|
|[Disable-DistributionGroup](http://technet.microsoft.com/en-us/library/aa997942%28v=exchg.150%29.aspx) <br/> |Quitar las funciones de correo de un grupo de distribución habilitado para correo.  <br/> |
|[Enable-DistributionGroup](http://technet.microsoft.com/en-us/library/aa998916%28v=exchg.150%29.aspx) <br/> |Habilitar para correo un grupo universal existente.  <br/> |
|[Get-DistributionGroup](http://technet.microsoft.com/en-us/library/bb124755%28v=exchg.150%29.aspx) <br/> |Consulta de grupos de distribución existentes.  <br/> |
|[New-DistributionGroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx) <br/> |Crear un grupo de distribución.  <br/> |
|[Remove-DistributionGroup](http://technet.microsoft.com/en-us/library/aa997627%28v=exchg.150%29.aspx) <br/> |Eliminar un grupo de distribución existente de AD DS.  <br/> |
|[Set-DistributionGroup](http://technet.microsoft.com/en-us/library/bb124955%28v=exchg.150%29.aspx) <br/> |Modificar la configuración de un grupo de distribución existente.  <br/> |
|[Agregar-DistributionGroupMember](http://technet.microsoft.com/en-us/library/bb124340%28v=exchg.150%29.aspx) <br/> |Agregar a un destinatario a un grupo de distribución.  <br/> |
|[Get-DistributionGroupMember](http://technet.microsoft.com/en-us/library/aa996367%28v=exchg.150%29.aspx) <br/> |Busque a los miembros del grupo de distribución existente.  <br/> |
|[Remove-DistributionGroupMember](http://technet.microsoft.com/en-us/library/aa998016%28v=exchg.150%29.aspx) <br/> |Quitar a un destinatario existente de un grupo de distribución.  <br/> |
|[Update-DistributionGroupMember](http://technet.microsoft.com/en-us/library/dd335049%28v=exchg.150%29.aspx) <br/> |Actualizar a un miembro de un grupo de distribución especificado.  <br/> |
|[Get-DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb124762%28v=exchg.150%29.aspx) <br/> |Recuperar la configuración de un grupo de distribución dinámica existente.  <br/> |
|[Nueva DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb125127%28v=exchg.150%29.aspx) <br/> |Crear un grupo de distribución dinámica.  <br/> |
|[Remove-DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb125038%28v=exchg.150%29.aspx) <br/> |Eliminar un grupo de distribución dinámica existente. Este cmdlet quita el grupo de distribución dinámico de AD DS.  <br/> |
|[Set-DynamicDistributionGroup](http://technet.microsoft.com/en-us/library/bb123796%28v=exchg.150%29.aspx) <br/> |Modificar la configuración de un grupo de distribución dinámica existente.  <br/> |
   
## <a name="in-this-section"></a>En esta sección
<a name="bk_UsingEMS"> </a>

- [Crear grupos de contactos mediante el uso de EWS en Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    
- [Expandir grupos de distribución mediante el uso de EWS en Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Cmdlets de Shell de administración de Exchange de llamadas desde código administrado](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)
    


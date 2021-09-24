---
title: Grupos de distribución y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fe08c2e3-92a0-43ec-bc61-69b14caee8fe
description: Obtenga información sobre los distintos tipos de grupos de distribución que están disponibles en Exchange y cómo puede administrarlos en su aplicación EWS o API administrada ews.
ms.openlocfilehash: 71dc1a1e4c71310943eb19f8a5d6b3f470ab7ccb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512306"
---
# <a name="distribution-groups-and-ews-in-exchange"></a>Grupos de distribución y EWS en Exchange

Obtenga información sobre los distintos tipos de grupos de distribución que están disponibles en Exchange y cómo puede administrarlos en su aplicación EWS o API administrada ews.
  
Un grupo de distribución es un conjunto de direcciones de correo electrónico que están asociadas con un solo alias o dirección de correo electrónico. Los grupos de distribución (también denominados listas de distribución) permiten a un usuario enviar correo electrónico a varias personas mediante una única dirección de destinatario. Dado que la pertenencia a grupos de distribución y, por lo tanto, los destinatarios del mensaje, se pueden administrar fuera de subprocesos de correo electrónico individuales, los grupos de distribución proporcionan una forma excelente de habilitar la distribución de correo a un grupo de usuarios. Puede crear y administrar grupos de distribución mediante programación mediante la API administrada ews, EWS y el Shell Exchange administración. Antes de empezar a programar, vamos a explorar los diferentes tipos de grupos de distribución que están disponibles y las opciones para administrarlos.
  
## <a name="types-of-distribution-groups"></a>Tipos de grupos de distribución

Exchange admite tres tipos de grupos de distribución:
  
- [Grupos de distribución universales:](distribution-groups-and-ews-in-exchange.md#bk_DistributionGroup) objetos de grupo de distribución universal de Active Directory habilitados para correo. Los grupos de distribución universal se usan para distribuir mensajes a un grupo de destinatarios. 
    
- [Grupos de seguridad:](distribution-groups-and-ews-in-exchange.md#bk_SecurityGroup) objetos de Active Directory habilitados para correo; también conocido como grupos de seguridad universales. Los grupos de seguridad se usan para asignar permisos de acceso a recursos de Servicios de dominio de Active Directory (AD DS), así como para distribuir mensajes. 
    
- [Grupos de contactos:](distribution-groups-and-ews-in-exchange.md#bk_ContactGroup) grupos de distribución privados que se encuentran en el buzón de un usuario. 
    
El tipo de grupo de distribución que elija dependerá de dónde planee almacenar el grupo de distribución, quién lo usará y para qué se usará.

<a name="bk_DistributionGroup"> </a>

### <a name="universal-distribution-groups"></a>Grupos de distribución universal

Puede usar grupos de distribución universales para consolidar grupos de destinatarios en un solo alias o dirección de correo electrónico. Dado que los grupos de distribución universal se almacenan en AD DS, cualquier persona puede usarlos para enviar correo electrónico, incluidos los usuarios de fuera de la organización. Puede usar la API administrada ews o EWS para expandir un grupo de distribución, pero para crear y administrar grupos de distribución, deberá usar los cmdlets del Shell de administración Exchange de [administración.](#bk_UsingEMS)
  
También puede usar grupos de distribución universales para contener una colección de salas; por ejemplo, para facilitar a los usuarios la búsqueda de una sala de conferencias para una reunión. Los usuarios pueden agregar una lista de salas (un grupo de distribución universal que contiene buzones de recursos de sala) a una solicitud de reunión para buscar una sala disponible sin tener que agregar cada sala individualmente.
  
Puede crear un grupo de distribución universal estático que permanezca igual hasta que actualice la pertenencia o puede crear un grupo de distribución universal dinámico. Un grupo de distribución universal dinámico consulta objetos habilitados para correo de Active Directory y crea la pertenencia al grupo en función de los resultados. La pertenencia a grupos se vuelve a calcular siempre que se envía un mensaje de correo electrónico al grupo. 

<a name="bk_SecurityGroup"> </a>

### <a name="security-groups"></a>Grupos de seguridad

Los grupos de distribución universal y los grupos de seguridad son idénticos en la mayoría de los casos. Sin embargo, a diferencia de los grupos de distribución universal, puede usar grupos de seguridad para asignar permisos a recursos de red en AD DS. No puede usar la API administrada ews o EWS para crear y administrar grupos de seguridad; en su lugar, usa [Exchange cmdlets del Shell de administración](#bk_UsingEMS). Pero, al igual que los grupos de distribución universal, puede usar la API administrada ews o EWS para expandir los grupos de seguridad.

<a name="bk_ContactGroup"> </a>

### <a name="contact-groups"></a>Grupos de contactos

Si no desea dar a todos los usuarios acceso administrativo al servidor para crear grupos de distribución, pero desea permitirles enviar un solo mensaje a una gran colección de personas, puede hacerlo mediante grupos de contactos. Un grupo de contactos no tiene una dirección de correo electrónico asociada y solo existe en el buzón de un usuario; otros usuarios no tendrán acceso a él. Puede usar [la API administrada ews o EWS para crear grupos de contactos.](how-to-create-contact-groups-by-using-ews-in-exchange.md)
  
## <a name="managing-distribution-groups-by-using-the-ews-managed-api-or-ews"></a>Administración de grupos de distribución mediante la API administrada ews o EWS

Puede usar la API administrada ews o EWS para expandir un grupo de distribución universal o un grupo de seguridad y para controlar la creación y administración de un grupo de contactos; sin embargo, no puede usar estas tecnologías para crear o editar los miembros de esos grupos. 
  
**Tabla 1. Métodos de API administrada ews y operaciones EWS para administrar grupos de distribución**

|**Método de la API administrada de EWS**|**Operación de EWS**|**Se usa para...**|
|:-----|:-----|:-----|
|[Métodos de clase ContactGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx)  <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |Cree un grupo de contactos en Exchange almacén.<br/><br/>**NOTA:** No puede crear un grupo de distribución universal o un grupo de seguridad mediante LA API administrada ews o EWS.           |
|[ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) <br/> |[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) <br/> |Expanda un grupo de distribución universal, un grupo de seguridad o un grupo de contactos recuperando una lista de sus miembros.  <br/> |
|[FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |Busque grupos de contactos en el buzón.  <br/> |
|[GetRooms](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.getrooms%28v=exchg.80%29.aspx) <br/> |[GetRooms](https://msdn.microsoft.com/library/5501ddc0-3bfa-4da6-8e15-4223ca5499a3%28Office.15%29.aspx) <br/> |Recuperar una colección de todas las salas de una lista de salas especificada de una organización. Una lista de sala es un grupo de distribución que solo contiene buzones de recursos de sala.  <br/> |
|[ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |Busque y devuelva posibles candidatos para que coincidan con un nombre ambiguo. Los candidatos pueden ser grupos de distribución.  <br/> |
   
Puede usar la información devuelta por el método [ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) o la operación [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) para determinar qué tipos de miembros están en el grupo. Los tipos de miembros se definen mediante la enumeración de API administrada EWS [MailboxType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.mailboxtype%28v=exchg.80%29.aspx) y [el elemento EWS MailboxType.](https://msdn.microsoft.com/library/696e5fdb-d8c5-40f0-9e79-885eae65dfa4%28Office.15%29.aspx) 
  
**Tabla 2. Tipos de miembros del grupo de distribución**

|**Valor de enumeración MailboxType**|**Valor del elemento MailboxType**|**Descripción**|
|:-----|:-----|:-----|
|Buzón de correo  <br/> |Buzón de correo  <br/> |Un objeto de Active Directory habilitado para correo.  <br/> |
|PublicGroup  <br/> |PublicDL  <br/> |Un grupo de distribución contenido en el grupo que acaba de expandir. Para obtener una lista completa de miembros, expanda este grupo también.  <br/> |
|ContactGroup  <br/> |PrivateDL  <br/> |Un grupo de contactos que se encuentra en el buzón y solo está disponible para los usuarios de ese buzón.  <br/> |
|Contacto  <br/> |Contacto  <br/> |Un contacto Exchange base de datos o un contacto de correo de Active Directory.  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="managing-distribution-groups-by-using-the-exchange-management-shell"></a>Administración de grupos de distribución mediante el Shell Exchange administración

Puede usar [los cmdlets Exchange Shell](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx) de administración para crear y administrar grupos de distribución universales y grupos de seguridad en el código. 
  
> [!NOTE]
> No puede usar los cmdlets Exchange Shell de administración para administrar grupos de contactos. 
  
**Tabla 3. Exchange Cmdlets del Shell de administración para trabajar con grupos de distribución**

|**Cmdlet**|**Se usa para...**|
|:-----|:-----|
|[Disable-DistributionGroup](https://technet.microsoft.com/library/aa997942%28v=exchg.150%29.aspx) <br/> |Quite las capacidades de correo de un grupo de distribución habilitado para correo.  <br/> |
|[Enable-DistributionGroup](https://technet.microsoft.com/library/aa998916%28v=exchg.150%29.aspx) <br/> |Habilitar correo para un grupo universal existente.  <br/> |
|[Get-DistributionGroup](https://technet.microsoft.com/library/bb124755%28v=exchg.150%29.aspx) <br/> |Consulta de grupos de distribución existentes.  <br/> |
|[New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx) <br/> |Crear un grupo de distribución.  <br/> |
|[Remove-DistributionGroup](https://technet.microsoft.com/library/aa997627%28v=exchg.150%29.aspx) <br/> |Eliminar un grupo de distribución existente de AD DS.  <br/> |
|[Set-DistributionGroup](https://technet.microsoft.com/library/bb124955%28v=exchg.150%29.aspx) <br/> |Modifique la configuración de un grupo de distribución existente.  <br/> |
|[Add-DistributionGroupMember](https://technet.microsoft.com/library/bb124340%28v=exchg.150%29.aspx) <br/> |Agregar un destinatario a un grupo de distribución.  <br/> |
|[Get-DistributionGroupMember](https://technet.microsoft.com/library/aa996367%28v=exchg.150%29.aspx) <br/> |Busque miembros de grupos de distribución existentes.  <br/> |
|[Remove-DistributionGroupMember](https://technet.microsoft.com/library/aa998016%28v=exchg.150%29.aspx) <br/> |Quite un destinatario existente de un grupo de distribución.  <br/> |
|[Update-DistributionGroupMember](https://technet.microsoft.com/library/dd335049%28v=exchg.150%29.aspx) <br/> |Actualice un miembro de un grupo de distribución especificado.  <br/> |
|[Get-DynamicDistributionGroup](https://technet.microsoft.com/library/bb124762%28v=exchg.150%29.aspx) <br/> |Recupere la configuración de un grupo de distribución dinámico existente.  <br/> |
|[New-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125127%28v=exchg.150%29.aspx) <br/> |Crear un grupo de distribución dinámico.  <br/> |
|[Remove-DynamicDistributionGroup](https://technet.microsoft.com/library/bb125038%28v=exchg.150%29.aspx) <br/> |Elimine un grupo de distribución dinámico existente. Este cmdlet quita el grupo de distribución dinámico de AD DS.  <br/> |
|[Set-DynamicDistributionGroup](https://technet.microsoft.com/library/bb123796%28v=exchg.150%29.aspx) <br/> |Modifique la configuración de un grupo de distribución dinámico existente.  <br/> |

<a name="bk_UsingEMS"> </a>

## <a name="in-this-section"></a>En esta sección

- [Crear grupos de contactos mediante EWS en Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)   
- [Expandir grupos de distribución mediante EWS en Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)   
- [Llamar Exchange cmdlets del Shell de administración desde código administrado](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx)
    


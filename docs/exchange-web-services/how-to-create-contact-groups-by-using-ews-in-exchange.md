---
title: Crear grupos de contactos mediante el uso de EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: Obtenga información sobre cómo crear un grupo de contactos mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: b3357f24e07a9c1b3b37ccb63b0f4f0d0a1d6fcf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763050"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a>Crear grupos de contactos mediante el uso de EWS en Exchange

Obtenga información sobre cómo crear un grupo de contactos mediante la API administrada de EWS o EWS en Exchange.
  
Puede crear un grupo de contactos, que es un [grupo de distribución](distribution-groups-and-ews-in-exchange.md)de privado, mediante el uso de la API administrada de EWS o EWS. Para crear grupos de contactos, use los métodos en la clase de la API administrada de EWS [ContactGroup](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) o usar la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) . 
  
Tenga en cuenta que no se puede usar la API administrada de EWS o EWS para crear un grupo de distribución universal o un grupo de seguridad. Para crear un grupo de distribución universal o un grupo de seguridad, puede usar el[cmdlet del Shell de administración de Exchange](http://msdn.microsoft.com/en-us/library/ff326159%28v=exchg.140%29.aspx)de [New-DistributionGroup](http://technet.microsoft.com/en-us/library/aa998856%28v=exchg.150%29.aspx). 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a>Crear un grupo de contactos mediante el uso de la API administrada de EWS
<a name="bk_EWSMA"> </a>

Para crear un grupo de contactos, sólo necesita un par fragmentos de información: un nombre para el grupo y los miembros para agregar al grupo. En el ejemplo siguiente se muestra cómo crear un grupo de contactos simple que contiene un par de miembros del grupo.
  
```cs
// Create a new contact group object.
ContactGroup myContactGroup = new ContactGroup(service);
// Give the group a name.
myContactGroup.DisplayName = "My Contact Group";
// Add some members to the group.
myContactGroup.Members.Add(new GroupMember("sadie@contoso.com"));
myContactGroup.Members.Add(new GroupMember("alfred@contoso.com"));
// Save the group.
myContactGroup.Save();

```

## <a name="create-a-contact-group-by-using-ews"></a>Crear un grupo de contactos mediante el uso de EWS
<a name="bk_EWSMA"> </a>

Puede tardar unas más líneas de código, pero puede crear un grupo de contactos mediante el uso de la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) . El siguiente ejemplo de solicitud XML muestra cómo puede crear un grupo de contactos. Esto también es la solicitud XML que se envía al [usar la API administrada de EWS para crear un grupo de contactos](#bk_EWSMA).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
MessageDisposition="SaveOnly">
      <Items xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
         <DistributionList xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <DisplayName xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               My Contact Group
            </DisplayName>
            <Members xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Member xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                        sadie@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
               <Member xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                        alfred@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
            </Members>
         </DistributionList>
      </Items>
   </CreateItem>
```

El siguiente es un ejemplo de una respuesta XML correcta para la solicitud. Tenga en cuenta que los valores devueltos incluyen un identificador de elemento para el nuevo grupo de contactos y una clave de cambio que puede usar en otro código para modificar el grupo de contactos o expandir el grupo para ver a los miembros. El identificador de elemento es más cortos para mejorar la legibilidad.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItemResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <CreateItemResponseMessage ResponseClass="Success" 
             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
            <ResponseCode xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
               NoError
            </ResponseCode>
            <Items xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
               <DistributionList xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
                  <ItemId xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                          Id="AAMkADBlY…" 
                          ChangeKey="EgAAABYAAAAD7hO1SJPWTbICFWZ4U3NMAABXzQiK" />
               </DistributionList>
            </Items>
         </CreateItemResponseMessage>
      </ResponseMessages>
   </CreateItemResponse>
```

## <a name="see-also"></a>Ver también


- [Grupos de distribución y EWS en Exchange](distribution-groups-and-ews-in-exchange.md)
    
- [Expandir grupos de distribución mediante el uso de EWS en Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    


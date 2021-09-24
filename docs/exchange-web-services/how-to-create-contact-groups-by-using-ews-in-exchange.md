---
title: Crear grupos de contactos mediante EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: Obtenga información sobre cómo crear un grupo de contactos mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: ade7fa68b00b055268cd5f0c34a75e0abbdb18ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513223"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a>Crear grupos de contactos mediante EWS en Exchange

Obtenga información sobre cómo crear un grupo de contactos mediante la API administrada ews o EWS en Exchange.
  
Puede crear un grupo de contactos, que es un grupo de [distribución privado,](distribution-groups-and-ews-in-exchange.md)mediante la API administrada ews o EWS. Para crear grupos de contactos, use los métodos de la clase de API administrada EWS [contactGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) o use la [operación EWS CreateItem.](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) 
  
Tenga en cuenta que no puede usar la API administrada ews o EWS para crear un grupo de distribución universal o un grupo de seguridad. Para crear un grupo de distribución universal o un grupo de seguridad, puede usar el cmdlet [New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Exchange Shell de administración](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx). 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a>Crear un grupo de contactos mediante la API administrada de EWS
<a name="bk_EWSMA"> </a>

Para crear un grupo de contactos, solo necesita un par de elementos de información: un nombre para el grupo y los miembros que se agregarán al grupo. En el ejemplo siguiente se muestra cómo crear un grupo de contactos simple que contenga un par de miembros del grupo.
  
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

## <a name="create-a-contact-group-by-using-ews"></a>Crear un grupo de contactos mediante EWS
<a name="bk_EWSMA"> </a>

Puede que se necesiten algunas líneas de código más, pero puede crear un grupo de contactos mediante la [operación EWS CreateItem.](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) En el siguiente ejemplo de solicitud XML se muestra cómo crear un grupo de contactos. Esta es también la solicitud XML que se envía cuando se usa la API administrada [ews para crear un grupo de contactos.](#bk_EWSMA)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
MessageDisposition="SaveOnly">
      <Items xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
         <DistributionList xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               My Contact Group
            </DisplayName>
            <Members xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Member xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                        sadie@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
               <Member xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                     <EmailAddress xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                        alfred@contoso.com
                     </EmailAddress>
                  </Mailbox>
               </Member>
            </Members>
         </DistributionList>
      </Items>
   </CreateItem>
```

A continuación se muestra un ejemplo de una respuesta XML correcta a la solicitud. Tenga en cuenta que los valores devueltos incluyen un identificador de elemento para el nuevo grupo de contactos y una clave de cambio que puede usar en otro código para modificar el grupo de contactos o expandir el grupo para ver los miembros. El identificador del elemento se abrevia para que sea legible.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
   <CreateItemResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <CreateItemResponseMessage ResponseClass="Success" 
             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
            <ResponseCode xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
               NoError
            </ResponseCode>
            <Items xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
               <DistributionList xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                  <ItemId xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
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
    
- [Expandir grupos de distribución mediante EWS en Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    


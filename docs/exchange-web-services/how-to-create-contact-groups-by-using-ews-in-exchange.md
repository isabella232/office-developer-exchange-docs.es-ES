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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763050"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a><span data-ttu-id="8acd2-103">Crear grupos de contactos mediante el uso de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8acd2-103">Create contact groups by using EWS in Exchange</span></span>

<span data-ttu-id="8acd2-104">Obtenga información sobre cómo crear un grupo de contactos mediante la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="8acd2-104">Learn how to create a contact group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="8acd2-105">Puede crear un grupo de contactos, que es un [grupo de distribución](distribution-groups-and-ews-in-exchange.md)de privado, mediante el uso de la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="8acd2-105">You can create a contact group, which is a private [distribution group](distribution-groups-and-ews-in-exchange.md), by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="8acd2-106">Para crear grupos de contactos, use los métodos en la clase de la API administrada de EWS [ContactGroup](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) o usar la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8acd2-106">To create contact groups, use the methods in the [ContactGroup](http://msdn.microsoft.com/es-es/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS Managed API class, or use the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="8acd2-107">Tenga en cuenta que no se puede usar la API administrada de EWS o EWS para crear un grupo de distribución universal o un grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8acd2-107">Note that you can't use the EWS Managed API or EWS to create a universal distribution group or security group.</span></span> <span data-ttu-id="8acd2-108">Para crear un grupo de distribución universal o un grupo de seguridad, puede usar el[cmdlet del Shell de administración de Exchange](http://msdn.microsoft.com/es-es/library/ff326159%28v=exchg.140%29.aspx)de [New-DistributionGroup](http://technet.microsoft.com/es-es/library/aa998856%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8acd2-108">To create a universal distribution group or security group, you can use the [New-DistributionGroup](http://technet.microsoft.com/es-es/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell cmdlet](http://msdn.microsoft.com/es-es/library/ff326159%28v=exchg.140%29.aspx).</span></span> 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a><span data-ttu-id="8acd2-109">Crear un grupo de contactos mediante el uso de la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="8acd2-109">Create a contact group by using the EWS Managed API</span></span>
<span data-ttu-id="8acd2-110"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="8acd2-110"></span></span>

<span data-ttu-id="8acd2-111">Para crear un grupo de contactos, sólo necesita un par fragmentos de información: un nombre para el grupo y los miembros para agregar al grupo.</span><span class="sxs-lookup"><span data-stu-id="8acd2-111">To create a contact group, you just need a couple pieces of information: a name for the group, and the members to add to the group.</span></span> <span data-ttu-id="8acd2-112">En el ejemplo siguiente se muestra cómo crear un grupo de contactos simple que contiene un par de miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="8acd2-112">The following example shows how to create a simple contact group that contains a couple of group members.</span></span>
  
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

## <a name="create-a-contact-group-by-using-ews"></a><span data-ttu-id="8acd2-113">Crear un grupo de contactos mediante el uso de EWS</span><span class="sxs-lookup"><span data-stu-id="8acd2-113">Create a contact group by using EWS</span></span>
<span data-ttu-id="8acd2-114"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="8acd2-114"></span></span>

<span data-ttu-id="8acd2-115">Puede tardar unas más líneas de código, pero puede crear un grupo de contactos mediante el uso de la operación de EWS [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8acd2-115">It might take a few more lines of code, but you can create a contact group by using the [CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="8acd2-116">El siguiente ejemplo de solicitud XML muestra cómo puede crear un grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="8acd2-116">The following XML request example shows how you can create a contact group.</span></span> <span data-ttu-id="8acd2-117">Esto también es la solicitud XML que se envía al [usar la API administrada de EWS para crear un grupo de contactos](#bk_EWSMA).</span><span class="sxs-lookup"><span data-stu-id="8acd2-117">This is also the XML request that is sent when you [use the EWS Managed API to create a contact group](#bk_EWSMA).</span></span>
  
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

<span data-ttu-id="8acd2-118">El siguiente es un ejemplo de una respuesta XML correcta para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8acd2-118">The following is an example of a successful XML response to the request.</span></span> <span data-ttu-id="8acd2-119">Tenga en cuenta que los valores devueltos incluyen un identificador de elemento para el nuevo grupo de contactos y una clave de cambio que puede usar en otro código para modificar el grupo de contactos o expandir el grupo para ver a los miembros.</span><span class="sxs-lookup"><span data-stu-id="8acd2-119">Notice that the values returned include an item ID for the new contact group and a change key that you can use in other code to modify the contact group or expand the group to see the members.</span></span> <span data-ttu-id="8acd2-120">El identificador de elemento es más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="8acd2-120">The item ID is shortened for readability.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="8acd2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8acd2-121">See also</span></span>


- [<span data-ttu-id="8acd2-122">Grupos de distribución y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8acd2-122">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="8acd2-123">Expandir grupos de distribución mediante el uso de EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8acd2-123">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    


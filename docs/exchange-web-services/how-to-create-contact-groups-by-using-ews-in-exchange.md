---
title: Crear grupos de contactos con EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acec6e73-c016-419d-be1a-8ec5d993addb
description: Obtenga información sobre cómo crear un grupo de contactos con la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 1da876bbda72f5bea08fd9855aa3f554135d54aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528142"
---
# <a name="create-contact-groups-by-using-ews-in-exchange"></a><span data-ttu-id="9106f-103">Crear grupos de contactos con EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9106f-103">Create contact groups by using EWS in Exchange</span></span>

<span data-ttu-id="9106f-104">Obtenga información sobre cómo crear un grupo de contactos con la API administrada de EWS o EWS en Exchange.</span><span class="sxs-lookup"><span data-stu-id="9106f-104">Learn how to create a contact group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="9106f-105">Puede crear un grupo de contactos, que es un [grupo de distribución](distribution-groups-and-ews-in-exchange.md)privado, mediante la API administrada de EWS o EWS.</span><span class="sxs-lookup"><span data-stu-id="9106f-105">You can create a contact group, which is a private [distribution group](distribution-groups-and-ews-in-exchange.md), by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="9106f-106">Para crear grupos de contactos, use los métodos de la clase API administrada de EWS de [ContactGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) o use la operación de EWS del [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9106f-106">To create contact groups, use the methods in the [ContactGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) EWS Managed API class, or use the [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> 
  
<span data-ttu-id="9106f-107">Tenga en cuenta que no puede usar la API administrada de EWS o EWS para crear un grupo de distribución universal o un grupo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9106f-107">Note that you can't use the EWS Managed API or EWS to create a universal distribution group or security group.</span></span> <span data-ttu-id="9106f-108">Para crear un grupo de distribución universal o un grupo de seguridad, puede usar el cmdlet [New-DistributionGroup Shell de](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Administración de Exchange](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9106f-108">To create a universal distribution group or security group, you can use the [New-DistributionGroup](https://technet.microsoft.com/library/aa998856%28v=exchg.150%29.aspx)[Exchange Management Shell cmdlet](https://msdn.microsoft.com/library/ff326159%28v=exchg.140%29.aspx).</span></span> 
  
## <a name="create-a-contact-group-by-using-the-ews-managed-api"></a><span data-ttu-id="9106f-109">Crear un grupo de contactos mediante la API administrada de EWS</span><span class="sxs-lookup"><span data-stu-id="9106f-109">Create a contact group by using the EWS Managed API</span></span>
<span data-ttu-id="9106f-110"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="9106f-110"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="9106f-111">Para crear un grupo de contactos, solo necesitará un par de datos: un nombre para el grupo y los miembros que se agregarán al grupo.</span><span class="sxs-lookup"><span data-stu-id="9106f-111">To create a contact group, you just need a couple pieces of information: a name for the group, and the members to add to the group.</span></span> <span data-ttu-id="9106f-112">En el ejemplo siguiente se muestra cómo crear un grupo de contactos sencillo que contiene un par de miembros del grupo.</span><span class="sxs-lookup"><span data-stu-id="9106f-112">The following example shows how to create a simple contact group that contains a couple of group members.</span></span>
  
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

## <a name="create-a-contact-group-by-using-ews"></a><span data-ttu-id="9106f-113">Crear un grupo de contactos con EWS</span><span class="sxs-lookup"><span data-stu-id="9106f-113">Create a contact group by using EWS</span></span>
<span data-ttu-id="9106f-114"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="9106f-114"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="9106f-115">Es posible que se necesiten varias líneas de código, pero se puede crear un grupo de contactos mediante la operación EWS del [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9106f-115">It might take a few more lines of code, but you can create a contact group by using the [CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) EWS operation.</span></span> <span data-ttu-id="9106f-116">El siguiente ejemplo de solicitud XML muestra cómo se puede crear un grupo de contactos.</span><span class="sxs-lookup"><span data-stu-id="9106f-116">The following XML request example shows how you can create a contact group.</span></span> <span data-ttu-id="9106f-117">Esta es también la solicitud XML que se envía cuando se [usa la API administrada de EWS para crear un grupo de contactos](#bk_EWSMA).</span><span class="sxs-lookup"><span data-stu-id="9106f-117">This is also the XML request that is sent when you [use the EWS Managed API to create a contact group](#bk_EWSMA).</span></span>
  
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

<span data-ttu-id="9106f-118">El siguiente es un ejemplo de una respuesta XML correcta para la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9106f-118">The following is an example of a successful XML response to the request.</span></span> <span data-ttu-id="9106f-119">Observe que los valores devueltos incluyen un identificador de elemento para el nuevo grupo de contactos y una clave de cambio que puede usar en otro código para modificar el grupo de contactos o expandir el grupo para ver los miembros.</span><span class="sxs-lookup"><span data-stu-id="9106f-119">Notice that the values returned include an item ID for the new contact group and a change key that you can use in other code to modify the contact group or expand the group to see the members.</span></span> <span data-ttu-id="9106f-120">El identificador de elemento se acorta para facilitar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9106f-120">The item ID is shortened for readability.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="9106f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9106f-121">See also</span></span>


- [<span data-ttu-id="9106f-122">Grupos de distribución y EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="9106f-122">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="9106f-123">Expandir grupos de distribución mediante EWS en Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9106f-123">Expand distribution groups by using EWS in Exchange 2013</span></span>](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    


---
title: Operación CreateItem (contacto)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 417e994b-0a17-4c24-9527-04796b80b029
description: La operación CreateItem se usa para crear contactos en el almacén de Exchange.
ms.openlocfilehash: e1d78392b94d328cf687655cd93e6c9568f6274f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457126"
---
# <a name="createitem-operation-contact"></a><span data-ttu-id="579b4-103">Operación CreateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="579b4-103">CreateItem operation (contact)</span></span>

<span data-ttu-id="579b4-104">La operación CreateItem se usa para crear contactos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="579b4-104">The CreateItem operation is used to create contacts in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="579b4-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="579b4-105">Remarks</span></span>

<span data-ttu-id="579b4-106">No se admite la creación de listas de distribución privadas.</span><span class="sxs-lookup"><span data-stu-id="579b4-106">The creation of private distribution lists is not supported.</span></span> <span data-ttu-id="579b4-107">Todas las propiedades del contenedor [CompleteName](completename.md) son de solo lectura y no se pueden establecer en un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="579b4-107">All properties within the [CompleteName](completename.md) container are read-only and cannot be set on a contact item.</span></span> 
  
## <a name="createitem-request-example"></a><span data-ttu-id="579b4-108">Ejemplo de solicitud CreateItem</span><span class="sxs-lookup"><span data-stu-id="579b4-108">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="579b4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="579b4-109">Description</span></span>

<span data-ttu-id="579b4-110">El siguiente ejemplo de una solicitud SOAP de CreateItem válida muestra cómo crear un contacto en la carpeta de contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="579b4-110">The following example of a valid CreateItem SOAP request shows how to create a contact in the default Contacts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="579b4-111">Código</span><span class="sxs-lookup"><span data-stu-id="579b4-111">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" >
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="contacts"/>
      </SavedItemFolderId>
      <Items>
        <t:Contact>
          <t:FileAs>SampleContact</t:FileAs>
          <t:GivenName>Tanja</t:GivenName>
          <t:CompanyName>Blue Yonder Airlines</t:CompanyName>
          <t:EmailAddresses>
            <t:Entry Key="EmailAddress1">tplate@example.com</t:Entry>
          </t:EmailAddresses>
          <t:PhysicalAddresses>
            <t:Entry Key="Business">
              <t:Street>1234 56th Ave</t:Street>
              <t:City>La Habra</t:City>
              <t:State>CA</t:State>
              <t: CountryOrRegion>USA</t: CountryOrRegion>
            </t:Entry>
          </t:PhysicalAddresses>
          <t:PhoneNumbers>
            <t:Entry Key="BusinessPhone">4255550199</t:Entry>
          </t:PhoneNumbers>
          <t:JobTitle>Manager</t:JobTitle>
          <t:Surname>Plate</t:Surname>
        </t:Contact>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="579b4-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="579b4-112">Request elements</span></span>

<span data-ttu-id="579b4-113">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="579b4-113">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="579b4-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="579b4-114">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="579b4-115">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="579b4-115">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="579b4-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="579b4-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="579b4-117">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="579b4-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="579b4-118">Contacto</span><span class="sxs-lookup"><span data-stu-id="579b4-118">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="579b4-119">FileAs</span><span class="sxs-lookup"><span data-stu-id="579b4-119">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="579b4-120">GivenName</span><span class="sxs-lookup"><span data-stu-id="579b4-120">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="579b4-121">CompanyName</span><span class="sxs-lookup"><span data-stu-id="579b4-121">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="579b4-122">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="579b4-122">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="579b4-123">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="579b4-123">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="579b4-124">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="579b4-124">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="579b4-125">Entrada (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="579b4-125">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="579b4-126">Drogas</span><span class="sxs-lookup"><span data-stu-id="579b4-126">Street</span></span>](street.md)
    
- [<span data-ttu-id="579b4-127">Ciudad</span><span class="sxs-lookup"><span data-stu-id="579b4-127">City</span></span>](city.md)
    
- [<span data-ttu-id="579b4-128">State</span><span class="sxs-lookup"><span data-stu-id="579b4-128">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="579b4-129">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="579b4-129">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="579b4-130">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="579b4-130">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="579b4-131">Entrada (PhoneNumber)</span><span class="sxs-lookup"><span data-stu-id="579b4-131">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="579b4-132">JobTitle</span><span class="sxs-lookup"><span data-stu-id="579b4-132">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="579b4-133">Apellido</span><span class="sxs-lookup"><span data-stu-id="579b4-133">Surname</span></span>](surname.md)
    
## <a name="successful-createitem-request"></a><span data-ttu-id="579b4-134">Solicitud CreateItem correcta</span><span class="sxs-lookup"><span data-stu-id="579b4-134">Successful CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="579b4-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="579b4-135">Description</span></span>

<span data-ttu-id="579b4-136">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateItem que creó un contacto.</span><span class="sxs-lookup"><span data-stu-id="579b4-136">The following example shows a successful response to the CreateItem request that created a contact.</span></span> <span data-ttu-id="579b4-137">En este ejemplo, la respuesta contiene el identificador del elemento que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="579b4-137">In this example, the response contains the identifier of the newly created item.</span></span>
  
### <a name="code"></a><span data-ttu-id="579b4-138">Código</span><span class="sxs-lookup"><span data-stu-id="579b4-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAtA=" ChangeKey="EQAAAB" />
            </t:Contact>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="579b4-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="579b4-139">Comments</span></span>

<span data-ttu-id="579b4-140">El identificador de elemento se ha abreviado para preservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="579b4-140">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="579b4-141">Elementos Response correcto</span><span class="sxs-lookup"><span data-stu-id="579b4-141">Successful response elements</span></span>

<span data-ttu-id="579b4-142">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="579b4-142">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="579b4-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="579b4-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="579b4-144">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="579b4-144">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="579b4-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="579b4-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="579b4-146">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="579b4-146">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="579b4-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="579b4-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="579b4-148">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="579b4-148">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="579b4-149">Contacto</span><span class="sxs-lookup"><span data-stu-id="579b4-149">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="579b4-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="579b4-150">ItemId</span></span>](itemid.md)
    
## <a name="invalid-createitem-request-example"></a><span data-ttu-id="579b4-151">Ejemplo de solicitud CreateItem no válida</span><span class="sxs-lookup"><span data-stu-id="579b4-151">Invalid CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="579b4-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="579b4-152">Description</span></span>

<span data-ttu-id="579b4-153">En el ejemplo siguiente se muestra una solicitud que contiene código XML válido, pero con instrucciones incompatibles.</span><span class="sxs-lookup"><span data-stu-id="579b4-153">The following example shows a request that contains valid XML but incompatible instructions.</span></span> <span data-ttu-id="579b4-154">No se puede crear un contacto en una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="579b4-154">A contact cannot be created in a search folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="579b4-155">Código</span><span class="sxs-lookup"><span data-stu-id="579b4-155">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id='searchfolders'/>
      </SavedItemFolderId>
      <Items>
        <t:Contact>
          <t:ItemClass>IPM.Contact</t:ItemClass>
        </t:Contact>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="createitem-contact-error-response"></a><span data-ttu-id="579b4-156">CreateItem (contacto) respuesta de error</span><span class="sxs-lookup"><span data-stu-id="579b4-156">CreateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="579b4-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="579b4-157">Description</span></span>

<span data-ttu-id="579b4-158">El ejemplo siguiente muestra una respuesta de error a una solicitud CreateItem (contact).</span><span class="sxs-lookup"><span data-stu-id="579b4-158">The following example shows an error response to a CreateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="579b4-159">Código</span><span class="sxs-lookup"><span data-stu-id="579b4-159">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot create a contact in a non-contact Folder.</m:MessageText>
          <m:ResponseCode>ErrorCannotCreateContactInNonContactFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="579b4-160">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="579b4-160">Error response elements</span></span>

<span data-ttu-id="579b4-161">Los siguientes elementos se usan en la respuesta de error:</span><span class="sxs-lookup"><span data-stu-id="579b4-161">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="579b4-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="579b4-162">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="579b4-163">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="579b4-163">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="579b4-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="579b4-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="579b4-165">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="579b4-165">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="579b4-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="579b4-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="579b4-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="579b4-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="579b4-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="579b4-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="579b4-169">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="579b4-169">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
## <a name="see-also"></a><span data-ttu-id="579b4-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="579b4-170">See also</span></span>



[<span data-ttu-id="579b4-171">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="579b4-171">CreateItem operation</span></span>](createitem-operation.md)


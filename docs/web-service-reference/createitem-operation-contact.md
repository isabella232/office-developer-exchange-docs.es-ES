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
description: Se usa la operación CreateItem para crear contactos en el almacén de Exchange.
ms.openlocfilehash: 05e4715f3c6675401ae7afac852395f7459c02c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763950"
---
# <a name="createitem-operation-contact"></a><span data-ttu-id="c3ca6-103">Operación CreateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-103">CreateItem operation (contact)</span></span>

<span data-ttu-id="c3ca6-104">Se usa la operación CreateItem para crear contactos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-104">The CreateItem operation is used to create contacts in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3ca6-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3ca6-105">Remarks</span></span>

<span data-ttu-id="c3ca6-106">No se admite la creación de listas de distribución privadas.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-106">The creation of private distribution lists is not supported.</span></span> <span data-ttu-id="c3ca6-107">Todas las propiedades del contenedor de [CompleteName](completename.md) son de solo lectura y no se puede establecer en un elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-107">All properties within the [CompleteName](completename.md) container are read-only and cannot be set on a contact item.</span></span> 
  
## <a name="createitem-request-example"></a><span data-ttu-id="c3ca6-108">Ejemplo de solicitud CreateItem</span><span class="sxs-lookup"><span data-stu-id="c3ca6-108">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="c3ca6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3ca6-109">Description</span></span>

<span data-ttu-id="c3ca6-110">El siguiente ejemplo de una solicitud de SOAP CreateItem válido, muestra cómo crear un contacto en la carpeta Contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-110">The following example of a valid CreateItem SOAP request shows how to create a contact in the default Contacts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="c3ca6-111">Código</span><span class="sxs-lookup"><span data-stu-id="c3ca6-111">Code</span></span>

```XML
<soap:Envelope
 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
 xmlns:xsd="http://www.w3.org/2001/XMLSchema"
 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" >
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

### <a name="request-elements"></a><span data-ttu-id="c3ca6-112">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3ca6-112">Request elements</span></span>

<span data-ttu-id="c3ca6-113">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c3ca6-113">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c3ca6-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="c3ca6-114">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="c3ca6-115">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="c3ca6-115">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="c3ca6-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c3ca6-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="c3ca6-117">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="c3ca6-118">Contact</span><span class="sxs-lookup"><span data-stu-id="c3ca6-118">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="c3ca6-119">Archivar como</span><span class="sxs-lookup"><span data-stu-id="c3ca6-119">FileAs</span></span>](fileas.md)
    
- [<span data-ttu-id="c3ca6-120">GivenName</span><span class="sxs-lookup"><span data-stu-id="c3ca6-120">GivenName</span></span>](givenname.md)
    
- [<span data-ttu-id="c3ca6-121">CompanyName</span><span class="sxs-lookup"><span data-stu-id="c3ca6-121">CompanyName</span></span>](companyname.md)
    
- [<span data-ttu-id="c3ca6-122">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="c3ca6-122">EmailAddresses</span></span>](emailaddresses.md)
    
- [<span data-ttu-id="c3ca6-123">Entrada (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-123">Entry (EmailAddress)</span></span>](entry-emailaddress.md)
    
- [<span data-ttu-id="c3ca6-124">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="c3ca6-124">PhysicalAddresses</span></span>](physicaladdresses.md)
    
- [<span data-ttu-id="c3ca6-125">Entrada (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-125">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md)
    
- [<span data-ttu-id="c3ca6-126">Calle</span><span class="sxs-lookup"><span data-stu-id="c3ca6-126">Street</span></span>](street.md)
    
- [<span data-ttu-id="c3ca6-127">Ciudad</span><span class="sxs-lookup"><span data-stu-id="c3ca6-127">City</span></span>](city.md)
    
- [<span data-ttu-id="c3ca6-128">State</span><span class="sxs-lookup"><span data-stu-id="c3ca6-128">State</span></span>](state-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c3ca6-129">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="c3ca6-129">CountryOrRegion</span></span>](countryorregion.md)
    
- [<span data-ttu-id="c3ca6-130">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="c3ca6-130">PhoneNumbers</span></span>](phonenumbers.md)
    
- [<span data-ttu-id="c3ca6-131">Entrada (PhoneNumber)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-131">Entry (PhoneNumber)</span></span>](entry-phonenumber.md)
    
- [<span data-ttu-id="c3ca6-132">JobTitle</span><span class="sxs-lookup"><span data-stu-id="c3ca6-132">JobTitle</span></span>](jobtitle.md)
    
- [<span data-ttu-id="c3ca6-133">Apellido</span><span class="sxs-lookup"><span data-stu-id="c3ca6-133">Surname</span></span>](surname.md)
    
## <a name="successful-createitem-request"></a><span data-ttu-id="c3ca6-134">Solicitud de CreateItem correcta</span><span class="sxs-lookup"><span data-stu-id="c3ca6-134">Successful CreateItem Request</span></span>

### <a name="description"></a><span data-ttu-id="c3ca6-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3ca6-135">Description</span></span>

<span data-ttu-id="c3ca6-136">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateItem que creó un contacto.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-136">The following example shows a successful response to the CreateItem request that created a contact.</span></span> <span data-ttu-id="c3ca6-137">En este ejemplo, la respuesta contiene el identificador del elemento recién creado.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-137">In this example, the response contains the identifier of the newly created item.</span></span>
  
### <a name="code"></a><span data-ttu-id="c3ca6-138">Código</span><span class="sxs-lookup"><span data-stu-id="c3ca6-138">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="c3ca6-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3ca6-139">Comments</span></span>

<span data-ttu-id="c3ca6-140">El identificador del elemento se ha acortado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-140">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="c3ca6-141">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="c3ca6-141">Successful response elements</span></span>

<span data-ttu-id="c3ca6-142">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c3ca6-142">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c3ca6-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c3ca6-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c3ca6-144">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="c3ca6-144">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="c3ca6-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c3ca6-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c3ca6-146">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c3ca6-146">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="c3ca6-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c3ca6-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c3ca6-148">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-148">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="c3ca6-149">Contact</span><span class="sxs-lookup"><span data-stu-id="c3ca6-149">Contact</span></span>](contact.md)
    
- [<span data-ttu-id="c3ca6-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="c3ca6-150">ItemId</span></span>](itemid.md)
    
## <a name="invalid-createitem-request-example"></a><span data-ttu-id="c3ca6-151">Ejemplo de solicitud CreateItem no válido</span><span class="sxs-lookup"><span data-stu-id="c3ca6-151">Invalid CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="c3ca6-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3ca6-152">Description</span></span>

<span data-ttu-id="c3ca6-153">En el ejemplo siguiente se muestra una solicitud que contiene XML válido pero instrucciones incompatibles.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-153">The following example shows a request that contains valid XML but incompatible instructions.</span></span> <span data-ttu-id="c3ca6-154">No se puede crear un contacto en una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c3ca6-154">A contact cannot be created in a search folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="c3ca6-155">Código</span><span class="sxs-lookup"><span data-stu-id="c3ca6-155">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
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

## <a name="createitem-contact-error-response"></a><span data-ttu-id="c3ca6-156">Respuesta de error CreateItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-156">CreateItem (Contact) error response</span></span>

### <a name="description"></a><span data-ttu-id="c3ca6-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3ca6-157">Description</span></span>

<span data-ttu-id="c3ca6-158">En el ejemplo siguiente se muestra una respuesta de error a una solicitud CreateItem (contactos).</span><span class="sxs-lookup"><span data-stu-id="c3ca6-158">The following example shows an error response to a CreateItem (Contact) request.</span></span>
  
### <a name="code"></a><span data-ttu-id="c3ca6-159">Código</span><span class="sxs-lookup"><span data-stu-id="c3ca6-159">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="c3ca6-160">Elementos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="c3ca6-160">Error response elements</span></span>

<span data-ttu-id="c3ca6-161">En la respuesta de error, se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="c3ca6-161">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="c3ca6-162">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c3ca6-162">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c3ca6-163">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="c3ca6-163">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="c3ca6-164">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c3ca6-164">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c3ca6-165">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c3ca6-165">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="c3ca6-166">MessageText</span><span class="sxs-lookup"><span data-stu-id="c3ca6-166">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c3ca6-167">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c3ca6-167">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c3ca6-168">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c3ca6-168">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="c3ca6-169">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="c3ca6-169">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
## <a name="see-also"></a><span data-ttu-id="c3ca6-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3ca6-170">See also</span></span>



[<span data-ttu-id="c3ca6-171">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="c3ca6-171">CreateItem operation</span></span>](createitem-operation.md)


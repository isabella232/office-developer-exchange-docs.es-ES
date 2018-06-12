---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: El elemento ResolveNames define una solicitud para resolver nombres ambiguos.
ms.openlocfilehash: e97b6e78d99cf8ffa3d680907916882d40963f59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837172"
---
# <a name="resolvenames"></a><span data-ttu-id="7fa85-103">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="7fa85-103">ResolveNames</span></span>

<span data-ttu-id="7fa85-104">El elemento **ResolveNames** define una solicitud para resolver nombres ambiguos.</span><span class="sxs-lookup"><span data-stu-id="7fa85-104">The **ResolveNames** element defines a request to resolve ambiguous names.</span></span> 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 <span data-ttu-id="7fa85-105">**ResolveNamesType**</span><span class="sxs-lookup"><span data-stu-id="7fa85-105">**ResolveNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fa85-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7fa85-106">Attributes and elements</span></span>

<span data-ttu-id="7fa85-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7fa85-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fa85-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7fa85-108">Attributes</span></span>

|<span data-ttu-id="7fa85-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7fa85-109">**Attribute**</span></span>|<span data-ttu-id="7fa85-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fa85-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fa85-111">**ReturnFullContactData**</span><span class="sxs-lookup"><span data-stu-id="7fa85-111">**ReturnFullContactData**</span></span> <br/> |<span data-ttu-id="7fa85-112">Describe si se devuelven los detalles de contacto para los contactos para un nombre resuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fa85-112">Describes whether the full contact details for public contacts for a resolved name are returned in the response.</span></span> <span data-ttu-id="7fa85-113">Este atributo es necesario para los contactos.</span><span class="sxs-lookup"><span data-stu-id="7fa85-113">This attribute is required for public contacts.</span></span> <span data-ttu-id="7fa85-114">Este valor no afecta a los contactos privados y listas de distribución privadas, para que siempre se devuelve [ItemId](itemid.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa85-114">This value does not affect private contacts and private distribution lists, for which [ItemId](itemid.md) is always returned.</span></span>  <br/> |
|<span data-ttu-id="7fa85-115">**SearchScope**</span><span class="sxs-lookup"><span data-stu-id="7fa85-115">**SearchScope**</span></span> <br/> |<span data-ttu-id="7fa85-116">Identifica la orden y el ámbito de una búsqueda ResolveNames.</span><span class="sxs-lookup"><span data-stu-id="7fa85-116">Identifies the order and scope for a ResolveNames search.</span></span>  <br/> |
|<span data-ttu-id="7fa85-117">ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="7fa85-117">ContactDataShape</span></span>  <br/> |<span data-ttu-id="7fa85-118">Identifica la propiedad establecida devuelta para los contactos.</span><span class="sxs-lookup"><span data-stu-id="7fa85-118">Identifies the property set returned for contacts.</span></span> <span data-ttu-id="7fa85-119">Este atributo se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="7fa85-119">This attribute was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a><span data-ttu-id="7fa85-120">Valores de atributo de ReturnFullContactData</span><span class="sxs-lookup"><span data-stu-id="7fa85-120">ReturnFullContactData attribute values</span></span>

|<span data-ttu-id="7fa85-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7fa85-121">**Value**</span></span>|<span data-ttu-id="7fa85-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fa85-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fa85-123">True</span><span class="sxs-lookup"><span data-stu-id="7fa85-123">True</span></span>  <br/> |<span data-ttu-id="7fa85-124">Se devuelven detalles de contacto para los contactos.</span><span class="sxs-lookup"><span data-stu-id="7fa85-124">Full contact details for public contacts are returned.</span></span>  <br/> |
|<span data-ttu-id="7fa85-125">False</span><span class="sxs-lookup"><span data-stu-id="7fa85-125">False</span></span>  <br/> |<span data-ttu-id="7fa85-126">No se devuelven datos de contacto completos para los contactos.</span><span class="sxs-lookup"><span data-stu-id="7fa85-126">Full contact details for public contacts are not returned.</span></span>  <br/> |
   
#### <a name="searchscope-attribute-values"></a><span data-ttu-id="7fa85-127">Valores de atributo de SearchScope</span><span class="sxs-lookup"><span data-stu-id="7fa85-127">SearchScope attribute values</span></span>

|<span data-ttu-id="7fa85-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7fa85-128">**Value**</span></span>|<span data-ttu-id="7fa85-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fa85-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fa85-130">ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="7fa85-130">ActiveDirectory</span></span>  <br/> |<span data-ttu-id="7fa85-131">Se busca en sólo el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fa85-131">Only the Active Directory directory service is searched.</span></span>  <br/> |
|<span data-ttu-id="7fa85-132">ActiveDirectoryContacts</span><span class="sxs-lookup"><span data-stu-id="7fa85-132">ActiveDirectoryContacts</span></span>  <br/> |<span data-ttu-id="7fa85-133">Active Directory se busca en primer lugar y, a continuación, se buscan las carpetas de contactos que se especifican en la propiedad [ParentFolderIds](parentfolderids.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa85-133">Active Directory is searched first, and then the contact folders that are specified in the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="7fa85-134">Contacts</span><span class="sxs-lookup"><span data-stu-id="7fa85-134">Contacts</span></span>  <br/> |<span data-ttu-id="7fa85-135">Se buscan sólo las carpetas de contactos que se identifican mediante la propiedad [ParentFolderIds](parentfolderids.md) .</span><span class="sxs-lookup"><span data-stu-id="7fa85-135">Only the contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="7fa85-136">ContactsActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="7fa85-136">ContactsActiveDirectory</span></span>  <br/> |<span data-ttu-id="7fa85-137">Carpetas de contactos que se identifican mediante la propiedad [ParentFolderIds](parentfolderids.md) se buscan en primer lugar y, a continuación, se busca en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fa85-137">Contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched first and then Active Directory is searched.</span></span>  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a><span data-ttu-id="7fa85-138">Valores de atributo de ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="7fa85-138">ContactDataShape attribute values</span></span>

|<span data-ttu-id="7fa85-139">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7fa85-139">**Value**</span></span>|<span data-ttu-id="7fa85-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fa85-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fa85-141">IdOnly</span><span class="sxs-lookup"><span data-stu-id="7fa85-141">IdOnly</span></span>  <br/> |<span data-ttu-id="7fa85-142">Se devuelve la propiedad de identificador de elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="7fa85-142">The contact item identifier property is returned.</span></span>  <br/> |
|<span data-ttu-id="7fa85-143">Default</span><span class="sxs-lookup"><span data-stu-id="7fa85-143">Default</span></span>  <br/> |<span data-ttu-id="7fa85-144">Se devuelve el conjunto predeterminado de propiedades de elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="7fa85-144">The Default set of contact item properties is returned.</span></span> <span data-ttu-id="7fa85-145">Para obtener más información, vea [las formas de respuesta de EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fa85-145">For more information, see [Response shapes in EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="7fa85-146">AllProperties</span><span class="sxs-lookup"><span data-stu-id="7fa85-146">AllProperties</span></span>  <br/> |<span data-ttu-id="7fa85-147">Se devuelven el conjunto de AllProperties de propiedades de elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="7fa85-147">The AllProperties set of contact item properties are returned.</span></span> <span data-ttu-id="7fa85-148">Para obtener más información, vea [las formas de respuesta de EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fa85-148">For more information, see [Response shapes in EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7fa85-149">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7fa85-149">Child elements</span></span>

|<span data-ttu-id="7fa85-150">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fa85-150">**Element**</span></span>|<span data-ttu-id="7fa85-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fa85-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fa85-152">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="7fa85-152">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="7fa85-153">Contiene una matriz de identificadores de la carpeta de contactos que se debería buscar si se establece el atributo **SearchScope** en ActiveDirectoryContacts, contactos o ContactsActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="7fa85-153">Contains an array of contact folder identifiers that would be searched if the **SearchScope** attribute is set to ActiveDirectoryContacts, Contacts, or ContactsActiveDirectory.</span></span> <span data-ttu-id="7fa85-154">La matriz de ParentFolderIds sólo puede contener un identificador único de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="7fa85-154">The ParentFolderIds array can only contain a single contact folder identifier.</span></span> <span data-ttu-id="7fa85-155">Si el elemento **ParentFolderIds** no está presente, se busca en la carpeta Contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7fa85-155">If the **ParentFolderIds** element is not present, the default Contacts folder is searched.</span></span>  <br/> <span data-ttu-id="7fa85-156">El identificador de la carpeta se puede usar para el acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="7fa85-156">The folder identifier can be used for delegate access.</span></span>  <br/> <span data-ttu-id="7fa85-157">Búsquedas en Active Directory se realizan mediante el uso de listas de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="7fa85-157">Active Directory searches are performed by using access control lists (ACLs).</span></span> <span data-ttu-id="7fa85-158">Algunos usuarios no puedan tener los derechos para ver algunos objetos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fa85-158">Some users might not have the rights to see some Active Directory objects.</span></span>  <br/> <span data-ttu-id="7fa85-159">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="7fa85-159">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="7fa85-160">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="7fa85-160">UnresolvedEntry</span></span>](unresolvedentry.md) <br/> |<span data-ttu-id="7fa85-161">Contiene el nombre de un contacto o lista de distribución para resolver.</span><span class="sxs-lookup"><span data-stu-id="7fa85-161">Contains the name of a contact or distribution list to resolve.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fa85-162">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7fa85-162">Parent elements</span></span>

<span data-ttu-id="7fa85-163">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7fa85-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7fa85-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fa85-164">Remarks</span></span>

<span data-ttu-id="7fa85-165">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7fa85-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fa85-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7fa85-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fa85-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7fa85-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7fa85-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7fa85-168">Schema name</span></span>  <br/> |<span data-ttu-id="7fa85-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7fa85-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7fa85-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7fa85-170">Validation file</span></span>  <br/> |<span data-ttu-id="7fa85-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7fa85-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7fa85-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7fa85-172">Can be empty</span></span>  <br/> |<span data-ttu-id="7fa85-173">False</span><span class="sxs-lookup"><span data-stu-id="7fa85-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fa85-174">Ver también</span><span class="sxs-lookup"><span data-stu-id="7fa85-174">See also</span></span>



[<span data-ttu-id="7fa85-175">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="7fa85-175">ResolveNames operation</span></span>](resolvenames-operation.md)
  
[<span data-ttu-id="7fa85-176">ResolveNamesType</span><span class="sxs-lookup"><span data-stu-id="7fa85-176">ResolveNamesType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[<span data-ttu-id="7fa85-177">ResolveNamesSearchScopeType</span><span class="sxs-lookup"><span data-stu-id="7fa85-177">ResolveNamesSearchScopeType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [<span data-ttu-id="7fa85-178">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7fa85-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="7fa85-179">Uso de la resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="7fa85-179">Using Name Resolution</span></span>](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)


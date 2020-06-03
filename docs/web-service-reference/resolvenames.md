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
ms.openlocfilehash: 9c36a5f84451f91e90a8e7148cf384b5cacd7f29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467952"
---
# <a name="resolvenames"></a><span data-ttu-id="63556-103">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="63556-103">ResolveNames</span></span>

<span data-ttu-id="63556-104">El elemento **ResolveNames** define una solicitud para resolver nombres ambiguos.</span><span class="sxs-lookup"><span data-stu-id="63556-104">The **ResolveNames** element defines a request to resolve ambiguous names.</span></span> 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 <span data-ttu-id="63556-105">**ResolveNamesType**</span><span class="sxs-lookup"><span data-stu-id="63556-105">**ResolveNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63556-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="63556-106">Attributes and elements</span></span>

<span data-ttu-id="63556-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="63556-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63556-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="63556-108">Attributes</span></span>

|<span data-ttu-id="63556-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="63556-109">**Attribute**</span></span>|<span data-ttu-id="63556-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63556-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63556-111">**ReturnFullContactData**</span><span class="sxs-lookup"><span data-stu-id="63556-111">**ReturnFullContactData**</span></span> <br/> |<span data-ttu-id="63556-112">Describe si se devuelven los detalles completos de contacto para los contactos públicos de un nombre resuelto en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63556-112">Describes whether the full contact details for public contacts for a resolved name are returned in the response.</span></span> <span data-ttu-id="63556-113">Este atributo es necesario para los contactos públicos.</span><span class="sxs-lookup"><span data-stu-id="63556-113">This attribute is required for public contacts.</span></span> <span data-ttu-id="63556-114">Este valor no afecta a contactos privados ni a listas de distribución privadas, para las que siempre se devuelve [Itemid](itemid.md) .</span><span class="sxs-lookup"><span data-stu-id="63556-114">This value does not affect private contacts and private distribution lists, for which [ItemId](itemid.md) is always returned.</span></span>  <br/> |
|<span data-ttu-id="63556-115">**SearchScope**</span><span class="sxs-lookup"><span data-stu-id="63556-115">**SearchScope**</span></span> <br/> |<span data-ttu-id="63556-116">Identifica el orden y el ámbito de una búsqueda de ResolveNames.</span><span class="sxs-lookup"><span data-stu-id="63556-116">Identifies the order and scope for a ResolveNames search.</span></span>  <br/> |
|<span data-ttu-id="63556-117">ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="63556-117">ContactDataShape</span></span>  <br/> |<span data-ttu-id="63556-118">Identifica el conjunto de propiedades devuelto para los contactos.</span><span class="sxs-lookup"><span data-stu-id="63556-118">Identifies the property set returned for contacts.</span></span> <span data-ttu-id="63556-119">Este atributo se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="63556-119">This attribute was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a><span data-ttu-id="63556-120">Valores del atributo ReturnFullContactData</span><span class="sxs-lookup"><span data-stu-id="63556-120">ReturnFullContactData attribute values</span></span>

|<span data-ttu-id="63556-121">**Valor**</span><span class="sxs-lookup"><span data-stu-id="63556-121">**Value**</span></span>|<span data-ttu-id="63556-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63556-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63556-123">True</span><span class="sxs-lookup"><span data-stu-id="63556-123">True</span></span>  <br/> |<span data-ttu-id="63556-124">Se devuelven los detalles de contacto completos para los contactos públicos.</span><span class="sxs-lookup"><span data-stu-id="63556-124">Full contact details for public contacts are returned.</span></span>  <br/> |
|<span data-ttu-id="63556-125">Falso</span><span class="sxs-lookup"><span data-stu-id="63556-125">False</span></span>  <br/> |<span data-ttu-id="63556-126">No se devuelven los detalles de contacto completos de los contactos públicos.</span><span class="sxs-lookup"><span data-stu-id="63556-126">Full contact details for public contacts are not returned.</span></span>  <br/> |
   
#### <a name="searchscope-attribute-values"></a><span data-ttu-id="63556-127">Valores de atributo de SearchScope</span><span class="sxs-lookup"><span data-stu-id="63556-127">SearchScope attribute values</span></span>

|<span data-ttu-id="63556-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="63556-128">**Value**</span></span>|<span data-ttu-id="63556-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63556-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63556-130">Directory</span><span class="sxs-lookup"><span data-stu-id="63556-130">ActiveDirectory</span></span>  <br/> |<span data-ttu-id="63556-131">Solo se busca en el servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63556-131">Only the Active Directory directory service is searched.</span></span>  <br/> |
|<span data-ttu-id="63556-132">ActiveDirectoryContacts</span><span class="sxs-lookup"><span data-stu-id="63556-132">ActiveDirectoryContacts</span></span>  <br/> |<span data-ttu-id="63556-133">Se busca primero en Active Directory y, a continuación, se busca en las carpetas de contactos que se especifican en la propiedad [ParentFolderIds](parentfolderids.md) .</span><span class="sxs-lookup"><span data-stu-id="63556-133">Active Directory is searched first, and then the contact folders that are specified in the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="63556-134">Contactos</span><span class="sxs-lookup"><span data-stu-id="63556-134">Contacts</span></span>  <br/> |<span data-ttu-id="63556-135">Solo se busca en las carpetas de contactos que se identifican mediante la propiedad [ParentFolderIds](parentfolderids.md) .</span><span class="sxs-lookup"><span data-stu-id="63556-135">Only the contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="63556-136">ContactsActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="63556-136">ContactsActiveDirectory</span></span>  <br/> |<span data-ttu-id="63556-137">Las carpetas de contactos que se identifican mediante la propiedad [ParentFolderIds](parentfolderids.md) se buscan primero en el directorio y, a continuación, se busca en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63556-137">Contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched first and then Active Directory is searched.</span></span>  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a><span data-ttu-id="63556-138">Valores del atributo ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="63556-138">ContactDataShape attribute values</span></span>

|<span data-ttu-id="63556-139">**Valor**</span><span class="sxs-lookup"><span data-stu-id="63556-139">**Value**</span></span>|<span data-ttu-id="63556-140">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63556-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="63556-141">IdOnly</span><span class="sxs-lookup"><span data-stu-id="63556-141">IdOnly</span></span>  <br/> |<span data-ttu-id="63556-142">Se devuelve la propiedad de identificador del elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="63556-142">The contact item identifier property is returned.</span></span>  <br/> |
|<span data-ttu-id="63556-143">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="63556-143">Default</span></span>  <br/> |<span data-ttu-id="63556-144">Se devuelve el conjunto predeterminado de propiedades del elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="63556-144">The Default set of contact item properties is returned.</span></span> <span data-ttu-id="63556-145">Para obtener más información, vea [formas de respuesta en EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="63556-145">For more information, see [Response shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="63556-146">AllProperties</span><span class="sxs-lookup"><span data-stu-id="63556-146">AllProperties</span></span>  <br/> |<span data-ttu-id="63556-147">Se devuelve el conjunto AllProperties de propiedades de elemento de contacto.</span><span class="sxs-lookup"><span data-stu-id="63556-147">The AllProperties set of contact item properties are returned.</span></span> <span data-ttu-id="63556-148">Para obtener más información, vea [formas de respuesta en EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="63556-148">For more information, see [Response shapes in EWS](https://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="63556-149">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63556-149">Child elements</span></span>

|<span data-ttu-id="63556-150">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="63556-150">**Element**</span></span>|<span data-ttu-id="63556-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63556-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63556-152">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="63556-152">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="63556-153">Contiene una matriz de identificadores de carpetas de contactos en los que se buscará si el atributo **SearchScope** está establecido en ActiveDirectoryContacts, Contacts o ContactsActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="63556-153">Contains an array of contact folder identifiers that would be searched if the **SearchScope** attribute is set to ActiveDirectoryContacts, Contacts, or ContactsActiveDirectory.</span></span> <span data-ttu-id="63556-154">La matriz ParentFolderIds solo puede contener un identificador de carpeta de contacto único.</span><span class="sxs-lookup"><span data-stu-id="63556-154">The ParentFolderIds array can only contain a single contact folder identifier.</span></span> <span data-ttu-id="63556-155">Si el elemento **ParentFolderIds** no está presente, se busca en la carpeta de contactos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="63556-155">If the **ParentFolderIds** element is not present, the default Contacts folder is searched.</span></span>  <br/> <span data-ttu-id="63556-156">El identificador de la carpeta se puede usar para el acceso delegado.</span><span class="sxs-lookup"><span data-stu-id="63556-156">The folder identifier can be used for delegate access.</span></span>  <br/> <span data-ttu-id="63556-157">Las búsquedas de Active Directory se realizan mediante listas de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="63556-157">Active Directory searches are performed by using access control lists (ACLs).</span></span> <span data-ttu-id="63556-158">Es posible que algunos usuarios no tengan derechos para ver algunos objetos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63556-158">Some users might not have the rights to see some Active Directory objects.</span></span>  <br/> <span data-ttu-id="63556-159">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="63556-159">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="63556-160">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="63556-160">UnresolvedEntry</span></span>](unresolvedentry.md) <br/> |<span data-ttu-id="63556-161">Contiene el nombre de un contacto o de una lista de distribución que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="63556-161">Contains the name of a contact or distribution list to resolve.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="63556-162">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="63556-162">Parent elements</span></span>

<span data-ttu-id="63556-163">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="63556-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63556-164">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63556-164">Remarks</span></span>

<span data-ttu-id="63556-165">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="63556-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63556-166">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="63556-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63556-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="63556-167">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="63556-168">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="63556-168">Schema name</span></span>  <br/> |<span data-ttu-id="63556-169">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="63556-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="63556-170">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="63556-170">Validation file</span></span>  <br/> |<span data-ttu-id="63556-171">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="63556-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="63556-172">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63556-172">Can be empty</span></span>  <br/> |<span data-ttu-id="63556-173">Falso</span><span class="sxs-lookup"><span data-stu-id="63556-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63556-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="63556-174">See also</span></span>



[<span data-ttu-id="63556-175">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="63556-175">ResolveNames operation</span></span>](resolvenames-operation.md)
  
[<span data-ttu-id="63556-176">ResolveNamesType</span><span class="sxs-lookup"><span data-stu-id="63556-176">ResolveNamesType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[<span data-ttu-id="63556-177">ResolveNamesSearchScopeType</span><span class="sxs-lookup"><span data-stu-id="63556-177">ResolveNamesSearchScopeType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [<span data-ttu-id="63556-178">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="63556-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="63556-179">Uso de la resolución de nombres</span><span class="sxs-lookup"><span data-stu-id="63556-179">Using Name Resolution</span></span>](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)


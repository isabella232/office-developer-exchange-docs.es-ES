---
title: Tratamiento de mensajes de error de detección automática
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e5939ec2-1100-4174-8a88-5a6e09b60b23
description: Obtenga información sobre los diferentes tipos de errores de detección automática y qué hacer con ellos.
ms.openlocfilehash: fcafc799f4d35e92159d2913845474ecf7bc5657
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763014"
---
# <a name="handling-autodiscover-error-messages"></a><span data-ttu-id="734ab-103">Tratamiento de mensajes de error de detección automática</span><span class="sxs-lookup"><span data-stu-id="734ab-103">Handling Autodiscover error messages</span></span>

<span data-ttu-id="734ab-104">Obtenga información sobre los diferentes tipos de errores de detección automática y qué hacer con ellos.</span><span class="sxs-lookup"><span data-stu-id="734ab-104">Learn about the different types of Autodiscover errors and what to do with them.</span></span>
  
<span data-ttu-id="734ab-105">Detección automática permite a las aplicaciones recuperar información de configuración automáticamente y funciona muy bien.</span><span class="sxs-lookup"><span data-stu-id="734ab-105">Autodiscover enables your applications to retrieve configuration information automatically, and it works great.</span></span> <span data-ttu-id="734ab-106">Sin embargo, las cosas no vaya siempre según el plan.</span><span class="sxs-lookup"><span data-stu-id="734ab-106">However, things don't always go according to plan.</span></span> <span data-ttu-id="734ab-107">Vamos a examinar los errores comunes que pueden surgir y cómo se puede controlar a fin de minimizar la necesidad de solicitar el usuario para configurar manualmente su cliente.</span><span class="sxs-lookup"><span data-stu-id="734ab-107">Let's look at the common errors that might occur and how you can handle them to minimize the need to prompt your user to manually configure your client.</span></span>
  
## <a name="http-status-errors"></a><span data-ttu-id="734ab-108">Errores de estado HTTP</span><span class="sxs-lookup"><span data-stu-id="734ab-108">HTTP status errors</span></span>
<span data-ttu-id="734ab-109"><a name="bk_HttpErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="734ab-109"></span></span>

<span data-ttu-id="734ab-110">El primer tipo de error que pueden surgir al enviar solicitudes de detección automática es el estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="734ab-110">The first type of error you might encounter when sending Autodiscover requests is the HTTP status.</span></span> <span data-ttu-id="734ab-111">Si el estado HTTP en la respuesta no es 200 (Aceptar), la carga de respuesta no contiene la respuesta de detección automática que estaba buscando.</span><span class="sxs-lookup"><span data-stu-id="734ab-111">If the HTTP status in your response is anything other than 200 (OK), the response payload doesn't contain the Autodiscover response you were looking for.</span></span> <span data-ttu-id="734ab-112">Por motivos de simplicidad, podemos agrupar los códigos de estado no es 200 en tres categorías.</span><span class="sxs-lookup"><span data-stu-id="734ab-112">For simplicity, we can group non-200 status codes into three categories.</span></span>
  
<span data-ttu-id="734ab-113">**La tabla 1. Códigos de estado HTTP**</span><span class="sxs-lookup"><span data-stu-id="734ab-113">**Table 1. HTTP status codes**</span></span>

|<span data-ttu-id="734ab-114">**Código de estado**</span><span class="sxs-lookup"><span data-stu-id="734ab-114">**Status code**</span></span>|<span data-ttu-id="734ab-115">**Tipo de error**</span><span class="sxs-lookup"><span data-stu-id="734ab-115">**Type of error**</span></span>|<span data-ttu-id="734ab-116">**Para controlar...**</span><span class="sxs-lookup"><span data-stu-id="734ab-116">**To handle…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="734ab-117">301 o 302</span><span class="sxs-lookup"><span data-stu-id="734ab-117">301 or 302</span></span>  <br/> |<span data-ttu-id="734ab-118">Error de redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="734ab-118">Redirect error</span></span>  <br/> |<span data-ttu-id="734ab-119">Volver a enviar la solicitud al URI de contenidos en el encabezado de respuesta HTTP "Location".</span><span class="sxs-lookup"><span data-stu-id="734ab-119">Resend your request to the URI contained in the "Location" HTTP response header.</span></span> <span data-ttu-id="734ab-120">Para obtener información detallada, vea [redirigir de tratamiento de errores](#bk_HandlingRedirects).</span><span class="sxs-lookup"><span data-stu-id="734ab-120">For details, see [Handling redirect errors](#bk_HandlingRedirects).</span></span>  <br/> |
|<span data-ttu-id="734ab-121">401</span><span class="sxs-lookup"><span data-stu-id="734ab-121">401</span></span>  <br/> |<span data-ttu-id="734ab-122">Error no autorizado</span><span class="sxs-lookup"><span data-stu-id="734ab-122">Unauthorized error</span></span>  <br/> |<span data-ttu-id="734ab-123">Debido a que el [proceso de detección automática](autodiscover-for-exchange.md) implica intentar varias direcciones URL posibles, podría obtener esto en una dirección URL sólo tiene siguiente Aceptar sus credenciales.</span><span class="sxs-lookup"><span data-stu-id="734ab-123">Because the [Autodiscover process](autodiscover-for-exchange.md) involves trying multiple potential URLs, you could get this on one URL only to have the next one accept your credentials.</span></span> <span data-ttu-id="734ab-124">Por este motivo, no debería tener en cuenta un error 401 único para indicar que las credenciales no son válidas.</span><span class="sxs-lookup"><span data-stu-id="734ab-124">For this reason, you shouldn't consider a single 401 error to indicate that the credentials are invalid.</span></span> <span data-ttu-id="734ab-125">Sin embargo, si recibe 401 errores de varias direcciones URL, es posible que desee pedir al usuario que vuelva a escribir su contraseña (si es posible).</span><span class="sxs-lookup"><span data-stu-id="734ab-125">However, if you receive 401 errors from multiple URLs, you might want to prompt the user to reenter their password (if possible).</span></span>  <br/> |
|<span data-ttu-id="734ab-126">Cualquier otro estado no es 200</span><span class="sxs-lookup"><span data-stu-id="734ab-126">Any other non-200 status</span></span>  <br/> |<span data-ttu-id="734ab-127">Error de extremo no válido de detección automática</span><span class="sxs-lookup"><span data-stu-id="734ab-127">Invalid Autodiscover endpoint error</span></span>  <br/> |<span data-ttu-id="734ab-128">Tenga en cuenta la dirección URL que devuelve cualquier otro código de estado no es 200 para que no sea válido y continuar intentando la dirección URL siguiente en la lista.</span><span class="sxs-lookup"><span data-stu-id="734ab-128">Consider the URL that returns any other non-200 status code to be invalid, and continue trying the next URL in your list.</span></span>  <br/> |
   
## <a name="autodiscover-errors"></a><span data-ttu-id="734ab-129">Errores de detección automática</span><span class="sxs-lookup"><span data-stu-id="734ab-129">Autodiscover errors</span></span>
<span data-ttu-id="734ab-130"><a name="bk_AutodiscoverErrors"> </a></span><span class="sxs-lookup"><span data-stu-id="734ab-130"></span></span>

<span data-ttu-id="734ab-131">Incluso si recibe un código de estado 200 (Aceptar) después de enviar una solicitud de detección automática, que no significa que el servidor envía la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="734ab-131">Even if you get a 200 (OK) status code after sending an Autodiscover request, that doesn't mean that the server sent the information you need.</span></span> <span data-ttu-id="734ab-132">El estado 200 sólo significa que tiene una respuesta de detección automática, y esa respuesta puede contener un error dentro de la carga.</span><span class="sxs-lookup"><span data-stu-id="734ab-132">The 200 status only means that you have an Autodiscover response, and that response might contain an error within the payload.</span></span> <span data-ttu-id="734ab-133">La ubicación de la información de error difiere dependiendo de si el formato es SOAP o POX.</span><span class="sxs-lookup"><span data-stu-id="734ab-133">The location of the error information differs depending on whether the format is SOAP or POX.</span></span>
  
### <a name="soap-autodiscover-errors"></a><span data-ttu-id="734ab-134">Errores de detección automática SOAP</span><span class="sxs-lookup"><span data-stu-id="734ab-134">SOAP Autodiscover errors</span></span>

<span data-ttu-id="734ab-135">Para la detección automática de SOAP, la respuesta puede contener uno o varios elementos [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) , en distintos lugares.</span><span class="sxs-lookup"><span data-stu-id="734ab-135">For SOAP Autodiscover, the response can contain one or more [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) elements, in different places.</span></span> <span data-ttu-id="734ab-136">Normalmente, puede esperar uno como un elemento secundario del elemento de [Respuesta (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) y otro como elemento secundario de cada elemento [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="734ab-136">Typically you can expect one as a child element of the [Response (SOAP)](http://msdn.microsoft.com/library/4c2bcdeb-95ce-4ffa-bd83-118af53b534f%28Office.15%29.aspx) element, and one as a child of each [UserResponse (SOAP)](http://msdn.microsoft.com/library/5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd%28Office.15%29.aspx) element in the response.</span></span> <span data-ttu-id="734ab-137">También se puede encontrar uno como un elemento secundario de un elemento [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) , si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="734ab-137">You might also encounter one as a child of a [UserSettingError (SOAP)](http://msdn.microsoft.com/library/abb175c5-4f38-4dcc-81e3-b511686862eb%28Office.15%29.aspx) element, if one is present.</span></span> <span data-ttu-id="734ab-138">El contexto del error depende de dónde **ErrorCode** se encuentra el elemento, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="734ab-138">The context of the error depends on where the **ErrorCode** element is located, as follows:</span></span> 
  
- <span data-ttu-id="734ab-139">Como un elemento secundario del elemento de **respuesta** , el elemento **ErrorCode** representa un error que se aplica a toda la petición.</span><span class="sxs-lookup"><span data-stu-id="734ab-139">As a child element of the **Response** element, the **ErrorCode** element represents an error that applies to the entire request.</span></span> 
    
- <span data-ttu-id="734ab-140">Como elemento secundario del elemento **UserResponse** , que representa un error que se aplica sólo a ese usuario específico.</span><span class="sxs-lookup"><span data-stu-id="734ab-140">As a child of the **UserResponse** element, it represents an error that applies just to that specific user.</span></span> 
    
- <span data-ttu-id="734ab-141">Como elemento secundario de un elemento **UserSettingError** , que representa un error que se aplica a una configuración específica que se solicitó.</span><span class="sxs-lookup"><span data-stu-id="734ab-141">As a child of a **UserSettingError** element, it represents an error that applies to a specific setting that was requested.</span></span> 
    
<span data-ttu-id="734ab-142">Vamos a echar un vistazo a un ejemplo de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="734ab-142">Let's take a look at an example of a response.</span></span> <span data-ttu-id="734ab-143">En este ejemplo, el elemento de **código de error** en el elemento de **respuesta** tiene un valor de "NoError", que indica el éxito general.</span><span class="sxs-lookup"><span data-stu-id="734ab-143">In this example, the **ErrorCode** element under the **Response** element has a value of "NoError", which indicates overall success.</span></span> <span data-ttu-id="734ab-144">Sin embargo, el elemento **ErrorCode** bajo el elemento **UserResponse** tiene un valor de "RedirectAddress", que indica que se ha producido un error para ese usuario concreto.</span><span class="sxs-lookup"><span data-stu-id="734ab-144">However, the **ErrorCode** element under the **UserResponse** element has a value of "RedirectAddress", which indicates that an error occurred for that particular user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:a="http://www.w3.org/2005/08/addressing">
  <s:Header>
    <a:Action s:mustUnderstand="1">http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettingsResponse</a:Action>
    <h:ServerVersionInfo xmlns:h="http://schemas.microsoft.com/exchange/2010/Autodiscover" 
        xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
      <h:MajorVersion>14</h:MajorVersion>
      <h:MinorVersion>3</h:MinorVersion>
      <h:MajorBuildNumber>136</h:MajorBuildNumber>
      <h:MinorBuildNumber>1</h:MinorBuildNumber>
      <h:Version>Exchange2010_SP2</h:Version>
    </h:ServerVersionInfo>
  </s:Header>
  <s:Body>
    <GetUserSettingsResponseMessage xmlns="http://schemas.microsoft.com/exchange/2010/Autodiscover">
      <Response xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
        <ErrorCode>NoError</ErrorCode>
        <ErrorMessage />
        <UserResponses>
          <UserResponse>
            <ErrorCode>RedirectAddress</ErrorCode>
            <ErrorMessage>Redirection address.</ErrorMessage>
            <RedirectTarget>elvin@mail.contoso.com</RedirectTarget>
            <UserSettingErrors />
            <UserSettings />
          </UserResponse>
        </UserResponses>
      </Response>
    </GetUserSettingsResponseMessage>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="734ab-145">El artículo [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) contiene una lista completa de posibles errores.</span><span class="sxs-lookup"><span data-stu-id="734ab-145">The [ErrorCode (SOAP)](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx) article contains a full list of possible errors.</span></span> <span data-ttu-id="734ab-146">La mayoría de estos indica un error irrecuperable, pero algunos requieran un tratamiento especial.</span><span class="sxs-lookup"><span data-stu-id="734ab-146">Most of these indicate an unrecoverable error, but a few warrant special handling.</span></span> 
  
<span data-ttu-id="734ab-147">**Tabla 2. Valores de Autodisover ErrorCode SOAP**</span><span class="sxs-lookup"><span data-stu-id="734ab-147">**Table 2. SOAP Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="734ab-148">**Valor de código de error**</span><span class="sxs-lookup"><span data-stu-id="734ab-148">**ErrorCode value**</span></span>|<span data-ttu-id="734ab-149">**Para controlar...**</span><span class="sxs-lookup"><span data-stu-id="734ab-149">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="734ab-150">RedirectAddress</span><span class="sxs-lookup"><span data-stu-id="734ab-150">RedirectAddress</span></span>  <br/> |<span data-ttu-id="734ab-151">[Reinicio de detección automática con una nueva dirección de correo electrónico](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="734ab-151">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectTarget (SOAP)](http://msdn.microsoft.com/library/f8162724-cf9a-4543-a1ad-5846c8b10bfa%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="734ab-152">RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="734ab-152">RedirectUrl</span></span>  <br/> |<span data-ttu-id="734ab-153">[Volver a enviar la solicitud a una nueva dirección URL](#bk_ResendRequest) a la dirección URL en el elemento **RedirectTarget** .</span><span class="sxs-lookup"><span data-stu-id="734ab-153">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the **RedirectTarget** element.</span></span>  <br/> |
|<span data-ttu-id="734ab-154">ServerBusy</span><span class="sxs-lookup"><span data-stu-id="734ab-154">ServerBusy</span></span>  <br/> |<span data-ttu-id="734ab-155">Vuelva a intentar esta dirección URL después de un pequeño retraso.</span><span class="sxs-lookup"><span data-stu-id="734ab-155">Retry this URL after a small delay.</span></span> <span data-ttu-id="734ab-156">Es posible que una cantidad de tiempo de espera o simplemente mover esta dirección URL hasta el final de la lista de direcciones URL para probar.</span><span class="sxs-lookup"><span data-stu-id="734ab-156">You might wait a set amount of time or simply move this URL to the end of your list of URLs to try.</span></span> <span data-ttu-id="734ab-157">Si recibe este error varias veces desde una dirección URL, debe tener en cuenta la dirección URL no es válido.</span><span class="sxs-lookup"><span data-stu-id="734ab-157">If you receive this error multiple times from a URL, you should consider the URL to be invalid.</span></span>  <br/> |
   
### <a name="pox-autodiscover-errors"></a><span data-ttu-id="734ab-158">Errores de detección automática POX</span><span class="sxs-lookup"><span data-stu-id="734ab-158">POX Autodiscover errors</span></span>

<span data-ttu-id="734ab-159">El servicio Detección automática POX informes de errores de forma un poco diferente.</span><span class="sxs-lookup"><span data-stu-id="734ab-159">The POX Autodiscover service reports errors a little differently.</span></span> <span data-ttu-id="734ab-160">Errores no recuperables están contenidos en el elemento de [Error (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="734ab-160">Non-recoverable errors are contained in the [Error (POX)](http://msdn.microsoft.com/library/91c63b62-ab68-4c32-a2f7-5a87c188335b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="734ab-161">El artículo [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) contiene una lista completa de posibles códigos de error.</span><span class="sxs-lookup"><span data-stu-id="734ab-161">The [ErrorCode (POX)](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx) article contains a full list of possible error codes.</span></span> 
  
<span data-ttu-id="734ab-162">Errores de redireccionamiento están contenidos en el elemento de [Acción (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="734ab-162">Redirect errors are contained in the [Action (POX)](http://msdn.microsoft.com/library/a3462c6b-453c-462a-830d-f29ee4a2babb%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="734ab-163">Cualquier valor del elemento de **acción** que no sea "configuración" indica un error de redirección.</span><span class="sxs-lookup"><span data-stu-id="734ab-163">Any value of the **Action** element other than "settings" indicates a redirect error.</span></span> 
  
<span data-ttu-id="734ab-164">**Tabla 3. Valores de Autodisover ErrorCode POX**</span><span class="sxs-lookup"><span data-stu-id="734ab-164">**Table 3. POX Autodisover ErrorCode values**</span></span>

|<span data-ttu-id="734ab-165">**Valor de acción**</span><span class="sxs-lookup"><span data-stu-id="734ab-165">**Action value**</span></span>|<span data-ttu-id="734ab-166">**Para controlar...**</span><span class="sxs-lookup"><span data-stu-id="734ab-166">**To handle…**</span></span>|
|:-----|:-----|
|<span data-ttu-id="734ab-167">redirectAddr</span><span class="sxs-lookup"><span data-stu-id="734ab-167">redirectAddr</span></span>  <br/> |<span data-ttu-id="734ab-168">[Reinicio de detección automática con una nueva dirección de correo electrónico](#bk_RestartAutodiscover) con la dirección de correo electrónico en el elemento [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="734ab-168">[Restarting Autodiscover with a new email address](#bk_RestartAutodiscover) with the email address in the [RedirectAddr (POX)](http://msdn.microsoft.com/library/0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4%28Office.15%29.aspx) element.</span></span>  <br/> |
|<span data-ttu-id="734ab-169">redirectUrl</span><span class="sxs-lookup"><span data-stu-id="734ab-169">redirectUrl</span></span>  <br/> |<span data-ttu-id="734ab-170">[Volver a enviar la solicitud a una nueva dirección URL](#bk_ResendRequest) a la dirección URL en el elemento [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="734ab-170">[Resending your request to a new URL](#bk_ResendRequest) to the URL in the [RedirectUrl (POX)](http://msdn.microsoft.com/library/c54f310f-8c99-4c37-8e73-ac87722b6229%28Office.15%29.aspx) element.</span></span>  <br/> |
   
<span data-ttu-id="734ab-171">En este ejemplo, el elemento de **acción** tiene un valor de "redirectAddr", que indica que se debe enviar una solicitud de nuevo con la nueva dirección de correo electrónico incluida en el elemento **RedirectAddr** .</span><span class="sxs-lookup"><span data-stu-id="734ab-171">In this example, the **Action** element has a value of "redirectAddr", which indicates that a new request should be sent with the new email address contained in the **RedirectAddr** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <Account>
      <Action>redirectAddr</Action>
      <RedirectAddr>elvin@mail.contoso.com</RedirectAddr>
    </Account>
  </Response>
</Autodiscover>
```

## <a name="handling-redirect-errors"></a><span data-ttu-id="734ab-172">Controlar errores de redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="734ab-172">Handling redirect errors</span></span>
<span data-ttu-id="734ab-173"><a name="bk_HandlingRedirects"> </a></span><span class="sxs-lookup"><span data-stu-id="734ab-173"></span></span>

<span data-ttu-id="734ab-174">Puede controlar los escenarios de error de redireccionamiento de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="734ab-174">You can handle redirect error scenarios in two ways:</span></span>
  
- <span data-ttu-id="734ab-175">Reiniciando detección automática con una nueva dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="734ab-175">By restarting Autodiscover with a new email address.</span></span>
    
- <span data-ttu-id="734ab-176">Reenviando la solicitud a una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="734ab-176">By resending your request to a new URL.</span></span>
    
<span data-ttu-id="734ab-177">Ambos escenarios requieren algunos validación antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="734ab-177">Both scenarios require some validation before proceeding.</span></span>
  
### <a name="restarting-autodiscover-with-a-new-email-address"></a><span data-ttu-id="734ab-178">Reinicio de detección automática con una nueva dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="734ab-178">Restarting Autodiscover with a new email address</span></span>
<span data-ttu-id="734ab-179"><a name="bk_RestartAutodiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="734ab-179"></span></span>

<span data-ttu-id="734ab-180">Al obtener una nueva dirección de correo electrónico en una detección automática redirigir respuesta, comprobar que la nueva dirección de correo electrónico que le ha proporcionado en la respuesta de error de redireccionamiento no es la misma dirección que envía en la solicitud que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="734ab-180">When you get a new email address in an Autodiscover redirect response, first verify that the new email address that was provided in the redirect error response is not the same address that you sent in the request that resulted in the error.</span></span> <span data-ttu-id="734ab-181">Si es así, no debe reiniciar la detección automática y en su lugar, tenga en cuenta la dirección URL que generó la respuesta para que no sea válido.</span><span class="sxs-lookup"><span data-stu-id="734ab-181">If it is, you should not restart Autodiscover and instead consider the URL that generated the response to be invalid.</span></span>
  
<span data-ttu-id="734ab-182">Si la nueva dirección de correo electrónico es distinto, descartar la lista existente de posibles direcciones URL de extremo de detección automática y generar una nueva lista en función de la nueva dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="734ab-182">If the new email address is different, discard your existing list of potential Autodiscover endpoint URLs and generate a new list based on the new email address.</span></span>
  
### <a name="resending-your-request-to-a-new-url"></a><span data-ttu-id="734ab-183">Volver a enviar la solicitud a una nueva dirección URL</span><span class="sxs-lookup"><span data-stu-id="734ab-183">Resending your request to a new URL</span></span>
<span data-ttu-id="734ab-184"><a name="bk_ResendRequest"> </a></span><span class="sxs-lookup"><span data-stu-id="734ab-184"></span></span>

<span data-ttu-id="734ab-185">Cuando se obtiene una nueva dirección URL en una respuesta de redirección de detección automática, primero debe validar la dirección URL como sigue:</span><span class="sxs-lookup"><span data-stu-id="734ab-185">When you get a new URL in an Autodiscover redirect response, you should first validate the URL as follows:</span></span>
  
- <span data-ttu-id="734ab-186">Compruebe que la dirección URL es una dirección URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="734ab-186">Verify that the URL is an HTTPS URL.</span></span>
    
- <span data-ttu-id="734ab-187">Compruebe que no ha recibido un error desde esta dirección URL con la dirección de correo electrónico actual antes.</span><span class="sxs-lookup"><span data-stu-id="734ab-187">Verify that you have not received an error from this URL with the current email address before.</span></span>
    
- <span data-ttu-id="734ab-188">Si es aplicable a su aplicación, que informan al usuario de la redirección y obtener sus permisos para seguir la redirección.</span><span class="sxs-lookup"><span data-stu-id="734ab-188">If applicable to your application, inform the user of the redirection and get their permission to follow the redirect.</span></span>
    
- <span data-ttu-id="734ab-189">Enviar una solicitud a la dirección URL y [Compruebe que el certificado SSL presentado por el servidor es válido](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span><span class="sxs-lookup"><span data-stu-id="734ab-189">Send a request to the URL and [verify that the SSL certificate presented by the server is valid](how-to-validate-a-server-certificate-for-the-ews-managed-api.md).</span></span>
    
<span data-ttu-id="734ab-190">Si la dirección URL pasa la validación, volver a enviar la solicitud a esta nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="734ab-190">If the URL passes validation, resend the request to this new URL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="734ab-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="734ab-191">See also</span></span>


- [<span data-ttu-id="734ab-192">Detección automática de Exchange</span><span class="sxs-lookup"><span data-stu-id="734ab-192">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="734ab-193">Busque los extremos de detección automática mediante el uso de búsqueda de SCP en Exchange</span><span class="sxs-lookup"><span data-stu-id="734ab-193">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="734ab-194">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="734ab-194">ErrorCode (SOAP)</span></span>](http://msdn.microsoft.com/library/5e5ec861-0191-4ecb-a906-47ce8ed96381%28Office.15%29.aspx)
    
- [<span data-ttu-id="734ab-195">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="734ab-195">ErrorCode (POX)</span></span>](http://msdn.microsoft.com/library/064d73e4-45b7-4797-828e-9df590830db8%28Office.15%29.aspx)
    


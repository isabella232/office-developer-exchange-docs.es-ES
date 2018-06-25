---
title: Busque los extremos de detección automática mediante el uso de búsqueda de SCP en Exchange
manager: kelbow
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b24228a8-5127-4bac-aef0-9c9e8843c9ff
description: Descubra cómo ubicar objetos SCP de detección automática en los servicios de dominio de Active Directory (AD DS) y usarlos para buscar direcciones URL de extremo de detección automática para usar con el servicio de detección automática de Exchange.
ms.openlocfilehash: 59fd316d0aa0feea81b60c279040da018c51b47d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763059"
---
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a>Busque los extremos de detección automática mediante el uso de búsqueda de SCP en Exchange

Descubra cómo ubicar objetos SCP de detección automática en los servicios de dominio de Active Directory (AD DS) y usarlos para buscar direcciones URL de extremo de detección automática para usar con el servicio de detección automática de Exchange.
  
Detección automática facilita recuperar la información que necesita para conectarse a los buzones de correo en los servidores de Exchange. Sin embargo, para poder usar la detección automática, se necesita una forma para buscar servidores de detección automática que son adecuados para el usuario que está recuperando la configuración para. Objetos de punto (SCP) de conexión de servicio en AD DS proporcionan una manera fácil para los clientes Unidos a un dominio buscar servidores de detección automática. 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a>Configurar la aplicación para buscar los extremos de detección automática
<a name="bk_PreReqs"> </a>

Para localizar objetos SCP de detección automática en AD DS, necesita tener acceso a lo siguiente:
  
- Un servidor que está ejecutando una versión de Exchange local iniciando con Exchange 2007 SP1.
    
- Un equipo cliente que se ha unido al dominio que se instala el servidor de Exchange en.
    
- Una cuenta de usuario que tenga un buzón en el servidor de Exchange. 
    
Además, antes de empezar, deberá estar familiarizado algunos conceptos básicos. Los siguientes son algunos recursos que le resultarán útiles.
  
**La tabla 1. Artículos relacionados de la búsqueda de los extremos de detección automática de objetos SCP**

|**Lea este artículo**|**Para obtener más información acerca de...**|
|:-----|:-----|
|[Detección automática de Exchange](autodiscover-for-exchange.md) <br/> |Cómo funciona el servicio Detección automática.  <br/> |
|[Publicación con puntos de conexión de servicio](http://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |Cómo se usan los objetos SCP para publicar datos específicos de servicio.  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a>Busque objetos SCP de detección automática en AD DS
<a name="bk_LocateScpObjects"> </a>

Es el primer paso para buscar los extremos de detección automática que se publican en AD DS localizar los objetos SCP de detección automática. Exchange publica dos tipos de objetos SCP para la detección automática:
  
- **Punteros de SCP** : contienen información que señala a servidores LDAP específicos que se deben usar para localizar objetos SCP de detección automática para el dominio del usuario. Punteros de SCP están marcados con el siguiente GUID: 67661d7F - 8FC 4-4fa7-BFAC-E1D7794C1F68. 
    
- **Direcciones URL de la SCP** : estos contienen direcciones URL de los extremos de detección automática. Direcciones URL de la SCP están marcadas con el siguiente GUID: 77378F46-2 66 C-4aa9-A6A6-3E7A48B19596. 
    
### <a name="to-locate-autodiscover-scp-objects"></a>Para buscar objetos SCP de detección automática

1. Leer la propiedad **configurationNamingContext** de la entrada DSE en AD DS para obtener la ruta de acceso para el contexto de nomenclatura de configuración para el dominio raíz. Puede hacerlo mediante el uso de la clase [DirectoryEntry](http://msdn2.microsoft.com/EN-US/library/z9cddzaa) , o cualquier otra API que puede obtener acceso a AD DS. 
    
2. Para buscar objetos SCP en el contexto de nomenclatura de configuración que tienen ya sea la SCP puntero GUID o el GUID de la dirección URL de SCP en la propiedad **keywords** . 
    
3. Compruebe que se ha encontrado un puntero de SCP que tiene como ámbito el dominio del usuario mediante la comprobación de la propiedad **palabras clave** para una entrada igual a los objetos de la SCP `"Domain=<domain>"`. Por ejemplo, si la dirección de correo electrónico del usuario es elvin@contoso.com, debe buscar un puntero SCP con una entrada en la propiedad de **las palabras clave** que es igual a `"Domain=contoso.com"`. Si se encuentra un puntero SCP coincidente, descartar el conjunto de objetos SCP y empezar de nuevo en el paso 1 con el valor de la propiedad **serviceBindingInformation** como el servidor para conectarse a la entrada de DSE raíz. 
    
4. Si no encuentra ningún punteros SCP en el ámbito el dominio del usuario, buscando cualquier punteros de SCP que no son el ámbito de cualquier dominio y guarda el valor de la propiedad **serviceBindingInformation** como un servidor de "reserva", en caso de que el servidor actual no obtendrá ninguna resultados. 
    
5. Si no encuentra ningún punteros SCP en el ámbito del dominio, estará listo pasar a la siguiente paso: generación de una lista de prioridades de los extremos de detección automática de los resultados.
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a>Generar una lista de prioridades de los extremos de detección automática
<a name="bk_GenerateList"> </a>

Puede generar una lista de prioridades de direcciones URL de extremo de detección automática, con el conjunto de objetos SCP que encuentra, haciendo lo siguiente:
  
1. Obtenga el nombre del sitio de Active Directory del equipo cliente.
    
2. Compruebe la propiedad **palabras clave** en cada dirección URL de SCP en el conjunto de objetos SCP encontró y asignar una prioridad a la dirección URL en función de las siguientes reglas: 
    
  - Si la propiedad **palabras clave** contiene un valor de `"Site=<site name>"`, donde `<site name>` es igual a sitio el nombre de Active Directory recuperado en el paso anterior, asigne la dirección URL de una prioridad de 1. 
    
  - Si la propiedad **palabras clave** no contiene una entrada con un valor que comienza por `"Site="`, asigne una prioridad de 2 de la dirección URL. 
    
  - Si la propiedad **palabras clave** contiene un valor de `"Site=<site name>`, donde `<site name>` no ser igual al nombre del sitio de Active Directory que ha recuperado en el paso anterior, asigne una prioridad de 3 de la dirección URL. 
    
## <a name="code-example-performing-an-scp-lookup"></a>Ejemplo de código: realiza una búsqueda de SCP
<a name="bk_CodeExample"> </a>

En el siguiente ejemplo de código, verá cómo ubicar objetos SCP de detección automática y generar una lista de prioridades de los extremos de detección automática.
  
```cs
using System;
using System.Collections.Generic;
using System.DirectoryServices;
using System.DirectoryServices.ActiveDirectory;
namespace ScpLookup
{
    // This sample is for demonstration purposes only. Before you run this sample, make sure 
    // that the code meets the coding requirements of your organization. 
    class Program
    {
        static void Main(string[] args)
        {
            string domain = args[0];
            Console.WriteLine("Performing SCP lookup for {0}.", domain);
            List<string> scpUrls = GetScpUrls(null, domain);
            Console.WriteLine("\nOrdered List of Autodiscover endpoints:");
            foreach (string url in scpUrls)
            {
                Console.WriteLine("  {0}", url);
            }
            Console.WriteLine("SCP lookup done.");
        }
        // GUID for SCP URL keyword.
        private const string ScpUrlGuidString = @"77378F46-2C66-4aa9-A6A6-3E7A48B19596";
        // GUID for SCP pointer keyword.
        private const string ScpPtrGuidString = @"67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68";
        static List<string> GetScpUrls(string ldapServer, string domain)
        {
            // Create a new list to return.
            List<string> scpUrlList = new List<string>();
            string rootDSEPath = null;
            // If ldapServer is null/empty, use LDAP://RootDSE to
            // connect to Active Directory Domain Services (AD DS). Otherwise, use
            // LDAP://SERVERNAME/RootDSE to connect to a specific server.
            if (string.IsNullOrEmpty(ldapServer))
            {
                rootDSEPath = "LDAP://RootDSE";
            }
            else
            {
                rootDSEPath = ldapServer + "/RootDSE";
            }
            SearchResultCollection scpEntries = null;
            try
            {
                // Get the root directory entry.
                DirectoryEntry rootDSE = new DirectoryEntry(rootDSEPath);
                // Get the configuration path.
                string configPath = rootDSE.Properties["configurationNamingContext"].Value as string;
                // Get the configuration entry.
                DirectoryEntry configEntry = new DirectoryEntry("LDAP://" + configPath);
                // Create a search object for the configuration entry.
                DirectorySearcher configSearch = new DirectorySearcher(configEntry);
                // Set the search filter to find SCP URLs and SCP pointers.
                configSearch.Filter = "(&amp;(objectClass=serviceConnectionPoint)" +
                    "(|(keywords=" + ScpPtrGuidString + ")(keywords=" + ScpUrlGuidString + ")))";
                // Specify which properties you want to retrieve.
                configSearch.PropertiesToLoad.Add("keywords");
                configSearch.PropertiesToLoad.Add("serviceBindingInformation");
                scpEntries = configSearch.FindAll();
            }
            catch (Exception ex)
            {
                Console.WriteLine("SCP lookup failed with: ");
                Console.WriteLine(ex.ToString());
            }
            // If no SCP entries were found, then exit.
            if (scpEntries == null || scpEntries.Count <= 0)
            {
                Console.WriteLine("No SCP records found.");
                return null;
            }
            string fallBackLdapPath = null;
            // Check for SCP pointers.
            foreach (SearchResult scpEntry in scpEntries)
            {
                ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                if (CollectionContainsExactValue(entryKeywords, ScpPtrGuidString))
                {
                    string ptrLdapPath = scpEntry.Properties["serviceBindingInformation"][0] as string;
                    // Determine whether this pointer is scoped to the user's domain.
                    if (CollectionContainsExactValue(entryKeywords, "Domain=" + domain))
                    {
                        Console.WriteLine("Found SCP pointer for " + domain + " in " + scpEntry.Path);
                        // Restart SCP lookup with the server assigned for the domain.
                        Console.WriteLine("Restarting SCP lookup in " + ptrLdapPath);
                        return GetScpUrls(ptrLdapPath, domain);
                    }
                    else
                    {
                        // Save the first SCP pointer that is not scoped to a domain as a fallback
                        // in case you do not get any results from this server.
                        if (entryKeywords.Count == 1 &amp;&amp; string.IsNullOrEmpty(fallBackLdapPath))
                        {
                            fallBackLdapPath = ptrLdapPath;
                            Console.WriteLine("Saved fallback SCP pointer: " + fallBackLdapPath);
                        }
                    }
                }
            }
            string computerSiteName = null;
            try
            {
                // Get the name of the ActiveDirectorySite the computer
                // belongs to (if it belongs to one).
                ActiveDirectorySite site = ActiveDirectorySite.GetComputerSite();
                computerSiteName = site.Name;
                Console.WriteLine("Local computer in site: " + computerSiteName);
            }
            catch (Exception ex)
            {
                Console.WriteLine("Unable to get computer site name.");
                Console.WriteLine(ex.ToString());
            }
            if (!string.IsNullOrEmpty(computerSiteName))
            {
                // Scan the search results for SCP URLs.
                // SCP URLs fit into three tiers:
                //   Priority 1: The URL is scoped to the computer's Active Directory site.
                //   Priority 2: The URL is not scoped to any Active Directory site.
                //   Priority 3: The URL is scoped to a different Active Directory site.
                // Temporary lists to hold priority 2 and 3 URLs.
                List<string> priorityTwoUrls = new List<string>();
                List<string> priorityThreeUrls = new List<string>();
                foreach (SearchResult scpEntry in scpEntries)
                {
                    ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                    // Check for SCP URLs.
                    if (CollectionContainsExactValue(entryKeywords, ScpUrlGuidString))
                    {
                        string scpUrlPath = scpEntry.Properties["adsPath"][0] as string;
                        Console.WriteLine("SCP URL found at {0}", scpUrlPath);
                        string scpUrl = scpEntry.Properties["serviceBindingInformation"][0] as string;
                        scpUrl = scpUrl.ToLower();
                        // Determine whether this entry is scoped to the computer's site.
                        if (CollectionContainsExactValue(entryKeywords, "Site=" + computerSiteName))
                        {
                            // Priority 1.
                            if (!scpUrlList.Contains(scpUrl.ToLower()))
                            {
                                Console.WriteLine("Adding priority 1 SCP URL: {0}", scpUrl.ToLower());
                                scpUrlList.Add(scpUrl);
                            }
                            else
                            {
                                Console.WriteLine("Priority 1 SCP URL already found: {0}", scpUrl);
                            }
                        }
                        else
                        {
                            // Determine whether this is a priority 2 or 3 URL.
                            if (CollectionContainsPrefixValue(entryKeywords, "Site="))
                            {
                                // Priority 3.
                                if (!priorityThreeUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 3 SCP URL: {0}", scpUrl);
                                    priorityThreeUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 3 SCP URL already found: {0}", scpUrl);
                                }
                            }
                            else
                            {
                                // Priority 2.
                                if (!priorityTwoUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 2 SCP URL: {0}", scpUrl);
                                    priorityTwoUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 2 SCP URL already found: {0}", scpUrl);
                                }
                            }
                        }
                    }
                }
                // Now add the priority 2 URLs into the main list.
                foreach (string priorityTwoUrl in priorityTwoUrls)
                {
                    // If the URL is already in the list as a priority 1, 
                    // don't add it again.
                    if (!scpUrlList.Contains(priorityTwoUrl))
                    {
                        scpUrlList.Add(priorityTwoUrl);
                    }
                }
                // Now add the priority 3 URLs into the main list.
                foreach (string priorityThreeUrl in priorityThreeUrls)
                {
                    // If the URL is already in the list as a priority 1
                    // or priority 2, don't add it again.
                    if (!scpUrlList.Contains(priorityThreeUrl))
                    {
                        scpUrlList.Add(priorityThreeUrl);
                    }
                }
                // If after all this, you still have no URLs in your list,
                // try the fallback SCP pointer, if you have one.
                if (scpUrlList.Count == 0 &amp;&amp; fallBackLdapPath != null)
                {
                    return GetScpUrls(fallBackLdapPath, domain);
                }
            }
            return scpUrlList;
        }
        private static bool CollectionContainsExactValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (string.Compare(value, entry, true) == 0)
                        return true;
                }
            }
            return false;
        }
        private static bool CollectionContainsPrefixValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (entry.StartsWith(value))
                        return true;
                }
            }
            return false;
        }
    }
}
```

## <a name="next-steps"></a>Siguientes pasos
<a name="bk_NextSteps"> </a>

El siguiente paso en el proceso de detección automática es enviar solicitudes de detección automática para las direcciones URL que encuentran, comenzando con direcciones URL de prioridad 1, a continuación, las direcciones URL de prioridad 2 y por último direcciones URL de prioridad 3. Para obtener más información acerca de cómo enviar solicitudes de detección automática y controlar las respuestas, lea los siguientes artículos:
  
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a>Vea también

- [Detección automática de Exchange](autodiscover-for-exchange.md)   
- [Configurar una aplicación de EWS](setting-up-your-ews-application.md)
    


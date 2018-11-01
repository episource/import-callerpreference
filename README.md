# About
Import preference variables from the caller of a powershell module script. This was inspired by [The Scripting Guys](https://blogs.technet.microsoft.com/heyscriptingguy/2014/04/26/weekend-scripter-access-powershell-preference-variables/). [Their blog](https://blogs.technet.microsoft.com/heyscriptingguy/2014/04/26/weekend-scripter-access-powershell-preference-variables/) also provides a good overview of the topic and its background.

# Quickstart
At the beginning of your powershell module script function invoke `Import-CallerPreference`:

```posh
Import-Module import-callerpreference
# …
function Receive-PreferencesExample {
    [CmdletBinding()]
    Param()
    
    Import-CallerPreference
    # …
}
```

# In-Depth
`Import-CallerPreference` copies the following proference variables from the caller's scope into the current scope:
 - ConfirmPreference             
 - DebugPreference               
 - ErrorActionPreference         
 - ErrorView                     
 - FormatEnumerationLimit        
 - InformationPreference         
 - LogCommandHealthEvent         
 - LogCommandLifecycleEvent      
 - LogEngineHealthEvent          
 - LogEngineLifecycleEvent       
 - LogProviderLifecycleEvent     
 - LogProviderHealthEvent                 
 - OFS                           
 - OutputEncoding                
 - ProgressPreference            
 - PSDefaultParameterValues      
 - PSEmailServer                 
 - PSModuleAutoLoadingPreference 
 - PSSessionApplicationName      
 - PSSessionConfigurationName    
 - PSSessionOption               
 - VerbosePreference             
 - WarningPreference             
 - WhatIfPreference    
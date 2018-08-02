<!-- Configure Open Microsoft Edge With-->

>*Supported versions: Microsoft Edge on Windows 10, next major update to Windows*<br> 
>*Default setting:  Enabled (A specific page or pages)*

[!INCLUDE [configure-open-microsoft-edge-with-shortdesc](../shortdesc/configure-open-microsoft-edge-with-shortdesc.md)]

**Version 1703 or later:**<br>If you don't want to send traffic to Microsoft, use the \<about:blank\> value, which honors both domain and non domain-joined devices when it's the only configured URL.

**Version 1810:**<br>When you enable this policy (Configure Open Microsoft Edge With) and select an option, and also enable the Configure Start Pages policy, Microsoft Edge ignores the Configure Start Page policy.<p>

### Supported values

|Group Policy  |MDM |Registry |Description |
|---|:---:|:---:|---|
|Not configured |Blank |Blank |If you don't configure this policy and you enable the Disable Lockdown of Start Pages policy, users can change or customize the Start page. |
|Enabled |0 |0 |Loads the Start page. |
|Enabled |1 |1 |Load the New tab page. |
|Enabled |2 |2 |Load the previous pages. |
|Enabled<br>**(default)** |3 |3 |Load a specific page or pages. |
---

### Configuration options

For more details about configuring the Start pages, see [Start pages configuration options](../group-policies/start-pages-gp.md).


>[!TIP]
>If you want to make changes to this policy:<ol><li>Set the **Disabled Lockdown of Start Pages** policy to not configured.</li><li>Make changes to the **Configure Open Microsoft With** policy.</li><li>Enable the **Disabled Lockdown of Start Pages** policy.</li></ol>



### ADMX info and settings
#### ADMX info
- **GP English name:** Configure Open Microsoft Edge With
- **GP name:** ConfigureOpenMicrosoftEdgeWith
- **GP path:** Windows Components/Microsoft Edge
- **GP ADMX file name:** MicrosoftEdge.admx

#### MDM settings
- **MDM name:** Browser/[ConfigureOpenEdgeWith](https://docs.microsoft.com/en-us/windows/client-management/mdm/policy-csp-browser#browser-configureopenmicrosoftedgewith)
- **Supported devices:** Desktop
- **URI full path:** ./Vendor/MSFT/Policy/Config/Browser/ConfigureOpenEdgeWith
- **Data type:** Integer

#### Registry settings
- **Path:** HLKM\Software\Policies\Microsoft\MicrosoftEdge\Internet Settings
- **Value name:** ConfigureOpenEdgeWith
- **Value type:** REG_DWORD

### Related policies

- [Configure Start pages](../available-policies.md#configure-start-pages): [!INCLUDE [configure-start-pages-shortdesc](../shortdesc/configure-start-pages-shortdesc.md)]

- [Disable lockdown of Start pages](../available-policies.md#disable-lockdown-of-start-pages): [!INCLUDE [disable-lockdown-of-start-pages-shortdesc](../shortdesc/disable-lockdown-of-start-pages-shortdesc.md)]





---
# Legal
**THERE IS NO WARRANTY OF ANY TYPE PROVIDED, EXPRESS, STATED, IMPLIED, OR OTHERWISE. THERE IS NO SAFETY GUARANTEE PROVIDED OF ANY KIND.** 

The provided descriptions and grade are for educational reference only, not a guarantee. There is no affiliation with the programs or developers of such programs by the author of the repository. The author of this repository shall not be held liable for any damages that come with the misuse or general use of any program on this list, nor held liable or responsible for any damages that come from the use of these security grades, descriptions, or audits. Nothing in this repository should be blindly trusted; your own independent research and verification should be conducted. The latest version of this document shall always supersede the previous versions. By viewing, scraping, or using, or accessing this readme file, the audits, the repository, or any other document listed in the repository, you submit consent to be bound by this legal disclaimer and agree to not hold the author liable for any damages related to these programs.

# Description
Agentic source-code security audits focused on auditing the security of certain projects/programs. The audit is done agentically with 6.1 Sol and 6.0 Astra from original source code, looking for server calls, ad-embedding, spyware and adware, credential security, and other potential security and privacy vulnerabilities. 

_**Disclaimer:** The audits are on the source code of each project itself, and only for the specified version, not on installers. I always recommend building the program yourself to avoid adware and spyware._

## Covered Programs
#### Grades
![Safe](https://img.shields.io/badge/SAFE-4ddf98?style=flat)
![Medium](https://img.shields.io/badge/MEDIUM-d26d00?style=flat)
![Issues](https://img.shields.io/badge/ISSUES-a93731?style=flat)

### Cheat Engine 7.5 ![Medium](https://img.shields.io/badge/MEDIUM-d26d00?style=flat) 
The reviewed source includes embedded ad support and an April Fools purchase handler that downloads and executes server-provided Lua without a separate script permission prompt. Ads can be enabled by scripts or generated trainers; the purchase handler requires a button click during the April Fools feature. CE Share adds network requests and approved identifier scripts that can run again on later queries. No covert credential theft or unrelated background uploads were found in the reviewed paths. 

_The remote Lua execution and advertising features support a **medium** rating; included precompiled DLLs and runtime traffic were not verified._

### DepotDownloader 3.4.0 ![Medium](https://img.shields.io/badge/MEDIUM-d26d00?style=flat)
The source archive matches the official release tag, and the reviewed application contains no ads, bundled offers, or separate telemetry endpoint. Its main concern is credential handling: returned Steam refresh tokens are saved in compressed storage without application-level encryption, even when the remember-password option is absent. Whether Steam returns a usable token for a nonpersistent session was not established. Passwords entered as command-line arguments can also appear in shell history and process information. 

_These credential risks support a **medium** rating; dependency internals and runtime authentication traffic were outside the review._


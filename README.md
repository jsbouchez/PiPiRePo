<br/>
<br/>
<p align="center">
  <img src="./assets/logo-header.svg" alt="RHELKB" width="30%">
</p>
<h1 align="center" font-size="3em">Red Hat Enterprise Linux Knowledge Base</h1>
<h3 align="center">(a.k.a. RHELKB)</h3>
<p align="center">
  Documentation for the adoption of Red Hat Enterprise Linux technologies.
  <br/><strong>(ASA-DTI-GSI-SA/rhel)</strong>
</p>
<br/>
<br/>

---

# Contents

## 00. Architecture

- [Approach][link-00-00]

[link-00-00]: ./00_architecture/README.md

## 10. Red Hat Enterprise Linux

- [Overview][link-10-00]
- [Installation Guide][link-10-01]
    - [Steps][link-10-01-99-steps]
- [Post Installation Guide][link-10-02]
    - [Docker][link-10-02-99-docker]
    - [Keys][link-10-02-99-keys]
    - [Security][link-10-02-99-security]
    - [Storage][link-10-02-99-storage] 
- [Kickstart][link-10-99-ks]
- [Red Hat Package Manager][link-10-99-rpm]

[link-10-00]: ./10_00_rhel/README.md
[link-10-01]: ./10_01_rhel_installation/README.md
[link-10-01-99-steps]: ./10_01_rhel_installation/99_steps.md
[link-10-02]: ./10_02_rhel_post_installation/README.md
[link-10-02-99-docker]: ./10_02_rhel_post_installation/99_docker.md
[link-10-02-99-keys]: ./10_02_rhel_post_installation/99_keys.md
[link-10-02-99-security]: ./10_02_rhel_post_installation/99_security.md
[link-10-02-99-storage]: ./10_02_rhel_post_installation/99_storage.md
[link-10-99-ks]: ./10_99_kickstart/README.md
[link-10-99-rpm]: ./10_99_rpm/README.md

## 20. Satellite

- [Overview][link-20-00]
    - [v6.14][link-20-00-v614] \*
    - [v6.13][link-20-00-v613]
- [Installation Guide][link-20-01]

[link-20-00]: ./20_00_satellite/README_6_14.md
[link-20-00-v614]: ./20_00_satellite/README_6_14.md
[link-20-00-v613]: ./20_00_satellite/README_6_13.md
[link-20-01]: ./20_01_satellite_installation/README.md

## 21. OpenShift Container Platform

- Overview
- [Installation Guide][link-40-01]
    - [Advanced Cluster Management][link-40-01-acm]
    - Advanced Security Management
    - OpenShift Data Foundation
    - Keycloak (Single Sign-On) 
    - Veeam
- Examples
    - [CSI driver for SAMBA and CIFS][link-40-99-csi-smb] 	

[link-40-01]: ./40_01_openshift_install/README.md
[link-40-01-acm]: ./40_01_openshift_install/advanced-cluster-management/README.md
[link-40-99-csi-smb]: ./40_99_openshift_examples/csi-cifs/README.md

## 22. Ansible Automation Platform

- Overview
- Installation Guide

## 99. Binnacles

- TBD

## General Approach

- [Life Cycle Environments](#Life-Cycle-Environments)
    - [Tagging](#Tagging)
- [Issue Workflow](#Issue-Workflow)
- [Hostname Definition](#Hostname-Definition)
- [Business Units](#Business-Units)
    - [Area](#area)
    - [Platform](#platform)

---

# Life Cycle Environments

![](./assets/rhel-assets-life-cycle-environments.svg)

**Life cycle environments** are <ins>linked</ins> to form an <ins>environment</ins> <ins>path</ins>. You can promote content along the environment path to the next life cycle environment when required.

## Tagging

|  #   | Full Name                          | Definition                           |  ISO#1  |   ISO#2   |    ISO#3     |   Range    |
| :--: | :--------------------------------- | ------------------------------------ | :-----: | :-------: | :----------: | :--------: |
|      | **-- Ambientes Altos (`high`) --** |                                      |         |           |              |            |
|  1   | Production                         | `PRoDuction`                         |   `P`   |   `PR`    |    `PRD`     | `00`..`09` |
|  2   | Pre-Production                     | `Pre-PRoduction`                     |   `R`   |   `PP`    |    `PPR`     | `10`..`19` |
|  3   | Hotfix                             | `HoTFix`                             |   `H`   |   `HT`    |    `HTF`     | `20`..`29` |
|      | **-- Ambientes Bajos (`low`) --**  |                                      |         |           |              |            |
|  4   | Quality                            | `QuaLiTy`, `User Acceptance Testing` | `Q`,`U` | `QL`,`UT` | `QLT`, `UAT` | `30`..`39` |
|  5   | Testing                            | `TeSTing`                            |   `T`   |   `TS`    |    `TST`     | `40`..`49` |
|  6   | Development                        | `DeVeLopment`                        |   `D`   |   `DV`    |    `DVL`     | `50`..`59` |
|  7   | Laboratory                         | `LaBoRatory`                         |   `L`   |   `LB`    |    `LBR`     | `90`..`99` |

> The zero range (00, 10, 20, ..., 90) is reserved for load balancers.

---

# Issue Workflow

![](./assets/rhel-assets-workflow.svg)

---

# Hostname Definition

- **LOWERCASE** characters must always be used for any identifier.

    - *[kebab-case][kebab-case] style are allowed.*
    - *[CamelCase][camel-case] style is not allowed.*
    - *[snake_case][snake-case] style is not allowed.*

- Names can <ins>only</ins> contain <ins>letters</ins> "`a-z`", <ins>numbers</ins> "`0-9`" and <ins>hyphens</ins> "`-`".

- Names must <ins>begin</ins> with a <ins>letter</ins> "`a-z`".

- <ins>Long</ins> names must be <ins>abbreviated</ins> by <ins>initials</ins> or <ins>acronyms</ins>.

    - (Red Hat Enterprise Linux) `rhel`
    - (Red Hat OpenShift Container Platform Plus) `rh-ocp-p` or `rh-ocpp` or `ocp`
    - (Red Hat Satellite) `rh-sat` or `rh-satellite`

- The <ins>maximum</ins> number of <ins>characters</ins> <ins>supported</ins> is **20**.

- Must **NOT** contain:

    - Blank spaces "` `"
    - Symbols "`!@#$%^&`...”
    - Consecutive  underscore "`__`”
    - Consecutive hyphen "`--`”
    - Prepositions and article "`ante, bajo, el, la`..."
    - Stressed vowels and/or consonants "`áéíöüýñ`...”
    - Uppercase characters "`ABC.Ñ.XYZ`"

## Examples

- **GSN, GIS, Estado de Servicio, Production**

    - `gsn-gis-es-00` Load Balancer
    - `gsn-gis-es-01` Worker #01
    - `gsn-gis-es-02` Worker #02

- **GSN, GIS, Containers, Production**

    - `gsn-gis-oci-01`

- **GSN, Containers, Development**

    - `gsn-oci-51`

- **GSU, AT, SAR APP, Development**

    - `gsu-at-sarapp-51` (better)
    - `gsu-sarapp-51`

- **GSU, AT, SAR DB, Development**

    - `gsu-at-sardb-51` (better)
    - `gsu-sardb-51`

[kebab-case]: https://www.theserverside.com/definition/Kebab-case
[snake-case]: https://www.theserverside.com/definition/Sanke-case
[camel-case]: https://www.techtarget.com/whatis/definition/CamelCase

---

# Business Units

## Area

| Area                                           | Depends | ISO  |   Prefix   |
| :--------------------------------------------- | :-----: | :--: | :--------: |
| **Dirección de Tecnologías de la Información** |    -    | DTI  |            |
| **Gerencia de Ciber Seguridad**                |   DTI   | GCS  |            |
| **Gerencia de Servicios Informáticos**         |   DTI   | GSI  |            |
| - Infraestructura Tecnologica                  |   GSI   |  IT  | `gsi-it-`  |
| - Soporte Aplicativos                          |   GSI   |  SA  | `gsi-sa-`  |
| **Gerencia de Sistemas Administrativos**       |   DTI   | GSA  |            |
| - Administración                               |   GSA   | ADM  | `gsa-adm-` |
| **Gerencia de Sistemas de Negocio**            |   DTI   | GSN  |            |
| - Business Intelligence                        |   GSN   |  BI  | `gsn-bi-`  |
| - Calidad                                      |   GSN   | CAL  | `gsn-cal-` |
| - Geographical Information System              |   GSN   | GIS  | `gsn-gis`  |
| **Gerencia de Sistemas de Usuario**            |   DTI   | GSU  |            |
| - Aplicaciones Técnicas                        |   GSU   |  AT  | `gsu-at-`  |
| - Servicio Web                                 |   GSU   |  SW  | `gsu-sw-`  |

## Platform

| Platform                           | Depends | ISO  |    Prefix     |
| :--------------------------------- | :-----: | :--: | :-----------: |
| **Bastion**                        |    -    | BST  |   `sa-bst-`   |
| **Red Hat Satellite**              |    -    | SAT  |   `sa-sat-`   |
| **Red Hat Satellite Capsule**      |   SAT   | CAP  |   `sa-cap-`   |
| **OpenShift Container Platform**   |    -    | OCP  |   `sa-ocp-`   |
| **Ansible Automation Platform**    |    -    | AAP  |   `sa-aap-`   |
| **Identity Management Platform**   |    -    | IDM  |   `sa-idm-`   |
| **Identity and Access Management** |    -    | IAM  |   `sa-iam-`   |
| **Keycloak**                       |    -    | KCK  |   `sa-kck-`   |

---

# :warning: Important

Please read the established [conventions][conventions] carefully before you start documenting.

[conventions]: ./99_conventions.md

---

<p align="center">
  <span font-size=".8em">
    (c) ASA-DTI-GSI-SA, Buenos Aires, Argentina
    <br/>
    <a href="https://www.aysa.com.ar">www.aysa.com.ar</a> | <a href="mailto:soporte_aplicativos@aysa.com.ar">soporte_aplicativos@aysa.com.ar</a>
  </span>
  <br/><br/>
  <a href="https://www.aysa.com.ar">
    <img src="./assets/logo-footer.png" alt="AySA S.A." height="64px">
  </a>
</p>

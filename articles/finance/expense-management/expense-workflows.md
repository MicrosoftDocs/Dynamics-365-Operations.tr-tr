---
title: Gider yönetimi için iş akışları ayarlama
description: Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154006"
---
# <a name="set-up-workflows-for-expense-management"></a>Gider yönetimi için iş akışları ayarlama

[!include [banner](../includes/banner.md)]

Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz. iş akışlarının tanımlandığı belgeler gider raporları, seyahat talepleri ve nakit avans taleplerini içerebilir.

İş akışı, bir iş sürecini temsil eder. Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar. İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:

-   **Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz. İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.

-   Süreç görünürlüğü — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz. Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.

-   Merkezi çalışma listesi — Kullanıcılar, iş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir. 

**Oluşturabileceğiniz iş akışı türleri**

Aşağıdaki tablo **Gider** içerisinde oluşturabileceğiniz iş akışı türlerini listeler.


|              <strong>Tip</strong>              |                   <strong>Bu türü aşağıdakileri gerçekleştirmek için kullanın:</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Gider raporu</strong>         |            Gider raporları için onay iş akışları oluşturun.             |
|  <strong>Gider raporu otomatik olarak deftere nakletme</strong>   |        Gider raporları için belge otomatik deftere nakil iş akışları oluşturun.        |
|       <strong>Gider satırı öğesi</strong>        |     Gider raporları üzerinde satır maddeleri için onay iş akışları oluşturun.      |
| <strong>Gider satırı öğesi otomatik olarak deftere nakletme</strong> | Gider raporları üzerinde satır maddeleri için otomatik deftere nakil iş akışları oluşturun. |
|       <strong>Seyahat talebi</strong>       |          Seyahat talepleri için onay iş akışları oluşturun.           |
|      <strong>Nakit avans isteği</strong>      |         Nakit avans talepleri için onay iş akışları oluşturun.          |
|        <strong>KDV vergisinden düşme</strong>        | Katma değer vergisi (KDV) düşürme için onay iş akışları oluşturun.  |


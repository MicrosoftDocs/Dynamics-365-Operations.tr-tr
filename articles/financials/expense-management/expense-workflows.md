---
title: "Gider için iş akışlarını ayarla"
description: "Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a>Gider için iş akışlarını ayarla

[!include[banner](../includes/banner.md)] Seyahat ve gider belgelerini gözden geçirmek ve onaylamakta kullanılan iş akışı işlemlerini ayarlayabilirsiniz. iş akışlarının tanımlandığı belgeler gider raporları, seyahat talepleri ve nakit avans taleplerini içerebilir.

İş akışı, bir iş sürecini temsil eder. Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar. İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:

-   **Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz. İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.

-   Süreç görünürlüğü — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz. Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.

-   Merkezi çalışma listesi — Kullanıcılar, iş akışı görevlerini ve kendilerine atanmış onayları görmek için merkezi bir çalışma listesini görüntüleyebilir. 

**Oluşturabileceğiniz iş akışı türleri**

Aşağıdaki tablo **Gider** içerisinde oluşturabileceğiniz iş akışı türlerini listeler.

| **Tip**                           | **Bu türü aşağıdakileri gerçekleştirmek için kullanın:**                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| **Gider raporu**                 | Gider raporları için onay iş akışları oluşturun.                       |      
| **Gider raporu otomatik olarak deftere nakletme**    | Gider raporları için belge otomatik deftere nakil iş akışları oluşturun.              |     
| **Gider satırı öğesi**              | Gider raporları üzerinde satır maddeleri için onay iş akışları oluşturun.         |     
| **Gider satırı öğesi otomatik olarak deftere nakletme** | Gider raporları üzerinde satır maddeleri için otomatik deftere nakil iş akışları oluşturun.|
| **Seyahat talebi**             | Seyahat talepleri için onay iş akışları oluşturun.                   |    
| **Nakit avans isteği**           | Nakit avans talepleri için onay iş akışları oluşturun.                 |     
| **KDV vergisinden düşme**               | Katma değer vergisi (KDV) düşürme için onay iş akışları oluşturun. |       


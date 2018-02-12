---
title: "Ürün yapılandırmalarını yeniden kullanma"
description: "Ürün için mevcut bir yapılandırmayı otomatik olarak yeniden kullanmak istediğinizi belirtebilirsiniz. Ardından bir kullanıcı bir yapılandırma oturumunu tamamladığında sistem, kullanıcının seçimiyle eşleşen bir yapılandırma olup olmadığını doğrular. Eşleşen bir yapılandırma bulunursa ürün reçetesine (BOM) karşılık gelen yapılandırma kodu ve rota yeniden kullanılır."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 528e158c82babf38ea975d46e3b4cd5eda1b0eda
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="reuse-product-configurations"></a>Ürün yapılandırmalarını yeniden kullanma

[!include[banner](../includes/banner.md)]


Ürün için mevcut bir yapılandırmayı otomatik olarak yeniden kullanmak istediğinizi belirtebilirsiniz. Ardından bir kullanıcı bir yapılandırma oturumunu tamamladığında sistem, kullanıcının seçimiyle eşleşen bir yapılandırma olup olmadığını doğrular. Eşleşen bir yapılandırma bulunursa ürün reçetesine (BOM) karşılık gelen yapılandırma kodu ve rota yeniden kullanılır.

<a name="requirements-for-reusing-configurations"></a>Yapılandırmaları yeniden kullanma gereksinimleri
---------------------------------------

Yapılandırmaları yeniden kullanmayı etkinleştirmek için **Ürün yapılandırma modeli ayrıntıları** sayfasında bileşenler ve öznitelikler için aşağıdaki bilgileri belirtmelisiniz:

-   **Bileşenler ve alt bileşenler**: **Genel** Hızlı sekmesinde **Konfigürasyonları yeniden kullan** alanında **Evet**'i seçin.
-   **Öznitelikler**: **Öznitelikler** Hızlı Sekmesinde **Yeniden kullanıma dahil et** seçeneğini belirleyin. Bu seçenek yalnızca ilgili bileşen yeniden kullanım için etkinleştirildiğinde görüntülenir. Yeniden kullanım için hiçbir öznitelik seçmezseniz, bir yapılandırma oturumu sırasında kullanıcının seçimlerinden bağımsız olarak yapılandırma her zaman yeniden kullanılır. Mevcut yapılandırmadaki öznitelik değerleri kullanıcının seçimleriyle eşleşmelidir. Örneğin, bir yapılandırma oturumu sırasında kullanıcı renk olarak **Mavi** seçerse sistem bileşenin mevcut bir yapılandırmasında renk olarak mavinin bulunup bulunmadığını doğrular.

## <a name="resetting-configuration-reuse"></a>Yapılandırma yeniden kullanmayı sıfırlama
Yapılandırma yeniden kullanmayı sıfırladığınızda önceden oluşturduğunuz yapılandırmalar artık değerlendirilmez. Ürün reçetesi veya rota değiştiğinde ancak ilgili öznitelikler değişmediğinde yapılandırma yeniden kullanmayı sıfırlamak isteyebilirsiniz. Yapılandırma yeniden kullanmayı bileşen için **Genel** Hızlı Sekmesinde sıfırlarsınız.





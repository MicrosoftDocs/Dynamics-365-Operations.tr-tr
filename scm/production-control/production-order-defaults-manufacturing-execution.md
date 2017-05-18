---
title: "İmalatın yürütülmesinde üretim emri varsayılanları"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: cc12a8d75ead1577cf0b31a0dbf3ac072c47dc08
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>İmalatın yürütülmesinde üretim emri varsayılanları

[!include[banner](../includes/banner.md)]




Çalışanlar üretim işleri üzerinde kayıtlar yapmaya başlamadan önce **Üretim emri varsayılanları** sayfasındaki tüm ayarları üzerinde dikkatlice düşünmelisiniz. Şirketiniz çoklu tesis işlevini kullanıyorsa, her tesis için üretim emirleri için farklı varsayılan değerler ayarlamak isteyebilirsiniz. Üretim denetimiyle entegrasyon için sipariş varsayılanları **Üretim emri varsayılanları** sayfasındaki şu sekmelerden ayarlanır:

-   **Genel** – Üretim yürütmedeki üretim işlerine ilişkin genel sipariş varsayılanları.
-   **Başlat** – Üretim işleri veya operasyonları başladığında kullanılan sipariş varsayılan değerleri.
-   **Operasyonlar** – Üretim işlerine veya operasyonlarına uygulanan sipariş varsayılan değerleri ve üretim süreci sırasındaki operasyonlarla ilgili geribildirim.
-   **Tamamlandı olarak bildir** – Bir üretim emrindeki son operasyonda maddeler tamamlandı olarak bildirildiğinde uygulanan sipariş varsayılan değerleri.
-   **Miktar doğrulaması** – Üretim emirlerindeki başlangıç ve geribildirim miktarlarını doğrulamak için kullanılan sipariş varsayılanları.

## <a name="types-of-production-jobs"></a>Üretim işleri tipleri
**Operasyonlar** sekmesinde, **İş kaydı sayfasında** kayıt yapılmasını gerektiren üretim işlerinin türlerini seçin. Genellikle, çalışanlar kurulum işlerine ve işlem işlerine kayıt yaptırır. Ancak, iş planlama uygulanması durumunda, çalışanların bir üretim emri işleme konduğunda kayıt yaptırmak zorunda oldukları taşıma işleri gibi diğer iş türlerini de seçebilirsiniz. **Önemli:** Tüm ilgili iş türlerinin seçildiğinden emin olun. Aksi halde, işler **İş kaydı** sayfasında kayıt için görüntülenmeyebilir. Seçimlerinizin **Rota grupları** sayfasındaki **İş yönetimi** sütununda yapılan seçimlerle uyumlu olmasını sağlayın. Rota grubunda **İş yönetimi** seçilirse, iş türü üretim emrinde tamamlandı olarak bildirilir. Bu rapor, işin Üretim yürütmede tamamlandı olarak bildirilmesi durumunda gerçekleştirilir. **İş yönetimi** seçimi yapılan tüm iş türleri bir operasyonda tamamlandı olarak bildirildiğinde, Üretim yürütme de operasyonu tamamlandı olarak raporlar. **Not:** Bazı iş türleri üretim günlükleri aracılığıyla el ile bildirilebilir. Bu durumda, iş türü için **İş yönetimi**'ni seçin ancak **Üretim emri varsayılanları** sayfasındaki **Operasyonlar** sekmesinde kayıt için iş türünü seçmeyin.

## <a name="bom-consumption-and-picking-list-journals"></a>Ürün reçetesi tüketimi ve malzeme çekme listesi günlükleri
Malzemeler, üretim sırasında otomatik olarak veya el ile tüketilmek üzere ayarlanabilir. Otomatik tüketim ürün reçetesi satırlarında ayarlanan otomatik tüketim kuralı ve üretim emri varsayılanlarındaki **Otomatik ürün reçetesi tüketimi** alanında bulunan ayar tarafından denetlenir Otomatik tüketim, bir üretim emri başlatıldığında veya tamamlandı olarak bildirildiğinde gerçekleşecek şekilde ayarlanabilir. Alternatif olarak, bir iş başlatıldığında veya tamamlandığında iş düzeyinde gerçekleşebilir.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Üretim emri başlatıldığında malzeme tüketimini denetleme

Bir üretim emri başlatıldığı sırada malzeme tüketimi **Başlat** sekmesindeki **Otomatik ürün reçetesi tüketimi** tarafından denetlenir. Aşağıdaki değerler kullanılabilir:

-   **Otomatik tüketim kuralı** – Bir üretim emri başlatıldığında, malzeme miktarları üretim ürün reçetesi satırlarında ayarlanan otomatik tüketim kuralına göre tüketilir. Üretim başlangıcı sırasında yalnızca otomatik tüketim kuralının **Başlat** olarak ayarlandığı malzeme satırları tüketilir.
-   **Her zaman** – Başlangıç miktarına orantılı malzeme miktarları her zaman tüketilir.
-   **Hiçbir zaman** – Malzeme miktarları hiçbir zaman tüketilmez.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Bir üretim işi başlatıldığında veya tamamlandığında malzeme tüketimini denetleme

Bir üretim emrinin başlatılması veya tamamlanması sırasındaki malzeme tüketimi **Operasyonlar** sekmesindeki **Otomatik ürün reçetesi tüketimi** alanı tarafından denetlenir. Aşağıdaki değerler kullanılabilir:

-   **Otomatik tüketim kuralı** – Bir üretim emrindeki miktar başlatıldığında veya tamamlandığında, malzeme miktarları üretim ürün reçetesi satırlarında ayarlanan otomatik tüketim kuralına göre tüketilir. Yalnızca otomatik tüketim kuralının **Başlat** veya **Bitir** olarak ayarlandığı malzeme satırları tüketilir.
-   **Her zaman** – İşteki başlangıç miktarına orantılı malzeme miktarları her zaman tüketilir.
-   **Hiçbir zaman** – Malzeme miktarları hiçbir zaman tüketilmez.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Üretim emri tamamlandı olarak bildirildiğinde malzeme tüketimini denetleme

Bir üretim emri Tamamlandı olarak bildirildiğinde malzeme tüketimi **Tamamlandı olarak bildir** sekmesindeki **Otomatik ürün reçetesi tüketimi** tarafından denetlenir. Aşağıdaki değerler kullanılabilir:

-   **Otomatik tüketim kuralı** – Bir üretim emri tamamlandı olarak bildirildiğinde, malzeme miktarları üretim ürün reçetesi satırlarında ayarlanan otomatik tüketim kuralına göre tüketilir. Yalnızca otomatik tüketim kuralının **Bitir** olarak ayarlandığı malzeme satırları tüketilir.
-   **Her zaman** – Tamamlandı olarak bildirilen miktara orantılı malzeme miktarları her zaman tüketilir.
-   **Hiçbir zaman** – Malzeme miktarları hiçbir zaman tüketilmez.






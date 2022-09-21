---
title: Satıcı faturalarını içe aktardığınızda fatura satırları oluşturun
description: Bu makalede, faturalar içeri aktarıldığında satıcı faturalarındaki fatura satırlarını otomatik olarak oluşturma işlevi açıklanmaktadır.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 5cb2c1234de03e9777921c18e4cbb81eec7feef9
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462287"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Satıcı faturalarını içe aktardığınızda fatura satırları oluşturun

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu makalede, faturalar içeri aktarıldığında satıcı faturalarındaki fatura satırlarını otomatik olarak oluşturma işlevi açıklanmaktadır.

Bazen, satıcı faturaları alıcı bilgileri ve alt toplamlar gibi sınırlı bilgiler içerir. Ancak, bunlar satır maddeleri ile ilgili hiçbir bilgi içermezler. Faturaları içe aktardığınızda, ilgili satınalma siparişindeki bilgileri temel alarak fatura satırları otomatik olarak oluşturulur.

Fatura satırlarının otomatik olarak oluşturulmasını etkinleştirmek için aşağıdaki adımları izleyin.

1.  **Borç hesapları \> Kurulum \> Borç hesapları parametreleri**'ne gidin.
2.  **Satıcı fatura otomasyonu** sekmesinde, **İçe aktarılan faturalar için otomatik satır oluşturma** altında **Otomatik olarak fatura satırları oluştur** seçeneğini **Evet** olarak ayarlayın. 
4.  **Otomatik fatura satırları oluşturma için varsayılan miktarı seç** alanında, otomatik olarak fatura satırı oluşturmak için kullanılacak miktarı seçin:

    - **Sipariş edilen miktar** - Satırlar, satınalma siparişi satırlarından oluşturulur. Bu değer, varsayılan değerdir.
    - **Ürün giriş miktarı** – İlgili ürün girişlerini bulmak için satınalma sipariş numaraları kullanılır. Daha sonra, fatura satırları oluşturmak için ürün giriş miktarlarını kullanır.

## <a name="data-entity-changes"></a>Veri varlığı değişiklikleri

Bu makalede açıklanan işlevleri desteklemek için, **Satıcı faturası başlığı** veri varlığı geliştirilmiştir. Üç alan eklendi:

- **HeaderOnlyImport** – Fatura başlıkları için satır oluşturulması için bu alan **Evet** olarak ayarlanmalıdır.
- **PurchIdRange** – Satınalma siparişi numaralarının listesi. Fatura numaraları **PO0001..PO0009** gibi bir aralık (burada iki nokta aralığın başlangıcını ve sonunu ayırır) veya **PO0001, PO0003, PO0006** gibi ayrı değerler olabilir. Tüm satınalma siparişleri, fatura başlığındaki aynı satıcı hesabına ait olmalıdır. Aksi takdirde, şu hata iletisini alırsınız: "Fatura satırları oluşturulamadı. Satınalma siparişlerinde farklı satıcı hesapları var."
- **PackingslipRange** – Ürün makbuz numaralarının listesi. Satıcı fatura satırları, ürün makbuzlarından oluşturulabilir. Ancak, ürün giriş numaraları normal olarak satıcı faturalarına dahil edilmez. Yalnızca belirli faturalar için hangi ürün makbuzlarının olduğunu açıkça belirleyebiliyorsanız, ürün makbuz numaralarını bu alana girin. Fatura satırları, ürün makbuzlarına dayalı olarak oluşturulabilir. Bu alan kullanılırsa, **Borç hesapları parametreleri** sayfasında **Otomatik fatura satırları oluşturma için varsayılan miktarı seçin** alanı dikkate alınmaz. 

**Sınırlama**: Birden fazla ürün makbuz numarası girerseniz, aynı fatura numarasıyla birden fazla bekleyen satıcı faturası oluşturulur. Faturayı daha fazla işlemeden önce, bunları el ile birleştirmeniz gerekir. Gelecekteki sürümlerde, faturaları otomatik olarak konsolide etmeyi planlıyoruz, bu nedenle sınırlama kaldırılacak.

Tüm ürün makbuzları, fatura başlığındaki aynı satıcı hesabına ait olmalıdır.

## <a name="result"></a>Sonuç

Satırlar başarıyla oluşturulursa, satıcı fatura otomasyon geçmişine aşağıdaki ileti kaydedilir: "Fatura satırlarını otomatik olarak oluştur: Başarılı oldu."

Satırlar üretilmezse, günlüğe aşağıdaki hata iletisi kaydedilir: "Fatura satırlarını otomatik olarak oluştur: Başarısız oldu."

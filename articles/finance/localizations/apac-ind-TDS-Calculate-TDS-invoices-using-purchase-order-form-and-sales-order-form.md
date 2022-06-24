---
title: Satın alma siparişi formu ve satış siparişi formunu kullanarak TDS faturalarını hesaplama
description: Bu makalede, çeşitli fatura türlerinde Kaynakta Kesilen Vergi (TDS) hesaplamaya yönelik adımlar listelenmektedir.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 72883741ee7eed6b0296736c80dd648c882ae53e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853299"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>Satın alma siparişi formu ve satış siparişi formunu kullanarak TDS faturalarını hesaplama

[!include [banner](../includes/banner.md)]

Bu makalede, **Satınalma siparişi**, **Satınalma günlüğü**, **Paket sipariş** ve **Satış siparişi** sayfaları kullanılarak çeşitli fatura türlerinde Kaynakta Kesilen Vergi (TDS) hesaplamaya yönelik adımlar listelenmektedir.

1. Listelenen sayfayı kullanarak bir satınalma siparişi, satınalma günlüğü, paket satınalma siparişi veya bir satış siparişi oluşturun. Gerekli ayrıntıları girin.

2. Satıcı veya müşterinin değerlendirilen yapısını görüntülemek için **Kurulum** sekmesini seçin. Bu bilgiler **Değerlendirilenin yapısı** alanında, **Stopaj vergisi grubu** alan grubu altında listelenmiştir.

3. **TDS grubu** alanında, satıcı veya müşteri için tanımlanan varsayılan TDS grubunu görüntüleyin veya değiştirin.

   > [!NOTE]
   > **TDS grubu** alanında TDS grubunu seçtiğinizde, **TCS grubu** alanı kullanılamaz. TDS yalnızca, **Tüm satıcılar** veya **Tüm müşteriler** sayfasındaki satıcı veya müşteri için **Stopaj vergisini hesapla** onay kutusu seçilmişse hesaplanır.  

4. **Satırlar** sekmesinde madde satırları oluşturun ve gerekli ayrıntıları girin.

5. Başlık düzeyinde tanımlanan TDS grubunu görüntülemek veya değiştirmek için **Kurulum** sekmesini (satır düzeyi) seçin. TDS grubu, **Stopaj vergisi grubu** alan grubunun altında olan **TDS grubu** alanında görüntülenir.

6. **Vergi bilgileri** sekmesini seçin ve ardından bu alanda görüntülenen şirket adı için ayarlanmış alternatif adresleri seçin. Şirket adı, **Şirket bilgileri** alan grubunun altında bulunan **Ad** alanında görüntülenir. 

   Seçilen şirket adının TAN değeri, **Stopaj vergisi** alan grubunun altında **Vergi Hesap Numarası** (**TAN**) alanında görüntülenir. 

7. **Geçici stopaj vergisi hareketleri** sayfasını açmak için **Stopaj vergisi**'ni seçin. **Geçici stopaj vergisi hareketleri** sayfasının üst bölmesinde aşağıdaki alanları görüntüleyin.

   - **Stopaj** **vergisinin** **toplam** **tutar** **değeri**- TDS grubunun hareketleri için hesaplanan toplam TDS.

   - **Değer** -Hareket için TDS hesaplamasında kullanılan toplam yüzde. Toplam yüzde, TDS grubuna iliştirilmiş TDS vergi kodları için tanımlanan formüle dayanır.

   - **Düzeltilmiş stopaj vergisi tutarı** - TDS grubundaki tüm vergi kodları için toplam düzeltilmiş TDS tutarı.

   - **TDS** - Seçilirse, hareketle bir TDS grubu ilişkilendirilir.

**Geçici stopaj vergisi hareketleri** sayfasındaki **Genel bakış**, **Genel** ve **Düzeltme** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.

8. **Eşik** sayfasını açmak için **Eşik**'i seçin. Bu sayfada, belirli bir TDS vergi koduna ilişkilendirilmiş TDS vergi bileşeni için tanımlanan eşik sınırını görüntüleyin.

9. **Formül tasarımcısı** sayfasını açmak için **Formül tasarımcısı**'nı seçin. Bu sayfada, belirli bir TDS vergi kodu için tanımlanan formülü görüntüleyin. 

10. Faturayı deftere nakledin. Satınalma faturalarında hesaplanan TDS tutarı, borç hesabına nakledilir ve satış faturalarında hesaplanan TDS tutarı, TDS grubundaki her bir TDS vergi kodu için tanımlanan alacak hesabına nakledilir. TDS vergi kodları için borç hesapları veya alacak hesapları **Stopaj vergisi kodları** sayfasında tanımlanmıştır.

11. **Stopaj vergisi hareketleri** sayfasını açmak **Sorgu** düğmesi **> Fatura > Deftere nakledilen stopaj vergisi** düğmesini seçin. **Değer** alanında, hareket için TDS hesaplamasında kullanılan toplam yüzdeyi görüntüleyebilirsiniz.

**Stopaj vergisi hareketleri** sayfasındaki **Genel bakış**, **Genel** ve **Tutar** sekmelerindeki alanlar, hareket için hesaplanan TDS bilgilerini görüntüler. TDS grubuna iliştirilmiş her TDS vergi kodu için TDS hesaplama bilgilerini görüntüleyin.

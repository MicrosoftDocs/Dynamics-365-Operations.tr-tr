---
title: Günlükleri kullanarak faturalardaki TDS'yi hesaplama
description: Bu konuda, günlüklerde Kaynakta Kesilen Vergi (TDS) hesaplamaya yönelik adımlar listelenmektedir.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023672"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Günlükleri kullanarak faturalardaki TDS'yi hesaplama

[!include [banner](../includes/banner.md)]

Bu konuda, günlüklerde Kaynakta Kesilen Vergi (TDS) hesaplamaya yönelik adımlar listelenmektedir.

**Yevmiye defterleri** sayfasını açarak (**Genel muhasebe > Günlük girişleri > Yevmiye defterleri**) başlayın.

[![Yevmiye defterleri](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Tabloda listelenen günlük formlarını kullanarak günlük satırları oluşturun. Hesap türü ve mahsup hesap türünü seçin ve hareketin tutarını girin. 

   > [!NOTE]
   > **Fatura onay günlüğü** sayfasında, **Fişleri bul**'u seçin TDS'nin hesaplanacağı faturaları seçin. **Fatura kaydı** sayfasında veya **Fişleri bul** sayfasında oluşturulan faturaları görüntüleyin.  

2. **Günlük fişi** sayfasının **Genel** sekmesinde, **TDS grubu** alanında satıcı veya müşteri için tanımlanan varsayılan TDS grubunu görüntüleyin veya değiştirin. Günlük satırlarında hesaplanan TDS tutarı, **TDS grubu** alanında listelenen TDS vergi kodları için belirlenen formüle dayanır. 

   > [!NOTE]
   > **TDS grubu** alanında bir TDS grubu seçtiğinizde, **Stopaj vergisi grubu** alanı ve **TCS grubu** alanı kullanılamaz. **Stopaj vergisi grubu** alanı yalnızca **Yevmiye defteri** sayfasında kullanılabilir. TDS yalnızca, **Tüm satıcılar** veya **Tüm müşteriler** sayfalarındaki satıcı veya müşteri için **Stopaj vergisini hesapla** onay kutusu seçilmişse hesaplanır.   

3. **Vergi bilgileri** sekmesini seçin. Ardından gerekliyse bu alanda şirket için ayarlanmış alternatif şirket adreslerini seçin. Şirket adını, **Şirket bilgileri** alan grubunun altında bulunan **Ad** alanından görüntüleyebilirsiniz. 

4. **Stopaj vergisi** alan grubunun altındaki **Değerlendirilenin yapısı** alanında bulunan satıcı veya müşterinin değerlendirilen yapısı kategorisini görüntüleyin. **Vergi Hesap Numarası** (**TAN**) alanında, görüntülenen şirket adının TAN değerini görüntüleyin.  

5. **Geçici stopaj vergisi hareketleri** sayfasını açmak için **Stopaj vergisi** menüsünde **Stopaj vergisi**'ni seçin. **Geçici stopaj vergisi hareketleri** sayfasının üst bölmesinde aşağıdaki alanlar görüntülenir.

   - **Stopaj vergisinin toplam tutar değeri** - TDS grubunun hareketleri için hesaplanan toplam TDS.

   - **Değer** -Hareket için TDS hesaplamasında kullanılan toplam yüzde. Toplam yüzde, TDS grubuna iliştirilmiş TDS vergi kodları için tanımlanan formüle dayanır.

   - **Düzeltilmiş stopaj vergisi tutarı** - TDS grubundaki tüm vergi kodları için toplam düzeltilmiş TDS tutarı.

   - **TDS** - Seçilirse, hareketle bir TDS grubu ilişkilendirilir.

  **Geçici stopaj vergisi hareketleri** sayfasındaki **Genel bakış**, **Genel** ve **Düzeltme** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.

6. **Eşik** sayfasını açmak için **Eşik**'i seçin. Bu sayfada, belirli bir TDS vergi koduna ilişkilendirilmiş TDS vergi bileşeni için tanımlanan eşik sınırı ve istisna eşik sınırını görüntüleyin.

   **Formül tasarımcısı** formunu açmak için **Formül tasarımcısı**'nı seçin. Bu sayfada, belirli bir TDS vergi kodu için tanımlanan formülü görüntüleyin. **Günlük fişi** sayfasına dönmek için **Formül tasarımcısı**'nı ve **Geçici stopaj vergisi hareketleri** sayfalarını kapatın.

8. Gerekli diğer ayrıntıları girin. Günlüğü doğrulayın ve deftere nakledin. Satınalma faturalarında hesaplanan TDS tutarı, borç hesabına nakledilir. Satış faturalarında hesaplanan TDS tutarı, TDS grubundaki her bir TDS vergi kodu için tanımlanan alacak hesabına nakledilir. TDS vergi kodları için borç hesapları veya alacak hesapları **Stopaj vergisi kodları** sayfasında tanımlanmıştır.

9. **Stopaj** **vergisi** **hareketleri** sayfasını açmak için **Deftere nakledilen stopaj vergisi**'ni seçin. **Değer** alanında, hareket için TDS hesaplamasında kullanılan toplam yüzde görüntülenir.

   Stopaj vergisi hareketleri sayfasındaki **Genel bakış**, **Genel** ve **Tutar** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.

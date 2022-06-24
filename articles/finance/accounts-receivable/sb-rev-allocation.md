---
title: Gelir tahsisatı
description: Bu makalede, Abonelik faturalamasında gelir tahsisini kullanma işlemi açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 18739e0871592bc9eefcdf00f67dd4dd18f5d6f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864382"
---
# <a name="revenue-allocation"></a>Gelir tahsisatı

Bu makalede, faturalama zamanlamasında gelir tahsisat parametrelerini ayarlama işlemi açıklanmaktadır. Ödeme planı oluştururken, gelir tahsisatını ayarlayabilir veya düzenleyebilirsiniz. Etkin veya sonlandırılmış bir faturalama planı için **Gelir tahsisatı** sayfasını açtığınızda, alanlar salt okunurdur.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Fatura planı için gelir tahsisatını belirtin

Fatura planı için gelir tahsisatını belirlemek üzere aşağıdaki adımları izleyin.

1. **Tüm/Etkin faturalama zamanlamaları** listesi sayfasında, bir faturalama zamanlamasını veya faturalama zamanlama satırını seçin.
2. Sayfanın üst kısmındaki **Gelir tahsisatı** sekmesinde, **Gelir tahsisatı**'nı seçin.
3. **Çoklu öğe düzenleme türü** alanında, çoklu öğe düzenleme (MEA) türünü seçin.
4. **Birden çok öğeli düzenleme numarası** alanında, MEA numarasını belirtin. Ardından, **Ertelenen sözleşme gelir hesabı** alanında, ertelenen sözleşme gelir hesabını belirtin.

    **Birden fazla öğe düzenleme türü** alanını **Tek** olarak ayarlarsanız, aynı **Çoklu öğe düzenleme numarası** ve **Ertelenen sözleşme gelir hesabı** değerleri her satıra uygulanır. **Birden fazla öğe düzenleme türü** alanını **Çoklu** olarak ayarlarsanız, her satır için farklı **Çoklu öğe düzenleme numarası** ve **Ertelenen sözleşme gelir hesabı** belirtebilirsiniz.
    
    Bir MEA numarası yalnızca iki veya daha fazla madde için atanabilir. Tek bir satır kendine ait bir MEA numarası içeremez.

5. **Kaydet**'i seçin.

### <a name="fields"></a>Alanlar

**Çoklu öğe ayarlaması** sayfası aşağıdaki alanları içerir.

| Alan | Açıklama |
|---|---| 
| Çoklu öğe düzenleme türü | <p>Hareket için MEA türünü seçin:</p><ul><li>**Çoklu** – Hareketteki satır maddeleri MEA'nın bir parçasıdır veya birden fazla düzenleme var.</li><li>**Yok** – Hareket herhangi bir gelir tahsisatı bulunmayan standart bir harekettir.</li><li>**Tek** – Hareketteki tüm maddeler tek bir MEA'nın bir parçasıdır.</li></ul> |
| Birden çok öğe düzenleme numarası | <p>Satırın MEA numarası. Bu alan, yalnızca **Çoklu öğe düzenlemesi türü** alanı **Çoklu** olarak ayarlandığında kullanılabilir.</p><p>Bu alan boşsa ve bir MEA numarası atarsanız, **Bağımsız satış fiyatı kaynağı** ve **Bağımsız satış fiyatı** alanları, **Madde bağımsız satış fiyatı** sayfasındaki değerleri temel alarak otomatik olarak güncelleştirilir. Yalnızca satış siparişindeki diğer satırlara atanan MEA numaraları kullanılabilir.</p> |
| Ertelenen sözleşme geliri hesabı | Bir eksik sözleşme faturası oluşturulduğunda, günlük girişleri için kullanılacak hesabı belirtin. Bu alan, yalnızca yinelenen sözleşme faturalaması kullanıldığında kullanılabilir. |
| **Satırlar** | |
| Çeşit numarası | Satış siparişinden alınan değişken numarası. |
| Madde numarası | Satış siparişinden alınan madde numarası. |
| Faturalama sıklığı | Gelir tahsisatı için sıklık: **Günlük**, **Aylık**, **Üç aylık**, **Altı aylık** veya **Yıllık**. |
| Miktar | Satış siparişinden alınan değer. |
| Sözleşme değeri | Sözleşme değeri. |
| Birden çok öğe düzenleme numarası | <p>Satırın MEA numarası. Bu alan, yalnızca **Çoklu öğe düzenlemesi türü** alanı **Çoklu** olarak ayarlandığında kullanılabilir.</p><p>Bu alan boşsa ve bir MEA numarası atarsanız, **Bağımsız satış fiyatı kaynağı** ve **Bağımsız satış fiyatı** alanları, **Madde bağımsız satış fiyatı** sayfasındaki değerleri temel alarak otomatik olarak güncelleştirilir. Yalnızca satış siparişindeki diğer satırlara atanan MEA numaraları kullanılabilir. Bu değerler madde için ayarlanmamışsa, **Çoklu öğe gelir tahsisatı parametreleri** sayfasındaki değerler kullanılır.</p> | 
| Tek başına satış fiyatı kaynağı | <p>Tek başına satış fiyatının kaynağı:</p><ul><li>**Tutar** – Tek başına satış fiyatı, 0'dan (sıfır) büyük olan ve sizin belirttiğiniz bir tutardır. Tutar, gereken şekilde işlevsel ve kaynak para birimleri arasında dönüştürülür.</li><li>**Temel satış fiyatı** – Tek başına satış fiyatı, maddenin temel satış fiyatıyla eşleşir.</li><li>**Fatura fiyatı** – Tek başına satış fiyatı, maddenin fatura fiyatıyla eşleşir.</li><li>**Madde yüzdesi** – Tek başına satış fiyatı yüzde değeri olarak belirtilir ve maddenin fiyatına göre hesaplanır. Bu seçenek belirlenirse varsayılan yüzdeyi belirtin.</li><li>**Kalan tutarı tahsis et** – Tek başına satış fiyatının kaynağı, *Ana maddenin toplam sözleşme değeri* – *Alt maddelerin toplam tek başına satış fiyatı* olarak hesaplanır:</p><ul><li>*Ana maddenin toplam sözleşme değeri*, net veya faturalanan tutardır.</li><li>*Alt maddelerin toplam tek başına satış fiyatı*, bu tek başına satış fiyatı kaynağını kullanan alt madde dışındaki tüm alt maddelerin genişletilmiş veya sözleşme tek başına satış fiyatı toplamıdır.</li></ul><p>Hesaplanan tutar negatif bir değer ise, tutar 0 (sıfır) olarak ayarlanır.</p><p>**Not:** Bu seçenek, gelir bölünmesi alanında yalnızca bir alt madde için seçilebilir.</p></li><li>**Yok** – Tek başına satış fiyatının kaynağı, alt maddelere dayanır. Bu seçenek, gelir bölünmesi şablonunda üst madde olarak tanımlanan maddelere uygulanır. **Gelir bölme** onay kutusu işaretliyse, bu seçenek otomatik olarak seçilir ve ayar değiştirilemez.</li><li>**Ana fatura fiyatının yüzdesi** – Tek başına satış fiyatının kaynağı, ana maddenin fatura fiyatının bir yüzdesidir. Bu seçenek yalnızca gelir bölme şablonundaki alt maddeler için kullanılabilir.</li><li>**Ana standart fiyatın yüzdesi** – Tek başına satış fiyatının kaynağı, ana maddenin standart fiyatının bir yüzdesidir. Bu seçenek yalnızca gelir bölme şablonundaki alt maddeler için kullanılabilir. Bir alt maddeye ait seçenek, **Ana standart fiyatın yüzdesi** ayarından **Ana fatura fiyatının yüzdesi** ayarına veya **Ana fatura fiyatının yüzdesi** ayarından **Ana standart fiyatın yüzdesi** ayarına değiştirilirse, hesaplanan değerler de güncelleştirilir.</li></ul> |
| Tek başına satış fiyatı | <p>Satır için, hareket para birimi cinsinden, bağımsız satış fiyatı.</p><p>**Tutar** alanındaki değer girilir veya hesaplanır.</p> |
| Sözleşme tek başına satış fiyatı | Sözleşme bağımsız satış fiyatı. |
| Kalan sözleşme geliri | Sözleşme için kalan sözleşme geliri miktarı. Bu tutar, fatura için henüz oluşturulmamış tüm satırların toplamıdır. |
| Toplam sözleşme geliri | Satır için toplam sözleşme geliri miktarı. Bu tutar, bunlarla ilgili faturaların oluşturulup oluşturulmadığından bağımsız olarak tüm satırların toplamıdır. |
| Ertelenen sözleşme geliri hesabı | <p>Bir eksik sözleşme faturası oluşturulduğunda, günlük girişleri için kullanılacak hesabı belirtin.</p><p>Bu alan, yalnızca yinelenen sözleşme faturalaması kullanıldığında kullanılabilir.</p> |
| Hata | Gelir tahsisatı için oluşan hatalar. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Satış siparişinde gelir tahsisatı kullan

Bir satış siparişinde gelir tahsisat işlevini kullanmak için, aşağıdaki adımları izleyin.

1. **Tüm satış siparişleri** sayfasında maddeleri olan bir satış siparişi oluşturun.
2. **Fatura** sekmesinde, **Gelir tahsisatı** altında, **Gelir tahsisatı**'nı seçin.
3. **Birden çok öğeli düzenleme türü** alanında, MEA türünü belirtin.
4. **Birden çok öğeli düzenleme numarası** alanında, MEA numarasını belirtin.
5. **Birden fazla öğe düzenleme türü** alanı **Birden çok** olarak ayarlanmışsa, istediğiniz satırları seçin ve **Seçilen için uygula**'yı seçin.
6. **Kaydet**'i seçin.

Gelir ve gider ertelemeyi kullanırsanız, erteleme zamanlaması otomatik olarak oluşturulur. Bunu, **Tüm erteleme planları** sayfasında görüntüleyebilirsiniz.

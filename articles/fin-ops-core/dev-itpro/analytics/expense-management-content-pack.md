---
title: Gider yönetimi Power BI içeriği
description: Bu konu, Power BI Gider Yönetimi içerik paketinde nelerin bulunduğunu açıklar.
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: aadf43d478eb4bf5af20df02dcc6399a7a2e71a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743519"
---
# <a name="expense-management-power-bi-content"></a>Gider yönetimi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, Power BI Gider Yönetimi'nde içeriğinde nelerin bulunduğunu açıklar. 

## <a name="overview"></a>Genel bakış
İki Power BI içerik paketi Gider yönetiminde kullanılmak üzere sürüm 8.1 ve sonrasında mevcuttur. 
- Gider raporu gönderen çalışanlar için tasarlanmış kişiselleştirilmiş bir pano mevcuttur. 

  Pano, kişilere gönderilmemiş ve gönderilmiş tutarlar hakkında kilit bilgi ve gider hareketleri geçmişine bakış ve içgörü sağlamak için tasarlanmıştır. Kişisel pano, kullanıcı için en önemli bilgileri içeren tek bir sayfadır.

- Borç hesapları elemanları ve yöneticileri için tasarlanmış bir yönetici panosu vardır. Pano, genel çalışan giderlerini izleme ve raporlamaya yönelik tasarlanmıştır. Kilit gider metrikleri, örneğin gönderilmemiş giderler, mesafe ve ortalama gider raporu tutarları sağlar. Hareket verileri kullanır ve gider yönetimi tüm şirket içindeki toplam görünümünü sağlar. Çalışan başına dökümü, finansal boyut verisi ekleme seçeneğiyle sunar. Yönetici gider analitik içeriği şunları içerir: 
  - Gider tutarları ve taslak, sürmekte olan ve tamamlanan gider raporları hakkında içgörüler içeren bir genel bakış sayfası. 
  - Bir çalışan istatistik sayfası, bir çalışanın zaman, maliyet türü ve istatistik grubun hakkında bireysel ayrıntılarını gözden geçirmek için. 
  - Bir çalışan dönüşüm sayfası, birden fazla çalışanı zaman içerisinde karşılaştırmak için. 

Gösterilen tüm tutarlar şirket para birimi cinsindendir. Tüm şirketler hakkında veri gösterilir, ancak ihtiyaç duyulursa bir şirket filtresi ekleyebilirsiniz. 

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
Gider Yönetici Panosu.pbix ve Gider Kişisel Pano.pbix Power BI içeriğini Microsoft Dynamics Lifecycle services (LCS) içindeki Paylaşılan varlıklarda bulabilirsiniz. İçeriği indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).
İçerik, Gider Yönetimi çalışma alanından, katıştırılmış Power Bi içeriği olarak kullanılabilir. Her gider sahibi, kendileri için kişisel giderlere erişebilir, ancak yalnızca Borç Hesapları elemanları ve yöneticilerinin tüm kullanıcı gider verisini görüntülemek için Yönetici içeriğine erişimleri vardır.

## <a name="refreshing-the-power-bi-content"></a>Power BI içeriğini yenilemek
Gider yönetimi Power BI içeriği, TrvBiExpenseMeasurement ölçüsünün ve BudgetActivityMeasure'ın Varlık Mağazasından yenilenmesini gerektirir. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan ölçümler
İçerik bir dizi rapor sayfası içermektedir. Her sayfa grafikler, döşemeler ve tablolar ile görselleştirilen bir dizi ölçüm kümesinden oluşur. Aşağıdaki tabloda Power BI içeriğindeki görselleştirmelere genel bakış sunulmaktadır.

**Kişisel gider analitikleri**

| Rapor sayfası | Gözde canlandırma                             |
|-------------|-------------------------------------------|
| Giderlerim | Mesafe tutarı                         |
|             | Devam etmekte olan gider raporları                |
|             | Hayır. Gönderilmemiş giderlerin               |
|             | Ödenecek kişisel giderler              |
|             | Gönderilmemiş tutar                        |
|             | Gönderilen tutar                          |
|             | Geri ödeme bekleyen tutar             |
|             | Tutarlar ve durum ile gider raporları   |
|             | Gönderilmiş ancak onaylanmamış gider raporları  |
|             | Maliyet türü bazında giderler                     |
|             | Satıcı bazında giderler                      |
|             | İşlen giderler bazında giderler            |
|             | Proje bazında giderler                       |
|             | Zaman içinde toplam hareket tutarı        |

**Yönetici giderleri analizi**

| Rapor sayfası         | Gözde canlandırma                           |           
|---------------------|-----------------------------------------|
| Gider Genel Bakışı    | Taslak giderler tutarı                   |
|                     | Taslak gider satırlarının sayısı           |
|                     | Taslak gider satırları                     |
|                     | Gider raporu ilke ihlalleri        |
|                     | Beklemedeki tutar                      |
|                     | Gönderilmiş ancak onaylanmamış giderler       |
|                     | Onaylanmış giderler                       |
|                     | Toplam gider tutarı                    |
|                     | Gider raporu özetleri                |
|                     | Maliyet türü bazında giderler                   |
|                     | Satıcı bazında giderler                    |
|                     | Çalışanlara göre giderler                   |
|                     | Giderler - proje                     |
| Çalışan Karşılaştırması | Gider tutarları                         |
|                     | Çalışana göre zaman içindeki gider tutarları   |
| Personel İstatistikleri | Gider türüne göre maliyet raporları            |
|                     | Kişisel giderler                       |
|                     | İstatistik grubuna göre gider raporları     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
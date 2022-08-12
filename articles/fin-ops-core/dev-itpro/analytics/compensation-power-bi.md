---
title: Maaş Power BI içeriği
description: Bu makalede, Ücret Power BI içeriği açıklanmaktadır. Raporlara nasıl erişileceğini açıklar ve kullanılan veri modeli hakkında bilgi sağlar.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.search.form: HcmCompensationWorkspace
ms.openlocfilehash: cd51bf429abea5693432643a5ea9441fb9e2e464
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206461"
---
# <a name="compensation-power-bi-content"></a>Maaş Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu makalede, **Ücret** Microsoft Power BI içeriği açıklanmaktadır. Bu raporlara nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**Ücret** Power BI içeriği **Ücret yönetimi** çalışma alanında, aşağıdaki ürünlerden birini kullanıyorsanız gösterilir:

- finans ve operasyon uygulamaları
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan raporlar
**Ücret** Power BI içeriği içinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                     | İçindekiler |
|----------------------------|----------|
| Ücret Genel Bakışı      | Diğer raporların özeti |
| Ücret Analizi      | Şirkete göre saatlik ve maaşlı personeller, ücret planına göre toplam personel, ücret planına göre kadın ve erkek personel, bölüme göre personel ücreti |
| Pozisyon Ödeme Analizi      | En yüksek ve en düşük saatlik ve maaş ödemesi, en yüksek ve en düşük ödemeye sahip pozisyonlar ve tam zamanlı ve yarı zamanlı pozisyonlar |
| Ücret Plan Analizi | Seçilen kazanca göre personel kaydı |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve Yapılandırma](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Aşağıdaki veriler **Ücret** Power BI içeriğindeki raporları doldurmak için kullanılır. Bu tablo, içeriğin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                   | İçindekiler                                                                                                   | Diğer varlıklarla ilişkiler |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Takvim Kaydırma          | Raporları dilimlemek için takvim kaydırmaları                                                                          | Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Personel Eğilimi, Sonlandırılan Personel |
| Şirket                  | Raporların filtreleneceği şirketler                                                                             | Geçerli Ücret, Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Ücret             | Zaman içerisindeki ödeme oranı ve sıklık                                                                           | Geçerli Ücret, Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Geçerli Ücret     | Günün tarihi itibariyle ödeme oranı ve sıklık                                                              | Şirket, Ücret, Demografi, İş, Pozisyon |
| Geçerli Pozisyon         | Günün tarihine göre konumlar, tam zaman eşdeği (FTE), açık konumlar ve açıktan doldurulana konumlar | İş, Pozisyon |
| Geçerli Personel         | Günün tarihi, ya ve insan sayısına göre çalışanlar                                                         | Şirket, Ücret, Coğrafi Konum, Personel Adı, Kime Rapor Verdiği, Personel Unvanı, Demografi, İş, Çalışma, Pozisyon, Kazançlar |
| Tarih                     | Günler, haftalar, aylar ve yıllar                                                                             | Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Sonlandırılan Personel, Personel Eğilimi |
| Demografi             | Doğum tarihi, cinsiyet, etnik köken ve medeni hal                                                   | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| İstihdam               | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                                                  | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Coğrafi Konum      | Şehir, ilçe, posta kodu ve eyalet veya bölge                                                           | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| İş                      | İşlev, tür ve başlık                                                                                  | Geçerli Pozisyon, Geçerli Personel |
| Geçmiş Pozisyon Ataması | Atama neden, başlangıç tarihi, bitiş tarihi ve iş                                                           | Takvim Sapması, Tarih, İş, Pozisyon |
| Bölme                 | Departman, FTE, konum, konum türü başlığı                                                        | Geçerli Pozisyon, Geçerli Personel |
| Pozisyon Eğilimi           | Zaman içerisindeki konumlar, FTE ve iş                                                                          | Takvim Sapması, Tarih, İş, Pozisyon |
| Rapor Verdiği Kişi               | Adı, ikinci ad ve tam adı                                                                       | Geçerli Çalışan, Sonlandırılan Personel, Personel Eğilimi |
| İşten Çıkarılmış Personel      | Çıkartılan personeller, çıkartılma tarihi, başlık, konum ve iş                                           | Şirket, Ücret, Coğrafi Konum, Personel Adı, Kime Rapor Verdiği, Takvim Kaydırma, Tarih, Personel Unvanı, Demografi, Çalışma, İş, Pozisyon, Kazançlar |
| Kazançlar                 | Yürürlük tarihi, kazanç seçeneği, kazanç planı ve kazanç türü                                             | Geçerli Ad, Sonlandırılan Personel, Personel Eğilimi |
| Personel Adı            | Adı, ikinci ad ve tam adı                                                                       | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Personel Unvanı           | Başlık ve kıdem tarihi                                                                                   | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Personel Eğilimi           | Zaman içerisinde çalışanlar, çalışan sayısı, şirket ve konum                                                        | Şirket, Ücret, Coğrafi Konum, Personel Adı, Kime Rapor Verdiği, Takvim Kaydırma, Tarih, Personel Unvanı, Demografi, Çalışma, İş, Kazançlar |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

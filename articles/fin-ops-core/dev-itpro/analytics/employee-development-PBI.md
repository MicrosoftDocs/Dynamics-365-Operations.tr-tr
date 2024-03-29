---
title: Personel gelişimi Power BI içeriği
description: Bu makalede, Personel gelişimi Power BI içeriği açıklanmaktadır.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 307a7ba2b885ba1437d5ef54c2f9d70ef00e2b14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284193"
---
# <a name="employee-development-power-bi-content"></a>Personel gelişimi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu makalede, **Personel gelişimi** Microsoft Power BI içeriği açıklanmaktadır.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan raporlar
**Personel gelişimi** Power BI içeriğinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                        | İçindekiler |
|-------------------------------|----------|
| Personel Gelişimi Genel Bakışı | Diğer raporların özeti |
| Personel Yetenek Analizi       | Personel yetenek türleri ve türe göre personel yetenekleri |
| Personel Yetenek Seviyesi Analizi | Bölüme göre personel yetenek seviyeleri, yetenek seviyesine ve yetenek türüne göre ve en düşük ve en yüksek seviyelere göre personeller |
| Yetenek Profili                 | Seçilen personelin yetenek profili |
| Yetenek Analizi                | Tür ve derecelendirmeye göre yetenekler |
| Performans Derecelendirme Analizi   | İşe göre en yüksek ve en düşük dereceli personeller, bölüme göre personel derecelendirmeleri, derecelendirme ve pozisyon türüne göre ve en yüksek ve en düşük pozisyonlara göre personeller |
| Personel Performans Analizi | Yöneticiye göre seçili derecelendirme için personel derecelendirmeleri |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve Yapılandırma](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

| Varlık                   | İçindekiler                                                                                                   | Diğer varlıklarla ilişkiler |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Takvim Kaydırma          | Raporları dilimlemek için takvim kaydırmaları                                                                          | Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Personel Eğilimi, Sonlandırılan Personel |
| Şirket                  | Raporların filtreleneceği şirketler                                                                             | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Geçerli Pozisyon         | Günün tarihine göre konumlar, tam zaman eşdeği (FTE), açık konumlar ve açıktan doldurulana konumlar | İş, Pozisyon |
| Geçerli Personel         | Günün tarihi, ya ve insan sayısına göre çalışanlar                                                         | Şirket, Coğrafi Konum, Personel Adı, Bağlı Olduğu Kişi, Personel Unvanı, Demografi, İş, İstihdam, Pozisyon |
| Tarih                     | Günler, haftalar, aylar ve yıllar                                                                             | Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Sonlandırılan Personel, Personel Eğilimi |
| Demografi             | Doğum tarihi, cinsiyet, etnik köken ve medeni hal                                                   | Geçerli Personel, Sonlandırılan, Personel, Personel Eğilimi |
| İstihdam               | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                                                  | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Coğrafi Konum      | Şehir, ilçe, posta kodu ve eyalet veya bölge                                                           | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| İş                      | İşlev, tür ve başlık                                                                                  | Geçerli Pozisyon, Geçerli Personel |
| Geçmiş Pozisyon Ataması | Atama neden, başlangıç tarihi, bitiş tarihi ve iş                                                           | Takvim Sapması, Tarih, İş, Pozisyon |
| Bölme                 | Departman, FTE, konum, konum türü başlığı                                                        | Geçerli Pozisyon, Geçerli Personel |
| Pozisyon Eğilimi           | Zaman içerisindeki konumlar, FTE ve iş                                                                          | Takvim Sapması, Tarih, İş, Pozisyon |
| Rapor Verdiği Kişi               | Adı, ikinci ad ve tam adı                                                                       | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| İşten Çıkarılmış Personel      | Çıkartılan çalışanlar, çıkartılma tarihi, başlık, konum ve iş                                             | Şirket, Coğrafi Konum, Personel Adı, Kime Rapor Verdiği, Takvim Kaydırma, Tarih, Personel Unvanı, Demografi, Çalışma, İş, Pozisyon |
| Personel Adı            | Adı, ikinci ad ve tam adı                                                                       | Geçerli Çalışan, Sonlandırılan Personel, Personel Eğilimi |
| Personel Unvanı           | Başlık ve kıdem tarihi                                                                                   | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Personel Eğilimi           | Zaman içerisinde çalışanlar, çalışan sayısı, şirket ve konum                                                        | Şirket, Coğrafi Konum, Personel Adı, Kime Rapor Verdiği, Takvim Kaydırma, Tarih, Personel Unvanı, Demografi, Çalışma, İş |
| İş                      | İşlev, tür ve başlık                                                                                  | Geçerli Personel, Geçerli Pozisyon, Personel Eğilimi, İş Tercih Edilen Yetenek, Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Sonlandırılan Personel |
| İş Tercih Edilen Yetenek      | Önem, derecelendirme, yetenek ve beceri düzeyi                                                                 | İş |
| Personel Yetenek Analizi  | Sertifikalı, seviye, seviye tarihi ve yetenek                                                                    | Personel Ad, Yetenek |
| Performans              | Değerlendirme, açıklama ve derecelendirme modeli                                                                      | Geçerli Personel, Geçerli Pozisyon, Personel Eğilimi, İş Tercih Edilen Yetenek, Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Sonlandırılan Personel |
| Yetenek                    | Beceri, beceri türü ve derecelendirme                                                                              | Personel Yetenek Analizi, İş Tercih Edilen Yetenek |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

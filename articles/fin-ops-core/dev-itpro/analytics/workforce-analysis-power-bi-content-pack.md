---
title: İş gücü ölçümleri Power BI içeriği
description: Bu makalede, İş gücü ölçümleri Power BI içeriği açıklanmaktadır.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.form: HcmWorkforceWorkspace
ms.openlocfilehash: 9d5c156eda3559394cb2723f0492b0ab575d815d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289831"
---
# <a name="workforce-metrics-power-bi-content"></a>İş gücü ölçümleri Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu makalede, **İş gücü ölçümleri** Microsoft Power BI içeriği açıklanmaktadır. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**İşgücü ölçümleri** Power BI içeriği **Personel yönetimi** çalışma alanında, aşağıdaki ürünlerden birini kullanıyorsanız görünür:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan ölçümler
Aşağıdaki tablo, her bir rapor sayfasında gösterilen ölçümleri listeler.

| Rapor                                           | Ölçümler |
|--------------------------------------------------|---------|
| Kişilerin Ölçümleri                                   | Diğer raporların özeti |
| Çalışan Sayısı Analizi Şirket, Departman, Konum | Şirkete, departmana, konuma göre çalışan sayısı ve toplam çalışan sayısı. |
| Çalışan sayısı Analiz İşi, Adım, Yönetici            | İşe, Adıma, Yöneticiye göre çalışan sayısı ve toplam çalışan sayısı. |
| Çalışan sayısı Trend Analizi                         | Şirkete göre bu yılki ve geçen yılki çalışan sayısı karşılaştırması ve geçmiş 12 ay için dönen çalışan sayısı |
| FTE Analizi                                     | Toplam tam zamanlı Eşdeğer (FTE), toplan atanmış FTE, bölüme göre FTE, son 12 ay için FTE, işe göre FTE |
| İşgücü Demografikleri                           | Yaş ve cinsiyet, etnik köken, kıdem ve medeni hale göre çalışan sayısı, tam zamanlı öğrencilerin sayısı, ortalama görev süresi, ortalma yaş ve kadın - erkek çalışan oranı ve personel tarafından konuşulan diller |
| Pozisyon Analizi                                | Departmana göre açık pozisyonlar, kapatılacak açık pozisyonlar, etkin - devre dışı pozisyonlar ve deparatmana göre pozisyonlar |
| Yıpranma Analizi                               | Bu yıl ve geçen yılki kayıp, kayıp, yaşa ve cinsiyete göre mevcut personeller, ayrılan personellerin ortalama kıdemi, bu ay ayrılan personeller, sebebe göre ayrılan personeller |
| Departmana göre kişiler                             | Departmana, pozisyona ve atama başlama ve bitiş tarihlerine göre personel sayısına sahip çalışanlar |
| Kıdemlilik Analizi                               | Ortalama kıdem, şirkete göre ortalama hizmet yılı ve kıdem listesi |
| Personel Yıldönümlerini                           | Bu aydaki yıldönümleri, önümüzdeki aydaki yıldönümleri, hizmet yılına ve yıldönümlerine göre personeller, bölüme göre hizmet yılları |
| Çalışan Doğum günleri                               | Bu aydaki doğum günleri, önümüzdeki aydaki doğum günleri, personel doğum günleri, bölüm ve aya göre doğum günleri |
| Toplu İşe Alma Projeleri                               | Toplam toplu işe alma projeleri, duruma göre toplu işe alma projeleri, bölüm ve sahibine göre toplu işe alma projeleri, işe göre toplu işe alma projeleri ve toplu işe alma projeleri |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve yapılandırma](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Kullanmakta olduğunuz Microsoft Dynamics 365 sürümü için geçerli **İşgücü ölçümleri** Power BI içeriğini indirdiğinizden emin olun.

> [!NOTE]
> Lifecycle Services'taki .pbix dosyaları yalnızca finans ve operasyon uygulamalarında kullanılabilir.

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Aşağıdaki tablo, içeriğin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                   | İçindekiler                                                                            | Diğer varlıklarla ilişkiler |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Takvim Kaydırma          | Raporları dilimlemek için takvim kaydırmaları                                                   | Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Personel Eğilimi, Sonlandırılan Personel |
| Şirket                  | Raporların filtreleneceği şirketler                                                      | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Geçerli Pozisyon         | Günün tarihine göre konumlar, FTE, açık konumlar ve açıktan doldurulana konumlar | İş, Pozisyon |
| Geçerli Personel         | Günün tarihi, ya ve insan sayısına göre çalışanlar                                  | Şirket, Coğrafi Konum, Personel Adı, Bağlı Olduğu Kişi, Personel Unvanı, Demografi, İş, İstihdam, Pozisyon |
| Tarih                     | Günler, haftalar, aylar ve yıllar                                                      | Geçmiş Pozisyon Ataması, Pozisyon Eğilimi, Sonlandırılan Personel, Personel Eğilimi |
| Demografi             | Doğum tarihi, cinsiyet, etnik köken ve medeni hal                            | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| İstihdam               | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                           | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Coğrafi Konum      | Şehir, ilçe, posta kodu ve eyalet veya bölge                                    | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| İş                      | İşlev, tür ve başlık                                                           | Geçerli Pozisyon, Geçerli Personel |
| Geçmiş Pozisyon Ataması | Atama neden, başlangıç tarihi, bitiş tarihi ve iş                                    | Takvim Sapması, Tarih, İş, Pozisyon |
| Bölme                 | Departman, FTE, konum, konum türü başlığı                                 | Geçerli Pozisyon, Geçerli Personel |
| Pozisyon Eğilimi           | Zaman içerisindeki konumlar, FTE ve iş                                                   | Takvim Sapması, Tarih, İş, Pozisyon |
| Rapor Verdiği Kişi               | Adı, ikinci ad ve tam adı                                                | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| İşten Çıkarılmış Personel      | Çıkartılan çalışanlar, çıkartılma tarihi, başlık, konum ve iş                      | Şirket, Coğrafi Konum, Personel Adı, Kime Rapor Verdiği, Takvim Kaydırma, Tarih, Personel Unvanı, Demografi, Çalışma, İş, Pozisyon |
| Personel Adı            | Adı, ikinci ad ve tam adı                                                | Geçerli Çalışan, Sonlandırılan Personel, Personel Eğilimi |
| Personel Unvanı           | Başlık ve kıdem tarihi                                                            | Geçerli Personel, Sonlandırılan Personel, Personel Eğilimi |
| Personel Eğilimi           | Zaman içerisinde çalışanlar, çalışan sayısı, şirket ve konum                                 | Şirket, Coğrafi Konum, Personel Adı, Kime Rapor Verdiği, Takvim Kaydırma, Tarih, Personel Unvanı, Demografi, Çalışma, İş |
| Toplu İşe Alma Projesi        | Toplu işe alma projelerinin, proje sahibinin ve proje durumunun sayısı                     | Şirket, Toplu İşe Alma Satırı |
| Toplu İşe Alma Satırı           | Departman, iş türü ve pozisyon                                           | Tarih, İş, Toplu İşe Alma Projesi |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

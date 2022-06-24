---
title: Öğrenme Power BI içeriği
description: Bu makalede, Öğrenme Power BI içeriği açıklanmaktadır.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 05146eef92fa0ef973df832aa3431ec32ea0c297
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847325"
---
# <a name="learning-power-bi-content"></a>Öğrenme Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu makalede, **Öğrenme** Microsoft Power BI içeriği açıklanmaktadır.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan raporlar

**Öğrenme** Power BI içeriği içinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                | İçindekiler |
|-----------------------|----------|
| Öğrenme Genel Bakışı     | Diğer raporların özeti |
| Kurs Analizi       | Konuma göre kayıt, duruma göre katılımcı, şirket başına türe göre kurslar, işe göre kurs katılımı |
| Kayıt Analizi | Kayıt listesi |
| Kurs Türleri          | Yeteneğe göre kurs türleri |
| Eğitmen Analizi   | Eğitmenlere kurs oranı, eğitmen sayısı, eğitmene göre kurslar, eğitmen başına kurslar ve eğitmene göre kurs ajandası |
| Sunulan Kurslar       | Kursların listesi |
| Kursların Tasarımı        | Kurs ajandası |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve Yapılandırma](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama

Aşağıdaki veriler **Öğrenme** Power BI içeriğindeki raporları doldurmak için kullanılır. Bu tablo, içeriğin üzerine dayandırıldığı varlıkları gösterir.

| Varlık           | İçindekiler                                                         | Diğer varlıklarla ilişkiler |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Takvim Kaydırma  | Raporları dilimlemek için takvim kaydırmaları                                | Kurs Ajandası, Kurs Katılımcıları |
| Şirket          | Raporların filtreleneceği şirketler                                   | Kurs Ajandası, Kurs Katılımcıları |
| Kurs           | Kurs, açıklama, eğitmen adı, konum, yer ve durum | Kurs Ajandası, Kurs Katılımcıları, Kurs Yeteneği |
| Kurs Ajandası    | Gündem, kurs, başlangıç ve bitiş saatleri                          | Şirket, Kurs Kaydırması, Tarih, Kurs |
| Kurs Katılımcıları | Ad, durum, iş ve kayıt tarihi                         | Şirket, Takvim Kaydırması, Tarih, Kurs, Demografi, İş Durumu, Kurs, Personel Adı, Personel Unvanı, İş Pozisyonu |
| Kurs Yeteneği     | Beceri, beceri türü ve düzey                                     | Kurs |
| Tarih             | Günler, haftalar, aylar ve yıllar                                   | Kurs Ajandası, Kurs Katılımcıları |
| Demografi     | Doğum tarihi, cinsiyet, etnik köken ve medeni hal         | Kurs Ajandası, Kurs Katılımcıları |
| İstihdam       | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                        | Kurs Ajandası, Kurs Katılımcıları |
| İş              | İşlev, tür ve başlık                                        | Kurs Ajandası, Kurs Katılımcıları |
| Bölme         | Pozisyon, unvan ve tam zamanlı eşdeğeri (FTE)                  | Kurs Ajandası, Kurs Katılımcıları |
| Personel Adı    | Adı, ikinci ad ve tam adı                             | Kurs Katılımcıları |
| Personel Unvanı   | Başlık ve kıdem tarihi                                         | Kurs Katılımcıları |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: "Kurumsal eğitim Power BI içeriği"
description: "Bu konu Finance and Operations - Kurumsal eğitim Power BI içeriğini açıklar."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 6c1855013dc449950877f8727a5453942aeb75de
ms.contentlocale: tr-tr
ms.lasthandoff: 08/13/2018

---

# <a name="organizational-training-power-bi-content"></a>Kurumsal eğitim Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu Finance and Operations - Kurumsal eğitim Power BI içeriğini açıklar.

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İçerik paketini Finance and Operations verinize bağladıktan sonra, raporlar kuruluşunuzun verilerinde görünür. Daha önce hiç Microsoft Power BI kullanmadıysanız daha fazla bilgiyi [Power BI için Destekli Öğrenme sayfasından](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) edinebilirsiniz. İçerik paketinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor          | İçindekiler                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurs Analizi | Konuma göre kayıt, duruma göre kurs katılımcıları ve kayıt listesi |
| Kurs Türleri    | Yeteneğe göre kurs türleri                                                       |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Finance and Operations verisi, Kurumsal eğitim içerik paketindeki raporları doldurmak için kullanılır. Aşağıdaki tablo, içerik paketinin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                    | İçindekiler                                                         | Diğer varlıklarla ilişkiler |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Eğitim\_CalendarOffset  | Raporları dilimlemek için takvim kaydırmaları                                | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees |
| Eğitim\_Şirket         | Raporların filtreleneceği şirketler                                   | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees |
| Eğitim\_Kurs          | Kurs, açıklama, eğitmen adı, konum, yer ve durum | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees, Eğitim\_CourseSkill |
| Eğitim\_CourseAgenda    | Gündem, kurs, başlangıç ve bitiş saatleri                          | Eğitim\_Company, Eğitim\_CalendarOffset, Eğitim\_Date, Eğitim\_Course |
| Eğitim\_CourseAttendees | Ad, durum, iş ve kayıt tarihi                         | Eğitim\_Company, Eğitim\_CalendarOffset, Eğitim\_Date, Eğitim\_Demographics, Eğitim\_Employment, Eğitim\_Course, Eğitim\_WorkerName, Eğitim\_WorkerTitle, Eğitim\_Job, Eğitim\_Position |
| Eğitim\_CourseSkill     | Beceri, beceri türü ve düzey                                     | Eğitim\_Kurs |
| Eğitim\_Tarih            | Günler, haftalar, aylar ve yıllar                                   | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees |
| Eğitim\_Demografi    | Doğum tarihi, cinsiyet, etnik köken ve medeni hal         | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees |
| Eğitim\_İstihdam      | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                        | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees |
| Eğitim\_İş             | İşlev, tür ve başlık                                        | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees |
| Eğitim\_Pozisyon        | Pozisyon, unvan ve tam zamanlı eşdeğeri (FTE)                  | Eğitim\_CourseAgenda, Eğitim\_CourseAttendees |
| Eğitim\_WorkerName      | Adı, ikinci ad ve tam adı                             | Eğitim\_CourseAttendees |
| Eğitim\_WorkerTitle     | Başlık ve kıdem tarihi                                         | Eğitim\_CourseAttendees |


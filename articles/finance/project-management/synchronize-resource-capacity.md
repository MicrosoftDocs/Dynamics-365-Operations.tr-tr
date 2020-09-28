---
title: Kaynak kapasitesini eşitleme
description: Bu konu, bir kaynağın takvimler ve projelerde kapasitesini eşitleme hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760682"
---
# <a name="synchronize-resource-capacity"></a>Kaynak kapasitesini eşitleme

[!include [banner](../includes/banner.md)]

Kaynak eşitleme işlemleri, takvim ve temel takvim bilgilerini, proje kaynak planlamasına doğru çekilmesinin sağlanmasına yardımcı olur. Takvim değiştirilse, işlemler proje kaynak planlama için gerekli güncelleştirmeleri yapar. İşlemler performansı iyileştirmeye yardımcı olur çünkü takvimin kaynak bilgisi önceden eşitlenir. Bu nedenle, kaynak zamanlama bilgisine güncelleştirmeler daha hızlı gerçekleşir. İşlemleri tek tek planlamak yerine toplu iş olarak planlamanızı öneririz. Aksi halde, birisinin bilgiler son eşitlendiğinde dahil edilen tarihleri unutma riski vardır. Dahil olan tarihler kullanılmazsa, tarih eşitleme sırasında boşluklar oluşabilir.

![Takvim eşitleme](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Kaynak kapasite toplamlarını eşitle

Eşitleme işlemi, tüm kaynak takvim bilgilerini eşitlemek üzere tasarlanmıştır. Bu bilgiler, projenin Kaynak takvimi kapasite tablosundaki değişikliklerle ilgili temel takvim bilgilerini içerir. Projeye yeni kaynaklar eklenirse, eşitleme güncellenen takvim bilgilerinin kullanılmasının sağlanmasına yardımcı olur. Eşitleme herhangi bir zamanda yapılabilir.

Toplu iş kullanmanızı öneririz. Eşitleme sırasında kapasite rezervasyonunda seçenekler bulunmaktadır.

1. **Proje yönetimi ve muhasebe** &gt; **Periyodik** &gt; **Kapasite eşitleme** &gt; **Kaynakların kapasite toplamlarını eşitle**'yi seçin.
2. Aşağıdaki tabloda seçenekleri ayarlayın.

    | Seçenek      | Tanım |
    |-------------|-------------|
    | Dönem kodu | İsteğe bağlı olarak Genel muhasebe tarihi aralık kodunu, kaynak kapasite yuvarlamaları için eşitleme işlemi için başlangıç ve bitiş tarihlerini ayarlamak için seçin. |
    | Başlangıç tarihi  | Kaynak kapasite yuvarlamaları için eşitleme işlemi için başlangıç tarihini girin. |
    | Bitiş tarihi    | Kaynak kapasite yuvarlamaları için eşitleme işlemi için bitiş tarihini girin. |

[![Eşitleme işlemi](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

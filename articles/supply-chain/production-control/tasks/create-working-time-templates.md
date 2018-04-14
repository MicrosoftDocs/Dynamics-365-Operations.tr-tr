--- 
title: "Çalışma süresi şablonları oluşturma"
description: "Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-working-time-templates"></a>Çalışma süresi şablonları oluşturma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Çalışma zamanı şablonları bir haftalık çalışma saatlerini tanımlar ve bir dönem için çalışma zamanları oluşturmak için kullanılır. Bu yordam, çalışma zaman aralıklarını kategorilere ayırmak için çalışma zamanı planlama özelliklerini kullanarak bir çalışma zamanı şablonunun nasıl tanımlanacağını gösterir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.

1. Tüm çalışma alanları > Kaynak yaşam döngüsü yönetimi'ne gidin.
2. Çalışma zamanı şablonları'nı tıklatın.

## <a name="create-working-time-template"></a>Çalışma zamanı şablonu oluşturma
1. Yeni'ye tıklayın.
2. Çalışma zamanı şablonu alanında bir değer girin.
3. İsim alanına bir değer yazın.
4. Pazartesi bölümünü genişletin.
5. Ekle öğesini tıklatın.
6. Başlangıç alanında bir saat girin.
    * İşin sabah başlayacağı saati belirtin.  
7. Bitiş alanında bir saat girin.
    * Çalışanların öğle yemeği saatini belirtin.  
8. Ekle öğesini tıklatın.
9. Başlangıç alanında bir saat girin.
    * Öğle yemeğinin ardından işin başlayacağı saati belirtin.  
10. Bitiş alanında bir saat girin.
    * İşin bitiş tarihini belirtin.  

## <a name="replicate-working-times-to-all-week-days"></a>Çalışma saatlerini haftanın tüm günleri için çoğaltma
1. Günü kopyala'yı tıklatın.
    * Çalışma saati tanımlarını Pazartesi gününden Salı gününe kopyalayın.  
2. Tamam'a tıklayın.
3. Günü kopyala'yı tıklatın.
    * Çalışma saati tanımlarını Pazartesi gününden Çarşamba gününe kopyalayın.  
4. Hafta içi bitiş tarihi alanında bir seçenek belirleyin.
5. Tamam'a tıklayın.
6. Günü kopyala'yı tıklatın.
    * Çalışma saati tanımlarını Pazartesi gününden Perşembe gününe kopyalayın.  
7. Hafta içi bitiş tarihi alanında bir seçenek belirleyin.
8. Tamam'a tıklayın.
9. Günü kopyala'yı tıklatın.
    * Çalışma saati tanımlarını Pazartesi gününden Cuma gününe kopyalayın.  
10. Hafta içi bitiş tarihi alanında bir seçenek belirleyin.
11. Tamam'a tıklayın.

## <a name="define-time-slots-for-special-operations"></a>Özel işlemler için zaman dilimi tanımlama
1. Cuma bölümünü genişletin.
2. Listede, istenen kaydı bulun ve seçin.
3. Özellik alanında bir değer girin veya bir değer seçin.
4. Listede, istenen kaydı bulun ve seçin.
5. Özellik alanında bir değer girin veya bir değer seçin.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Haftasonlarını malzeme çekme için kapatıldı olarak işaretleme
1. Cumartesi bölümünü genişletin.
2. Malzeme çekme için Kapatıldı alanında Evet seçeneğini belirleyin.
3. Pazar bölümünü genişletin.
4. Malzeme çekme için Kapatıldı alanında Evet seçeneğini belirleyin.



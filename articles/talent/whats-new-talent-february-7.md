---
title: Dynamics 365 for Talent'daki yenilikler veya değişiklikler (7 Şubat 2019)
description: Bu konuda, Microsoft Dynamics 365 for Talent'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b89fc15130755a80b56f26cf7c61674a26f43e36
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519280"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a>Dynamics 365 for Talent'daki yenilikler veya değişiklikler (7 Şubat 2019)

[!include [banner](includes/banner.md)]

Bu konuda, Talent'daki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

### <a name="interview-scheduling-enhancements"></a>Mülakat zamanlama geliştirmeleri
Uçtan uca görüşme deneyiminde iyileştirmeler yapılmıştır. Şimdi bir dahili adayın takvim uygunluğunu görebilir ve dahili adayın takvimini zamanlama önerileri için kullanabilirsiniz. Daha fazla bilgi için bkz. [Mülakat zamanlama ve geribildirim](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>LinkedIn'e iş ilanı verme - şirket eşleştirme sorunu düzeltildi
LinkedIn'e Attract'ten açılan iş ilanlarının yanlış şirket adı altında görüntülendiği bir sorun çözülmüştür. Daha fazla bilgi için bkz. [Attract için iş ilanları oluştur, onayla ve yayınla](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Yönetici ayarlarında kariyer sitesi URL'si
Kariyer sitesi ana sayfa URL'si şimdi **Kariyer Sitesi yönetimi** altında **Yönetici Ayarları** içinde görüntülenmektedir.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

**Derleme 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>İşlerde çoklu ücret düzeyleri desteklenmektedir
Bu değişiklik bir iş üzerinde birden fazla ücret seviyesinin tanımlanmasına izin vererek, çalışan sabit ücret aralıklarını etkinleştirmeyi sağlar ve bunlar aynı işi kullanırken planlar arasında fark gösterebilir. 

Örneğin:    
*İş* - Hesap Yöneticisi *İlişkilendirilmiş ücret düzeyleri:* B1 ve B2 - Her bir düzeyin tanımlanmış aralık değeri vardır. B1 = Min 50.000, Orta 60.000, Maks 75.000 ve B2 = Min 65.000, Orta 74.000, Maks 85.000. Çalışanlar için sabit ücret oluştururken, tanımlanan uygunluk kurallarına dayanarak her bir sabit plan şimdi aynı işe ve iş üzerindeki farklı düzeylere işaret edebilir. Bu, planların farklı bölgeler/şirketler içinde tanımlanmasına ve aynı işe ancak farklı aralıklara, bu farklılıkları hesaba katmak için işleri yinelemeden işaret etmesine olanak verir.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Ücret düzeyi alanı, Personel sabit ücret varlığına eklenmiştir 
Bu güncelleştirme ile personel sabit ücret varlığı **Ücret düzeyi** alanını dahil etmek üzere güncelleştirilmiştir. Bu eklenti, personel sabit ücret planlarını güncelleştirmeyi kolaylaştırır. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Yeni pozisyonlar güncelleştirirken ve oluştururken İş ailesini yükseltme
Bir pozisyondaki işi değiştirirken **İş ailesi** şimdi seçilen işe varsayılan olur.

### <a name="performance-improvements-when-rendering-workspaces"></a>Çalışma alanlarını oluştururken performans iyileştirmeleri
Çalışma alanlarındaki analiz sekmeleri artık yalnızca bu sayfalara erişirken yüklenir. Bir gösterge, sayfanın ilk oluşturulması sırasında sayfanın sol üst köşesinde görüntülenecektir.

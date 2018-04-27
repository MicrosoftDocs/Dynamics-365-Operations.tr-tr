--- 
title: "Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanana bir biçimi çalıştırma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2d705d0d2803b5254adc27e6715c1eac311898a7
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a>Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanana bir biçimi çalıştırma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar. Bu adımlar DEMF şirketinde gerçekleştirilebilir.

Bu adımları tamamlamak için öncelikle "ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 1: Biçimi tasarlama)" yordamındaki adımları tamamlamalısınız.

Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.


## <a name="find-created-format"></a>Oluşturulan biçimi bulma
1. Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.
2. Ağaçta, 'Mali boyutlar örnek modeli' öğesini genişletin.
3. Ağaçta, "Mali boyutlar örnek modeli\Yatay olarak genişletilebilir aralıklarla örnek rapor" öğesini seçin.

## <a name="execute-format-to-create-excel-output"></a>Excel çıktısı oluşturmak için biçimi yürütme
1. Çalıştır öğesine tıklayın.
2. Boyut adı alanına "BusinessUnit;CostCenter;Department" yazın.
    * Boyut adı alanına bir değer girin veya seçin.  Geçerli şirket için tüm boyutları seçmek için şunları girin:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
3. Eklenecek kayıtlar bölümünü genişletin.
4. Filtre'ye tıklayın.
5. Genel muhasebe günlük tablosu satırını ve Günlük toplu iş numarası alanını seçin.
6. Ölçütler alanına "00057..00058" yazın.
    * 00057..00058  
7. Tamam'a tıklayın.
8. Tamam'a tıklayın.
    * Ortaya çıkan sonucu inceleyin. Yeni oluşturulan Excel dosyasının mali boyutlar için seçilen ile aynı sayıda sütun içerdiğini unutmayın. Bu sütunlardaki rapor başlığı mali boyutların adlarını temsil eder. Bu sütunlardaki hareketlerin satırları mali boyutları temsil eder. Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu , Dynamics 365 for Finance and Operations kurulumu için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.  



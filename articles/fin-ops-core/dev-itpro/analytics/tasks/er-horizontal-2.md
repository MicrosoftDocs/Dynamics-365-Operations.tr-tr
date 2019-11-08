---
title: ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 2 - Biçimi çalıştırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, gerekli sütunların yatay olarak genişletilebilir aralıklar şeklinde oluşturulabileceği OPENXML çalışma sayfası (Excel) dosyaları şeklinde raporlar oluşturmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b76a2df5cd7714ffda6d0563d3d9013f032db7c2
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550894"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma (Bölüm 2 - Biçimi çalıştırma)

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    * Ortaya çıkan sonucu inceleyin. Yeni oluşturulan Excel dosyasının mali boyutlar için seçilen ile aynı sayıda sütun içerdiğini unutmayın. Bu sütunlardaki rapor başlığı mali boyutların adlarını temsil eder. Bu sütunlardaki hareketlerin satırları mali boyutları temsil eder. Bu raporu çalıştırın ve raporun seçili boyutların sayısına veya bu kurulum için yapılandırılmış boyutların sayısına bağlı olmadığını görmek için farklı boyutlar seçin.  


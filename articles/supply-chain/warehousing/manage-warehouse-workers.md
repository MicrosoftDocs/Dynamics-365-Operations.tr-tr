---
title: Ambar çalışanlarını yönetme
description: Bu makalede, ambar uygulamasını ambarlarınızdaki çalışanlarca yürütülen işi denetlemeye ve izlemeye yardımcı olacak şekilde nasıl kullanabileceğiniz açıklanmaktadır.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage, WHSResetUserPassword
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2156b5de6abc3751cae1822b3825acbbd0b9a712
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017104"
---
# <a name="manage-warehouse-workers"></a>Ambar çalışanlarını yönetme

[!include [banner](../includes/banner.md)]

Bu makalede, ambar uygulamasını ambarlarınızdaki çalışanlarca yürütülen işi denetlemeye ve izlemeye yardımcı olacak şekilde nasıl kullanabileceğiniz açıklanmaktadır.

Ambar yönetimindeki işlevleri kullanıyorsanız, tüm ambar çalışan operasyonları *iş* olarak adlandırılır. Çekme, taşıma ve eldeki stokun sayımı gibi işler mobil cihazlar kullanılarak kaydedilir. Bir ambar çalışanı işi yapmadan önce, İnsan Kaynakları'ndaki bir çalışan ile ilişkilendirilmiş olması gerekir. Her **Çalışan** hesabının, bu hesapla ilişkilendirilmiş birden çok ambar işi kullanıcısı olabilir. Bu iş kullanıcıları farklı ambarlarda çalışabilir ve çeşitli mobil cihaz menülerine farklı düzeylerde erişimleri olabilir. Ambar iş kullanıcılarını seçili çalışanın birden çok oturum açması gibi düşünebilirsiniz. Her iş kullanıcısının varsayılan bir ambarı vardır ve belirli iş akışları, o iş kullanıcısı tarafından kullanılabilen menü öğeleri ile ortaya çıkarılır. 

Yeni bir iş kullanıcısı oluşturmak için, **Çalışanlar** sayfasında, **Genel** öğesinde **Ambarlar** bölümünde, **Çalışan** öğesine tıklayın. Bir kullanıcı kimliği, kullanıcı adı, bir varsayılan ambar ve menü adı belirtmeniz gerekir. Bu menü, kullanıcı Ambar Mobil Cihaz Portalı'na giriş yaptığında yüklenir ve size kullanıcının erişebileceği menü öğelerini tanımlama olanağı verir. 

Her iş kullanıcısına ilişkin kurulum işleminin bir parçası olarak, belirli işlem iş akışları da tanımlayabilirsiniz. Örneğin, kullanıcının bir sayım işlemi sırasında döngü sayımı uyuşmazlıklarına işlem ayarlamaları yapıp yapamayacağını veya bu ayarlamaların önce başka bir kişi tarafından gözden geçirilmesinin gerekli olup olmadığını belirlemek için **Bir döngü sayım gözetmenidir** alanını kullanabilirsiniz.

## <a name="defining-labor-standards"></a>İşgücü standartlarını tanımlama
**İşgücü standartlarına** sayfası, sistemin belirli bir iş türüne gereksinim duyduğunuz tahmini süreyi hesaplamak için kullandığı hesaplama yöntemlerini tanımlamanıza olanak sağlar. Bu tanım genel düzeyde veya belirli bir düzeyde ayarlanabilir. Örneğin, belirli çekme işlemi kullanıldığında, belirli bir birim tanımı için ağırlık başına satış siparişi çekme işlemini gerçekleştirmek amacıyla gerekli olması gereken süreyi tanımlayabilirsiniz. Aynı zamanda, çekilen eldeki stokun indirme işlemi için, başka bir hesaplama yöntemine dayanarak zamanı kaydedebilirsiniz. 

Tanımladığınız işgücü standartlarını etkinleştirmek için, işgücü standartlarının kullanılacağı her ambar için **İşgücü standartlarına izin ver** seçeneğini seçmeniz gerekir.

## <a name="monitoring-and-controlling-warehouse-work"></a>Ambar işini izleme ve denetleme
**Tüm işler** sayfası planlanan, devam eden ve tamamlanan tüm işleri izleme ve sürdürme olanağı verir. Bu sayfadan, ambar iş kullanıcısı atamaları ve iş öncelikleri gibi çeşitli işlemleri güncelleştirebilirsiniz. Ayrıca beklenen veya tamamlanan iş süreçlerini anlamak için iş başlığı ve iş satırları ile ilgili ayrıntılara da inebilirsiniz. 

**İşgücü standartları** seçeneğini etkinleştirirseniz, iş için hesaplanan tahmini süreyi görebilirsiniz. Daha sonra iş işlendiğinde, gerçek zaman da her iş operasyonu için gösterilecektir. Bu şekilde, tahmini süre hesaplamalarını gerçek süre ile karşılaştırabilirsiniz. 

Ayrıca, iş oluşturma sırasında işi otomatik olarak bölme kurallarındaki tahmin edilen süreyi kullanabilirsiniz. Bu şekilde, görevleri tamamlamak için beklenen süreye göre bakiye işini yükleyebilirsiniz. 

İş öğelerini işlemek için kullanılan süreni analizi ambar çalışanlarının verimliliğini arttırmaya yardımcı olabilir. Bu analize yardımcı olmak üzere aşağıdaki raporlar mevcuttur:

-   **Kullanıcı tarafından işgücü** – Bu raporda, beklenen sürelere karşı gerçek sürelere göre çalışan verimliliği gösterilir.
-   **İş hareket türüne göre işgücü** – Bu raporu belirli ambar işlemlerindeki verimsizlikleri araştırmak için kullanabilirsiniz. Örneğin, transfer siparişleri için çekmelerin bu hafta önceki haftadan daha uzun süreceği dikkatinizi çekti. Daha sonra bu bilgiyi daha ileri düzeyde araştırma için kullanabilirsiniz.





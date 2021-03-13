---
title: Ödeme faturaları oluşturma
description: Bu konuda, aylık kiralama faturalarının nasıl oluşturulacağı açıklanmaktadır. Kiralamalar için ayrı ayrı fatura oluşturabilir veya birden fazla kiralama için faturalar oluşturmak için toplu iş işlemini kullanabilirsiniz.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969590"
---
# <a name="create-payment-invoices"></a>Ödeme faturaları oluşturma

[!include [banner](../includes/banner.md)]

Kiralamalar için ayrı ayrı aylık fatura oluşturabilir veya birden fazla kiralama için faturalar oluşturmak için toplu iş işlemini kullanabilirsiniz. Aşağıdaki yordamda, **Kiralama defteri kurulumu** sayfasındaki **Satıcıya Öde** parametresi açıldığında tek bir kira ödemesi girişinin nasıl oluşturulacağı gösterilmektedir.

1. **Kiralama özeti** sayfasında bir kiralama seçin ve ardından **Defterler \> Ödeme planı**'nı seçin.
2. Yapılması gereken ödemeyi seçin ve ardından **Günlük oluştur**'u seçin. Seçili ödemeyle ilgili bir günlüğün oluşturulduğunu bildiren bir ileti alırsınız.
3. **Fatura günlükleri**'ni seçin ve ardından ödenmesi gereken faturayı seçin.
4. **Satırlar** sekmesinde, günlük girişini genel muhasebe defterine nakletmeden önce gözden geçirin.

    > [!NOTE]
    > Varsayılan olarak, oluşturulan satıcı faturası satırları **Borç hesapları parametreleri** sayfasındaki satıcı deftere nakil profilini kullanır.

5. Doğru günlüğü seçin ve ardından ödenmesi gereken faturayı seçin.

    Bu örnekte, kiralama defterine **Satıcıya Öde** parametresi açıktır. Bu nedenle, fatura fatura günlüğünde olacaktır. **Genel Bakış** bölümü günlük girişinin özetini gösterir ve **Satırlar** bölümü, gerçek günlük satırlarının ayrıntılarını gösterir.

    > [!NOTE]
    > **Satıcıya Öde** parametresi kapalıysa ödeme günlüğü girişleri kiralama defteri için **Varlık kiralama** sayfasında listelenir ve sistem fatura yerine bir varlık kiralama girişi oluşturur. Kira ödemesi girişi, **Aylık kiralama günlüğü** alanındaki günlük adına deftere nakledilir.

6. Hareket deftere nakledildikten sonra kiralama defterinde **Yükümlülük hareketleri**'ni seçerek hareket bilgilerini ve kiralama yükümlülüğünün defter değerini görüntüleyebilirsiniz.

    Ödeme planında, **Günlük deftere nakledildi** onay kutusu seçili olur ve satırda fatura günlük numarası gösterilir. Ödeme günlüğü ve söz konusu günlük için bir giriş oluşturulduktan sonra, yeniden oluşturulabilmesi için girişi tersine çevirmeniz gerekir.
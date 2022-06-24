---
title: Deftere nakledilen kira hareketlerini ters kaydetme
description: Bu makalede, deftere nakledilen bir kira hareketinin nasıl ters kaydedilebileceği açıklanmaktadır. Varlık Kiralama üzerinden oluşturulan tüm hareketler için ters kayıt oluşturulabilir.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4f23b6cca6ddf4da7a0232a5bc61785dbd451d55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908081"
---
# <a name="reverse-posted-lease-transactions"></a>Deftere nakledilen kira hareketlerini ters kaydetme

[!include [banner](../includes/banner.md)]

Varlık Kiralama üzerinden oluşturulan tüm hareketler için ters kayıt oluşturulabilir. Varlık kiralama aracılığıyla tersine çevrilen hareketler kiralama verilerinizi güncelleştirir. Bu nedenle, kiralama yükümlülüğün ve kullanım hakkı (ROU) varlığının defter değerlerini de güncelleştirirler.

Bir kiralamanın ters kaydedilen hareketini oluşturmak için aşağıdaki adımları izleyin.

1. **Varlık hareketleri** sayfası veya **Yükümlülük hareketleri** sayfasında hareketi seçin ve ardından **Ters hareket**'i seçin.
2. Görüntülenen iletişim kutusunda, ters kaydedilen girişinin deftere nakledileceği tarihi düzenleyebilirsiniz. Varsayılan olarak, **Tarih** alanı seçtiğiniz hareketin hareket deftere nakil tarihine ayarlanır. Ters kaydedilen giriş, seçili hareketin asıl deftere nakil tarihinden daha önceki bir tarihle deftere nakledilemez.
3. **Tamam**'ı seçin. Seçtiğiniz girişi tersine çeviren bir günlük girişi deftere nakledilir. Ters kayıt işlemi, **Varlık hareketleri** veya **Yükümlülük hareketleri** sayfasında gösterilir ve sayfada gösterilen geçerli bakiyenin net toplamı güncelleştirilir.

**Ters kayıt izleme**'yi seçtiğinizde, hem orijinal hareketleri, hem de ters kayıt hareketlerini, *izleme numarası* olarak bilinen bağlı bir sayıyla birlikte gösteren bir iletişim kutusu görüntülenir. Ters kayıtların daha iyi anlaşılması ve görünürlüğün artması için kira planlarını kullanarak da ters kayıtları izleyebilirsiniz.

**Planlama** sayfasındaki **En son günlük numarası** alanı hareketlerin günlük numaralarını gösterir. Bir hareket ters kaydedildiğinde, bu alan ters kaydedilen hareketin günlük numarasıyla güncelleştirilir. Ayrıca, hareketin ters kaydedildiğini gösteren **Ters kaydedildi** onay kutusu ile **Deftere nakledildi** alanı seçilidir.

## <a name="revoke-a-reversed-transaction"></a>Ters kaydedilen hareketi iptal etme

Tersine kaydedilen hareketi iptal etmek için aşağıdaki adımları izleyin.

1. **Planlama** veya **Hareketler** sayfasında orijinal hareketi seçin.
2. Şu adımlardan birini izleyin:

    - Hareketi **Planlama** sayfasında seçtiyseniz [Toplu işte aylık günlük girişleri oluşturma](create-monthly-journals-batch.md) konusundaki günlük oluşturma adımlarını izleyin. Günlüğü el ile deftere nakletmeniz gerekir.
    - Hareketi **Hareketler** sayfasında seçtiyseniz **Ters hareket**'i seçin. Bu iptal işleminin daha önceki bir ters kayıt işleminin iptali olduğunu ve bu iptal işlemi için deftere nakil tarihini düzenleyebileceğinizi bildiren bir ileti alırsınız. Ancak, genel iş doğrulamaları **Tarih** alanına girilebilecek tarihleri etkiler. 

3. **Tamam**'ı seçin. Seçtiğiniz girişi tersine çeviren bir günlük girişi deftere nakledilir. Ters kayıt **Hareketler** sayfasında gösterilir ve net toplam geçerli bakiyesi ilk ters kayıt işleminden önceki durumuna geri yüklenir. Böylece, ters kayıt işleminin bakiyelerdeki etkisi kaldırılmış olur.

**Ters kayıt izleme**'yi seçtiğinizde, hem orijinal hareketleri, hem de ters kayıt hareketlerini, bağlı izleme numarasıyla birlikte gösteren bir iletişim kutusu görüntülenir.

İlgili **Planlamalar** sayfasını kullanarak iptal işlemlerini de izleyebilirsiniz. **Ters kayıt** alanının işareti kaldırılmış, **Günlük deftere nakledildi** alanı seçilidir. Ayrıca, **En son günlük numarası** alanı iptal hareketinin günlük numarasıyla güncelleştirilir ve **Günlük numarası** alanı ters kayıt günlük numarasıyla güncelleştirilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

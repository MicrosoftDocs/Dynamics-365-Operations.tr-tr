---
title: Common Data Service'da şirket kavramı
description: Bu konu, Finance and Operations ve Common Data Service arasındaki şirket verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9a39cf5fa980d9a815ba675e410589dbd1279c83
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172912"
---
# <a name="company-concept-in-common-data-service"></a>Common Data Service'da şirket kavramı

[!include [banner](../../includes/banner.md)]


Finance and Operations'da *şirket* kavramı hem yasal bir yapı hem de bir işletme yapısıdır. Ayrıca veriler için bir güvenlik ve görünürlük sınırıdır. Kullanıcılar her zaman tek bir şirket bağlamında çalışır ve verilerin çoğu şirket tarafından çıkarılır.

Common Data Service'da eşdeğer bir kavram yoktur. En yakın kavram, birincil olarak kullanıcı verileri için bir güvenlik ve görünürlük sınırı olan *iş birimidir*. Bu kavram, şirket kavramıyla aynı yasal veya iş etkilerine sahip değildir.

İş birimi ve şirket eşdeğer kavramlar olmadığından, Common Data Service tümleştirmesi amacıyla aralarında bire bir (1:1) eşlemesini zorlamak mümkün değildir. Ancak, kullanıcılar varsayılan olarak, uygulamada ve Common Data Service'da aynı kayıtları görebilmelidir; bu nedenle Microsoft, Common Data Service'da cdm\_Şirket adlı yeni bir varlık tanıttı. Bu varlık uygulamadaki Şirket varlığına eşdeğerdir. Kayıtların görünürlüğünün uygulamak ve Common Data Service'ta eşdeğer olmasını sağlamaya yardımcı olmak için, Common Data Service'da aşağıdaki veri ayarının yapılmasını öneriyoruz.

+ Çift yazma için etkinleştirilmiş her Finance and Operations Şirket kaydı için, ilişkili bir cdm\_Şirket kaydı oluşturulur.
+ cdm\_Şirket kaydı oluşturulduğunda ve çift yazma için etkinleştirildiğinde, aynı ada sahip bir varsayılan iş birimi oluşturulur. Bu iş birimi için otomatik olarak varsayılan bir ekip oluşturulsa da, iş birimi kullanılmaz.
+ Aynı ada sahip ayrı bir sahip olan takım oluşturulur. Ayrıca iş birimi ile de ilişkilidir.
+ Varsayılan olarak, oluşturulan ve Common Data Service'a çift yazılan herhangi bir kaydın sahibi, ilişkili iş birimine bağlı "DW Sahibi" ekibine ayarlanır.

Aşağıdaki şekilde, Common Data Service'daki bu veri ayarının bir örneğini gösterir.

![Common Data Service'da veri ayarı](media/dual-write-company-1.png)

Bu yapılandırma nedeniyle, USMF şirketiyle ilgili herhangi bir kayıt, Common Data Service'daki USMF iş birimine bağlı olan bir takıma ait olacaktır. Bu nedenle, iş birimi düzeyinde görünürlük için ayarlanan bir güvenlik rolü aracılığıyla bu iş birimine erişimi olan herhangi bir kullanıcı artık bu kayıtları görebilir. Aşağıdaki örnek, takımlara bu kayıtlara doğru erişimi sağlamak amacıyla nasıl kullanılabileceğini gösterir.

+ "Satış Yöneticisi" rolü "USMF Satış" takımı üyelerine atanır.
+ "Satış Yöneticisi" rolüne sahip kullanıcılar, üye oldukları aynı işi birimine üye olan hesap kayıtlarına erişebilir.
+ "USMF Satış" ekibi, daha önce bahsedilen USMF iş birimine bağlıdır.
+ Bu nedenle, "USMF Satış" ekibinin üyeleri Finance and Operations'taki USMF Şirket varlığından gelen "USMF DW" kullanıcısı tarafından sahip olunan herhangi bir hesabı görebilir.

![Ekipler nasıl kullanılabilir](media/dual-write-company-2.png)

Önceki örnekte gösterildiği gibi iş birimi, şirket ve ekip arasındaki bu 1:1 eşleme yalnızca bir başlangıç noktasıdır. Bu örnekte, yeni bir "Avrupa" iş birimi hem DEMF hem de ESMF için üst öğe olarak Common Data Service'ta el ile ayarlanır. Bu yeni kök iş birimi çift yazma ile ilgili değildir. Ancak, "EUR Satış" ekibinin üyelerine, ilgili güvenlik rolündeki **Üst/Alt İş Birimi** veri görünürlüğünü ayarlayarak hem DEMF hem de ESMF'deki hesap verilerine erişim vermek için kullanılabilir.

Tartışılması gereken son bir konu da çift yazmanın kayıtların sahip olan hangi takıma atayacağının nasıl belirlendiğidir. Bu davranış, cdm\_Şirket kaydındaki **Varsayılan sahibi olan takım** alanı tarafından denetlenir. Bir cdm\_Şirket kaydı çift yazma için etkinleştirildiğinde, bir eklenti otomatik olarak ilişkili iş birimi ve sahibi olan takımı (zaten yoksa) oluşturur ve **Varsayılan sahibi olan takım** alanını ayarlar. Yönetici bu alanı farklı bir değere değiştirebilir. Ancak, varlık çift yazma için etkinleştirildiği sürece yönetici alanı temizleyemez.

> [!div class="mx-imgBorder"]
![Varsayılan sahibi olan takım alanı](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Şirket bölümleme ve yeniden örnekleme

Common Data Service tümleştirmesi verileri bölümlemek için şirket tanımlayıcısını kullanarak şirket eşliği getirir. Aşağıdaki örnekte gösterildiği gibi, tüm şirkete özgü varlıklar, cdm\_Şirket varlığıyla çok-bir (N:1) ilişkisine sahip olmaları için genişletilir.

> [!div class="mx-imgBorder"]
![Şirkete özgü varlık ile cdm_Şirket varlığı arasındaki N:1 ilişkisi](media/dual-write-bootstrapping.png)

+ Kayıtlar için, bir şirket eklendikten ve kaydedildikten sonra, değer salt okunur olur. Bu nedenle, kullanıcılar doğru şirketi seçtiğinden emin olmalıdır.
+ Yalnızca şirket verilerine sahip kayıtlar uygulama ile Common Data Service arasında çift yazma için uygundur.
+ Var olan Common Data Service verileri için, yönetici tarafından yürütülen bir yeniden örnekleme deneyimi yakında kullanıma sunulacaktır.

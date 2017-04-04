---
title: Barkod maskesi ayarlama
description: "Bu konuda Barkod maskesi karakterleri, barkod maskeleri ayarlama yöntemi açıklanır ve nasıl bar kod atamak barkodlar için maskeler."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Barkod maskesi ayarlama

Bu konuda Barkod maskesi karakterleri, barkod maskeleri ayarlama yöntemi açıklanır ve nasıl bar kod atamak barkodlar için maskeler.

<a name="set-up-bar-code-mask-characters"></a>Barkod maskesi karakterlerini ayarlama
-------------------------------

Barkod maskeleri barkodlar oluşturmak ve satış (POS) Notasına taranan barkodları hızla tanımlamak için kullanılır. Oluşturulacak barkodlar biçimini gösteren yer tutucu olarak davranan karakterlerin maskeleri kapsar. Bar kod maskesi yapılandırmanız için bar kod maskesi karakterlerini ayarlamanız gerekir. Git **perakende ve ticaret**&gt;**Stok Yönetimi**&gt;**bar kodlar ve etiketler**&gt;**maske karakterleri**. ' I **yeni** Barkod maskesi karakterleri oluşturmak için. Maske karakterleri aşağıdaki barkod verileri göstermek için oluşturulabilir.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Ürün kimliği için yer tutucu                                                                                     |
| **Any number**       | Kodlanmış barkodları sabit olacak bir sayı belirtmek için kullanılır.                                                  |
| **Check digit**      | Bar kod maskesi barkod biçiminde bir barkod geçerliliğini doğrulamak için denetim hanesi kullandığını gösterir. |
| **Size digit**       | Boyutu içeren bir ürün değişken için oluşturulan bir barkod boyutunu belirtir.                                 |
| **Color digit**      | Oluşturulan renk içeren bir ürün değişken için bir barkod renkte gösterir.                               |
| **Style digit**      | Stil içeren bir ürün değişken için oluşturulan bir barkod stili belirtir.                             |
| **EAN license code** | EAN lisans kodları için verilen EAN lisans için yer tutucu.                                                       |
| **Fiyat**            | Fiyat embedded bar kodlar için fiyatı gösterir.                                                                   |
| **Quantity**         | Barkodları gömülü miktar/rasgele ağırlık miktarı gösterir.                                                |
| **Employee**         | Bar kod bölütü için Barkod POS oturum açma için kullanılan çalışan kimlik numarasını gösterir.                                  |
| **Customer**         | Müşteri Kimliği segment gösterir.                                                                                  |
| **Data entry**       | *Henüz uygulanmadı.*                                                                                          |
| **İskonto kodu**    | İndirim bir satış hareketi noktasına eklemek için kullanılan bir bar kod indirim kodunu gösterir.             |
| **Hediye kartı**        | Verme veya Hediye kartı ile ödemeye bir hediye kartı numarasını gösterir.                                               |
| **Bağlılık kartı**     | Bağlılık programı müşteri harekete ekler ve bağlılık programı tarafından ödenirken kullanılabilir.                             |

## <a name="define-bar-code-masks"></a>Bar kod maskesi tanımla
Barkod maskesi karakterleri için gerekli bar kod maskesi belirtilir, sonra Git **perakende ve ticaret**&gt;**Stok Yönetimi**&gt;**bar kodlar ve etiketler**&gt;**Barkod maskesi Kurulumu**. Bu sayfada, daha önce belirtilen karakterleri kullanan Barkod maskeleri tanımlayabilirsiniz. Bu maskeler barkodlar oluştururken kullanılacak ve kazandırır barkod POS'a taranan bar kodları tanımlamak için yardımcı olur.

1.  ' I **yeni** yeni bir bar kod maskesi oluşturmak için.
2.  Değerleri girin **maske kodu** ve **açıklama** alanları ve Barkod Maske türü seçin **türü** alan.
3.  İçinde **genel** bölümünde, bir değer seçin **barkod standardı** alan ve gerekliyse bar kod önekini belirtin.
4.  İçinde **Barkod Maske Segmenti** bölümünde, kullanılacak barkod parçaları oluşturulacak bar kod ekleyin.

Örnek olarak, maske kodu 'Ürün' ile bir bar kod maskesi oluşturmak için aşağıdakileri:

1.  Yeni bir bar kod maskesi oluşturun ve 'Ürün' türü seçin.
2.  Örneğin, 'Kod 39' bir barkod standardı seçin.
3.  Barkod kolayca tanımlamak için kullanılacak önek sağlar. Örneğin, '22'.
4.  Bir maske segmenti ekleyin. 'Ürün' Maske Segmenti seçilecektir.
5.  Uzunluğu, '10' ürün segment için sağlar. Depoda yaygın olarak kullanılan bir ürün kimliği uzunluğu uzunluk eşleşmesi gerekir. Maskeyi Önizleme'olarak görüntülenen **genel** altında bölümünde **maskesi**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Barkod maskeleri barkodlar atamak
Kullanılabilmesi için önce barkod maskeleri barkodlar için atanmış olması gerekir. Önceki örnekle devam etme bir barkod Barkod maskesi atamanız, aşağıdakileri yapın:

1.  Git **kuruluş yönetim**&gt;**Kurulum**&gt;**Bar Kodları**. ' I **yeni** yeni bir bar kod oluşturmak için.
2.  Değerleri girin **barkod****Kurulum** ve ** Kur ** alanları.
3.  İçinde **genel** bölümünde **barkod türü** alan, 'Kod 39' seçin. İçinde **maskesi****ID** alanında, önceden oluşturduğunuz 'Ürün' Maske'yi seçin.
4.  Altında **boyutu**, '12' girin.
5.  Click **Save**.

Bar kod maskesi şimdi ürünleri için barkodlar oluşturmak için kullanılabilir. Yukarıdaki adımları ürünlerin Barkod maskeleri oluşturmak nasıl bir örnektir, ancak bunlar aynı zamanda herhangi bir desteklenen barkod türleri için Barkod maskeleri oluşturmak nasıl göstermek. Barkod maskeleri, türleri ve uzunlukları belirli ortamınızda kullanmak için ayarlanması.



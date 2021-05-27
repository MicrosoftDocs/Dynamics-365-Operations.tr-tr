---
title: TaxTrans'ta hatalı alan değeri
description: Bu konu, TaxTrans'taki hatalı alan değerleriyle ilgili sorunları giderme hakkında bilgi sağlar.
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 488ff54f1dd99208db940024a2fe8b2d25861f44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020175"
---
# <a name="incorrect-field-value-in-taxtrans"></a>TaxTrans'ta hatalı alan değeri

[!include [banner](../includes/banner.md)]

**TaxTrans**'taki bir alan değeri yanlışsa, sorunu gidermeye çalışmak için bu konudaki bilgileri kullanın.

## <a name="overview-of-values"></a>Değerlere genel bakış
Aşağıdaki listede **TaxTrans**, **TaxUncommitted** ve **TmpTaxWorkTrans**'ın nasıl benzer veri kümeleri olduğu ancak farklı şekilde çalıştıkları anlatılmaktadır.

  - **TaxTrans**, veritabanında kalıcı, deftere nakledilen nihai vergi hareketi sonucudur.
  - **TaxUncommitted**, veritabanında (geçerliyse) kalıcı olan ve daha sonra deftere nakil için kullanılacak ortadaki hesaplanan vergi sonucudur.
  - **TmpTaxWorkTrans**, bellek içi tabloda (Tablo Türü = InMemory) geçici olarak hesaplanan vergi sonucudur.

Yanlış bir **TaxTrans** sütununun kök nedenini bulursanız, aynı zamanda yanlış **TaxUncommitted** veya **TmpTaxWorkTrans** sütununun da kök nedenini bulmuş olursunuz. Bunun nedeni, üç sütunun birbirinden kopyalanmasıdır.

Tipik olarak, vergi hesaplaması sırasında, **TmpTaxWorkTrans** oluşturulur ve daha sonra geçerliyse **TaxUncommitted** oluşturulur. Verginin deftere nakli sırasında, **TaxTrans** oluşturulur.


## <a name="add-breakpoints"></a>Kesme noktaları ekleme
Kesme noktaları eklemek için aşağıdaki adımları tamamlayın: 

1. Uzantılarda *insert()* ve *update()* içindeki uzantıları ve kesme noktalarını aşağıda gösterildiği gibi ekleyin.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Alternatif olarak, **TaxUncommitted** dahil olmadığında doğrudan kesme noktaları ekleyebilirsiniz.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Yeniden oluşturma ve hata ayıklama

Kesme noktaları ayarladıktan sonra, hata ayıklama sırasında her veri kalıcılığı değişikliği görünür. Yanlış bir **TaxTrans**, **TaxUncommitted** veya **TmpTaxWorkTrans** sütununun kök nedenini bulmak için, aşağıdaki hususları gözden geçirin ve not alın:

- Sütunun doğru olduğu son kesme noktası.
- Sütunun hatalı olduğu ilk kesme noktası.
- Bu iki nokta arasında ne gerçekleştiği.

## <a name="determine-whether-customization-exists"></a>Özelleştirme olup olmadığını belirleyin
Önceki bölümlerdeki adımları tamamladıysanız ve sorunu çözemediyseniz bir özelleştirme olup olmadığını belirleyin. Hiç özelleştirme yoksa yardım için Microsoft Desteğine başvurun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


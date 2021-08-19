---
title: Tahsilat mektuplarını işleme örneği
description: Bu konu, Tahsilat mektuplarının oluşturulması, yazdırılması ve deftere nakledilmesi sürecini gösteren bir örnek sunar.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fdde6ebaebf37a883aef0dcc3ea12909c3d43532d604ff78d708d737b26bc57e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721863"
---
# <a name="process-collection-letters-example"></a>Tahsilat mektuplarını işleme örneği

[!include [banner](../../includes/banner.md)]

Bu konu, Tahsilat mektuplarının oluşturulması, yazdırılması ve deftere nakledilmesi sürecini gösteren bir örnek sunar. Bu örnek, alacak ve tahsilatlardaki **tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneğini temel alır. USMF demo şirketinde bulunan verileri ve yeni bir müşteri olan US-045'i kullanır.

Başlamak için **Alacak hesapları \> müşteriler \> tüm müşteriler**'e gidin, **Yeni**'yi seçin ve sonra müşteri US-045'i oluşturmak için gerekli bilgileri girin.

Bitirdiğinizde aşağıdaki adımları izleyin.

1. **Alacak ve tahsilatlar \> tahsilat mektubu \> Tahsilat mektubu sırasına ayarla**'ya gidin  ve tahsilat mektubu sırasını, müşteri deftere nakil profiline atanan aşağıdaki tabloda gösterildiği şekilde ayarlayın.

|     Tahsilat mektubu kodu      |     Tanım                           |     Para Birimi      |     Ana hesap        |     Para birimi cinsinden ücret     |     En az        |     Bloklanan gün sayısı      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     Tahsilat mektubu 1         |     Ücretli ikinci bildirim        |     ABD Doları           |                           |     0,00                  |     0,00                  |     2                 |
|     Tahsilat mektubu 2         |     Ücretli ikinci bildirim        |     USC           |     403150                |     20.00                 |     10,00                 |     3                 |
|     Tahsilat                    |     Ücretli son bildirim         |     ABD Doları           |     403150                |     50.00                 |     100.00                |     15                |

Aşağıdaki resimde tabloda gösterilen bilgiler, **tahsilat mektupları** sayfasında görüneceği şekilde gösterilmektedir. 

[![Tahsilat mektubu sırası ayarlama.](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Şimdi bu örnek için gereken iki parametreyi ayarlamanız gerekir.

2. **Alacak ve tahsilatlar \> Kurulum \> Alacak hesabı parametreleri**'ne gidin ve şu adımları izleyin:

    1. **Tahsilatlar** sekmesinde **tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneğini **Evet** olarak ayarlayın.
    2. **Her seferinde tahsilat mektubu oluştur** alanının **Müşteri** olarak ayarlandığından emin olun.

    [![Alacak Tahsilatları için alacak hesapları parametreleri ayarlama.](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. **Alacak hesapları \> faturalar \> Tüm serbest metin faturaları** kısmına gidin, **Yeni**'yi seçin ve şu adımları izleyin:

    1. **Müşteri hesabı** alanında **US-045**'i seçin.
    2. **Fatura tarihi** alanına **1/15/2021** tarihini girin.
    3. **Son tarih** alanına **1/16/2021** tarihini girin.
    4. **Fatura satırları** hızlı sekmesinde, **ana hesap** alanına **401100** girin.
    5. **Birim fiyatı** alanına **500.00** yazın.
    6. **Naklet**'i seçin.

    Şimdi müşteri için iki alacak dekontu girmeniz gerekir.

4. **Yeni**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Müşteri hesabı** alanında **US-045**'ü seçin.
    2. **Fatura tarihi** alanına **1/15/2021** tarihini girin.
    3. **Son tarih** alanına **1/16/2021** tarihini girin.
    4. **Fatura satırları** hızlı sekmesinde, **ana hesap** alanına **401100** girin.
    5. **Birim fiyatı** alanına **-100,00** yazın.
    6. **Naklet**'i seçin.

5. 4. adımı yineleyin, ancak **birim fiyat** alanına **-200,00** girin.
6. **Alacak hesapları \>müşteriler \> tüm müşteriler**'e gidin ve müşteri **US-045**'i seçin. Sonra, eylem bölmesinde, daha önce deftere naklettiğiniz müşteri işlemlerini gözden geçirmek üzere **İşlemler \> İşlemler**'i seçin.

    [![Deftere nakledilen müşteri işlemlerini gözden geçirme.](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Şimdi müşteri US-045 için tahsilat mektupları oluşturmanız gerekir.

7. **Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını oluştur**'a gidin ve şu adımları izleyin:

    1. **Fatura** ve **alacak dekontu** seçeneklerini **Evet** olarak ayarlayın.

        Varsayılan olarak, **tahsilat mektubu** alanı **müşteri başına tahsilat** olarak ayarlanmalıdır.

    2. **Tahsilat mektubu tarihi** alanına **1/19/2021** tarihini girin.
    3. **Dahil edilecek kayıtlar** hızlı sekmesinde, **filtre**'yi seçin ve **müşteri hesabı** alanına, müşteri **US-045**'i ekleyin.
    4. **Tamam**'ı seçin.
    5. Tahsilat mektupları oluşturmak için **Tamam**'ı seçin.

8. **Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını incele ve işle**'ye gidin ve şu adımları izleyin:

    1. Bu tahsilat mektubu dizideki ilk tahsilat mektubu olduğundan, hem başlık, hem işlem satırlarında tahsilat mektubu kodunun **tahsilat mektubu 1** olduğuna dikkat edin. (İşlem satırlarını görüntülemek için, **İşlemler** Hızlı sekmesini seçmeniz gerekebilir.)

   [![Başlıkta ve satırlarda aynı tahsilat mektubu kodunun göründüğünü doğrulama.](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Eylem Bölmesinde **Deftere naklet**'i seçin.
    3. **Deftere nakletme tarihi** alanına **1/19/2021** tarihini girin.

    Şimdi müşteri US-045 için tahsilat mektuplarını tekrar oluşturmanız gerekir.

9. **Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını oluştur**'a gidin ve şu adımları izleyin:

    1. **Fatura** ve **alacak dekontu** seçeneklerini **Evet** olarak ayarlayın.

        Varsayılan olarak, **tahsilat mektubu** alanı **müşteri başına tahsilat** olarak ayarlanmalıdır.

    2. **Tahsilat mektubu tarihi** alanına **1/23/2021** tarihini girin.
    3. **Dahil edilecek kayıtlar** hızlı sekmesinde, **filtre**'yi seçin ve **müşteri hesabı** alanına, müşteri **US-045**'i ekleyin.
    4. **Tamam**'ı seçin.
    5. Tahsilat mektupları oluşturmak için **Tamam**'ı seçin.

10. **Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını incele ve işle**'ye gidin ve şu adımları izleyin:

    1. Başlıktaki tahsilat mektubu kodunun **tahsilat mektubu 1** olduğuna dikkat edin. Ancak, işlem satırlarındaki kod **Tahsilat mektubu 2**'dir.

   [![Başlıkta ve satırlarda farklı tahsilat mektubu kodlarının göründüğünü doğrular.](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  **Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneği **Evet** olarak ayarlandığı için kodlar farklıdır.

  2. Bu Tahsilat mektubunu deftere nakletmeyin.

11. **Alacak ve tahsilatlar \> Kurulum \> Alacak hesapları parametrelerine** gidin ve ardından **Tahsilatlar** sekmesinde, **tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneğini **Hayır** olarak ayarlayın.

    [![Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak notlarını yoksayma seçeneğini Hayır olarak ayarlama.](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Şimdi müşteri US-045 için tahsilat mektuplarını tekrar oluşturmanız gerekir.

12. **Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını oluştur**'a gidin ve şu adımları izleyin:

    1. **Fatura** ve **alacak dekontu** seçeneklerini **Evet** olarak ayarlayın.

        Varsayılan olarak, **tahsilat mektubu** alanı **müşteri başına tahsilat** olarak ayarlanmalıdır.

    2. **Tahsilat mektubu tarihi** alanına **1/23/2021** tarihini girin.
    3. **Dahil edilecek kayıtlar** hızlı sekmesinde, **filtre**'yi seçin ve **müşteri hesabı** alanına, müşteri **US-045**'i ekleyin.
    4. **Tamam**'ı seçin.
    5. Tahsilat mektupları oluşturmak için **Tamam**'ı seçin.

13. **Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını gözden geçir ve izle** bölümüne gidin ve hem başlık, hem işlem satırlarında tahsilat mektubu kodunun **tahsilat mektubu 2** olduğuna dikkat edin.

    [![Başlıkta ve satırlarda aynı tahsilat mektubu kodunun olduğunu tekrar gösterme.](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    **Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneği şimdi **Hayır** olarak ayarlandığı için her iki yerde de aynı kod görünür.

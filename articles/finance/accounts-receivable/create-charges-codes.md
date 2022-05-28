---
title: Masraf kodlarını oluşturma
description: Bu konu; hem Borç hesapları hem de Alacak hesapları için masraf kodlarının nasıl konfigüre edileceğini açıklar.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8526fa0f3c6e3d1b545703f6e6ef72f558b57bd
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735041"
---
# <a name="create-charges-codes"></a>Masraf kodlarını oluşturma

Bu konu; hem Borç hesapları hem de Alacak hesapları için masraf kodlarının nasıl konfigüre edileceğini açıklar. Organizasyonunuz, satış siparişindeki veya satınalma siparişindeki satır maddelerine ek olarak satış miktarları veya satınalma tutarlarının izlenmesini gerektiriyorsa, bu amaç için masraf kodlarını kullanabilirsiniz. Örneğin, bir satınalma siparişindeki navlun ve sigorta ödemesini yaptığınızda, bu tutarlar satınalma siparişinde ayrı olarak da listelenir. Bu durumda, tutarların gider hesaplarına nakledilip nakledilmeyeceğini veya maddelerin maliyetine eklenip eklenmeyeceğini belirtebilirsiniz.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Alacak hesapları için masraf kodlarını ayarlama

Alacak hesapları için masraf kodları oluşturmak üzere aşağıdaki adımları izleyin.

1. **Alacak hesapları** &gt; **Giderler kurulumu** &gt; **Gider kodu**'na gidin.
2. **Yeni**'yi seçin.
3. **Masraflar kodu** alanında, masraf için bir kod girin.
3. **Açıklama** alanında masraf için bir açıklama girin.
4. İsteğe bağlı: **Madde satış vergisi grubu** alanında bir satış vergisi grubu seçin.
5. **Deftere nakil** hızlı sekmesinde, masrafın otomatik olarak borç ve alacak olarak yapılacağını belirtin.
6. Borç türü veya kredi türü olarak **Genel muhasebe hesabı**'nı seçtiyseniz, **Deftere nakil** alanlarını belirtin ve **Hesap** alanlarında ana hesabı belirtin.

### <a name="example"></a>Örnek

Müşteriniz masrafı öder. Bu nedenle, satış siparişi toplamlarına eklenir. Aşağıdaki deftere nakil bilgilerini ayarlarsınız:

- **Borç** kısmındaki **Tür** alanında, fatura giderini müşterinin hesabına eklemek için **Müşteri/Satıcı** seçeneğini belirleyin.
- **Alacak** kısmındaki **Tür** alanında **Genel muhasebe hesabı**'nı seçin. Ardından, **Hesap** alanında, fatura masraflarından gelir için ana hesabı seçin.

> [!NOTE]
> Seçili kod için alacak türü veya borç türü **Genel muhasebe hesabı** veya **Madde** ise masraf hareketi için farklı bir para birimi girebilirsiniz.

Masraflar metnini müşteriye atanmış dilde yazdırabilirsiniz. Diğer dillerdeki masraf koduna ait metni belirtmek için **Çeviriler**'i seçin.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Borç hesapları için masraf kodlarını ayarlama

Borç hesapları için masraf kodları oluşturmak üzere aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - **Borç hesapları** &gt; **Giderler** **kurulumu** &gt; **Gider kodu**'na gidin.
    - **Tedarik ve kaynak** &gt; **Kurulum** &gt; **Masraflar** &gt; **Masraflar kodu**'na gidin.

2. **Yeni**'yi seçin.
3. **Masraflar kodu** alanında, masraf için bir kod girin.
3. **Açıklama** alanında masraf için bir açıklama girin.
4. İsteğe bağlı: **Madde satış vergisi grubu** alanında bir satış vergisi grubu seçin.
5. İsteğe bağlı: **Maksimum tutar** alanında masraf kodu için izin verilen maksimum tutarı girin.

    Bu alan, satıcı faturaları için masrafları doğrulamak amacıyla kullanılır. Giderlerin doğrulanmasını etkinleştirmek için, **Borç hesapları parametreleri** sayfasındaki **Fatura doğrulama** sekmesinde **Fatura eşleştirme doğrulamasını etkinleştir** onay kutusunu seçin.

    > [!IMPORTANT]
    > Faturaların giderlerini doğrulamak için, belirli satıcı fatura ilkesinin giderlerini temel alan bir ilke kuralı türü örneği de oluşturmanız gerekir.

6. **Deftere nakil** hızlı sekmesinde, masrafın otomatik olarak borç ve alacak olarak yapılacağını belirtin.
7. Borç türü veya kredi türü olarak **Genel muhasebe hesabı**'nı seçtiyseniz, **Borç deftere nakil** ve **Alacak deftere nakil** alanlarını yazın ve **Borç hesabı** ve **Alacak hesabı** alanlarında ana hesabı belirleyin.
8. İlgili satınalma siparişi başlığından veya satırlarından giderleri içeren bir fatura için gider değerlerinin karşılaştırılmasını etkinleştirmek için, **Satınalma siparişi ve fatura değerlerini karşılaştır** onay kutusunu seçin.

### <a name="example"></a>Örnek

Giderleri, satınalma siparişi veya satıcı faturası toplamının bir parçası olarak gider olarak kaydedebilirsiniz. Deftere nakil bilgilerini ayarlamak için aşağıdaki adımları izleyin. 

- **Alacak** kısmındaki **Tür** alanında, fatura giderini satıcının hesabına eklemek için **Müşteri/Satıcı** seçeneğini belirleyin.
- **Borç** kısmındaki **Tür** alanında **Genel muhasebe hesabı**'nı seçin. Ardından, **Hesap** alanında, fatura masraflarından giderler için ana hesabı seçin.

Birim gideri madde maliyetine eklenecek şekilde deftere nakil bilgilerini ayarlamak için bu adımları izleyin.

- **Alacak** kısmındaki **Tür** alanında, fatura giderini satıcının hesabına eklemek için **Müşteri/Satıcı** seçeneğini belirleyin.
- **Borç** kısmındaki **Tür** alanında, madde maliyetine masrafı eklemek için **Madde**'yi seçin.

> [!NOTE]
> Satınalma siparişi veya faturada belirtilen para biriminden farklı bir para birimi kullanmak isteyebilirsiniz. Seçili gider kodu için borç türü veya alacak türü **Genel muhasebe hesabı** veya **Madde** olarak ayarlanırsa farklı bir para birimi girebilirsiniz.

Masraflar metnini müşteriye atanmış dilde yazdırabilirsiniz. Diğer dillerdeki masraf koduna ait metni belirtmek için **Çeviriler**'i seçin.

---
title: Fatura havuzu kullanarak fatura verilerini AP sistemine girme
description: Bu konu, fatura kaydının faturaları oluşturmak için nasıl kullanılacağını açıklar.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c54f610e45d288ed58fd209d290d73bfe1ff2f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820677"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Fatura havuzu kullanarak fatura verilerini AP sistemine girme

[!include [banner](../../includes/banner.md)]

Bu konu, fatura kaydının faturaları oluşturmak için nasıl kullanılacağını açıklar. Bunun ardından, faturayı bir satınalma siparişiyle eşleştirmek ve satıcı faturası sayfasında gideri sonlandırmak için fatura havuzunu kullanın.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. Gezinti bölmesinde **Modüller > Borç hesapları > Satınalma siparişleri > Satın alma siparişleri** öğesine gidin.
2. Satınalma siparişi oluşturmak için **Yeni**'yi seçin.
3. **Satıcı hesabı** alanında, açılır liste için bir satıcı belirleyin. Örneğin, satıcı **1001**'i seçin.
4. **Tamam**'ı seçin.
5. **Madde numarası** alanında, açılık menüde hizmet madde numarasını seçin. Örneğin, **S0001**'i seçin. Net tutar 75,00'tir.  Bu, faturada olmasını beklediğimiz tutardır.  
6. Eylem Bölmesinde, **Satınalma** öğesine tıklayın.
7. **Onayla**'yı seçin.

## <a name="create-and-post-and-invoice"></a>Fatura oluşturun ve nakledin
1. Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura kaydı**'na gidin.
2. **Yeni**'yi seçin.
3. Kullanmak istediğiniz fatura kaydının adını seçmek için aramayı açın.
4. Kullanmak istediğiniz fatura kaydının adını seçin.
5. Defteri açıp gider satırlarını girmek için **Satırlar**'ı seçin.
6. Aramada bir satıcı seçin. Örneğin, satıcı **1001**'i seçin.
7. **Fatura** alanına fatura numarasını girin.
8. **Tanım** alanına bir değer girin.
9. **Alacak** alanına bir sayı girin.
10. **Satınalma siparişi** alanında, önceden oluşturduğunuz satınalma siparişini seçmek için açılır listeyi açın.
11. **Onaylayan** alanında açılır listeden bir onaylayan seçin ve o onaylayanı seçmek için **Seç**'e tıklayın.
12. **Naklet**'i seçin.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Havuzdan bir fatura açın ve bir satınalma siparişiyle eşleştirerek fatura işlemini tamamlayın.
1. Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura havuzu**'na gidin.
2. Havuzdaki faturadan bir satıcı faturası oluşturmak için **Satınalma siparişi**'ni seçin.
3. İncelemek istediğiniz faturayı seçin.
4. Eşleşmeyi tamamlamak için **Eşleştirme durumunu güncelleştir**'i seçin.
5. Eylem Bölmesinde, **Seçenekler**'i seçin.
6. **Görünümü değiştir**'i seçin.
7. **Izgara görünümü**'nü seçin.
8. **Naklet**'i seçin.
9. Formu kapatın.
10. Gezinti Bölmesi'nde **Modüller > Borç hesapları > Satıcılar > Satıcılar**'a gidin.
11. Satınalma siparişindeki satıcıyı seçin. Örneğin, satıcı **1001**'i seçin.
12. Eylem Bölmesinde, **Satıcılar**'ı seçin.
13. **Hareketler**'i seçin.
14. Oluşturduğunuz faturayı seçin. Fatura kaydı tahakkuku ters kaydedilmiş ve ilgili gider hesabına nakledilmiştir.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
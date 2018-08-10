--- 
title: Fatura havuzu kullanarak fatura verilerini AP sistemine girme
description: "Bu görev kılavuzunda size fatura oluşturmak için fatura kaydının nasıl kullanılacağı gösterilecek."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Fatura havuzu kullanarak fatura verilerini AP sistemine girme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda size fatura oluşturmak için fatura kaydının nasıl kullanılacağı gösterilecek.  Bunun ardından, faturayı bir satınalma siparişiyle eşleştirmek ve satıcı faturası sayfasında gideri sonlandırmak için fatura havuzunu kullanın.


## <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma
1. Borç hesapları > Satın alma siparişleri > Satınalma siparişleri'ne gidin.
2. Satınalma siparişi oluşturmak için Yeni'ye tıklayın.
3. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listeden satıcıyı seçin. Örneğin, satıcı 1001.
5. Tamam'a tıklayın.
6. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
7. Listede hizmet madde numarasını bulun. Örneğin, S0001 seçin.
8. Madde numarasına tıklayarak seçin.
    * Net tutar 75,00'tir.  Bu, faturada olmasını beklediğimiz tutardır.  
9. Eylem bölmesinde, Satınalma'ya tıklayın.
10. Onayla seçeneğine tıklayın.

## <a name="create-and-post-and-invoice"></a>Fatura oluşturun ve nakledin
1. Borç hesapları > Faturalar > Fatura kaydı'na gidin.
2. Yeni'ye tıklayın.
3. Kullanmak istediğiniz fatura kaydının adını seçmek için aramayı açın.
4. Kullanmak istediğiniz fatura kaydının adını seçin.
5. Defteri açıp gider satırlarını girmek için Satırlar'a tıklayın.
6. Aramada bir satıcı seçin. Örneğin, satıcı 1001'e tıklayın.
7. Fatura alanına fatura numarasını girin.
8. Tanım alanına bir değer girin.
9. Alacak alanına bir sayı girin.
10. Satınalma siparişi alanında, açılır menü düğmesine tıklayarak aramayı açın.
11. Daha önce oluşturduğunuz satınalma siparişini seçin.
12. Onaylayan alanında, açılır menü düğmesine tıklayarak aramayı açın.
13. Bir onaylayanı vurgulayın ve o onaylayanı seçmek için Seç'e tıklayın.
14. Deftere Naklet öğesine tıklayın.
15. Formu kapatın.
16. Formu kapatın.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Havuzdan bir fatura açın ve bir satınalma siparişiyle eşleştirerek fatura işlemini tamamlayın.
1. Borç hesapları > Faturalar > Fatura havuzu'na gidin.
2. Havuzdaki faturadan bir satıcı faturası oluşturmak için Satınalma siparişi'ne tıklayın.
3. İncelemek istediğiniz faturayı seçin.
4. Eşleşmeyi tamamlamak için Eşleştirme durumunu güncelleştir'e tıklayın.
5. Eylem bölmesinde, Seçenekler'e tıklayın.
6. Görünümü değiştir'e tıklayın.
7. Izgara görünümü'ne tıklayın.
8. Deftere Naklet öğesine tıklayın.
9. Formu kapatın.
10. Borç hesapları > Satıcılar > Satıcılar'a gidin.
11. Satınalma siparişindeki satıcıyı seçin. Örneğin, satıcı 1001'i seçin.
12. Listede, seçili satırdaki bağlantıya tıklayın.
13. Eylem bölmesinde, Satıcı'ya tıklayın.
14. Hareketler'e tıklayın.
15. Oluşturduğunuz faturayı seçin.
    * Fatura kaydı tahakkuku ters kaydedilmiş ve ilgili gider hesabına nakledilmiştir.  



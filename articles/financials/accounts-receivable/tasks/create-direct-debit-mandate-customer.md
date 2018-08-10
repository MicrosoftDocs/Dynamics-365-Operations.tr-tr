--- 
title: "Müşteri için hesaptan ödeme talimatı oluşturma"
description: "Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Müşteri için hesaptan ödeme talimatı oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir.


## <a name="create-a-bank-account"></a>Banka hesabı oluşturun
1. Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.
2. Örneğin, TR-001 seçin.
3. Eylem Bölmesinde, Müşteri'ye tıklayın.
4. Banka hesapları'na tıklayın.
5. Yeni'ye tıklayın.
6. Banka hesabı alanına bir değer girin.
7. İsim alanına bir değer yazın.
8. IBAN alanına bir değer girin.
9. Para birimi alanına bir değer yazın.
10. Kaydet'e tıklayın.
11. Sayfayı kapatın.
12. Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.
13. Listede, istenen kaydı bulun ve seçin.
14. Listede, seçili satırdaki bağlantıya tıklayın.
15. Düzenle öğesine tıklayın.
16. Ek kimlik bölümünü genişletin.
17. Otomatik ödeme kodu alanına bir değer girin.
18. IBAN alanına bir değer girin.
19. Sayfayı kapatın.
20. Sayfayı kapatın.

## <a name="define-the-electronic-payment-method"></a>Elektronik ödeme yöntemini tanımlayın
1. Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi'ne gidin.
2. Yeni'ye tıklayın.
3. Ödeme yöntemi alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Ödemenin hesaptan ödeme talimatı yönteminin ödeme türü Elektronik ödeme olmalıdır.
6. Talimat iste alanında Evet'i seçin.
7. Sayfayı kapatın.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Müşteriye bir hesaptan ödeme talimatı ekleyin.
1. Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.
2. Örneğin, TR-001 seçin.
3. Düzenle öğesine tıklayın.
4. Ödeme varsayılanları bölümünü genişletin.
5. Ödeme yöntemi alanında bir değer girin veya bir değer seçin.
6. Ödeme varsayılanları bölümünü genişletin.
7. Hesaptan ödeme talimatları bölümünü genişletin.
8. Ekle öğesini tıklatın.
9. Banka hesabı alanında bir değer girin veya seçin.
10. Alacaklı banka hesabı alanına bir değer girin veya seçin.
11. Bu talimat için işleneceğini tahmin ettiğiniz ödeme sayısını girin.
12. Tamam'a tıklayın.
13. Yazdır'ı tıklatın.
14. Talimat raporu'na tıklayın.
15. Sayfayı kapatın.
16. Düzenle öğesine tıklayın.
17. İmza tarihi alanına bir tarih girin.
18. Evet'i tıklatın.
19. Talimatın imzalandığı yeri girin.
20. Tamam'a tıklayın.
21. Sayfayı kapatın.

## <a name="create-a-free-text-invoice-with-mandate"></a>Talimatlı bir serbest metin faturası oluşturun
1. Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.
2. Yeni'ye tıklayın.
3. Talimatı eklediğiniz müşteriyi seçin.
4. Hesaptan ödeme talimatı alanında bir değer girin veya bir değer seçin.



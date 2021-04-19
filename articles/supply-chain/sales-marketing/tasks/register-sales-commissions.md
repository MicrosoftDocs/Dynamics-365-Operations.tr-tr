---
title: Satış komisyonlarını kaydetme
description: Bu konu, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini açıklar.
author: omulvad
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee75f3a0c9dea7a7c4a4f927651aaab1d6bdb5c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836386"
---
# <a name="register-sales-commissions"></a>Satış komisyonlarını kaydetme

[!include [banner](../../includes/banner.md)]

Bu konu, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini açıklar. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Bu kılavuzu başlatmadan önce, gerekli tüm komisyon hesaplama ayarlarını yaptığınızdan emin olmak için "Satış komisyonu kuralları ayarlama" adlı kılavuzu çalıştırın.

Komisyon işlemi için seçtiğiniz müşteri ve ürün numaralarını not edin ve sorulduğunda bu kılavuzda bir satış siparişi oluşturmak için bunları kullanın.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Bir satış elemanının bir komisyon için uygun olduğunu gösteren satış siparişini faturalama
1. Gezinti bölmesinde **Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Müşteri numarası** alanında, açılır menüden istediğiniz kaydı seçin.
4. **Tamam**'ı seçin.
5. Eylem Bölmesinde, **Seçenekler**'i seçin.
6. **Görünümü değiştir**'i seçin.
7. **Başlık görünümü**'nü seçin.
8. **Kurulum** bölümünü genişletin.

    - **Satış grubu** alanındaki değer, bir veya daha fazla satış temsilcisinin atandığı bir grubu temsil eder. Sipariş faturalandırıldığında, gruptaki kişiler önceden tanımlanmış oranlara ve dağıtıma göre komisyonlarını alır.   
    - Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.  
    - Satış grubu, satış siparişi satırına da kopyalanır. Bir üstbilgiden ve/veya satırlar arası bilgiden farklı olabilmesi için bunu değiştirebilirsiniz.  
    - **Komisyon grubu** alanındaki değer, bir veya daha fazla müşteri için komisyonları izleme amacıyla oluşturduğunuz bir grubu temsil eder.   
    - Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.   

9. Eylem Bölmesinde, **Seçenekler**'i seçin.
10. **Görünümü değiştir**'i seçin.
11. **Satır görünümü**'nü seçin.
12. **Madde numarası** alanının açılır menüsünde, komisyonlar için ayarladığınız maddeyi seçin. 
13. **Miktar** alanına bir sayı girin. Satırın Net tutarını not edin. Bu, bu örnekte komisyon hesaplamasının temeli olan satış geliri temsil eder.  
14. **Kaydet**'i seçin.
15. Eylem Bölmesinde, **Fatura**'yı seçin.
16. **Fatura**'yı seçin.
17. **Parametreler** bölümünü genişletin.
18. **Miktar** alanında **Tümü** seçeneğini seçin.
19. **Deftere nakil** alanında **Evet**'i seçin.
20. **Tamam**'ı seçin ve sonraki bölmede **Tamam**'ı seçin. Bir hareketin deftere nakledilmesi bir dakika kadar sürebilir. İşleme koyulmasını ve tamamlanmasını bekleyin ve sayfayı kapatmayın.  

## <a name="review-the-registered-sales-commissions"></a>Kayıtlı satış komisyonlarını gözden geçirme
1. Eylem Panosunda, **Fatura**'yı ve sonra tekrar **Fatura**'yı seçin.
2. Eylem Panosunda, **Fatura**'yı ve sonra **Komisyon hareketleri**'ni seçin.

    - **Genel bakış** öğesi, faturalanan satış siparişiyle ilişkili satış temsilcilerine ödenecek komisyon tutarlarını temsil eden satırları gösterir. Ayrıntıları gözden geçirelim.  
    - **Komisyon satışı** grubu ayarlamak için "Satış komisyonu kuralları ayarlama" kılavuzunu kullandıysanız, bir satış komisyonunu alacak iki satış elemanı olur ve komisyon ikisi arasında eşit olarak bölünür.  
    - Bu örnekte, komisyonun tutarı satış gelirinin (sipariş satırının net tutarı) bir yüzdesi olarak hesaplanır.  
3. Sayfayı kapatın.
4. **Fiş**'i seçin. Önceden tanımlanmış komisyon giderlerine ve komisyon borç hesaplarına nakledilen komisyon tutarlarının fiş hareketlerini gözden geçirebilirsiniz.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
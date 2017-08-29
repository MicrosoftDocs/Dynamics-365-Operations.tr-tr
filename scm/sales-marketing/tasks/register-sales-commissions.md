--- 
title: "Satış komisyonlarını kaydetme"
description: "Bu yordam, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f1e22f15e98b563f7d2aae812aee3df1d454524c
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="register-sales-commissions"></a>Satış komisyonlarını kaydetme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini göstermektedir. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Bu kılavuzu başlatmadan önce, gerekli tüm komisyon hesaplama ayarlarını yaptığınızdan emin olmak için "Satış komisyonu kuralları ayarlama" adlı kılavuzu çalıştırın.

Komisyon işlemi için seçtiğiniz müşteri ve ürün numaralarını not edin ve sorulduğunda bu kılavuzda bir satış siparişi oluşturmak için bunları kullanın.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Bir satış elemanının bir komisyon için uygun olduğunu gösteren satış siparişini faturalama
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Tamam'a tıklayın.
7. Eylem Bölmesinde, Seçenekler'e tıklayın.
8. Görünümü değiştir'e tıklayın.
9. Başlık görünümü'ne tıklayın.
10. Kurulum bölümünü genişletin.
    * Satış grubu alanındaki değer, bir veya daha fazla satış temsilcisinin atandığı bir grubu temsil eder. Sipariş faturalandırıldığında, gruptaki kişiler önceden tanımlanmış oranlara ve dağıtıma göre komisyonlarını alır.   Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.  Satış grubu, satış siparişi satırına da kopyalanır. Bir üstbilgiden ve/veya satırlar arası bilgiden farklı olabilmesi için bunu değiştirebilirsiniz.  
    * Komisyon grubu alanındaki değer, bir veya daha fazla müşteri için komisyonları izleme amacıyla oluşturduğunuz bir grubu temsil eder.   Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.   
11. Eylem Bölmesinde, Seçenekler'e tıklayın.
12. Görünümü değiştir'e tıklayın.
13. Satır görünümü'nü tıklatın.
14. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
15. Listede, komisyonlar için ayarlamış olduğunuz ürünü seçin. 
16. Miktar alanına bir sayı girin.
    * Satırın Net tutarını not edin. Bu, bu örnekte komisyon hesaplamasının temeli olan satış geliri temsil eder.  
17. Kaydet'e tıklayın.
18. Eylem Bölmesinde, Fatura öğesine tıklayın.
19. Fatura'ya tıklayın.
20. Parametreler bölümünü genişletin.
21. Miktar alanında, 'Tümü' öğesini seçin.
22. Deftere nakil alanında 'Evet'i seçin.
23. Tamam'a tıklayın.
24. Tamam'a tıklayın.
    * Bir hareketin deftere nakledilmesi bir dakika kadar sürebilir. İşleme koyulmasını ve tamamlanmasını bekleyin ve sayfayı kapatmayın.  

## <a name="review-the-registered-sales-commissions"></a>Kayıtlı satış komisyonlarını gözden geçirme
1. Eylem Bölmesinde, Fatura öğesine tıklayın.
2. Fatura'ya tıklayın.
3. Eylem Bölmesinde, Fatura öğesine tıklayın.
4. Komisyon hareketleri'ni tıklatın.
    * Genel bakış sekmesi, faturalanan satış siparişiyle ilişkili satış temsilcilerine ödenecek komisyon tutarlarını temsil eden satırları gösterir. Ayrıntıları gözden geçirelim.     
    * Komisyon satışı grubu ayarlamak için "Satış komisyonu kuralları ayarlama" kılavuzunu kullandıysanız, bir satış komisyonunu alacak iki satış elemanı olur ve komisyon ikisi arasında eşit olarak bölünür.  
    * Bu örnekte, komisyonun tutarı satış gelirinin (sipariş satırının net tutarı) bir yüzdesi olarak hesaplanır.   
5. Sayfayı kapatın.
6. Fiş'e tıklayın.
    * Önceden tanımlanmış komisyon giderlerine ve komisyon borç hesaplarına nakledilen komisyon tutarlarının fiş hareketlerini gözden geçirebilirsiniz.  



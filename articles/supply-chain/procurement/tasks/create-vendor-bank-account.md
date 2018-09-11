--- 
title: "Satıcı banka hesabı oluşturma"
description: "Bu prosedür, bir satıcının banka hesabının nasıl oluşturulacağını gösterir."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: adb759c59d7275e7323dbb760de56acdef2e3cff
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-vendor-bank-account"></a>Satıcı banka hesabı oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, bir satıcının banka hesabının nasıl oluşturulacağını gösterir. Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.

1. Tedarik ve kaynak > Satıcılar > Tüm satıcılar'a tıklayın.
2. Banka hesabını oluşturmak istediğiniz satıcıyı seçin ve sonra Satıcı hesap kodundaki bağlantıya tıklayın.
3. Eylem Bölmesinde, Satıcı'ya tıklayın.
4. Banka hesapları'na tıklayın.
5. Yeni'ye tıklayın.
6. Banka hesabı alanına bir değer girin.
    * Bu kimlik satıcı kaydı üzerinden banka hesabını tanımlamak için kullanılır.  
7. İsim alanına bir değer yazın.
8. Banka grupları alanında bir değer girin veya seçin.
9. Rota numarası türü alanında, bir seçenek belirleyin.
    * Bu uluslararası ödemeler için kullanılan rota numarası türüdür.  
10. Banka hesabı numarası alanında bir değer girin.
11. SWIFT kodu alanına bir değer girin.
12. IBAN alanına bir değer girin.
    * IBAN numarası doğru biçimde olmalıdır. Örneğin, DE89370400440532013000'ı kullanabilirsiniz.  
    * Etkin tarihe ulaşılmışsa banka hesabının durumu Etkin'dir ve Bitiş tarihi geçmemiştir. Ayrıca, Etkin tarih ve Bitiş tarihi alanları boşsa da etkindir. Etkin tarih ve Bitiş tarihi alanlarının her ikisindeki tarihler gelecekteyse, elektronik ödemeler kullanılamaz. Diğer ödeme tipleri kullanılabilir ve banka hesabı etkindir.  
13. Kurulum bölümünü genişletin.
14. Metin kodu alanına bir değer girin.
    * Bu alan, alıcının banka ekstresinde görünecek bir kod belirtir.  
15. Bankaya ileti alanına bir değer girin.
16. Döviz kuru referansı alanında bir değer girin.
    * Bu gelecek veya sabit dönemli döviz kuru için referans numarasıdır.  
17. Para birimi alanında bir değer girin veya bir değer seçin.
    * Bu bölümde açık provizyonlar düzenlenirken durum özeti verilir (beklemede veya onaylanmış).  
18. Adres bölümünü genişletin.
19. Açık provizyonlar bölümünü genişletin.
20. İletişim bilgileri bölümünü genişletin veya daraltın.
21. Telefon alanına bir değer yazın.
22. Sayfayı kapatın.
23. Düzenle öğesine tıklayın.
24. Ödeme bölümünü genişletin.
25. Banka hesabı alanında, yeni oluşturduğunuz hesabı seçin.
26. Kaydet'e tıklayın.
    * Belirtilmişse adres banka grubundan devralınabilir veya buradan ekleyebilirsiniz.  



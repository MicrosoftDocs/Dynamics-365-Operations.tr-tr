---
title: Satış tekliflerini toplu olarak oluştur
description: Bu yordam, birden fazla müşteriye gönderilecek ürünler ve hizmetler kümesi sunan tekliflerin nasıl etkin biçimde oluşturulacağını göstermektedir.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ea50500ed52069ab9f6aae0dfb2d6cffc47cbff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006853"
---
# <a name="mass-create-sales-quotations"></a>Satış tekliflerini toplu olarak oluştur

[!include [banner](../../includes/banner.md)]

Bu yordam, birden fazla müşteriye gönderilecek ürünler ve hizmetler kümesi sunan tekliflerin nasıl etkin biçimde oluşturulacağını göstermektedir. Bu toplu teklif oluşturma işlemi teklif şablonlarını temel alır. Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz.


## <a name="create-a-quotation-template"></a>Bir teklif şablonu oluşturma
1. Sales and marketing > Setup > Quotations > Template groups (Satış ve pazarlama > Ayarlama > Teklifler > Şablon grupları) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Grup Kodu alanında seçtiğiniz kod türünü girin.
4. Açıklama alanına bir değer girin.
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.
7. Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.
8. Yeni'ye tıklayın.
9. Hesap türü alanında 'Müşteri' seçeneğini belirleyin.
10. Müşteri hesabı alanında bir değer girin veya seçin.
11. Tamam'a tıklayın.
    * Bir teklifin şablona dönüşmesi için teklif başlığındaki kurulum adımlarını gerçekleştirmeniz gerekir. Bunu teklife satır eklemeden önce yapmanız gerekir.   
12. Eylem Bölmesinde, Seçenekler'e tıklayın.
13. Görünümü değiştir'e tıklayın.
14. Başlık görünümü'ne tıklayın.
15. Kurulum bölümünü genişletin.
16. Grup kodu alanında bir değer girin veya bir değer seçin.
17. Şablon adı alanına bir değer girin.
18. Etkin alanında 'Evet'i seçin.
    * Yeni bir satış teklifine bir şablon uyguladığınızda, yalnızca etkin şablonlar kullanılabilir.  
19. Eylem Bölmesinde, Seçenekler'e tıklayın.
20. Görünümü değiştir'e tıklayın.
21. Satır görünümü'nü tıklatın.
22. Ürün alanında bir değer girin veya bir değer seçin.
23. Ürün alanında bir değer yazın.
24. Sayfayı kapatın.
25. İskonto yüzdesi alanında bir sayı girin.
26. Satır ekle'ye tıklayın.
27. Ürün alanında bir değer girin veya bir değer seçin.
28. Ürün alanında bir değer yazın.
29. Sayfayı kapatın.
30. Birim fiyat alanında, yeni fiyat girin veya geçerli olanı değiştirin.
31. Satır ekle'ye tıklayın.
32. Ürün alanında bir değer girin veya bir değer seçin.
33. Ürün alanında bir değer yazın.
34. Sayfayı kapatın.
35. Miktar alanına bir sayı girin.
36. İskonto alanında bir sayı girin.
37. Kaydet'e tıklayın.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Tek bir teklif oluşturmak için şablon uygulama
1. Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.
    * Yeni oluşturduğunuz teklifin şablon olarak işaretlendiğini unutmayın.  
2. Yeni'ye tıklayın.
3. Hesap türü alanında 'Müşteri' seçeneğini belirleyin.
4. Müşteri hesabı alanında bir değer girin veya seçin.
5. Şablon bölümünü genişletin.
6. Grup kodu alanında bir değer girin veya bir değer seçin.
7. Şablon adı alanında bir değer girin veya bir değer seçin.
8. Hesaplama yöntemi alanında 'Şablon değerlerine dayalı' öğesini seçin.
9. Tamam'a tıklayın.
    * Yeni teklif şablonun verileri ve koşulları temel alınarak oluşturuldu.  
10. Sayfayı kapatın.
11. Sayfayı kapatın.

## <a name="apply-the-template-to-mass-create-quotations"></a>Teklifleri toplu şekilde oluşturmak için şablon uygulama
1. Sales and marketing > Sales quotations > Quotation update > Mass create quotations (Satış ve pazarlama > Satış teklifleri > Teklif güncelleştirmesi > Teklifleri toplu olarak oluştur) menüsüne gidin.
2. Hesap türü alanında 'Müşteri' seçeneğini belirleyin.
3. Grup kodu alanında bir değer girin veya bir değer seçin.
4. Şablon adı alanında bir değer girin veya bir değer seçin.
5. Hesaplama yöntemi alanında 'Şablon değerlerine dayalı' öğesini seçin.
6. Eklenecek kayıtlar bölümünü genişletin.
7. Filtre'ye tıklayın.
8. Ölçüt alanında, bu toplu teklif oluşturma işlemine dahil etmek istediğiniz müşterileri kapsamına alan bir filtre ayarlayın. Şu biçimi kullanın: "Customer1..CustomerN.
    * Örneğin, filtreyi US-001..US-004 olarak ayarlayabilirsiniz  
9. Tamam'a tıklayın.
10. Tamam'a tıklayın.
11. Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.
    * Tekliflerin seçili şablon temel alınarak toplu güncelleştirme rutininde belirtilen tüm müşteriler için oluşturulduğundan emin olun.  


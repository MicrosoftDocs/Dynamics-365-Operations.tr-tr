--- 
title: "Serbest metin faturası oluşturma"
description: "Bu makalede, serbest metin faturasının nasıl oluşturulduğu gösterilmektedir."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: tr-tr
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Serbest metin faturası oluşturma

[!include [banner](../includes/banner.md)]

Bu makalede, serbest metin faturasının nasıl oluşturulduğu gösterilmektedir. Bu prosedür için USMF demo şirketini kullanın.

## <a name="create-a-free-text-invoice"></a>Serbest metin faturası oluşturma

1. Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer seçin.
    * Fatura hesabı, varsayılan olarak müşteri hesabı için kullanılan hesap olacaktır.   
    * Fatura deftere nakledilmediyse, muhasebe durumunun başlangıç değeri İşlemde olur.   
    * Fatura numarası fatura deftere nakledildiğinde atanır.  
    * SEPA yönergelerini kullanıyorsanız, otomatik ödeme yönergesi müşteri hesabını seçtiğinizde otomatik olarak bir yönergeyle doldurulur.  
4. Açıklama alanına bir değer girin.
5. Ana hesap alanında, boyutları olmayan bir hesap numarası belirtin.
    * Ayrıca ana hesap için bir veya daha fazla karakter girebilir ve hesabınızı bulmak için arama özelliğini kullanabilirsiniz. Bu kılavuzda boyutları daha sonra gireceksiniz.  
6. Ana hesabınıza boyutlar eklemek için Satır ayrıntıları hızlı sekmesini genişletin.
7. Mali boyutlar satırı sekmesine tıklayın.
    * Boyutlar yalnızca seçilen satır için kullanılır.    
    * Satış vergisi grubu müşteriden doldurulur. Müşterinin satış vergisi grubu yoksa, ana hesaptan alınan satış vergisi grubu kullanılır.  
    * Madde satış vergisi grubu ana hesaptan doldurulur. Ana hesapta madde satış vergisi grubu yoksa, Genel muhasebe satış vergisi parametrelerindeki madde satış vergisi grubu kullanılır.    
8. Miktar alanına bir sayı girin.
    * Miktar isteğe bağlıdır.  
9. Birim fiyatı alanına bir sayı girin.
    * Birim fiyatı isteğe bağlıdır.  
    * Tutar, miktarla birim fiyatı çarpılarak hesaplanır. Ancak, hesabı geçersiz kılıp kendiniz bir tutar girebilirsiniz.  
10. Faturanız için hesaplanan satış vergisini görüntülemek için Satış vergisi öğesine tıklayın.
    * Bu sayfada satış vergisi tutarlarını görüntüleyebilir veya Ayarlama sekmesinde tutarları geçersiz kılabilirsiniz.  
11. Tamam'a tıklayın.
12. Faturanıza masraf eklemek için Masraflar'a tıklayın. 
13. Masraf kodu alanına bir değer girin.
14. Masraf değeri alanına bir sayı girin.
15. Sayfayı kapatın.
16. Özet fatura ayrıntılarını ve toplamları görüntülemek için Toplamlar öğesine tıklayın.
17. Kapat’a tıklayın.
18. Faturayı deftere nakletmek için Deftere naklet'e tıklayın. Deftere nakletmeden önce iptal edebilirsiniz.
    * Faturanızı yazdırma zamanını değiştirmek için:  Her faturayı güncelleştirilir güncelleştirilmez   yazdırmak için Geçerli'yi, tüm faturalar güncelleştirildikten sonra yazdırmak için  Sonra'yı seçin.  
    * Nakledilmeden önce müşteri kredi limitini kontrol etme yolunu değiştirmek isterseniz Kredi limiti türü'nü değiştirin.  
    * Faturayı yazdırmak isterseniz Evet'i seçin.  
    * Faturayı nakletmek isterseniz Evet'i seçin. Faturayı nakletmeden yazdırabilirsiniz.  
19. Tamam'a tıklayın.

## <a name="copy-lines"></a>Satırları kopyala
Serbest metin faturasında satırları kopyalamak için bir veya birden fazla satırı seçin ve Seçili satırları kopyala'ya tıklayın. Almak istediğiniz kopya sayısını belirtebilir, notları ve ekleri de kopyalayabilirsiniz. Dağıtımları da kopyalayabilir ve deftere naklederken yeniden oluşturulmalarına da izin verebilirsiniz. Satırları kopyaladıktan sonra bilgilerde gerekli düzenlemeleri yapabilirsiniz. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Şablondan serbest metin faturası oluşturma
Şablondan serbest metin faturası oluşturabilirsiniz. Fatura sekmesinden "Şablondan yeni"yi seçtiğiniz zaman yeni serbest metin faturası için bir şablon adı ve müşterinin hesabını seçebilirsiniz. Ayrıca müşterinin ödeme yöntemi ve ödeme koşulları gibi varsayılan değerler belirlemeyi tercih edebilir veya şablonla kaydedilmiş değerleri kullanabilirsiniz. Yeni bir serbest metin faturası oluşturulur ve bu faturadaki değerleri düzenleyebilirsiniz. 



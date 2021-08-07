---
title: Kanal için iade ve para iadesi ilkesi oluşturma ve güncelleştirme
description: Bu konu, bir kanal için iade ve para iadesi ilkesinin nasıl ayarlanacağını açıklar.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: ca5797cfc2d92c4cbc98d3f64d60e1fd260f0418
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558309"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanal için iade ve para iadesi ilkesi oluşturma ve güncelleştirme

[!include [banner](includes/banner.md)]

Dynamics 365 Commerce'deki kanal iade ilkesi, perakendecilerin, bir satış noktasında (POS) iadeyi işleme için izin verilen, tüm ödeme faaliyetlerde zorlayıcı olarak ayarlanmasını sağlar.  

Bu konu, bir kanal için iade ve para iadesi ilkesinin nasıl ayarlanacağı adımlarını açıklar.

İlkenin kapsamı şu anda bir kanal için izin verilmeyen ödeme koşullarını ayarlama ile sınırlı. "İzin verildi" listesi, satın alma işlemi yapmak için kullanılan ödeme yöntemlerine dayanır. Örneğin:

- Bir satın alma, hediye kartı kullanılarak yapılmışsa, mağaza ilkesi para iadelerini yalnızca yeni bir hediye kartına veya mağaza kredisi vermeye yönelik olarak işler. 
- Nakit olarak satış yapıldığında, para iadesi için izin verilen seçenekler nakit, hediye kartı ve müşteri hesabı olmasına karşın kredi kartınının yer aldığı bir hesaptır. 

## <a name="enable-return-policy"></a>İade İlkesini etkinleştir

Commerce genel merkezinde kanal iade ilkesi işlevini etkinleştirmek için şu adımları izleyin.

1. Dynamics 365 Commerce'de **Özellik yönetimi** çalışma alanına gidin.
1. **Kanal iade ilkelerini etkinleştirme** özelliğini, özellik adları listesinde arayın.
1. **Şimdi etkinleştir**'i seçin.
1. **Dağıtım planlaması** sayfasında, özellik değişikliğini dağıtmak için **1110** (Genel yapılandırma) işini çalıştırın.

## <a name="initialize-the-commerce-scheduler"></a>Commerce planlayıcısını başlatma

**Kanal iade ilkelerini etkinleştir** özelliğini etkinleştirdikten sonra, yeni özellik veritabanı değişikliklerinin Commerce Data Exchange (CDX) eşitlemesi yoluyla eklenmesini sağlamak için Commerce planlayıcısını başlatmanız gerekir. 

Commerce genel merkezinde Commerce planlayıcısınıı başlatmak için şu adımları izleyin.

- **Retail ve Commerce \> Genel merkez ayarı \> Commerce planlayıcısı \> Commerce planlayıcısını başlat**'a gidin. Alternatif olarak, "Commerce planlayıcısını başlatma" araması yapabilirsiniz.
- **Commerce Planlayıcısı Başlat** iletişim kutusunda, **Var olan yapılandırmayı sil** seçeneğinin **Hayır** olarak ayarlandığından emin olun ve **Tamam**'ı seçin.

## <a name="configure-return-policy"></a>İade İlkesi yapılandırma

Bir perakende mağaza veya çevrimiçi perakende kanalında iade ilkesi konfigüre etmek için bu adımları izleyin.

1. **Retail ve Commerce** \> **Kanal kurulumu** \> **İadeler** \> **Kanal iade ilkesine** gidin.

1. Yeni bir iade politikası şablonu oluşturmak için **Yeni**'yi seçin. Varolan bir şablonu kullanmak için, sol bölmedeki şablonu seçin. Yeni şablonlar için, kanala uygulandığında ilkeyi tanımlamanıza yardımcı olacak bir ad ve açıklama ekleyin.

   ![Yeni iade ilkesi Ekle.](media/Return-policy-page1.png)
     
   
1. **İzin verilen iade ödeme yöntemleri** bölümünde, her bir ödeme yöntemine özgü olan **izin verilen** iade ödeme yöntemlerini tanımlayın.
   ![Ödeme türü başına izin verilen ödeme yöntemlerini ayarlama.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Ödeme yöntemleri, organizasyon için ayarlanan ödeme yöntemlerinden türetilir.
    > - Listelenen her ödeme yöntemine izin verilen bir ödeme türü eklenmesi, iadenin izin verilen iade ödeme tipine yapılabilmesi için bunların yapılmasına olanak sağlar.
    
1. İade politikası şablonunu, kullanılacak mağazalar ile ilişkilendirin. **Perakende kanalları** sekmesinde **Ekle**'yi seçin ve kullanılabilir kanalları ilişkilendirin. 

    - **Kuruluş düğümlerini Seç** iletişim kutusunda, şablonun ilişkilendirilmesi gereken depoları, bölgeleri ve organizasyonları seçin.
    - Her bir mağaza ile yalnızca bir iade ilkesi şablonu ilişkilendirilebilir.
    - Mağaza, bölge veya organizasyon seçmek için ok düğmelerini kullanın.
    - İlkedeki yürürlülük tarihi ilkelerin kanallara uygulandığı ve kanal işlerinin çalıştırıldığı tarih olacaktır. 

    ![Kuruluş düğümlerini seç iletişim kutusu.](media/Return-policy-page3.png)

1. **Dağıtım zamanlaması** sayfasında, POS'un kanal iade ilkesini kullanabilmesini sağlamak için, **1070** işini çalıştırın.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>POS 'ta kanal iade ilkesini Önizle

POS 'ta izin verilen iade ödeme tiplerini görüntülemek için aşağıdaki örneklerden birinde bulunan adımları izleyin.

1. POS'ta kasiyer veya yönetici olarak oturum açın.
1. **Üst karakter ve çekmece** altında **günlüğü göster**'i seçin.
1. İade işleminin parçası olan hareketi seçin. 
1. Para iadesi yapılacak maddeleri seçin ve ödeme yöntemini seçin.  
    - Seçilen ödeme, izin verilen iade ödeme tipleri listesinde ise, kasiyer hareketi tamamlayabilir.
    - Ödeme ödemesine izin verilmiyorsa, bir hata mesajı görüntülenir.
    - Tüm izin verilen iade ödeme tiplerinin listesini görüntülemek için **tutar vadesini** seçin.

-veya-

1. POS'ta kasiyer veya yönetici olarak oturum açın.
1. **İade hareketi** seçin ve barkod taraması veya el ile giriş kullanarak giriş kodunu girin. 
1. İade işleminin parçası olan hareketi seçin. 
1. Para iadesi yapılacak maddeleri seçin ve ödeme yöntemini seçin.  
    - Seçilen ödeme, izin verilen iade ödeme tipleri listesinde ise, kasiyer hareketi tamamlayabilir.
    - Ödeme ödemesine izin verilmiyorsa, bir hata mesajı görüntülenir.
    - Tüm izin verilen iade ödeme tiplerinin listesini görüntülemek için **tutar vadesini** seçin.

![Geri ödeme türüne izin verilmiyor.](media/Return-policy-page6.png)



![Geri ödeme türlerine izin veriliyor.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

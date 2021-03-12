---
title: Kanal için iade ve para iadesi ilkesi oluşturma ve güncelleştirme
description: Bu konu, bir kanal için iade ve para iadesi ilkesinin nasıl ayarlanacağını açıklar.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 89e8fe78414e73053317ebe19e3afcc89231d440
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979738"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanal için iade ve para iadesi ilkesi oluşturma ve güncelleştirme

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce'deki kanal iade ilkesi, perakendecilerin, bir satış noktasında (POS) iadeyi işleme için izin verilen, tüm ödeme faaliyetlerde zorlayıcı olarak ayarlanmasını sağlar.  

Bu konu, bir kanal için iade ve para iadesi ilkesinin nasıl ayarlanacağı adımlarını açıklar.

İlkenin kapsamı şu anda bir kanal için izin verilmeyen ödeme koşullarını ayarlama ile sınırlı. "İzin verildi" listesi, satın alma işlemi yapmak için kullanılan ödeme yöntemlerine dayanır. Örneğin:

- Bir satın alma, hediye kartı kullanılarak yapılmışsa, mağaza ilkesi para iadelerini yalnızca yeni bir hediye kartına veya mağaza kredisi vermeye yönelik olarak işler. 
- Nakit olarak satış yapıldığında, para iadesi için izin verilen seçenekler nakit, hediye kartı ve müşteri hesabı olmasına karşın kredi kartınının yer aldığı bir hesaptır. 


## <a name="enable-return-policy"></a>İade İlkesini etkinleştir

Kanal iade ilkesi işlevini etkinleştirmek için aşağıdakileri yapın:

1. Dynamics 365 Commerce'de **Özellik yönetimi** çalışma alanına gidin.
2. **Kanal iade ilkelerini etkinleştirme** özelliğini, özellik adları listesinde arayın.
3. **Şimdi etkinleştir**'i seçin. 

## <a name="configure-return-policy"></a>İade İlkesi yapılandırma

Bir perakende mağaza veya çevrimiçi perakende kanalında iade ilkesi konfigüre etmek için bu adımları izleyin.

1. **Retail ve Commerce** \> **Kanal kurulumu** \> **İadeler** \> **Kanal iade ilkesine** gidin.

2. Yeni bir iade politikası şablonu oluşturmak için **Yeni**'yi seçin. Varolan bir şablonu kullanmak için, sol bölmedeki şablonu seçin. Yeni şablonlar için, kanala uygulandığında ilkeyi tanımlamanıza yardımcı olacak bir ad ve açıklama ekleyin.

   ![Yeni iade ilkesi Ekle](media/Return-policy-page1.png "Yeni iade ilkesi Ekle")
     
   
3. **İzin verilen iade ödeme yöntemleri** bölümünde, her bir ödeme yöntemine özgü olan **izin verilen** iade ödeme yöntemlerini tanımlayın.
   ![Ödeme yöntemleri ekle](media/Return-policy-page2.PNG "Ödeme türü başına izin verilen ödeme yöntemlerini ayarla")
   
    > [!IMPORTANT]
    > - Ödeme yöntemleri, organizasyon için ayarlanan ödeme yöntemlerinden türetilir.
    > - Listelenen her ödeme yöntemine izin verilen bir ödeme türü eklenmesi, iadenin izin verilen iade ödeme tipine yapılabilmesi için bunların yapılmasına olanak sağlar.
    
4. İade politikası şablonunu, kullanılacak mağazalar ile ilişkilendirin. **Perakende kanalları** sekmesinde **Ekle**'yi seçin ve kullanılabilir kanalları ilişkilendirin. 

    - **Kuruluş düğümlerini Seç** iletişim kutusunda, şablonun ilişkilendirilmesi gereken depoları, bölgeleri ve organizasyonları seçin.
    - Her bir mağaza ile yalnızca bir iade ilkesi şablonu ilişkilendirilebilir.
    - Mağaza, bölge veya organizasyon seçmek için ok düğmelerini kullanın.
    - İlkedeki yürürlülük tarihi ilkelerin kanallara uygulandığı ve kanal işlerinin çalıştırıldığı tarih olacaktır. 

    ![Organizasyon kırılımını seç iletişim kutusu](media/Return-policy-page3.PNG "Organizasyon kırılımını seç iletişim kutusu")

5. **Dağıtım zamanlaması** sayfasında, POS'un kanal iade ilkesini kullanabilmesini sağlamak için, **1070** işini çalıştırın.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>POS 'ta kanal iade ilkesini Önizle

POS 'ta izin verilen iade ödeme tiplerini görüntülemek için aşağıdaki örneklerden birinde bulunan adımları izleyin.

1. POS'ta kasiyer veya yönetici olarak oturum açın.
2. **Üst karakter ve çekmece** altında **günlüğü göster**'i seçin.
3. İade işleminin parçası olan hareketi seçin. 
4. Para iadesi yapılacak maddeleri seçin ve ödeme yöntemini seçin.  
- Seçilen ödeme, izin verilen iade ödeme tipleri listesinde ise, kasiyer hareketi tamamlayabilir.
- Ödeme ödemesine izin verilmiyorsa, bir hata mesajı görüntülenir.
- Tüm izin verilen iade ödeme tiplerinin listesini görüntülemek için **tutar vadesini** seçin.

-veya-

1. POS'ta kasiyer veya yönetici olarak oturum açın.
2. **İade hareketi** seçin ve barkod taraması veya el ile giriş kullanarak giriş kodunu girin. 
3. İade işleminin parçası olan hareketi seçin. 
4. Para iadesi yapılacak maddeleri seçin ve ödeme yöntemini seçin.  
- Seçilen ödeme, izin verilen iade ödeme tipleri listesinde ise, kasiyer hareketi tamamlayabilir.
- Ödeme ödemesine izin verilmiyorsa, bir hata mesajı görüntülenir.
- Tüm izin verilen iade ödeme tiplerinin listesini görüntülemek için **tutar vadesini** seçin.

![Geri ödemeye izin verilmiyor](media/Return-policy-page6.png "Geri ödeme türüne izin verilmiyor")



![Ödeme yöntemleri listesi](media/Return-policy-page5.PNG "Geri ödeme türlerine izin veriliyor")

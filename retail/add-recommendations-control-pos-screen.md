---
title: "POS aygıt hareket sayfasında önerileri denetimi ekleyin"
description: "Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Operations kullanarak nasıl ekleneceğini açıklar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 590a009fa4afaf8020b9905020266c4b7293d228
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>POS aygıt hareket sayfasında önerileri denetimi ekleyin

[!include[banner](includes/banner.md)]


Bu konu, öneri denetiminin bir satış noktası (POST) cihazına, ekran düzeni tasarımcısını Microsoft Dynamics 365 for Operations kullanarak nasıl ekleneceğini açıklar.

Microsoft Dynamics 365 for Operations kullanırken ürün önerilerini POS cihazınızda görüntüleyebilirsiniz. *Öneriler*, satınalma geçmişi, istek listelerindeki maddeler ve diğer müşterilerin çevrimiçi ve fiziksel mağazalardan aldıkları maddelere dayanarak müşterilerinizin ilgi duyabilecekleri maddelerdir. Ürün önerilerini görüntülemek için, ekran düzeni tasarımcısını kullanarak bir denetimi hareket ekranına eklemeniz gerekir.

## <a name="open-layout-designer"></a>Açık Düzen tasarımcısı
1.  **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri** öğelerini seçin.
2.  Denetimi eklemek istediğiniz ekranı bulmak için Hızlı Filtre'yi kullanın. Örneğin **Ekran düzeni kimliği** üzerinde, 'F2CP16:9M' kullanarak filtrele.
3.  Listede, istenen kaydı bulun ve seçin. Örneğin, ‘Ad: F2CP16:9M Ekran Düzeni Kimliği: F2CP16:9M’ seçin.
4.  **Düzen tasarımcısı**'na tıklayın.
5.  Düzeni tasarımcısını başlatmak için istemleri izleyin. Kimlik bilgileri istendiğinde, Düzen tasarımcısı **Ekran düzenleri** sayfasından başlatıldığında girilenle aynı kimlik bilgilerini girin.
6.  Oturum açtığınızda, aşağıdakine benzer bir sayfa görüntülenir. Düzen, mağazanız için yapılan özelleştirmelere bağlı olarak farklı olacaktır.

[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Bir görüntüleme seçeneği seçin
-----------------------

İki yapılandırma seçeneği mevcuttur. Mağazanız için en iyi çalışan seçeneği seçin ve denetimin kurulumunu tamamlamak için kalan yönergeleri izleyin. İki seçenek şunlardır:
-   Önerileri her zaman görünür durumdadır.
-   Bir **Öneriler** sekmesi, ekranın sağ tarafındaki kılavuzda görüntülenir.

#### <a name="to-make-recommendations-always-visible"></a>Önerileri her zaman görünür yapmak için

1.  Hareket satırı ayrıntıları alanının yüksekliğini, solundaki müşteri paneliyle aynı boyda olacak şekilde azaltın.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Soldaki menüden, öneriler denetimini hareket satırı ayrıntıları alanı ve hareket erkanının alt ortasındaki düğme kılavuzu arasında sürükleyip bırakın. Bu alana sığacak şekilde yeniden boyutlandırın.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.
4.  Dynamics 365 for Operations içinde, **Perakende ve ticaret** &gt; **Perakende BT** &gt; **Dağıtım tabloları**'na gidin.
5.  Listede **1090 Kayıtları**'nı seçin.
6.  **Şimdi çalıştır** üzerine tıklayın.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Ekranın sağ tarafındaki düğme kılavuzuna bir Öneriler sekmesi eklemek için

1.  Sayfanın sağ tarafında bulunan düğme kılavuzundaki son sekmenin altındaki boş alana sağ tıklayın.
2.  **Özelleştir** üzerine tıklayın.[![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  **Yeni sekme** üzerine tıklayın.
4.  Şimdi eklemiş olduğunuz yeni sekmeyi bulun. Aşağı doğru gitmeniz gerekebilir.
5.  **İçerikler** açılır listesinde, **Önerilen ürünler**'i seçin. [![pic-6](./media/pic-6.png)](./media/pic-6.png)
6.  **Etiket** alanında, önerilenler sekmesi için bir ad yazın. Örneğin, 'Önerilen ürünler' yazın.
7.  **Resim** alanında, sekme üzerinde görünecek resmi seçin.
8.  **Tamam** seçeneğini tıklatın. Yeni sekme düğme kılavuzunda görüntülenir.
9.  Kaydedip Düzen tasarımcısından çıkmak için **X**'i tıklatın.
10. Dynamics 365 for Operations içinde, **Perakende ve ticaret** &gt; **Perakende BT** &gt; **Dağıtım tabloları**'na gidin.
11. Listede **1090 Kayıtları**'nı seçin.
12. **Şimdi çalıştır** üzerine tıklayın.


<a name="see-also"></a>Ayrıca bkz.
--------

[Kişiselleştirilmiş ürün önerilerine genel bakış](personalized-product-recommendations.md)




---
title: "POS aygıt hareket sayfasında önerileri denetimi ekleyin"
description: "Bu konuda öneriler denetim işlemleri için Microsoft Dynamics 365 ekran düzeni tasarımcısı kullanarak satış (POS) aygıtı noktası ekranda hareket eklemek nasıl açıklar."
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>POS aygıt hareket sayfasında önerileri denetimi ekleyin

Bu konuda öneriler denetim işlemleri için Microsoft Dynamics 365 ekran düzeni tasarımcısı kullanarak satış (POS) aygıtı noktası ekranda hareket eklemek nasıl açıklar.

Microsoft Dynamics 365 işlemleri için kullandığınızda, ürün önerileri POS aygıtınızda görüntüleyebilirsiniz. *Öneriler* müşteri kendi satın alma geçmişi, onların istek listesindeki öğeleri ve diğer müşterilerin çevrimiçi satın alınan maddeleri ve Tuğla Dibek depolarında göre ilgilenebileceğiniz maddelerdir. Ürün önerileri görüntülemek için ekran düzeni tasarımcısı kullanarak hareket ekrana bir denetimi eklemeniz gerekir.

## <a name="open-layout-designer"></a>Düzeni tasarımcısı açın
1.  Git **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS**&gt;**ekran düzenleri**.
2.  Hızlı Süzgeç denetimini eklemek istediğiniz ekran bulmak için kullanın. Örneğin, filtre **ekran düzeni kimliği** 'F2CP16:9M' değerini kullanarak alan.
3.  Listede, istenen kaydı bulun ve seçin. Örneğin, Seç ' adı: F2CP16:9M ekran düzeni kimliği: F2CP16:9M'.
4.  ' I **düzeni tasarımcısı**.
5.  Düzeni tasarımcısı başlatmak için istemleri izleyin. Kimlik bilgileri istendiğinde, düzeni tasarımcısı tarafından başlatıldı, kullanımda olan kimlik bilgilerini girin **ekran düzenleri** sayfa.
6.  Oturum açtığınızda, aşağıdaki benzer bir sayfa görüntülenir. Düzen deponuz için yapılan özelleştirmeler bağlı olarak farklı olacaktır.

[![screenlayout-Al-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) bir görüntüleme seçeneği belirleyin
-----------------------

İki yapılandırma seçeneği vardır. Deponuz için en uygun seçeneği seçin ve denetimin ayarlamayı tamamlamak için yönergeleri izleyin. İki seçenek vardır:
-   Önerileri her zaman görünür durumdadır.
-   A **önerileri** sekmesini ekranın sağındaki kılavuzda görüntülenir.

#### <a name="to-make-recommendations-always-visible"></a>Önerileri her zaman görünür yapmak için

1.  Müşteri paneli solunda olarak aynı yükseklikte olması için hareket satırlarını ayrıntı alanının yüksekliğini azaltın. [](./media/pic-2.png)[![screenlayout-Al-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Sol taraftaki menüden sürükleyip öneriler denetimine hareket satırı detaylar alanı ve merkezi ekranın hareket düğme grubundaki arasında. Bu alana sığacak şekilde yeniden boyutlandırın. [](./media/pic-3.png)[![screenlayout-Al-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  ' I **X** kaydetmek ve düzeni Tasarımcısı'ndan çıkmak için.
4.  İşlemler için Dynamics 365 içinde gitmek **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım tabloları**.
5.  Listeden seçin **1090 kaydeder**.
6.  ' I **şimdi çalıştırmak**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Öneriler sekmesini ekranın sağ tarafındaki düğme grubu eklemek için

1.  Sayfanın sağ tarafında bulunan düğme grubu üzerinde son sekmesinin altındaki boş alana sağ tıklatın.
2.  ' I **özelleştirme**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  ' I **yeni sekme**.
4.  Yeni eklediğiniz yeni sekmesini bulun. Aşağı doğru gitmeniz gerekebilir.
5.  İçinde **içeriği** açılır, select **ürünleri tavsiye**. [![PIC-6](./media/pic-6.png)](./media/pic-6.png)
6.  İçinde **etiket** alanında, öneriler sekme için bir ad yazın. Örneğin, 'Önerilen ürünler' yazın.
7.  İçinde **görüntü** alanında, sekmesinde görünen resim seçin.
8.  Click **OK**. Yeni Sekme düğmesinin kılavuzda görüntülenir.
9.  ' I **X** kaydetmek ve düzeni Tasarımcısı'ndan çıkmak için.
10. İşlemler için Dynamics 365 içinde gitmek **perakende ve ticaret**&gt;**perakende BT**&gt;**dağıtım tabloları**.
11. Listeden seçin **1090 kaydeder**.
12. ' I **şimdi çalıştırmak**.


<a name="see-also"></a>Ayrıca bkz.
--------

[Kişiselleştirilmiş ürün önerileri genel bakış](personalized-product-recommendations.md)



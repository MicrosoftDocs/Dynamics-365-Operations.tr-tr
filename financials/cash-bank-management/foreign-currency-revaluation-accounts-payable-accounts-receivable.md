---
title: "Borç hesapları ve Alacak hesapları için yabancı para biriminde yeniden değerleme"
description: "Döviz kuru dalgalanmaları, yabancı para birimlerindeki açık hareketlerin teorik değerinin (defter değerinin) zaman içinde değişmesine neden olur. Bu makalede, Borç hesapları ve Alacak hesaplarındaki açık hareketlerin değerini güncelleştirmek için çalıştırdığınız yabancı para birimi yeniden değerleme işlemi hakkında bilgiler verilmektedir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 69a57cc5a2d652efc2ee14906c64b0dc741da31c
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Borç hesapları ve Alacak hesapları için yabancı para biriminde yeniden değerleme

Döviz kuru dalgalanmaları, yabancı para birimlerindeki açık hareketlerin teorik değerinin (defter değerinin) zaman içinde değişmesine neden olur. Bu makalede, Borç hesapları ve Alacak hesaplarındaki açık hareketlerin değerini güncelleştirmek için çalıştırdığınız yabancı para birimi yeniden değerleme işlemi hakkında bilgiler verilmektedir. 

Yabancı para birimlerindeki açık hareketlerinin teorik değeri veya defter değeri, döviz kurlarındaki dalgalanmalar nedeniyle zaman içinde değişiklik gösterebilir. Borç hesapları ve Alacak hesapları altındaki açık hareketlerin değerini güncelleştirmek için yabancı para birimi yeniden değerleme sürecini işletin. Yabancı para biriminde yeniden değerleme hem Borç hesapları hem Alacak hesapları için yürütülebilir. Süreç, belirli bir tarihteki açık hesapları veya kapatılmamış tutarları yeniden değerlemek için yeni bir döviz kuru kullanır. Bir gerçekleşmemiş kazanç veya kayıp her açık hareket için deftere nakledilen tutarların orijinal tutarlarla yeniden değerlendirilen tutarlar arasındaki farkı neden olur. Borç hesapları ve Alacak hesapları subledgers sonra gerçekleşmemiş kazanç veya kayıp yansıtacak şekilde güncelleştirilir ve muhasebe girişi genel muhasebeye nakledilir.

## <a name="simulate-a-foreign-currency-revaluation"></a>Yabancı para birimi yeniden değerleme simülasyonu
Açık hareketlerde yabancı para birimi tutarlarını yeniden değerlemeden önce aynı tarih ve yöntem için yabancı para birimi yeniden değerleme simülasyon raporu çalıştırabilirsiniz. Simülasyon raporunu çalıştırmak için **Yabancı para birimi yeniden değerleme** sayfasında **Simülasyon** düğmesine basın. Rapor, simülasyon için tanımlanan parametrelere dayalı olarak gerçekleşmemiş kazanç veya kayıp tutarının önizlenmesini sağlar.

## <a name="process-a-foreign-currency-revaluation"></a>Bir yabancı para birimi yeniden değerleme işlemi gerçekleştirin
Kullanım **yabancı para birimi yeniden değerleme** altında sayfa **periyodik görevler** açık hareketler yeniden değerlemek için. Süreci gerçek zamanlı olarak yürütebilir veya bir toplu işlem kullanarak yürütülmek üzere programlayabilirsiniz. Yeniden değerleme işlemi ayarlarını tanımlarken, sonuçları bir rapor yazdırmak istediğinizi doğrulamak emin olun. İşlem tamamlandıktan sonra yeniden değerleme raporu yeniden yazdırılmaları olamaz. Yabancı para birimi yeniden değerleme raporu oluşturduğunuzda müşteri/satıcı düzeyinde ve para birimi düzeyinde çeşitli bakiyeler gösterilir:

-   Yeniden değerlenen yabancı para birimlerinde hareketlere sahip olan müşterilerin veya satıcıların bakiyeleri. Şu bakiyeler gösterilir:
    -   Yabancı para birimindeki toplam orijinal bakiye.
    -   Önceki yeniden değerleme itibariyle, muhasebe para birimi cinsinden toplam yabancı para birimi tutarı.
    -   Önceki yeniden değerleme itibariyle, muhasebe para birimindeki toplam yabancı para birimi tutarı.
    -   Önceki ve güncel yeniden değerleme arasındaki fark. Bu fark ilave gerçekleşmemiş kazanç veya kayıptır.
-   Her bir para birimi için toplam gerçekleşmemiş kazanç veya kayıp.

Bir yabancı para birimi yeniden değerleme işlemi yürüttüğünüzde her seferinde bir kayıt tutulur. **Yabancı para birimi yeniden değerleme** sayfasındaki kayıttan, yeniden değerleme nedeniyle oluşturulmuş hareketlerin ayrıntılı listesini görmek için **Hareketler** öğesini seçin. Her fiş hareketi Yeniden Değerlenmiş açık hareket temsil eder. Açık bir hareketi birden fazla kez yeniden Değerlenmiş aynı fiş kullanan iki kayıtları görürsünüz. Önceki gerçekleşmemiş kazanç veya kayıp ters işlem için bir kayıt olur ve diğer kayıt için yeni gerçekleşmemiş kazanç veya kayıp olacaktır. Yeniden değerleme süresini yürütmek için **Yabancı para birimi yeniden değerleme işlemi** düğmesini tıklayın. Aşağıdaki parametreler için doğru ayarları yapılandırın:

-   **Yöntem** – Seçilen yabancı para birimi yeniden değerleme işleminde kullanılan yöntem:
    -   **Standart** – Yabancı para birimi yeniden değerleme işlerinin sonucun kar ya da zarar olmasından bağımsız olarak nakledildiği anlamına gelir.
    -   **Minimum** – Yabancı para birimi yeniden değerleme işlerinin yalnızca sonucun zarar olması durumunda nakledildiği anlamına gelir.
    -   **Fatura tarihi** – Yabancı para birimi yeniden değerleme işlerinin, muhasebe para birimi cinsinden yeniden orijinal değerine değerleme yapılan hareketlerin orijinal döviz kurunu kullandığı anlamına gelir. Önceden gerçekleştirilen tüm yabancı para birimi yeniden değerleme işlemlerinin etkisi iptal edilir.
-   **İlgili tarih** – Söz konusu tarihte açık (kapatılmamış) tutarlar taşıyan tüm hareketleri bulunduğu tarih. Yabancı para birimindeki tutarlar, ** Para birimi döviz kurları** sayfasında söz konusu tarih için girilen döviz kurları kullanılarak yeniden değerlendirilir. Yabancı para birimi tutarlarına ilgili tarihte yeniden değerleme yapıldığında, bu tarih düzenleme yapılan son yabancı para birimi değerleme işlemi tarihi olur. Halihazırda düzeltilmiş durumdaki hareketler üzerinde son yabancı para birimi değerleme işleminden daha erken bir ilgili tarih için bir yabancı para birimi yeniden değerleme işlemi çalıştırırsanız, daha erken ilgili tarihte açık durumda olan ancak daha yeni bir yabancı para birimi yeniden değerleme tarihine sahip hareketler periyodik iş tarafından düzeltilmez.
-   **Kur tarihi** – Yabancı para birimi yeniden değerleme işleminde kullanılan döviz kurunun belirlendiği tarih.
-   **Şu nakil profilini kullan** – Yabancı para birimi yeniden değerleme işleminin muhasebe girişleri için Alacak hesapları veya Borç hesapları için varsayılan ana hesabı girmek için kullanılan nakil profili:
    -   **Nakil** – Müşteri hareketinin nakil profili kullanılır.
    -   **Seç** – Nakil profilini **Nakil profili** alanına girin.
-   **Nakil profili** – **Şu nakil profilini kullan** alanından **Seç** seçimini yaparsanız bu alana girdiğiniz nakil profili, yabancı para birimi yeniden değerleme hareketlerinin nakil profilini belirler.
-   **Mali boyutlar** – Yabancı para birimi yeniden değerleme hareketlerinin muhasebe girişlerine nakledilen mali boyutlar:
    -   **Yok** – Hiçbir mali boyut nakledilmez. Hesap yapınızda bir zorunlu mali boyut bulunuyorsa yeniden değerleme süreci hala çalışır ve mali boyutları olmayan muhasebe girişleri oluşturur. Öncelikle bir uyarı mesajı alırsınız, ardından yeniden değerlemeyi iptal edebilirsiniz.
    -   **Tablo** – Yabancı para birimi yeniden değerleme işlemi ayarlama hareketlerinde müşteri hesabı veya satıcı hesabı mali boyutlarının nakledildiği anlamına gelir.
    -   **Nakletme** – Yeniden değerleme yapılan hareketin mali boyutlarının yabancı para birimi yeniden değerleme işlemi hareketlerine nakledildiğini gösterir. Varsayılan olarak, orijinal hareketlerin AR/AP genel muhasebe hesabındaki mali boyutlar, yeniden değerleme hareketlerinin AR/AP ana hesabı için kullanılırken, orijinal hareketlerin gider/kıymet/gelir ana muhasebe hesabındaki mali boyutlar yeniden değerleme hareketinin gerçekleşmemiş kazanç/kayıt ana hesabı için kullanılır.




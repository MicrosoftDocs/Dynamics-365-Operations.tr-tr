--- 
title: "Satış komisyonu kurallarını ayarlama"
description: "Bu yordam, satış komisyonu hesaplamanın ve izlemenin nasıl ayarlanacağını ve etkinleştirileceğini gösterir."
author: omulvad
manager: AnnBe
ms.date: 11/03/2017
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
ms.sourcegitcommit: 8e7d2198b4976a6f60f05690d7b6f11f3da55e28
ms.openlocfilehash: 3d5c38b1f07803242350fe016b45c45d49c0b59b
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---
# <a name="set-up-sales-commission-rules"></a>Satış komisyonu kurallarını ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, satış komisyonu hesaplamanın ve izlemenin nasıl ayarlanacağını ve etkinleştirileceğini gösterir. Bu yordam, hem müşteri hem de ürün komisyon gruplarının nasıl oluşturulacağını ve seçili bir müşterinin ve ürünün ilgili gruplara nasıl bağlanacağını gösterir. Bu gruplar daha sonra bir müşteri, ürün ve satış temsilcisinin komisyona hak kazanabilmesi için satış siparişiyle eşleşmesi gereken bir satış temsilcisi kombinasyonu oluşturmak üzere komisyon hesaplaması ayarlarında kullanılır. Komisyonun hesaplanması tek bir müşteri ve/veya ürün için de yapılabileceğinden müşteri mi yoksa ürün komisyon grubu oluşturulacağı isteğe bağlıdır. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisyon gruplarını ve komisyon oranlarını ayarlama
1. Satış ve pazarlama > Komisyonlar > Komisyon için müşteri grupları'na gidin.
2. Yeni'ye tıklayın.
3. Grup alanında bir değer girin.
4. İsim alanına bir değer yazın.
5. Kaydet'e tıklayın.
6. Sayfayı kapatın.
7. Satış ve pazarlama > Komisyonlar > Ürün grupları'na gidin.
8. Yeni'ye tıklayın.
9. Grup alanında bir değer girin.
10. İsim alanına bir değer yazın.
11. Sayfayı kapatın.
12. Satış ve pazarlama > Komisyonlar > Satış grupları'na gidin.
    * Komisyon satış grubu, ilgili satış grubuyla ilişkili bir müşteri belirli ürünler satın aldığında bir komisyon kazanmaya uygun olan satış temsilcisi rollerini belirtir.  
    * USMF demo verisi şirketinde, "Satış temsilcileri ABD." adında bir satış grubu vardır.  
13. Eylem Bölmesinde, Genel öğesine tıklayın.
14. Satış temsilcisi'ne tıklayın.
    * Satış temsilcisi sayfası, şirketin bir özel komisyon grubu ile ilişkili olan satış personelinin bir listesini görüntüler. Aynı gruba birden fazla satış temsilcisi atayabilirsiniz ve bunların ilgili toplam komisyon ücreti payını bir yüzde değeri olarak tanımlayabilirsiniz. Tüm çalışanlar arasında toplam komisyon payı 100'ü geçemez.  
15. Listede, seçili satırı işaretleyin.
16. Düzenle öğesine tıklayın.
17. Komisyon payını '50' olarak ayarlayın.
18. Yeni'ye tıklayın.
19. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
20. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ad alanını 'Sema Yıldırım' değeriyle filtreleyin.
21. Seç'e tıklayın.
22. Komisyon payını '50' olarak ayarlayın.
23. Kaydet'e tıklayın.
24. Satış ve pazarlama > Komisyonlar > Komisyon hesaplama'ya gidin.
    * Komisyon hesaplama sayfasında, müşteri ve ürüne ilişkin önceden ayarlanmış bir kombinasyon içerdiğinde satış hareketi için çalışanın alacağı komisyon oranını tanımlarsınız. Komisyon oranı ayarının bir parçası olarak, komisyon hesaplama temelini ve iskonto içerip içermeyeceğini belirtmeniz gerekir. Komisyon oranı etkin olduğunda bir geçerlilik dönemi de girebilirsiniz.  
25. Yeni'ye tıklayın.
26. Madde kodu alanında, "Grup"u seçin.
27. Madde ilişkisi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
28. Listede, daha önce oluşturduğunuz grubu bulun ve seçin.
29. Listede, seçili satırdaki bağlantıya tıklayın.
30. Müşteri kodu alanında 'Grup' öğesini seçin.
31. Müşteri ilişkisi alanında, aramayı açmak için açılır menü düğmesini tıklatın.
32. Listede, daha önce ayarladığınız grubu seçin.
33. Satış temsilcisi ilişkisi alanında, aramayı açmak için açılır menü düğmesini tıklatın.
34. Listede, istenen kaydı bulun ve seçin.
    * "Satır iskontosundan önce" seçeneğini tutun.  
    * Komisyon değeri hesaplaması için temel olarak "Gelir" seçeneği tutun.    
35. Komisyon yüzdesi alanında bir sayı girin.
36. Kaydet'e tıklayın.

## <a name="setting-up-commission-posting"></a>Komisyon nakil ayarları
1. Satış ve pazarlama > Komisyonlar > Komisyon nakil'e gidin.
    * Komisyon ücretleri çalışanlara ödeneceğinden Genel muhasebe'de mali nakli uygun hesaplara doğru şekilde yapılacak biçimde ayarlanmış olması gerekir. Bu komisyon nakil sayfasında yapılır. Geçerli şirket için kullanılabilir ayarı gözden geçirin. Genellikle, komisyon tutarları özel bir gider hesabına nakledilir ve özel bir alacaklı hesabına mahsup edilir. Komisyon nakil kuralları ayarlanmamışsa, sistem komisyona uygun olan satış siparişini faturalama işlemini tamamlayamaz.  
2. Sayfayı kapatın.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Bir müşteri ve bir ürün için bir komisyon grubu atama
1. Satış ve pazarlama > Komisyonlar > Tüm müşteriler'e gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Düzenle'yi tıklatın.
5. Satış siparişi varsayılanları bölümünü genişletin.
6. Komisyon grubu alanında, aramayı açmak için açılır menü düğmesini tıklatın.
7. Listede, daha önce oluşturduğunuz grubu seçin.
8. Satış grubu alanında, aramayı açmak için açılır menü düğmesini tıklatın.
9. Listede, istenen kaydı bulun ve seçin.
10. Kaydet'e tıklayın.
11. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
12. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Ürün numarası alanını 'T0020' değeriyle filtreleyin.
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. Düzenle'yi tıklatın.
15. Satış bölümünü genişletin.
16. Komisyon grubu alanında, aramayı açmak için açılır menü düğmesini tıklatın.
17. Listede, daha önce oluşturduğunuz komisyon grubunu seçin.



---
title: Satış komisyonu kurallarını ayarlama
description: Bu yordam, satış komisyonu hesaplamanın ve izlemenin nasıl ayarlanacağını ve etkinleştirileceğini gösterir.
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b1ea016817462269a13e450c8c7576546c7f0eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439223"
---
# <a name="set-up-sales-commission-rules"></a>Satış komisyonu kurallarını ayarlama

[!include [banner](../../includes/banner.md)]

Bu yordam, satış komisyonu hesaplamanın ve izlemenin nasıl ayarlanacağını ve etkinleştirileceğini gösterir. Bu yordam, hem müşteri hem de ürün komisyon gruplarının nasıl oluşturulacağını ve seçili bir müşterinin ve ürünün ilgili gruplara nasıl bağlanacağını gösterir. Bu gruplar daha sonra bir müşteri, ürün ve satış temsilcisinin komisyona hak kazanabilmesi için satış siparişiyle eşleşmesi gereken bir satış temsilcisi kombinasyonu oluşturmak üzere komisyon hesaplaması ayarlarında kullanılır. Komisyonun hesaplanması tek bir müşteri ve/veya ürün için de yapılabileceğinden müşteri mi yoksa ürün komisyon grubu oluşturulacağı isteğe bağlıdır. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-commission-groups-and-commission-rates"></a>Komisyon gruplarını ve komisyon oranlarını ayarlama
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Komisyonlar > Komisyon için müşteri grupları**'na gidin.
2. **Yeni**'yi seçin.
3. **Grup** alanına bir değer girin.
4. **Ad** alanına bir değer yazın.
5. **Kaydet**'i seçin.
6. Sayfayı kapatın.
7. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Komisyonlar > Madde grupları**'na gidin.
8. **Yeni**'yi seçin.
9. **Grup** alanına bir değer girin.
10. **Ad** alanına bir değer yazın.
11. **Kaydet**'i seçin.
12. Sayfayı kapatın.
13. **Satış ve pazarlama > Komisyonlar > Satış grupları**'na gidin.
    - Komisyon satış grubu, ilgili satış grubuyla ilişkili bir müşteri belirli ürünler satın aldığında bir komisyon kazanmaya uygun olan satış temsilcisi rollerini belirtir.  
    - USMF demo verisi şirketinde, "Satış temsilcileri ABD." adında bir satış grubu vardır.  
14. **Eylem Bölmesinde**, **Genel**'i seçin.
15. **Satış temsilcisi**'ne tıklayın. Satış temsilcisi sayfası, şirketin bir özel komisyon grubu ile ilişkili olan satış personelinin bir listesini görüntüler. Aynı gruba birden fazla satış temsilcisi atayabilirsiniz ve bunların ilgili toplam komisyon ücreti payını bir yüzde değeri olarak tanımlayabilirsiniz. Tüm çalışanlar arasında toplam komisyon payı 100'ü geçemez. 
16. Listede, seçili satırı işaretleyin.
17. **Düzenle** öğesini seçin.
18. **Komisyon hissesi**'ni "50" olarak ayarlayın.
19. **Yeni**'ye tıklayın.
20. **Ad** alanında, açılır menü düğmesine tıklayarak aramayı açın.
21. Kayıtları bulmak için **Hızlı Filtre**'yi kullanın. Örneğin, Ad alanını 'Sema Yıldırım' değeriyle filtreleyin.
22. **Seç**'e tıklayın.
23. **Komisyon hissesi**'ni "50" olarak ayarlayın.
24. **Kaydet**'e tıklayın.
25. **Satış ve pazarlama > Komisyonlar > Komisyon hesaplama**'ya gidin. **Komisyon hesaplama** sayfasında, müşteri ve ürüne ilişkin önceden ayarlanmış bir kombinasyon içerdiğinde satış hareketi için çalışanın alacağı komisyon oranını tanımlarsınız. Komisyon oranı ayarının bir parçası olarak, komisyon hesaplama temelini ve iskonto içerip içermeyeceğini belirtmeniz gerekir. Komisyon oranı etkin olduğunda bir geçerlilik dönemi de girebilirsiniz.  
26. **Yeni**'ye tıklayın.
27. **Madde kodu** alanında, "Grup"u seçin.
28. **Madde ilişkisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
29. Listede, daha önce oluşturduğunuz grubu bulun ve seçin.
30. **Müşteri kodu** alanında "Grup"u seçin.
31. **Müşteri ilişkisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
32. Listede, daha önce ayarladığınız grubu seçin.
33. **Satış temsilcisi ilişkisi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
34. Listede, istenen kaydı bulun ve seçin.
    - "Satır iskontosundan önce" seçeneğini tutun.  
    - Komisyon değeri hesaplaması için temel olarak "Gelir" seçeneği tutun.    
35. Komisyon yüzdesi alanında bir sayı girin.
36. **Kaydet**'e tıklayın.

## <a name="setting-up-commission-posting"></a>Komisyon nakil ayarları
1. **Gezinti bölmesi > Satış ve pazarlama > Komisyonlar > Deftere komisyon nakli**'ne gidin. Komisyon ücretleri çalışanlara ödeneceğinden **Genel muhasebe**'de mali nakli uygun hesaplara doğru şekilde yapılacak biçimde ayarlanmış olması gerekir. Bu, **Deftere komisyon nakli** sayfasında yapılır. Geçerli şirket için kullanılabilir ayarı gözden geçirin. Genellikle, komisyon tutarları özel bir gider hesabına nakledilir ve özel bir alacaklı hesabına mahsup edilir. Komisyon nakil kuralları ayarlanmamışsa, sistem komisyona uygun olan satış siparişini faturalama işlemini tamamlayamaz.  
2. Sayfayı kapatın.

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>Bir müşteri ve bir ürün için bir komisyon grubu atama
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Müşteriler > Tüm müşteriler**'e gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Düzenle**'yi tıklatın.
5. **Satış siparişi varsayılanları** bölümünü genişletin.
6. **Komisyon grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, daha önce oluşturduğunuz grubu seçin.
8. **Satış grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, istenen kaydı bulun ve seçin.
10. **Kaydet**'e tıklayın.
11. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.
12. Kayıtları bulmak için **Filtre**'yi kullanın. Örneğin, Ürün numarası alanını 'T0020' değeriyle filtreleyin.
13. Listede, seçili satırdaki bağlantıya tıklayın.
14. **Düzenle**'yi tıklatın.
15. **Satış** bölümünü genişletin.
16. **Komisyon grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
17. Listede, daha önce oluşturduğunuz komisyon grubunu seçin.
18. **Kaydet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Kullanıcı arabirimi öğeleri
description: Bu makalede, uygulamadaki kullanıcı arabirimi (UI) öğeleri açıklanmaktadır.
author: jasongre
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: ''
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: de6e4f8472cf73fb1d9874a57442622c0da23b54
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275957"
---
# <a name="user-interface-elements"></a>Kullanıcı arabirimi öğeleri


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu makalede, uygulamada kullanılan kullanıcı arabirimi (UI) öğeleri açıklanmaktadır. Kullanıcıların arabirimde gezinebilmeleri için önce, arabirimi oluşturan öğelerin adlarını ve işlevlerini bilmeniz önemlidir.

## <a name="overview"></a>Genel bakış

- **Eylem bölmesi** - Gezinti çubuğunun altındaki çubuk. Burada, sayfada gösterilen kayıtları değiştirmek için sekmeler seçebilirsiniz. Kayıtları düzenleyebilir ve burada kaydedebilirsiniz.  
- **Bilgi kutusu** - Bilgileri görebilir ve belirli kayıtların faaliyetlerini bu bölmede takip edebilirsiniz.  
- **Bilgi kutusu bölmesi** Burada bir kaydın farklı yönlerini bilgi kutusunda görüntülemek üzere kaydırabilirsiniz.  
- **Filtre bölmesi** - Bazı sayfalarda bu bölmeyi açmak için **Filtreleri göster**'i seçebilirsiniz. Sayfada görünür durumda olan sonuçları daraltmanıza olanak tanır.  
- **Gezinti çubuğu** - Arabirimin en üstündeki çubuktur. **Dynamics 365 portalı**, **Arama**, **şirket seçici**, **Eylem merkezi**, **Ayarlar**, **Yardım ve Destek** ve kullanıcı profilini içerir.  
- **Gezinti listesi** - Bazı sayfalarda belirli bir kaydı bulmak için bu bölmeyi kaydırabilirsiniz. Seçildiğinde, kaydın ayrıntıları sayfada görüntülenir.  
- **Gezinti bölmesi** - En soldaki bölmedir. Buradan, üründe herhangi bir sayfayı bulabilirsiniz.  
- **Sayfa** - Arabirimin merkezi odağıdır. Diğer Kullanıcı arabirimi bileşenlerinde yaptığınız seçimler, burada gösterilen kayıtları etkileyecektir.  
- **Bölme** - En sağdaki bölmedir. Bu, bir kaydın özelliklerinin değiştirilmesi ve kaydedilmesi gereken bazı durumlarda açılacaktır.  
- **Sekme** - Eylem bölmesine başvurulduğunda, eylem bölmesinde belirli bir seçeneği belirlediğinizde görünen seçenekler menüsüdür.  

![Aşağıdaki resim bu öğelerin arabirim üzerinde yerleşimini gösterir.](media/user-interface-01.png)

## <a name="tabs-fields-and-sections"></a>Sekmeler, alanlar ve bölümler

*Sekme* sayfada aynı sayfadaki bir kaydın farklı bir bölümünü açan bir seçimdir. Genellikle, belirli *alanları* veya yazılı girişe izin veren kullanıcı arabirimi öğelerini değiştirmenizi sağlar. 

*Hızlı sekme* aynı zamanda birden fazla sekmenin görünür olmasını sağlayan bir sekmedir. Bir FastTab'ı sağ ucundaki aşağı dönük oku seçerek genişletebilirsiniz.

![Aşağıdaki resimde sekme ve hızlı sekmeler örneği gösteriliyor.](media/user-interface-02.png)

*Bölüm* bir sekmeye benzer. "Bölüm" sözcüğü çoğunlukla, belirli bir bilgi kategorisini düzenleyen bir sayfanın herhangi bir alanını tanımlamak için kullanılır. Aşağıdaki resimde, Özet, siparişler ve Sık Kullanılanlar ve bağlantılar bölümlerin tüm örnekleridir.

![Aşağıdaki resimde sekme ve bölüm örneği gösteriliyor.](media/user-interface-03.png)

## <a name="dialog-boxes-and-drop-down-menus"></a>İletişim kutuları ve açılan menüler

*İletişim kutusu*, bir kayıt oluşturmak veya değiştirmek için belirli seçimler yapıldığında açılan bir bölmedir. İletişim kutuları, yazılı giriş girmenizi sağlayan alanlar içerir. Bazen, belirli bir alan, seçim yapabileceğiniz seçeneklerin listesini açan aşağı doğru bakan bir ok seçmenize izin verir. Buna *açılır menü* adı verilir. Aşağıdaki resimde, **Tür** ve **Müşteri grubu** alanları, açılan menüyü açma seçeneğini içerir.

![Aşağıdaki resimde iletişim kutusu örneği gösteriliyor.](media/user-interface-04.png)

Bazı durumlarda, bir iletişim kutusu seçtiğinizde belirli bir düğmenin yakınında açılır. Buna *iletişim kutusu* adı verilir. Aşağıdaki resimde, açılır iletişim kutusunu açan **Başlangıç tarihi** düğmesi seçilmiştir.

![Aşağıdaki resimde açılır menüdeki iletişim kutusu örneği gösteriliyor.](media/user-interface-05.png)

## <a name="notifications"></a>Bildirimler

Gördüğünüz nesnelerde yapılan belirli değişiklikler *bildirim* olarak görüntülenecektir. Belirli bir müşterinin bilgileri değiştirildiğinde bildirimler size bildirebilir veya sistem belirli alanlara eklediğiniz girişleri kabul edemediyseniz sizi uyarabilir. [Uyarılara genel bakış](../get-started/alerts-overview.md) konusunda bildirim aldığın nasıl özelleştirileceğini öğrenebilirsiniz.

Bildirimler çeşitli şekillerde görünür.
- **Özellik Açıklamaları** – Özelliğin ne için kullanıldığın açıklamasını sunmak için bir alan, sekme veya başka bir düğmenin yanında görünür. 
- **Eylem Merkezi** - Bildirimi içeren bir kutu gezinti çubuğundaki Eylem Merkezi düğmesinin yanında görüntülenir. **Eylem Merkezi**'ni seçerek bildirimle ilgili ayrıntıları görebilirsiniz.  
- **İleti çubuğu** - Bu Işlem, eylem bölmesinin altında görünür.  

Aşağıdaki resimde bu tür bildirimlerin örnekleri gösterilmektedir.

![Aşağıdaki resimde bildirimlerin örnekleri gösterilmektedir.](media/user-interface-06.png)

- **İleti kutusu** - Bu, arabirimin üzerinde görünür ve ürünü kullanmaya devam edebilmek için önce birlikte işlem yapılmalıdır.  

![Aşağıdaki resimde ileti kutusu örneği gösteriliyor.](media/user-interface-07.png)

## <a name="toolbars-grids-and-lists"></a>Araç çubukları, kılavuzlar ve listeler

*Araç çubuğu*, alan ekleme veya kayıt kaldırma gibi araçlar içerir. Bazen, sayfada bir *kılavuz*'un üstündeki bir araç çubuğu görünür. Bu alan, kılavuz, çeşitli veri sütunlarına sahip kayıt satırları için verilen addır. Tüm kılavuzların üzerinde araç çubukları yoktur.

*Liste*, içinden kaydırabileceğiniz bir kayıt koleksiyonuna verilen addır. Bu kayıtları, seçerek sayfaya getirebilirsiniz. Bu durum genellikle bir kılavuz açar.

![Aşağıdaki resim araç çubukları, kılavuzlar ve listelere örnekler gösterir.](media/user-interface-08.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

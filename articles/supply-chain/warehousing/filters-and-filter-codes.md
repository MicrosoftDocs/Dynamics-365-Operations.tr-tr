---
title: Ambar hareketleri için ürün filtrelerini yapılandırma
description: Bu konuda, bir ambardaki stok maddelerini kategorilere ayırmak için ürün filtrelerinin ve filtre kodlarının nasıl yapılandırılacağı açıklanmaktadır. Ayrıca, belirli bir maddeyi hangi müşterilerin sipariş edebileceğini ve belirli bir satıcıdan hangi maddelerin satın alınabileceğini belirtmek için de filtreleri kullanabilirsiniz.
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: dbf92c5e199ecadb3e4f7c6130427d449ef5b6c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251781"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Ambar hareketleri için ürün filtrelerini yapılandırma

[!include [banner](../includes/banner.md)]

Bu konuda, bir ambardaki stok maddelerini kategorilere ayırmak için ürün filtrelerinin ve filtre kodlarının nasıl yapılandırılacağı açıklanmaktadır. Ayrıca, belirli bir maddeyi hangi müşterilerin sipariş edebileceğini ve belirli bir satıcıdan hangi maddelerin satın alınabileceğini belirtmek için de filtreleri kullanabilirsiniz.

Ayrıca, bir ambardaki stok maddelerini otomatik olarak düzenlemek ve filtre uygulanmış maddeleri filtre gruplarında bir araya getirmek için ürün filtreleri ayarlayabilir ve kullanabilirsiniz. Filtreler; işleme, satın alma ve satış işlemleri için maddeleri kategorilere ayrımak için kullanılabilir. Maddelerin işlenme şekli ağırlıklarına veya işlenme kısıtlamalarına bağlı olduğunda maddeleri bir grup altında toplamak veya farklı gruplara ayırmak isteyebilirsiniz. Ayrıca, bir maddenin hangi müşterilere satılabileceğini veya hangi satıcılardan satın alınabileceğini de belirtebilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce yerine getirilmesi gereken önkoşullar aşağıdaki tabloda gösterilmiştir.

| Önkoşul | Yönergeler |
|---|---|
| **Serbest bırakılan ürün ayrıntıları** sayfasında ürünleri yapılandırmaya başlamadan önce, ürünün depolama boyutu grubu için ambar işlemesini açmanız gerekir. | **Ürün bilgileri yönetimi \> Kurulum \> Boyut ve varyant grupları \> Depolama boyut grupları**'na gidin ve **Ambar yönetimi süreçlerini kullan** seçeneğinin *Evet* olarak ayarlandığı bir depolama boyutu grubu seçin veya oluşturun. |
| Müşteri filtreleri ve/veya satıcı filtrelerini kullanacaksanız bunların kullanımını Ambar yönetimi parametrelerinde etkinleştirmeniz gerekir. | **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin. **Ürün filtreleri** sekmesinde, **Müşteri filtrelerini etkinleştir** ve/veya **Satıcı filtrelerini etkinleştir** seçeneğini *Evet* olarak ayarlayın. |

## <a name="set-up-product-filters"></a>Ürün filtrelerini ayarlama

Ürün filtreleri, numaralandırma (enum) değerleri olan en fazla 10 **Filtre başlığı** özelliği sağlar. Bu enum değerleri, ürün filtresi oluşturduğunuzda seçilebilir. *Kod 1*'den *Kod 10*'a kadar olan enum değerleri, sistem tarafından tanımlanır ve bir maddenin belirli bir özelliğini veya özniteliğini temsil eder. Örneğin, *Kod 1* tehlikeli madde sınıflandırmasına sahip maddeleri temsil edebilir. *Kod 2*, yalnızca satıcıların satın alabileceği maddeleri temsil edebilir. Ürün filtreleri, **Filtre başlığı** değeriyle ilişkilendirilen özel **Filtre kodu** değerini tanımlar.

1. **Ambar Yönetimi \> Kurulum \> Ürün filtreleri \> Ürün filtreleri**'ne gidin.
1. Eylem Bölmesinde, ızgaraya ürün filtresi eklemek için **Yeni**'yi seçin.
1. **Filtre başlığı** alanında bir değer seçin.
1. **Filtre kodu** alanına bir değer girin.

    ![Ürün filtresi ayarlama](media/Product_Filters10.png "Ürün filtresi ayarlama")

1. **Açıklama** alanına, kodun adını girin. Örneğin, *Kod 2* satıcıları temsil edebilir. Böylece, belirli bir satıcı veya satıcı grubu için bir ürün filtresi oluşturabilirsiniz. Daha fazla bilgi için bu konunun ilerleyen kısımlarında yer alan [Satıcı filtre kodlarını ayarlama](#vendor-product-filters) bölümüne bakın.

    ![Ürün filtreleri kümesi](media/Product_Filters.png "Ürün filtreleri kümesi")

## <a name="set-up-product-filter-groups"></a>Ürün filtresi gruplarını ayarlama

Filtre kodlarını gruplandırmak için filtre gruplarını kullanabilirsiniz. Bu özellik, grubun bir yerleşim yönergesi sorgusunda kullanıldığı durumlarda ve kod serileri yerine grup için arama yapmak istediğinizde yararlıdır. Her filtre grubu, bir madde grubuyla ilişkilidir.

> [!IMPORTANT]
> Tüm ürün filtre grupları, *Kod 4*'ten yüksek (*Kod 5* ile *Kod 10* arası) filtre grupları için uygun olmayabilir. Örneğin, serbest bırakılan ürünler için tüm ürün filtre kodları eklenebilse de filtre kodları gruplandırması güncelleştirilmez. Bu davranış sonraki sürümlerde güncelleştirilebilir.

Filtre gruplarını ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ürün filtreleri \> Ürün filtresi grupları**'na gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Grup 1** ve **Grup 2** alanlarında, maddeleri kategorilere ayırmak için kullanılacak adları girin.
1. **Ayrıntılar** hızlı sekmesinde, satır eklemek için **Yeni**'yi seçin.
1. **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarına filtre grubu için başlangıç ve bitiş tarihlerini girin.
1. **Madde grubu** alanında, ürün filtresinin uygulanacağı madde grubunu seçin.
1. **Kod 1** ile **Kod 10** alanları arasında, gruba eklenecek filtre kodlarını gereken şekilde seçin.

    ![Madde grubu](media/ProdFilterGroup.png "Madde grubu")

> [!NOTE]
> Sayfayı kapatırken bir hata iletisi alırsanız, kod kurulumu eksik olabilir. **Madde grupları** sayfasında, **Madde grubu için filtre kodu 1 ata**, **Madde grubu için filtre kodu 2 ata** vb. onay kutularını seçerek kodları bir madde grubu için zorunlu hale getirebilirsiniz.

## <a name="set-up-filter-codes-on-item-groups"></a>Madde gruplarında filtre kodları ayarlama

Bir madde grubunda filtre kodları ayarlayarak söz konusu madde grubuna iliştirilmiş ürünler için gerekli kodları yapabilirsiniz.

Madde gruplarında filtre kodlarını ayarlamak için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Kurulum \> Stok \> Madde grupları**'na gidin.
1. Eylem bölmesinde, bir öğe grubu oluşturmak için **Yeni**'yi seçin.
1. **Madde grubu** alanına bir ad girin.
1. **Ad** alanında, bir açıklama girin.
1. **Ambar** hızlı sekmesindeki **Filtre gerekli** alanında, madde grubuyla ilişkili ürünler için belirtilmesi gereken filtre kodlarının onay kutularını seçin.

    Yayınlanmış bir ürünü güncelleştirmek için **Serbest bırakılan ürün ayrıntıları** sayfasını açın ve ardından Eylem Bölmesinde **Düzenle**'yi seçin. Kodlarla ilişkilendirilmiş filtreler **Ambar** hızlı sekmesinde kullanılabilir hale gelir.

    ![Madde grupları](media/ItemGroup10.png "Madde grupları")

1. **Madde grubu filtresi** bölümünde, filtre grubunun bir madde için varsayılan filtre grubu olması için eşleşmesi gereken filtrelerin onay kutularını seçin.

    Örneğin, **Filtre kodu 1 kullan** ve **Filtre kodu 2 kullan** onay kutuları seçiliyse, filtre grubunun seçilmesi için maddenin hem filtre kodu 1'inin hem de filtre kodu 2'sinin madde grubunun filtre grubu kurulumuyla eşleşmesi gerekir. Yeni bir madde oluşturduğunuzda seçili filtre grubu, **Serbest bırakılan ürün ayrıntıları** sayfasının **Ambar** hızlı sekmesindeki **Grup 1** ve **Grup 2** alanlarında varsayılan filtre grubu olur.

> [!IMPORTANT]
> Ürün filtresi kodları yalnızca gelişmiş ambar yönetimini kullanan maddeler için etkinleştirilir.

## <a name="specify-filter-codes-for-released-products"></a>Serbest bırakılan ürünler için filtre kodları belirtme

Serbest bırakılan ürünlerin filtre kodlarını belirtmek için bu adımları izleyin. Örneğin, belirli satıcıların satın aldığı tehlikeli ürünleri gruplandırmak için filtre kodlarını kullanabilirsiniz.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Eylem bölmesinde **Yeni**'yi seçerek ürün oluşturun.
1. **Serbest bırakılan yeni ürün** iletişim kutusunda, yeni bir ürünün temelini oluşturmak için gereken verileri girin ve **Tamam**'ı seçin.

    Ürüne eklenen madde grubu, filtre kodları için yapılandırılmadığı sürece ürün filtre kodları etkinleştirilmez.

    Daha fazla bilgi için [Yeni ürün oluşturma](../pim/tasks/create-new-product.md) konusuna bakın.

1. **Ambar** hızlı sekmesindeki **Ürün filtresi kodları** bölümünde, ürünün filtre kodlarını belirtmek için gereken şekilde **Kod 1** ile **Kod 10** arasındaki filtre kodlarını seçin.

## <a name="set-up-generally-available-items"></a>Genel olarak kullanılabilir maddeleri ayarlama

Belirli stok maddelerini yalnızca müşteriler için, satıcılar için veya hem müşteriler hem de satıcılar için kullanılabilir hale getirebilirsiniz.

> [!NOTE]
> Müşteri ve satıcı filtreleri, genel olarak kullanılabilir olarak ayarlanmış maddeler için geçerli değildir.

Genel olarak kullanılabilir maddeleri ayarlamak için aşağıdaki adımları takip edin.

1. **Ambar yönetimi \> Kurulum \> Ürün filtreleri \> Genel olarak kullanılabilir ürünler**'e gidin.
1. Eylem bölmesinde **Yeni**'yi seçerek kayıt oluşturun.
1. **Müşteri veya satıcı** alanında, maddeleri müşteriler, satıcılar veya her ikisi tarafından kullanılabilir hale getirmek için *Müşteri*, *Satıcı* veya *Tümü* seçeneklerinden birini belirleyin.
1. **Başlangıç tarihi/saati** alanına maddenin kullanılabilir olacağı tarih ve saati girin.
1. **Madde grubu** alanında madde grubunu seçin.
1. **Kod 1**-**Kod 10** alanlarında, genellikle kullanılabilir olan maddeleri sınırlandırmak üzere filtre kodlarını seçin.

    Bir madde grubu seçtiğinizde, bu madde grubunu genel olarak kullanılabilir biçiminde ayarlarsınız. Bu alanlardaki filtre kodlarını seçerek, kullanılabilir maddeleri sınırlandırırsınız.

## <a name="set-up-customer-product-filters"></a>Müşteri ürün filtrelerini ayarlama

**Genel olarak kullanılabilir maddeler** sayfasındaki filtre kurulumuyla kullanılabilir hale getirilen maddelere ek olarak belirli bir müşteri tarafından kullanılabilir olması gereken maddeleri belirtmek için bu isteğe bağlı yordamı kullanabilirsiniz. Tek bir müşteri için birden fazla filtre ayarlayabilirsiniz.

Müşteri filtre kodlarını ayarlamak için aşağıdaki adımları izleyin.

1. **Satış ve pazarlama \> Müşteriler \> Tüm müşteriler** öğesine gidin.
1. Müşteri seçin.
1. Eylem Bölmesi'nde, **Müşteri** sekmesindeki **Kurulum** grubunda **Ürün filtreleri**'ni seçin.
1. **Ürün filtresi kodları** sayfasında, Eylem Bölmesindeki **Yeni**'yi seçin.
1. **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarına, seçili madde grubu için başlangıç ve bitiş tarihlerini girin.
1. **Madde grubu** alanında madde grubunu seçin.
1. **Kod 1**-**Kod 10** alanlarında, seçili madde grubundaki müşterilere kullanılabilir olarak sunulacak maddeleri sınırlandırırken ölçüt olarak kullanmak üzere filtre kodlarını seçin. Madde grubu için ayarlanmış her filtre kodu için bir seçim yapmalısınız.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Satıcı ürün filtrelerini ayarlama

**Genel olarak kullanılabilir maddeler** sayfasındaki filtre kurulumuyla kullanılabilir hale getirilen maddelere ek olarak belirli bir satıcı tarafından kullanılabilir olması gereken maddeleri belirtmek için bu isteğe bağlı yordamı kullanabilirsiniz. Tek bir satıcı için birden fazla filtre ayarlayabilirsiniz.

Satıcı filtre kodlarını ayarlamak için aşağıdaki adımları izleyin.

1. **Tedarik ve kaynak \> Satıcılar \> Tüm satıcılar**'a gidin.
1. Bir satıcı seçin.
1. Eylem Bölmesi'nde, **Satıcı** sekmesindeki **Kurulum** grubunda **Ürün filtreleri**'ni seçin.
1. **Filtre kodları** sayfasında, Eylem Bölmesindeki **Yeni**'yi seçin.
1. **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarına, seçili madde grubu için başlangıç ve bitiş tarihlerini girin.
1. **Madde grubu** alanında madde grubunu seçin.
1. **Kod 1**-**Kod 10** alanlarında, seçili madde grubundaki satıcılara kullanılabilir olarak sunulacak maddeleri sınırlandırırken ölçüt olarak kullanmak üzere filtre kodlarını seçin. Madde grubu için ayarlanmış her filtre kodu için bir seçim yapmalısınız.

> [!NOTE]
> Satıcı ürün filtrelerinin kurulumu, ilişkili depolama boyutu grubu için ambar yönetimi işlemlerinin etkinleştirildiği serbest bırakılan ürünler için geçerlidir. Sistemin, kullanıcıların satınalma siparişi satırları oluşturduğu sırada belirli bir maddeyi belirli bir satıcıdan almalarına izin verip vermeyeceğini belirlemek için filtre kodları kullanılır. Microsoft Dynamics 365 Supply Chain Management, satıcı onayını işlemek için iki yönteme sahiptir. **Onaylanan satıcı denetim yöntemi** alanının *Yalnızca uyarı* veya *İzin verilmez* olarak ayarlandığı bir durumda bir veya daha fazla serbest bırakılan ürün varsa, her iki satıcı onayı yöntemi de bu maddeler için etkinleştirilebilir. Bu durum, kullanıcılar satınalma siparişi satırları oluştururken sorunlara neden olabilir.

## <a name="see-also"></a>Ayrıca bkz.

[Daha fazla bilgi için WMS Ambar Filtre Kodları blog gönderisini inceleyin](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
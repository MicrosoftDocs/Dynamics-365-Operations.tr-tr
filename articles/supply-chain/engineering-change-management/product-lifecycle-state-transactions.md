---
title: Ürün yaşam döngüsü durumu ve hareketler
description: Bu konu, bir mühendislik ürünü yaşam döngüsü boyunca ilerlerken her yaşam döngüsü durumu için hangi hareketlere izin verileceğini nasıl denetleyebileceğinizi açıklamaktadır.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9c6ba9831b84e1220ee158d8186675107b490124
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266187"
---
# <a name="product-lifecycle-states-and-transactions"></a>Ürün yaşam döngüsü durumu ve hareketler

[!include [banner](../includes/banner.md)]

Bir mühendislik ürünü yaşam döngüsü boyunca ilerlerken her yaşam döngüsü durumu için hangi hareketlere izin verileceğini belirlemeniz önemlidir. Örneğin, henüz olgun durumda olmayan ürünler bir satış siparişine yerleştirilmemelidir. Alternatif olarak, bir ürün kullanım ömrü durumunun sonuna geliyorsa o ürünün içe akışını denetlemek isteyebilirsiniz.

Bir mühendislik ürünü için, yaşam döngüsü durumunda yapılan değişiklikler ürünün mühendislik sürümlerine bağlıdır. Bu nedenle, ürünün yaşam döngüsü durumu ürünün mühendislik sürümlerine de bağlanabilir. Ürün yaşam döngüsü durumu bir mühendislik sürümüne bağlıyken, mühendislik sürümünde hangi hareketlere izin verileceğini denetlemek için yaşam döngüsü durumu kullanılabilir.

## <a name="create-and-manage-product-lifecycle-states"></a>Ürün yaşam döngüsü durumlarını oluşturma ve yönetme

Ürün yaşam döngüsü durumlarıyla çalışmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Ürün yaşam döngüsü durumu**'na gidin. Ardından şu adımlardan birini izleyin.

- Yeni yaşam döngüsü durumu oluşturmak için, Eylem bölmesinden **Yeni**'yi seçin ve sonra alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.
- Mevcut yaşam döngüsü durumlarını düzenlemek için,liste bölmesinden durumu seçin ve Eylem bölmesinden **Düzenle**'yi seçin ve sonra alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.
- Var olan bir yaşam döngüsü durumunu silmek için bunu liste bölmesinden seçin ve sonra Eylem bölmesinden **Sil**'i seçin.

> [!NOTE]
> Mühendislik ürünleri, standart (mühendislik olmayan) ürünler gibi aynı ürün yaşam döngüsü durumlarını kullanır. **Ürün bilgileri yönetimi \> Kurulum \> Ürün yaşam döngüsü durumu**'na giderek bu konuda açıklanan **Ürün yaşam döngüsü durumu** sayfasını da açabilirsiniz. Hem mühendislik ürünleri hem de standart ürünler için ürün yaşam döngüsü durumları hakkında daha fazla bilgi için [Ürün yaşam döngüsü durumu](../pim/product-lifecycle.md) başlığına bakın.

### <a name="header"></a>Üst bilgi

Ürün yaşam döngüsü durumunun üst bilgisinde aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| İl | Ürün yaşam döngüsü durumu için bir ad girin. |
| Tanım | Ürün yaşam döngüsü durumu için bir açıklama girin. |

### <a name="general-fasttab"></a>Genel FastTab

**Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Tüzel bir kişiliğe serbest bırakıldığında varsayılan değer | Bu yaşam döngüsü durumunun ilk yayımlandıklarında varsayılan olarak tüm ürünlere uygulanması gerekiyorsa, standart ürünler için bu seçeneği *Evet* olarak ayarlayın. Yaşam döngüsü durumu daha sonra el ile uygulanacaksa, bunu *Hayır* olarak ayarlayın.<p>Bu ayar mühendislik ürünleri için geçerli değildir. Mühendislik şirketinde oluşturulduktan sonra mühendislik ürün sürümünün yaşam döngüsü durumu, mühendislik değişikliği kategorisinde belirtilir. Ürün bir operasyonel şirkete serbest bırakıldığında, ürünün yaşam döngüsü durumu kopyalanır. Başka bir deyişle, bir mühendislik ürünü operasyonel bir şirkete serbest bırakıldığında, mühendislik şirketindeki aynı yaşam döngüsü durumuna sahip olur. Yaşam döngüsü durumu, operasyonel şirkette geçersiz kılınabilir.</p> |
| Planlama için etkin | Master planlama ve ürün reçetesi düzeylerindeki hesaplamalara bu yaşam döngüsü durumundaki ürünleri dahil etmek için bu seçeneği *Evet* olarak ayarlayın. Bu yaşam döngüsü durumundaki ürünleri hesaplamalardan dışlamak için *Hayır* olarak ayarlayın. |

### <a name="enabled-business-processes-fasttab"></a>Etkin iş süreçleri hızlı sekmesi

Mevcut iş süreçlerinin hangilerinin geçerli yaşam döngüsü durumundaki ürünlerle kullanılabileceğini kontrol etmek için **Etkin iş süreçleri** hızlı sekmesini kullanın. Bu hızlı sekmede listelenen süreçler otomatik olarak aşağıdaki şekilde bulunur:

- Yeni bir yaşam döngüsü durumunu ilk kaydedişinizde, sayfa şu anda kullanılabilir olan iş süreçlerini yükler.
- Sisteminize yeni iş süreçleri eklerseniz mevcut bir yaşam döngüsü durumu için **Etkin iş süreçleri** hızlı sekmesindeki listeyi, Eylem bölmesindeki **Güncelleştirmeleri denetle**'yi seçerek güncelleştirebilirsiniz.

**Etkin iş süreçleri** hızlı sekmesinde listelenen her işlem için aşağıdaki alanlar kullanılabilir.

| Alan | Tanım |
|---|---|
| İşle | Bu salt okunur alan var olan bir iş sürecinin adını gösterir. |
| İşlem alanı | Bu salt okunur alan var olan bir süreç alanının adını gösterir. |
| Poliçe | Bu yaşam döngüsü durumunda olan ürünler için geçerli işleme izin verilip verilmediğini denetlemek üzere aşağıdaki değerlerden birini seçin:<ul><li>**Etkin**: İş sürecine izin verilir.</li><li>**Engellendi**: İşleme izin verilmez. Bir kullanıcı, bu yaşam döngüsü durumunda olan bir üründe işlem kullanmaya çalışırsa, sistem girişimi engeller ve bir hata görüntüler. Örneğin, kullanım ömrü sonundaki ürünlerin satın alınmasını engelleyebilirsiniz.</li><li>**Uyarı ile etkinleştirildi**: İşleme izin verilir ancak bir uyarı görüntülenir. Örneğin, araştırma ve geliştirme departmanı tarafından oluşturulan bir üretim emrine bir prototip ürününün yerleştirilmesini isteyebilirsiniz. Ancak diğer departmanlar ürünü henüz üretmemelidir.</li></ul> |

Daha fazla yaşam döngüsü durumu kuralını özelleştirme olarak ekliyorsanız üst bölmede **Süreçleri yenile**'yi seçerek bu kuralları kullanıcı arabiriminde (UI) görüntüleyebilirsiniz. **Süreçleri yenile** düğmesi yalnızca yöneticiler tarafından kullanılabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
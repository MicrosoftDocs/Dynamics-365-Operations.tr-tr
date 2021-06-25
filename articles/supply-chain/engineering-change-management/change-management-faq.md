---
title: Mühendislik değişim yönetimi SSS
description: Bu konu, mühendislik değişim yönetimi özelliği hakkında sık sorulan soruların yanıtlarını verilmektedir.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9c95c1f2342654ca2bbee57959becc85291eebbc
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187283"
---
# <a name="engineering-change-management-faq"></a>Mühendislik değişim yönetimi SSS

[!include [banner](../includes/banner.md)]

Bu konu, mühendislik değişim yönetimi özelliği hakkında sık sorulan soruların yanıtlarını verilmektedir.

## <a name="should-i-track-the-version-in-transactions"></a>Sürümü hareketlerde takip etmeli miyim?

Bir mühendislik değişikliği kategorisi oluşturduğunuzda, **Mühendislik kategori ayrıntıları** sayfası, **Sürümü hareketlerde takip et** olarak adlandırılan bir seçenek sağlar. Bu ayar nedir ve ne yapar?

- **Sürümü hareketlerde takip et** seçeneğini *Evet* olarak ayarlarsanız, **Boyut grubu** alanına filtre uygulanır ve böylece yalnızca sürümün etkin bir boyut olduğu boyut grupları gösterilir.
- **Sürümü hareketlerde takip et** seçeneğini *Hayır* olarak ayarlarsanız, **Boyut grubu** alanına filtre uygulanır ve böylece yalnızca sürüm boyutunun etkin bir boyut **olmadığı** boyut grupları gösterilir.

### <a name="if-you-track-the-version-in-transactions"></a>Sürümü hareketlerde takip ederseniz

Sürümün etkin bir boyut olduğu bir boyut grubu seçtiğiniz mühendislik kategorileri için, bu kategorideki ürünlerin hareketlerini takip edersiniz. Bu durumda, mühendislik ürünü bir ana ürün olur ve ürünün her sürümü sürüm boyututu kullanan bir ürün varyantı olur. Diğer boyutlar sürüm boyutuyla birlikte kullanılabilir.

Bu durumda, her mühendislik sürümü tüm işlemlerde bir varyant olarak kabul edilir. Bu nedenle, bir harekette belirli bir varyantınız varsa (hangi varyantın satıldığını veya satın alındığını belirleyebilmeniz için), her sürümün stoğunu yönetmeniz gerekir, master planlama her sürüm için tedarik planı yapar vb. Bir sürümü pazardan kaldırırsanız, değişikliği yansıtması için geçerlilik tarihi ve geçerlilik bitiş tarihlerini el ile ayarlamanız gerekir. Ambarlarınızda maddelerin kullanılmayan sürümleri bulunmadığından emin olmak için stoğunuzu da yönetmeniz gerekir.

Bu seçenek daha fazla yönetim çabası gerektirmekle birlikte, her harekette kullanılan belirli sürümlerin yüksek izlenebilirliği olmasını istiyorsanız bunu öneririz.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Sürümü hareketlerde takip etmezseniz

Sürümün etkin bir boyut **olmadığı** bir boyut grubu seçtiğiniz mühendislik kategorileri için, bu kategorideki ürünlerin hareketlerini takip **etmezsiniz**. Bu durumda, başka bir boyut kullanmıyorsanız mühendislik ürünü farklı bir ürün olacaktır. Ürünün yine de sürümlenir ve belirli versiyonlar (örneğin, ürün reçetesi\[BOM] ve rota) hakkındaki bilgileri de yönetebilirsiniz ancak her harekette hangi belirli sürümün kullanıldığını takip edemezsiniz. Geçerlilik başlangıcı ve geçerlilik bitiş tarihleri her sürümün geçerliliğini gösterir.

Bu seçeneği yönetmek daha kolaydır çünkü bir sürümden diğerine geçmek istediğinizde gerekli değişiklikleri değişiklik siparişte yapmanız, sonra da mühendislik sürümündeki geçerlilik ve geçerlilik bitiş tarihlerini güncelleştirmeniz yeterli olur. Ardından üretim süreçleri, ürün (ve belirli sürümü) için gerekli ürün reçetesini ve rotayı alır.

Birçok kuruluş, sürüm ve değişiklik yönetimi sağlayıp da her harekette sürümü izleme, stok ve master planlama sırasında fazladan ek yük eklemediği için bu özelliği tercih eder.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Serbest bırakılan madde şablonundan hangi alanlar kopyalanır?

Bir mühendislik şirketi mühendislik ürünü oluşturduğunda, söz konusu ürün, mühendislik şirketinde serbest bırakılmış bir ürün olarak oluşturulur. Oluşturulan serbest ürün, seçilen *serbest bırakılmış madde şablonunu* temel alır. (Serbest bırakılan madde şablonu, kendi başına var olan serbest bir üründür.) Serbest bırakılmış madde şablonu, ürün bir operasyonel şirkette serbest bırakıldığında da kullanılır. Her durumda, serbest bırakılmış madde şablonu serbest bırakılan ürün için alan değerlerinin çoğunu tanımlar ve bu değerler, ilgili **Serbest bırakılan ürün ayrıntıları** sayfasından gelir.

Aşağıdaki tablolarda, bu işlemler sırasında kopyalanan alanlar gösterilmiştir.

| Hızlı sekme | Mühendislik şirketinde ürün oluşturmada kopyalanan alanlar | Bir operasyonel şirkete serbest bırakıldığında kopyalanan alanlar |
|---|---|---|
| **Genel** | **Yönetim** bölümündeki tüm alanlar | Mühendislik şirketi için kopyalanan alanların aynıları |
| **Satınalma** | Tüm alanlar | **Birim** dışındaki tüm alanlar |
| **Satış** | Şu bölümlerdeki tüm alanlar: **Satış siparişi**, **Yönetim**, **Vergilendirme**, **Fiyat güncelleştirmesi**, **Temel satış fiyatı**, **Masraflar**, **İndirimler** ve **Alternatif ürün** | **Birim** hariç, mühendislik şirketi için kopyalanan alanların tümü |
| **Dış Ticaret** | Tüm alanlar | Tüm alanlar |
| **Stok yönetimi** | **Fiziksel boyutlar** ve **Fiili ağırlık** *hariç* tüm alanlar ve bölümler | **Birim** hariç, mühendislik şirketi için kopyalanan alanların tümü |
| **Mühendis**, **Planlama**, **Maliyetleri yönetme**, **Projeleri yönetme**, **Mali boyutlar** ve **Ambar** | Tüm alanlar | **Ürün Reçetesi Birimi** dışındaki tüm alanlar |
| **Ürün çeşitleri** | **Varsayılan ürün varyantı** bölümündeki tüm alanlar | Mühendislik şirketi için kopyalanan alanların aynıları |

Önceki tabloda gösterilen alanlara ek olarak, tüm varsayılan sipariş ayarları serbest bırakılmış madde şablonundan kopyalanır (hem ürün mühendislik şirketinde oluşturulduğunda hem de operasyonel şirkete serbest bırakıldığında). (Serbest bırakılan bir madde şablonunun varsayılan sipariş ayarlarını görüntülemek için ilgili **Serbest bırakılan ürün ayrıntıları** sayfasını açın ve ardından Eylem Bölmesi'nde **Stoğu Yönet** sekmesinde **Varsayılan sipariş ayarları**'nı seçin.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Mühendislik ürünleri için ayrı bir tüzel kişilik mi oluşturmalıyım yoksa mevcut tüzel kişiliği mi kullanmalıyım?

İş gereksinimleriniz, mühendislik ürünleri için yeni bir tüzel kişilik oluşturmanız gerekip gerekmeyeceğini belirler.

Ayrı bir mühendislik şirketi oluşturarak, mühendislik verilerinin ayrı kalmasını sağlayabilirsiniz ve ardından yerel operasyonel şirketleriniz için gerekli değişiklikleri ekleyebilirsiniz. Bu sayede aşağıdaki hedefleri gerçekleştirebilirsiniz:

- Mühendislik ürünlerinin oluşturulduğu ve yönetildiği ayrı bir varlık saklama.
- Mühendislik ürünlerinin, hazır ve serbest bırakılıncaya kadar serbest bırakılan ürünlerin geri kalanıyla birlikte gösterilmesini engelleme.
- Mühendislik ve yerel veriler tarafından dikte edilen verileri açıkça ayırt etme.

Diğer taraftan, aşağıdaki koşulların geçerli olması durumunda, mühendislik şirketi olarak mevcut bir tüzel kişiliği kullanmalısınız:

- Sisteminizde yalnızca bir tüzel kişilik var ve/veya oluşturulan ürünler arasında net bir ayrım gerekmiyor.
- Kaynak grupları, kaynaklar, operasyonlar ve (belki) siteler gibi bazı verileri çoğaltmak istemiyorsunuz.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Mühendislik sürümleri ve varyantlar için terminoloji nedir?

Mühendislik ürünleri ve ürün varyantları için terminoloji aşağıdaki şekilde çalışır:

- Mühendislik ürünü (yani boyut kullanılmadıysa ayrı bir ürün veya boyut kullanılmışsa ana ürün) için, numara kuralı terminolojisi, mühendislik ürün kategorisinde tanımlanır. Burada; numara sırası, metin sabitleri ve öznitelik adları ve değerleri kullanma seçeneğiniz vardır.
- Mühendislik ürününün her çeşidi için (mühendislik ürününüz bir ana ürün ise varyantlar boyut grubunu belirttiğiniz mühendislik ürün kategorisinde ayarlanır), her varyantın numara kuralı terminolojisi, boyut grubunda tanımlanır. Bu durumda, ana ürünün ürün kodunu ve boyut değerlerini ve adlarını kullanabilirsiniz.

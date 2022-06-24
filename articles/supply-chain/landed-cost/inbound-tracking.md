---
title: Gelen seyahatleri ve sevkiyat konteyneri seyahatlerini izleme
description: Bu makale, seyahatlerinizin ve sevkiyat konteyneri seyahatlerinizin ilerlemesini izlemek için Gelen izleme sayfasını nasıl kullanabileceğinizi açıklar.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 17874f984945b27e036eafda841ec1fd95d345be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854369"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Gelen seyahatleri ve sevkiyat konteyneri seyahatlerini izleme

[!include [banner](../../includes/banner.md)]

**Gelen izleme** sayfası, seyahatlerinizin ve sevkiyat konteyneri seyahatlerinizin ilerlemesini izlemenizi sağlar. Her seyahat ve sefer, her birinin sayfada kendi satırı olan *etkinliklere* ayrılır. Etkinliğe göre tahmini tarihleri ve gerçek tarihleri görüntülemek ve girmek için sayfayı kullanabilirsiniz.

Genellikle, [İzleme denetim merkezindeki](delivery-information-setup.md#tracking-control-center) kuruluma bağlı olarak bu etkinlikler son hedefteki tahmini varış tarihini otomatik olarak gösterir. Ayrıca kuruluma bağlı olarak, son tarih genellikle satın alma siparişi satırlarındaki teslimat tarihini veya onaylanma tarihini güncelleştirir. Transfer emri satırları için sistemi giriş tarihini güncelleştirecek şekilde ayarlayabilirsiniz.

**Geliş izleme** sayfasını açmak için **Varış yeri maliyeti \> İzleme \> Geliş izleme**'ye gidin.

## <a name="filter-the-activities-list"></a>Etkinlik listesine filtre uygulama

Sayfayı yalnızca seçili seyahat ve/veya sevkiyat konteyneriyle ilişkili etkinlikler kalacak şekilde filtrelemek için **Geliş izleme** sayfasının üst kısmındaki **Seyahat** ve **Sevkiyat konteyneri** alanlarını kullanabilirsiniz.

## <a name="update-tracking-information"></a>İzleme bilgilerini güncelleştirme

Bir seyahat veya yolculuğun programını güncelleştirmek için ilk etkinliğin başlangıç tarihini girin. Son etkinliğin tahmini bitiş tarihi daha sonra güncelleştirilir. [İzleme denetim merkezindeki](delivery-information-setup.md#tracking-control-center) her durak ve yolculuk şablonu için kurulum, tahmini sağlama sürelerini belirler. Tahmini bitiş tarihleri, etkinliğin başlangıç tarihindeki sağlama süresini kullanır. Ardından, gerçek bitiş tarihi kaydedildiğinde, bir sonraki etkinliğin başlangıç tarihi önceki etkinliğin fiili bitiş tarihiyle aynı tarihe güncelleştirilir. Karşılaştırma ve analiz yapılabilmesi için fiili sağlama süresi güncelleştirilir. Ek notlar **Not** alanına girilebilir.

Kılavuzdaki etkinliklerin sırası, ilgili yolculuk şablonundaki durakların sırasına göre belirlenir. Ekli yolculukta durakların sırası değişirse izleme denetimi de değişir.

Eylem Bölmesinde **Başlangıç tarihini güncelleştir** veya **Fiili bitiş tarihini güncelleştir**'i seçerek tüm konteynerlerin tarihlerini güncelleştirebilirsiniz. Alternatif olarak sevkiyatta konteyner başına tarihleri girebilirsiniz. Bu yaklaşım daha fazla esneklik sağlar çünkü konteynerler çok yolculuklu bir ortamda bölünebilir.

## <a name="buttons-on-the-action-pane"></a>Eylem Bölmesindeki düğmeler

Geliş seyahatleri ve yolculuklarıyla çalışmak için **Geliş izleme** sayfasının Eylem Bölmesindeki düğmeleri kullanabilirsiniz. Aşağıdaki tabloda, kullanılabilecek düğmeler açıklanmıştır.

| Düğme | Tanım |
|---|---|
| Düzenle | Bir seyahat veya sevkiyat konteyneri yolculuğunu düzenleyin. |
| Yeni | Yeni bir seyahat veya sevkiyat konteyneri yolculuğu oluşturun. |
| Delete | Seçili bir seyahati veya sevkiyat konteyneri yolculuğunu silin. |
| Başlangıç tarihini güncelle | Bir seyahatteki tüm konteynerler için bir etkinliğin başlangıç tarihini güncelleştirin. Bir yolculuğun belirli bir etkinliğinin veya durağının başlangıç tarihi güncelleştirildiğinde, sonraki tahmini başlangıç tarihleri belirtilen sağlama süresine göre güncelleştirilir. |
| Fiili bitiş tarihini güncelleştir | Bir seyahatteki tüm konteynerler için bir etkinliğin bitiş tarihini güncelleştirin. Belirli bir etkinliğin bitiş tarihi güncelleştirildiğinde, sonraki etkinlikler belirtilen sağlama süresine göre güncelleştirilir. |
| Faaliyet ekle | Seyahate el ile etkinlik ekleyin. Örneğin, bir fümigasyon etkinliği ekleyebilirsiniz. Ekleme işlemi, gemideki veya seyahatteki malların onaylanmış teslimat tarihinin değişmesine neden olabilir. Yolculuğa bir etkinlik eklendiğinde, yolculuk durağının başlangıç tarihi güncelleştirilene kadar tahmini günler girilmez. |

## <a name="information-and-settings-on-the-overview-tab"></a>Genel bakış sekmesindeki bilgiler ve ayarlar

**Genel bakış** sekmesi, sayfanın üst kısmında seçilen yolculuk ve/veya kargo konteynerine ait tüm etkinliklerin listesini gösterir. Aşağıdaki tabloda, her etkinlikte kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Durak | Yolculuk şablonu tarafından tanımlanan etkinliğin durak kimliği. |
| Teslimat şekli | Etkinlik için beklenen teslimat yöntemi. |
| Faaliyet | Bu alan genellikle etkinlikle ilişkili proje veya görevi tanımlar. Tipik örnekler arasında *Seyir* ve *Gümrük İzni* sayılabilir. |
| Tanım | Etkinliğin daha uzun bir açıklaması. |
| Başlangıç tarihi | Bu alanda başlangıçta etkinliğin tahmini başlangıç tarihi gösterilir. Ancak önceki etkinliğin fiili bitiş tarihi girildikten sonra, gerçek başlangıç tarihini gösterir. Bu alan, sağlama süresine bağlı olarak tahmini bitiş tarihini belirlemek için kullanılır. |
| Tahmini bitiş tarihi | Bu alanın değeri başlangıç tarihi ve sağlama saati temel alınarak hesaplanır. Genellikle değeri doğrudan düzenleyemezsiniz. |
| Fiili bitiş tarihi | Bir kullanıcı, etkinlik gerçekleştikten sonra bu alanı en kısa sürede güncelleştirmelidir. Gerçek sağlama süresi daha sonra güncelleştirilir. |
| Tahmini gün | Etkinliği tamamlamak için gereken tahmini süre (gün olarak). |
| Gerçek gün sayısı | Etkinliği tamamlamak için gereken fiili süre (gün olarak). |
| Dekont | Etkinlikle ilgili çeşitli notlar ve ayrıntılar eklemek için bu alanı kullanın. |

## <a name="information-and-settings-on-the-general-tab"></a>Genel sekmesindeki bilgiler ve ayarlar

**Genel** sekmesinde, **Genel bakış** sekmesinde seçili durakla ilgili bilgiler gösterilir. **Genel bakış** sekmesinde görünen bazı bilgileri yinelese de, seçilen durak hakkında ek bilgiler de içerir.

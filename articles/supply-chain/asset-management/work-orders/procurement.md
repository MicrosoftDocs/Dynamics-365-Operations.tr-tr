---
title: Tedarik
description: Bu konuda Kıymet Yönetimi'ndeki tedarikleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6ed3bc581c4260ca5b4f673f9f66853f4f6f490b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223518"
---
# <a name="procurement"></a>Tedarik

[!include [banner](../../includes/banner.md)]

Varlık Yönetiminde, iş emirleriyle ilgili satınalma taleplerinin ve satınalma siparişlerinin genel görünümünü alabilirsiniz. Bir iş emrinden bir satınalma siparişi veya satınalma talebi de oluşturabilirsiniz.

**İş emri satınalma talebi** liste sayfası (**Varlık yönetimi** > **Ortak** > **Tedarik** > **İş emri satınalma talebi**), iş emirleriyle ilgili satınalma taleplerinin listesini görüntüler. Bu sayfada bir iş emri işi seçtiğinizde, çeşitli eylemleri gerçekleştirmek için **İş emri satınalma talebi** Eylem bölmesi sekmesindeki **Göster** grubunda bulunan düğmeleri kullanabilirsiniz:

- İlgili satınalma talebini açmak için **Satınalma talebi** seçeneğini belirleyin. 
- İlgili iş emrini açmak için **İş emri**'ni seçin.
- Seçilen satırdaki maddenin Varlık Yönetiminde varlıklar, bakım işi türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin. Bu genel bakış hakkında daha fazla bilgi için bkz. [Maddenin kullanıldığı yer](../controlling-and-reporting/item-where-used.md).

Aşağıdaki şekilde **İş emri satınalma talebi** liste sayfası örneği gösterilmektedir.

![Şekil 1](media/08-work-orders.png)


**İş emri satınalma** liste sayfası (**Varlık yönetimi** > **Ortak** > **Tedarik** > **İş emri satınalma talebi**), iş emirleriyle ilgili satınalma siparişlerinin listesini görüntüler. Bu sayfada bir iş emri işi seçtiğinizde, çeşitli eylemleri gerçekleştirmek için Eylem bölmesindeki **İş emri satınalma** sekmesinde bulunan **Göster** grubunda bulunan düğmeleri kullanabilirsiniz:

- İlgili satınalma sipairşini açmak için **Satınalma siparişi**'ni seçin. 
- İlgili iş emrini açmak için **İş emri**'ni seçin.
- Seçilen satırdaki maddenin Varlık Yönetiminde varlıklar, bakım işi türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin. Bu genel bakış hakkında daha fazla bilgi için bkz. [Maddenin kullanıldığı yer](../controlling-and-reporting/item-where-used.md).

Aşağıdaki şekilde **İş emri satınalma** liste sayfası örneği gösterilmektedir.

![Şekil 2](media/09-work-orders.png)


Hem **İş emri satınalma** listesi sayfasında, hem de **İş emri satınalma talebi** liste sayfasında, her satırın sağ tarafında teslimat tarihi denetimiyle ilişkili bir simge görüntülenir. Simge kırmızı daire içinde bir ünlem işareti gösteriyorsa, ilgili satınalma talebinde veya satınalma siparişinde teslimat gecikebilir.

Satınalma siparişi için, satınalma siparişi satırı ile ilgili tarih, olası bir gecikmeyi hesaplamak üzere kullanılır. Bu tarihi görüntülemek için **Satınalma siparişi** sayfasında satınalma siparişi satırını seçin. Tarih, **Satır ayrıntıları** hızlı sekmesinin **Kurulum** sekmesindeki **Onaylanan teslimat tarihi** alanında gösterilir. **Onaylanan teslimat tarihi** alanı ayarlanmamışsa, **Satınalma siparişi başlığı** hızlı sekmesindeki **Teslimat tarihi** alanında bulunan tarih, hesaplama için kullanılır. Bu tarihlerden biri, iş emri veya iş emri işindeki mevcut tarihle aşağıdaki sırayla karşılaştırılır:

1. İş emri üzerindeki gerçek başlangıç tarihi  

2. İlgili iş emri işi üzerinde planlanan başlangıç tarihi 

3. İş emri üzerindeki zamanlanan başlangıç tarihi 

4. İş emri üzerindeki beklenen başlangıç tarihi 

Bir satınalma talebi için, **Satınalma talepleri** sayfasının **Satınalma talebi başlığı** hızlı sekmesindeki **Talep tarihi** alanında bulunan tarih olası gecikmeyi hesaplamak için kullanılır. Bu alandaki tarih, satınalma siparişi için kullanılan aynı sırayla iş emri veya iş emri işinde kullanılabilir tarihle karşılaştırılır.


## <a name="create-a-purchase-order-from-a-work-order"></a>İş emrinden satınalma siparişi oluşturma

**Tüm iş emirleri** liste sayfasında, bir iş emri işi seçip ilgili satınalma siparişi veya satınalma talebini oluşturabilirsiniz. Bu şekilde, satınalma siparişi veya satınalma talebi ile iş emri arasında proje ilişkileri olmasını sağlamaya yardımcı olursunuz.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.

2. Satınalma siparişi oluşturmak için iş emrini seçin ve sonra **Düzenle**'yi seçin.

3. **İş emri bakım işleri** hızlı sekmesinde, satınalma siparişi oluşturmak istediğiniz iş emri işini seçin.

4. **Madde görevleri** > **İş emri işinden satınalma siparişi**'ni seçin.

5. **Proje satınalma siparişleri** liste sayfasında, **Yeni**'ye tıklayın.

6. Satınalma siparişi oluşturun.

>[!NOTE]
>İlgili satınalma talebi oluşturmak için aynı adımları izleyin. Ancak, adım 4'te **Madde görevleri** > **İş emri işinden satınalma talebi**'ni seçin.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>İş siparişi ve satınalma siparişi veya satınalma talebi arasındaki proje ilişkisi

Satınalma siparişi satırı veya satınalma talebi satırı, iş emri ile ilgili proje faaliyet numarası aracılığıyla iş emri işiyle ilgilidir. Bir iş emri işinden satınalma siparişi veya satınalma talebi oluşturduğunuzda, ilgili proje faaliyet numarası zorunludur. İlgili iş emrindeki tüm iş emri işler aynı bakım işi türüne sahipse, proje faaliyet numarası bir satınalma siparişine veya satınalma talebine otomatik olarak eklenir. İş emri işleri farklı bakım işi türlerine sahipse, proje faaliyet numarasını bir satınalma siparişine veya satınalma talebine el ile girmeniz gerekir.

Bir satınalma siparişi satırıyla ilişkili faaliyet numarasını görüntülemek veya girmek için **İş emri satınalma** liste sayfasında satınalma siparişi kaydını seçin ve ardından **Satınalma siparişi** sütununda, satınalma siparişi bağlantısını seçin. **Satır ayrıntıları** hızlı sekmesinin **Proje** sekmesinde **Faaliyet numarası** alanını bulabilirsiniz.

Aşağıdaki örnekte **Faaliyet numarasına** odaklanılmış **Satınalma siparişi** sayfası örneği gösterilmektedir.

![Şekil 3](media/10-work-orders.png)

Benzer şekilde, bir siş emri satınalma talebi satırıyla ilgili faaliyet numarasını görüntülemek veya girmek için **İş emri satınalma talebi** liste sayfasında satınalma talebi kaydını seçin ve ardından **Satınalma talebi** sütununda, satınalma talebi bağlantısını seçin. **Satır ayrıntıları** hızlı sekmesinin **Proje** sekmesinde **Faaliyet numarası** alanını bulabilirsiniz.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
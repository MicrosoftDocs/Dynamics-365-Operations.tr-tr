---
title: Şirketlerarası planlama
description: Bu konu, şirketlerarası planlamayı açıklar ve Microsoft Dynamics 365 Supply Chain Management'taki Planlama İyileştirmesi ile şirketlerarası planlamayı nasıl yapılandıracağınızı açıklar.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6ef551e1c2c4d90510f967855a5aa61646dc8eab
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538578"
---
# <a name="intercompany-planning"></a>Şirketlerarası planlama

[!include [banner](../../includes/banner.md)]

Lojistik işlemleri, bazı kuruluşlar için kuruluştaki diğer tüzel kişiliklere (şirketler) bağlıdır. Bu işlemler, şirketlerarası satış ve satın alma işlemleri kullanılarak yönetildiğinden, her tüzel kişiliğin ayrı bir hesap planı vardır.

Bu konu, şirketlerarası planlamayı açıklar ve Microsoft Dynamics 365 Supply Chain Management'taki Planlama İyileştirmesi ile şirketlerarası planlamayı nasıl yapılandıracağınızı açıklar.

Bu konu, aşağıdaki önemli şirketlerarası hükümleri kullanır:

- **Yukarı akış**: Bir firma veya tedarik zincirindeki göreli bir başvurudur. Ham madde tedarikçisi yönüne doğru hareketi gösterir.
- **Aşağı akış**: Bir firma veya tedarik zincirindeki göreli bir başvurudur. Müşteri yönüne doğru hareketi gösterir.
- **Şirketlerarası planlı talep**: Bir aşağı akış şirketindeki ürünün planlı talebine göre bir şirketteki ürün için planlanan talep.

Master planlamada, bir şirketteki plan, başka bir şirketteki bir plandaki planlı siparişlerle ilgili planlı şirketlerarası talep içerebilir. Şirketler arasında planlı siparişlerde tam görünürlük sağladığından, bu özellikler faydalıdır. Ayrıca, planlı siparişlerin şirketlerarası talep için kesinleştirilmesini gerektirmeden, gerekli tüm planlı tedarik emirlerinin oluşturulmasını da sağlar.

Master planlamayı planlı aşağı akış talebini içeren bir ana plandan çalıştırırsanız, ilgili şirketlerarası satıcılardan planlı satın alma siparişleri talep olarak plana dahil edilir.

## <a name="required-setup"></a>Gerekli kurulum

Şirketlerarası planlamayı kullanmak için sisteminizi aşağıdaki şekilde hazırlamanız gerekir:

1. İlgili ürünlerin ilgili tüm şirketlerde serbest bırakılması gerekir. Daha fazla bilgi için bkz. [Dynamics 365 Supply Chain Management'ta şirketlerarası ticareti yapılandırma ve kullanma](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Aşağı akış talebi, yukarı akış şirketi ve müşterinin ilgili varsayılan stok boyutlarına (tesis ve ambar) şirketlerarası ilşikisi olan bir satıcıdan yapılan satın almalarla kapsanmalıdır. Daha fazla bilgi için bkz. [Dynamics 365 Supply Chain Management'ta şirketlerarası ticareti yapılandırma ve kullanma](/training/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).
1. Yukarı akış şirketindeki master plan, planlanan aşağı akış talebini içermeli ve ilgili şirket ile master plan, aşağı akış planlarında belirtilmelidir.

## <a name="include-planned-downstream-demand"></a>Çıkıştaki planlanan talebi ekle

Master planınızı planlanan aşağı akış talebini içerecek şekilde yapılandırmak için bu adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Bir master plan seçin veya oluşturun.
1. **Şirketlerarası planlama** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Planlanan aşağı akış talebini dahil et**: Master plan için şirketlerarası planlamayı etkinleştirmek üzere bu seçeneği *Evet* olarak ayarlayın.
    - **Aşağı akış planları**: **Planlanan aşağı akış talebini dahil et** seçeneğini *Evet* olarak ayarlarsanız diğer şirketlerdeki istediğiniz master planları eklemek için araç çubuğunu ve kılavuzu kullanın.

## <a name="peg-across-companies-by-using-multilevel-pegging"></a>Çok düzeyli bir ilişkilendirme kullanarak şirketler arasında ilişkilendirme yapma

Çok düzeyli bir ilişkilendirmede, arz ile kapsanmakta olan talebin ilk kaynağını görmek için şirketler arasındaki ilişkilendirmeyi görüntüleyebilirsiniz.

Çok düzeyli bilgileri görüntülemek için aşağıdaki adımları izleyin.

1. **Master planlama \> Master planlama \> Planlı siparişler** öğesine gidin.
1. Planlanan bir sipariş seçin veya açın.
1. Eylem Bölmesinde **Görünüm** sekmesinde **Gereklilikler** grubunda **Çok düzeyli ilişkilendirme** öğesini seçin.

### <a name="intercompany-example-that-involves-two-companies"></a>İki şirket içeren şirketlerarası ilişki örneği

Bu örnekte, USMF şirketinde DEMF şirketindeki bir satış siparişini kapsayacak bir planlanan üretim emri oluşturulur. USMF'de, doğrudan talep, planlanan şirketlerarası taleptir. Bu talebin USMF'de görünmesini sağlamak için önce DEMF ve sonra USMF'de master planlama çalıştırılır.

Aşağıdaki şekil, bu örneğin planlanan üretim emri için **Çok düzeyli bir ilişkilendirme** sayfasında nasıl görünebileceğini gösterir.

![İki şirket içeren şirketlerarası ilişki örneği.](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a>Üç şirket içeren şirketlerarası ilişki örneği

Bu örnekte, USMF şirketinde FRRT şirketindeki bir satış siparişini kapsayacak bir planlanan satın alma siparişi oluşturulur. DEMF ve USMF şirketlerinde, doğrudan talep, planlanan şirketlerarası taleptir. Bu talebin USMF'de görünmesini sağlamak için önce FRRT ve sonra DEMF'de ve son olarak USMF'de master planlama çalıştırılır.

Aşağıdaki şekil, bu örneğin planlanan üretim emri için **Çok düzeyli bir ilişkilendirme** sayfasında nasıl görünebileceğini gösterir.

![Üç şirket içeren şirketlerarası ilişki örneği.](media/IntercompanyPlanning2.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Tehlikeli malzemelere genel bakış
description: Bu konuda, ürün bilgileri yönetimi ve ambar yönetimi sırasında tehlikeli malzemelerin işlenmesi ve belgelenmesi ile ilgili özelliklere genel bir bakış sağlanır.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 22e1b0838160378f3ff9484faaf87c9aec6e8964
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570693"
---
# <a name="hazardous-materials-overview"></a>Tehlikeli malzemelere genel bakış

[!include [banner](../includes/banner.md)]

Sevkiyat ve taşıma yönetmeliklerine uyumluluğu korumak için tehlikeli mal olarak sınıflandırılmış malzemeler sevk eden kuruluşların, sevkiyatlarına ek belgeler eklemeleri gerekir. Tehlikeli malzemeler özelliği, müşterilerin serbest bırakılmış maddelerle ilgili bilgileri depolamasına olanak tanır. Bu bilgiler daha sonra sevkiyat belgelerinin hazırlanmasına yardımcı olarak kullanılabilir. Tehlikeli mal sevk eden bir kuruluşun, sevkiyat sürecini yönetmeye yönelik kendi süreçleri ve yordamları olmalıdır. Microsoft Dynamics 365 Supply Chain Management, yalnızca gerekli belgelerin oluşturulmasına yardımcı olabilecek bir araçtır.

Aşağıdaki diyagramda, tehlikeli malzeme özelliğini ayarlamak ve kullanmak için gerekli adımlar gösterilmektedir.

![Tehlikeli malzeme özelliğinin ayarlanması ve kullanımı.](media/hazmat-overview.png "Tehlikeli malzeme özelliğinin ayarlanması ve kullanımı")

Tehlikeli malzemeler özelliği, Ürün bilgileri yönetiminde ayarlanır ve Ambar yönetimi üzerinden yazdırılabilen belgeler sağlar. Bu nedenle, genel anlamda bu özelliğin işlevini inceleyeceğiniz, ayarlayacağınız ve kullanacağınız iki ana alan bunlardır.

- **Ürün bilgileri yönetimi:** Serbest bırakılan ürüne uygulanacak kodları ayarlayın.
- **Ambar yönetimi**: Sevkiyatlar için yazdırılacak ek sevkiyat belgeleri üzerinde çalışın.

> [!IMPORTANT]
> Supply Chain Management'daki tehlikeli malzeme özellikleri, tehlikeli ürünlerinizle ilgili bilgileri kaydetmenize ve bu bilgilere başvurmanıza yardımcı olabilecek kullanışlı ürün bilgisi alanları ve ilgili işlevler koleksiyonu sağlar. Bu özellikler, sevk ettiğiniz tehlikeli malzemeler hakkındaki bilgilerin aynısını içeren sevkiyat belgelerini tasarlamanıza ve yazdırmanıza yardımcı olur. Ancak, sistem ülkenizdeki veya bölgenizdeki geçerli tüm yönetmeliklerle otomatik olarak uyumlu hale gelmez. Bu araçlar ortak yönetmeliklere uymanıza yardımcı olacak şekilde tasarlanmış olsa da kendi başlarına yeterli değillerdir ve bununla ilgili bir garanti sunulmaz. Geçerli tüm yönetmelikleri bilmek ve bunlara uymak için gerekli tüm adımları atmaktan kuruluşunuz sorumludur.

## <a name="product-information-management"></a>Ürün bilgileri yönetimi

Ürün bilgileri yönetiminde, kara, hava ve deniz yoluyla taşıma için çeşitli tehlikeli mallar listelerinde sağlanan referans bilgilerini girebileceğiniz bir dizi kurulum tablosu bulunur.

Bu işlevin geliştirilmesi sırasında aşağıdaki ortak yönetmeliklere başvurulmuştur:

- **ADR** – Tehlikeli malların uluslararası karayollarında taşınmasıyla ilgili düzenlemeler
- **CFR 49** – ABD'de tehlikeli malların taşınmasına yönelik düzenlemeler
- **IMDG** – Uluslararası Denizcilik Tehlikeli Maddeler (IMDG) kodu
- **IATA** – Uluslararası Hava Taşımacılığı Birliği (IATA) tehlikeli mal düzenlemeleri

Her yönetmelik kümesi, tehlikeli malların ve referans kodlarının standart listelerini sağlar. Bu nedenle, Supply Chain Management bu listelerdeki ortak kodlar için bir başvuru tablosu sunar. Her listede, tanımlayabileceğiniz bazı benzersiz kodlar da vardır.

Tehlikeli malzemelerle ilgili yönetmeliklerin ve değerlerin nasıl ayarlanacağı ve değerlerin ilgili ürünlere nasıl atanacağı hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [Tehlikeli malzemeleri ayarlama](hazmat-setup.md)
- [Ürün, sipariş, sevkiyat ve yüklerdeki tehlikeli malzemeler](hazmat-items.md)

## <a name="warehouse-management"></a>Ambar yönetimi

Ambar yönetiminde sevkiyat hazırlarken, Ürün bilgileri yönetiminde ayarladığınız bilgileri kullanan bazı yeni raporlar yazdırabilirsiniz. Kullanılabilir raporlar ve bunların nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [Tehlikeli malzeme sorguları ve raporları](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
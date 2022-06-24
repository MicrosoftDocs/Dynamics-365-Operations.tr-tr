---
title: Abonelik iş akışı özeti
description: Bu makale, abonelik iş akışına genel bir bakış sağlar.
author: sorenva
ms.date: 05/07/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c112e1816d7ede80e0e30fe318d159e22ab540b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897443"
---
# <a name="subscription-workflow-overview"></a>Abonelik iş akışı özeti 

[!include [banner](../includes/banner.md)]


Aydınlatma donanımı bakımı için abonelikler sunan bir aydınlatma şirketi için abonelik yöneticisisiniz. Bir müşteriniz, aydınlatma donanımı bakımı için yıllık bir abonelik satın almak amacıyla şirketinize başvuruyor.

## <a name="setting-up-subscriptions"></a>Abonelikler ayarlama

Bir abonelik ayarlamak için öncelikler yeni hizmet sözleşmesi için bir abonelik grubu oluşturmanız veya bir abonelik grubu bulunduğunu doğrulamanız gerekir. Bir abonelik grubu zaten varsa, bunu müşteriyi yıllık olarak faturalandırmak ve satış gelirini yılın her ayı tahakkuk edecek şekilde ayarlamanız gerekir. Aboneliklerin nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Abonelik grupları ayarlama](set-up-subscription-groups.md).

Abonelik grubu oluşturulduktan sonra aboneliği oluşturabilirsiniz. Servis abonelikleri oluşturma hakkında daha fazla bilgi için bkz. [Abonelik grubundan servis abonelikleri oluşturma](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Abonelik hareketleri oluşturma ve değiştirme

Abonelik ayarladıktan sonra bir yıl olan ilk faturalama dönemine yönelik abonelik ücreti hareketi oluşturabilirsiniz. Hareketler **Normal** türünde olur. Bu nedenle, yalnızca başlangıç tarihi ve bitiş tarihi **Dönem türleri** formunda önceden oluşturulmuş döneme karşılık gelen abonelik hareketleri oluşturabilirsiniz. Ücret hareketleriyle ilgili daha fazla bilgi için bkz. [Abonelik ücreti hareketleri oluşturma](create-subscription-fee-transactions.md).

Müşteriniz için abonelik ayarladıktan sonra servis teklifleri için tüm fiyat listesi üzerinden yüzde 10 indirim anlaşması yapmış olduğunuzu hatırlarsınız. Bu nedenle, oluşturduğunuz hareket ücretinin fiyatını indirmeniz gerekir.

Günün ilerleyen bölümünde, müşteriniz sizi arayacak aydınlatma donanımı için servis sözleşmesini hala istediklerini ancak yıl içinde yeni bir aydınlatma donanımı edineceklerini bildirir. Bu nedenle, yalnızca Ekim 2013'e kadar bakım hizmetine gereksinim duymaktadırlar. Müşteri aboneliğinden ay sayısını indirmek için **Azaltma günleri** türünde yeni bir abonelik ücreti hareketi oluşturursunuz. Gün azaltma hakkında daha fazla bilgi için bkz. [Abonelik ücretlerinde günleri azaltma](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Abonelik hareketlerini faturalandırma ve tahakkuk ettirme

Abonelik ayarlamayı tamamladınız ve müşterinizi bunun için faturalandırmaya hazırsınız. Aboneliklerin nasıl faturalandırılacağı hakkında daha fazla bilgi için bkz. [Abonelik hareketlerini faturalandırma](invoice-subscription-transactions.md).

İki gün sonra, müşteriniz sizi arayarak aboneliğin Euro değil ABD doları olarak faturalandırılması gerektiğini söyler. Bu nedenle, bir alacak dekontu ve doğru para birimi cinsinde yeni bir abonelik hareketi oluşturursunuz. Abonelik hareketlerini alacaklandırma hakkında daha fazla bilgi için bkz. [Abonelik hareketlerini alacaklandırma](credit-subscription-transactions.md).

Her ayın sonunda, müşterinin aboneliğinden gelen bir aylık geliri kar-zarar hesabına ve süren iş hesaplarına tahakkuk ettirebilirsiniz. Abonelikler için gelir tahakkuk ettirme hakkında daha fazla bilgi için, bkz. [Abonelik geliri tahakkuku](accrue-subscription-revenue.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]